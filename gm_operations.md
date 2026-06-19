# GM OPERATIONS — running the campaign

*The operational companion to `game_bible.md`. The Bible says what is true (rules and setting that change only by deliberate decision); this file says how to run and maintain the campaign session to session — the start, save-point, and close protocols, the change-tag rule, the file manifest and reading guide, the glossary of renamed terms, and the content index. This file never overrides canon: where it touches a rule, `game_bible.md` wins, and where it touches a tracked value, the JSON authority layer wins. Read this file and the Bible together at the start of every session, alongside the current `campaign_state.md` and the JSON sheet.*

*(Procedural core rewritten at the v3-migration Phase 0 for the JSON + arc-file + NPC architecture; manifest and reading-order finalized at Phase 5, with the `npcs/` files and the closed-block arc files now in place. The only block still on the transition footing is **26–30**, whose arc file waits on Session 30's close — until then its raw `Session_26–29.md` bodies and the live S30 SavePoint stand as that block's history.)*

---

## THE ARCHITECTURE IN ONE SCREEN

Each kind of fact has exactly one home. Nothing authoritative is written twice, so nothing drifts.

- **Tracked values** (attributes, money, ammo, mana, prices, crew stats, NPC warmth) → the **JSON authority layer**: `bill_weaver_sheet.json`, `fortunes_folly_crew.json`, `pricing.json`. These are the numbers. Never re-derive a current value from prose.
- **Current narrative** (story-so-far, live threads/clocks, the resume point) → `campaign_state.md`.
- **History** → a write-once `Session_N.md` per session; every fifth session those combine into an arc file (`sessions_01-05.md`, `sessions_06-10.md`, …).
- **NPC voice, knowledge-of-Bill, relationship texture, key dialogue** → the `npcs/` files.
- **Rules / world mechanics** → `game_bible.md` and the catalogs.
- **Procedures** (start, save point, close-out, the change-tag rule) → this file.

**Migration status (Phase 5 complete).** The architecture is in place: the JSON authority layer, `campaign_state.md`, the `npcs/` files, and the arc files `sessions_01-05.md` … `sessions_21-25.md` all exist and are canonical. The single remaining piece is the **26–30 arc**, which waits on Session 30's close; until then read that block's history from the raw `Session_26.md` … `Session_29.md` bodies and the live S30 SavePoint. The JSONs are authoritative for every tracked value.

---

## 1. Start-of-session protocol

Load the exact current state, in order, with zero guessing — then confirm before playing.

1. **Read `game_bible.md`, `gm_operations.md` (this file), and `campaign_state.md` in full.** Between them: the rules, the running machinery, the setting, and all current narrative state (story-so-far, live threads/clocks, the town, the resume point). The resume point and any "⚠ DM owed" block are the first things to honor.
2. **If a SavePoint exists for an in-progress session, read it (§2).** The most recent SavePoint **governs the exact field state** over `campaign_state.md`'s resume point — it is the more precise mid-session marker. Treat the most recently uploaded SavePoint as source-of-truth over any older clone.
3. **Load the JSON authority layer** — `bill_weaver_sheet.json` (sheet, money, inventory, relationships), `fortunes_folly_crew.json` (crew stats), `pricing.json` (prices). These are the numbers; do not re-derive them from prose.
4. **Read `dm_directors_notes_v1.md`** — the standing loops, scheduled beats, running clocks, and the most recent `[S-N]` close-summary block, which names exactly what is owed, spent, and carried into this session.
5. **Read the glossary (Appendix B) before narrating anything.** Old session and arc files use retired terms; the glossary converts them on sight (the old metal ranks → the new guild ranks; old progression terms → points / Delver Level; **"Forceread" → Deep Inspection** where read as current; **the old six-grade rarity ladder / "Epic" → the four-tier scarcity scale**). A retired term echoed into narration is a continuity error — this read prevents it.
6. **Just-in-time entity pull (the rule that prevents mis-narration).** Before narrating any scene that turns on a **named NPC, location, item, deal, rank, or established fact**, pull that entity's current entry first — an NPC from its `npcs/` file (or, until it has one, `campaign_state.md`'s roster + the archives); a tracked value from the JSON that owns it; a thread from `campaign_state.md`; a closed outcome from `resolved_threads.md`. Do **not** narrate a named entity or a current number from memory or a search fragment. If two passes of searching don't surface the entity, say so plainly rather than inventing a version. *(One wrong pull corrupts continuity as badly as a contradiction; see §9.)*
7. **Read the `npcs/` files for any NPC in play this session** (per the resume point's roster). Read a DM-only truth file, a catalog, `mystery_anchors_v1.md`, or the active location file (e.g. `infernal_dungeon_the_ashen_descent.md`) only as a scene approaches its subject — not as routine. Consult `living_world_truth_v1.md` when Bill reads the newspaper, hears depot talk, or reaches toward the wider world.
8. **Read a `Session_N.md` or arc file only for a specific archived detail.** Do not re-read the history in full each session — the story-so-far in `campaign_state.md` replaces that. For a *closed* thread's outcome, check `resolved_threads.md` first.
9. **Confirm before playing.** State back, in one or two lines, exactly where we are, what's live, and whose move it is. A read-back to catch a mis-load before it becomes a mistake.

**Where each fact comes from:** a current sheet number → `bill_weaver_sheet.json`; a price → `pricing.json`; a crew stat → `fortunes_folly_crew.json`; an NPC's warmth → the sheet's `relationships`; what an NPC knows or how they sound → their `npcs/` file; what happened before → `campaign_state.md` story-so-far, then the arc files; a rule → `game_bible.md`/the catalogs; a hidden truth → the DM truth files.

---

## 2. Save-point protocol

A SavePoint is a **mid-session marker** capturing the exact stop-state so play resumes precisely across a context break. **A SavePoint is not a close** — `campaign_state.md` and the JSONs are NOT rewritten at a SavePoint; the running numbers stay live in the SavePoint's deltas until the session actually closes.

**When to make one:** stopping or pausing mid-session without reaching a close (the context window filling, or simply pausing play).

**Format** (the model is the Session 30 SavePoint):
- **Header** — WHEN (in-world date/time), WHERE (exact location), and the live-moment framing.
- **Exact stop — the live moment** — whose move it is; what is resolved and what is not.
- **What happened this session so far** — numbered beats.
- **Sheet deltas off the session open** — only what changed (ammo, mana, money, warmth, etc.); the full sheet stays in the JSON. **Reflect every change-tag fired so far (§4)**, so nothing is lost across the break.
- **Live field** — scene/combat state: enemies, hazards, positions.
- **Still owed / deferred.**
- **Resume point** — one paragraph: exactly where, what's live, whose call.

**Rules:**
- The most recent SavePoint is **source-of-truth for the exact stop**, over any older state or clone.
- **Name** it `Session_<N>_SavePoint_<k>.md`, incrementing `k`.
- It is a **working file**: kept until the session closes, then its content is folded into the close (§3) and the SavePoint is retired (git history keeps it).

---

## 3. Close-out protocol (in order)

**STANDING CONVENTION — file delivery (rewrite-and-post; the player pushes).** The assistant cannot commit to the GitHub repo; the repo is the player's to write. Whenever the player asks to "update," "advance," or "fix" any game file — at session close or mid-session — this means: the assistant **rewrites the file (or a scoped update block) in full and POSTS it as a downloadable document, and the player replaces the file in GitHub.** JSONs, save points, authored canon, and new rules files are delivered the same way. The assistant never assumes a file is live in the repo until the player confirms the push.

**Step 0 — Identify the changed files, and pull each in full before rewriting it (the gate).** Before writing anything, list every file this session moved: always `bill_weaver_sheet.json`, `campaign_state.md`, and the new `Session_N.md`; plus `fortunes_folly_crew.json` if a crew stat changed; `pricing.json` if a price changed; the engaged `npcs/` files; `resolved_threads.md` if a thread closed or an archive needs errata; and `living_world_truth_v1.md` / `dm_directors_notes_v1.md` if anything offstage or any plan/clock moved. **For each file you will rewrite, read its current full text first** — a faithful rewrite is impossible from memory or search fragments, and a partial rewrite silently drops standing content. If a file genuinely cannot be read whole, advance it with an explicit, scoped **update block** rather than a full rewrite, and say so. Never produce a "delta only because I didn't read it" rewrite.

1. **Gather the close ledger.** Aggregate every change-tag fired this session (§4) into one block: the net final values for ammo by type, mana, the money lines, attributes/skills, ability levels, delver/class level, and relationship warmth. This is the single list the JSON updates copy from.
2. **Update the JSON authority layer from the ledger** — `bill_weaver_sheet.json` (sheet/money/inventory/relationships), `fortunes_folly_crew.json` (if crew stats changed), `pricing.json` (if prices changed). One copy-down per field; no value re-derived from prose. **Bump each touched JSON's `current_to` stamp.** This is what kills the recurring coin/sheet-drift problem — do it every session.
3. **Write the session's write-once body** — `Session_N.md`, the dated record of what happened (the recap contents in §5). Created once; **never edited afterward** (corrections to a past archive go in `resolved_threads.md`'s errata block — step 6 — never back into the archive). Consolidated into an arc file every fifth session (step 10).
4. **Rewrite `campaign_state.md` in place — every session, without exception.** Refresh the story-so-far, the live threads/clocks, the NPC roster (note standings that shifted), and reset the resume point and any "⚠ DM owed" block. **Pointers only — do not restate JSON numbers** (the sheet, money, prices, crew stats, and warmth live in the JSONs; `campaign_state.md` points to them). Rewrite, do not append, so the file stays about the same length session over session. The state doc is never allowed to lag the latest session. **Bump `current_to`.**
5. **Update the `npcs/` files.** For each NPC engaged: append the key exchange (dated, session-ref'd; key beats, not a transcript) and update the relationship texture if it shifted. The warmth *number* was already updated in the sheet (step 2).
6. **Move resolved threads to `resolved_threads.md`.** In the same motion as the prune in step 4, every genuinely-closed thread leaves `campaign_state.md` and lands here with its outcome — what it was, how it resolved, the session it closed in, and a pointer to the archive holding the full detail. Outcome-only; do not re-narrate. This file also holds the **errata block**: corrections to write-once archives live here, never edited into the archive.
7. **Run the skill/attribute audit against `game_bible.md` §§3, 5, 6, 12** and apply ticks to `bill_weaver_sheet.json` (step 2). State each award and each held gate with its reason; bank gains earned but gated on a future event. No within-band attribute tick without real training in play; no growth past 20 and no points without an open core.
8. **Advance the DM truth files if anything offstage moved** — `living_world_truth_v1.md` (small and caused, reason logged), and `dm_directors_notes_v1.md` (mark spent beats SPENT with the session number, move clocks, prune overtaken plans, append a new `[S-N]` close-summary block, log every System ruling and price in its ledger). Per Step 0, read each file (or produce a scoped update block) before advancing it.
9. **Retire the SavePoint(s)** for the session — their content is now folded in.
10. **Consistency check, then (every fifth session) consolidate.** Verify: the ledger's final values match the JSONs; `campaign_state.md`'s resume point matches reality; no references to deleted files; all `current_to` stamps bumped to this session. On every fifth close, **consolidate** the just-finished block into its arc file (§11 — combine, lore-correct, pare), tag the pre-consolidation commit, and retire the raw five session bodies.
11. **Tell the player exactly what to do in the project:** which JSONs to replace, which living files to replace, which `npcs/` files to add or replace, the new session body to add, what to append to `resolved_threads.md`, and what is deliberately left alone. Name every file touched and every file left alone.

---

## 4. The change-tag rule

**Whenever a tracked value changes during play, surface it inline in a bold-bracketed tag at the moment of change, showing the delta and/or the resulting value.** This keeps the JSON-owned numbers visible in context so the player can log them, and so the close ledger (§3 step 1) is a copy-down rather than a hunt through prose.

```
[Hellfire fired this turn: 3]   [Hellfire in magazine: 7]   [Hellfire total: 33]
[Relationship: Mrs. Maddox +2]   [Relationship: Mrs. Maddox: 86]
```

**What gets tagged:** anything a JSON owns — ammo by type, mana, cash and the money lines, attributes/skills/ability levels when they change, delver and class level, and relationship warmth. Not trivial flavor; only values that map to a field the player will update. **Keying:** a relationship tag uses the NPC's canonical name, matching the key in the sheet's `relationships` block, so a tag maps to exactly one field.

---

## 5. The recap contents

The recap (in the session body, and reflected as pointers-and-narrative in the state doc): location; date or rough time; health, wounds, fatigue, conditions, mana; credits and debts; ammunition; weapons, armor, meaningful inventory; companions, hirelings, allies, rivals, enemies; active quests, contracts, bounties, obligations; known factions and current reputation; important NPCs; clues, rumors, mysteries, unresolved threads; consequences in motion; next obvious options. (The exact current *numbers* among these live in the JSONs; the body records them as the dated state at close.)

---

## 6. The rules that keep it lean — and keep it true

- **One current value per fact.** The JSON holds the current number; the session body and arc files hold dated history; `campaign_state.md` holds current narrative and *points* at the JSON for values; `resolved_threads.md` holds closed outcomes. Nothing lives authoritatively in two places.
- **Rewrite, never append** (the living markdown). Prune on every update — but prune correctly (below).
- **Resolved vs. compressed — the rule that stops live threads from being flattened.** A **resolved** thread is genuinely closed — it *leaves* `campaign_state.md` and moves to `resolved_threads.md` with its outcome. A **live or pending** thread *stays* and may be written shorter, but **its status tag and its pointer may never be dropped.** Shortening a live fact is not the same as the fact being settled.
- **Status-and-pointer discipline.** Every live thread in the state doc carries (a) a **status tag** when it isn't obvious — *live / pending / standing-indefinitely* — and (b) a **pointer** to where its full record lives. The few load-bearing items also carry a short **"do not compress"** flag. Narrative history does not go in the state doc — the archives, arc files, and `resolved_threads.md` are for that; the state doc carries the current narrative, its status, and a pointer.
- **Closed-event vs. standing-thing.** Only genuinely-closed *events* go to `resolved_threads.md`. A thing that *happened* but remains operative — a standing protection, a live relationship condition, an open fork — stays live in the state doc even though its triggering event is past.
- **Filename discipline (this stops version sprawl).** The living files and JSONs always keep the **same filename** — `campaign_state.md`, `bill_weaver_sheet.json`, never `_v5` or a `-1` copy. The only files that increment are the session archive (`Session_11.md`, …) and the arc files (`sessions_06-10.md`, …), each a distinct dated record. If a duplicate or version-suffixed copy of a living file ever appears, delete the older one — overlapping copies are how a superseded fact resurfaces.
- **What never changes at session end.** `game_bible.md`, this file, the four mystery truth files, the seven catalogs, and `essence_aspects_v1.md` move only when a rule or the world is deliberately changed — never as part of normal play. The exceptions advanced at close are `living_world_truth_v1.md` and `dm_directors_notes_v1.md`. `mystery_anchors_v1.md` changes only when a new mystery's answer must be fixed.

---

## 7. The character sheet and the JSON authority layer

Bill's sheet is **`bill_weaver_sheet.json`** — attributes, mundane skills, cultivation/abilities, gear, ammunition, money, banked cores/captures, and the `relationships` block. It is the authority for every one of those values; the skill/attribute audit (§3 step 7) applies ticks there, and the change-tag/close-ledger (§4, §3 step 1) feed it. The crew's mechanical data is **`fortunes_folly_crew.json`**; all prices are **`pricing.json`**. `campaign_state.md` no longer holds a sheet, money table, price book, or crew stats — it points to these. *(Older references to a sheet "inside `campaign_state.md`" or to `Bill_Weaver_Character_Sheet.*` are retired — Appendix B.)*

---

## 8. The relationship / warmth system

Each recurring NPC carries a **1–100 warmth** value toward Bill, stored in `bill_weaver_sheet.json` → `relationships` (with a per-NPC `ceiling`). The **band definitions** (Hostile → Bonded) and the starting/movement/ceiling/visibility rules live once in **`game_bible.md` §4**; read the band off the number, never store it. **Bill never sees the number** — he reads warmth from behavior; it surfaces to the player only through the change-tag (§4). NPC files carry relationship *texture* and history, not the number. At close, a warmth change is copied into the sheet (§3 step 2) and the NPC file's texture updated if it shifted (§3 step 5).

---

## 9. Continuity

Maintain continuity carefully — names, places, injuries, promises, debts, inventory, faction reactions, relationship changes. If uncertain about a past fact, say so and make the smallest reasonable assumption or ask. Do not casually retcon established facts.

**When the player references canon you don't recognize.** If the player speaks as though something is already established — a name, person, place, item, rule, event, debt, or relationship — and you don't recognize it, do not contradict it, brush it aside, or invent a version on the spot. First read the file or files most likely to hold it, using Appendix C to choose where to look, and read enough to actually find it. Only after checking: if it is there, treat it as canon and continue; if it is genuinely in none of the files, say so plainly and either ask or make the smallest reasonable assumption and note it. Treating a real established fact as unknown corrupts continuity as badly as contradicting one.

**Precedence when records conflict:** `game_bible.md` first for rules; the **JSON authority layer** for any tracked value (a number); `campaign_state.md` for current narrative state; `resolved_threads.md` for the outcome of a closed thread; then the most recent arc/session file. Older archives are dated history and do not override newer state. Where a write-once archive contains an error, the correction lives in `resolved_threads.md`'s errata block and wins over the archive's wrong figure — the archive is left intact as the dated record. `gm_operations.md` governs procedure but never overrides canon or a JSON value.

---

## Appendix A — Companion files and when to read them

**Project manifest — the project should contain exactly these files, and nothing else.** Anything not on this list is superseded cruft: delete it (Appendix B says what each retired file became). A duplicate or version-suffixed copy of a living file or JSON is the main way a stale fact resurfaces — there is only ever one current copy, under the canonical name.

- **Authority layer (JSON; values only):** `bill_weaver_sheet.json`, `fortunes_folly_crew.json`, `pricing.json`.
- **Rules & setting (static):** `game_bible.md`; `gm_operations.md` (this file); the seven catalogs (`ability_orbs_v1`, `auras_v1`, `monster_categories_v1`, `cultivation_body_forging_v1`, `dungeon_materials_v1`, `magic_domains_v1`, `ability_framework_v1`); `essence_aspects_v1` and `dungeon_economy_v1` (aspects/filtering/cores and the tier × rarity pricing model); the four truth files (`hollow_reach_truth_v3`, `system_engineer_truth_v1`, `delve_progression_truth_v1`, `system_cosmology_truth_v1`); `mystery_anchors_v1`.
- **Living (rewritten or advanced at session close):** `campaign_state.md`, `resolved_threads.md`, `living_world_truth_v1.md`, `dm_directors_notes_v1.md`.
- **NPC reference:** `npcs/` — one file per recurring NPC: `_index.md` (the roster), `pearce.md`, `calloway.md`, `doss.md`, `hessler.md`, `pickering.md`, `mrs_maddox.md`, `pem.md`, `tasker.md`, `the_gunsmith.md`, `the_firm.md`, `the_mission.md`, `the_dunmore_brothers.md`, `fortunes_folly.md`. (Add a file when a new NPC becomes a standing speaking part; until then a one-off lives in `campaign_state.md`'s roster.)
- **History (write-once):** the closed-block arc files `sessions_01-05.md`, `sessions_06-10.md`, `sessions_11-15.md`, `sessions_16-20.md`, `sessions_21-25.md`, plus — for the still-open block — the raw `Session_26.md` … `Session_29.md` bodies and the live S30 SavePoint, which consolidate into `sessions_26-30.md` once Session 30 closes. (Once a block's arc file exists, its raw `Session_N.md` bodies — and any `Session_N_closeout.md` sheets — are retired to git history under the `pre-consolidation-snapshot` tag, not kept in the project.)
- **Active location:** `infernal_dungeon_the_ashen_descent.md` while the Ashen Descent runs.
- **Map:** `Updated_Map.png`.
- **Working scaffolding:** a current `Session_<N>_SavePoint_<k>.md` may sit in the project until the session closes; once folded in (§3 step 9), retire it.

DM-only, read as the story approaches their subjects (never reveal directly): `hollow_reach_truth_v3.md` (central mystery), `system_engineer_truth_v1.md` (Bill's awakening/System), `delve_progression_truth_v1.md` (the layer beneath Bible §12), `system_cosmology_truth_v1.md` (the cross-world cosmology — deepest spoiler), `living_world_truth_v1.md` (offstage world; advanced at close), `mystery_anchors_v1.md` (fixed answers to minor mysteries).

Reference, pull when a scene needs them: the seven catalogs and `essence_aspects_v1.md`.

---

## Appendix B — Glossary of renamed and retired terms (for reading old session and arc files)

Old archives used earlier names since corrected. When reading them, convert:
- "The Veyrish Territories" / "Veyrish Territory" → **Oregon Territory.**
- "The Meridian States" → **the East** ("Meridian" survives only in the *Meridian Rail Combine*, a company name).
- *Veyrish Clarion* → ***Oregon Clarion***.
- "Bureau of Thaumaturgic Licensure" → **U.S. Bureau of Delving (USBD).**
- "Order of Saint Veyr" → **the Catholic Church** (the New Abilene mission is Catholic; Sister Beatrice is a nun there).
- All dollar/cent amounts → **credits** (1¢ = 1 cr).
- The "~10 years" timeline in Session 2 → **twelve years** (Appearance 1850, now 1862).
- "drummer" → **traveling salesman** in narration (characters may still say "drummer" in dialogue).
- Old metal license ranks → new guild ranks (Bible §19): **Bronze → Rookie; Iron → Member; Silver → Senior Member; Gold → an officer rank (Captain by default).** An NPC described as an *officer* who held an old metal rank converts to an **officer** rank — Doss is a **1st Lieutenant**. The old **Black Seal** is now the **sealed warrant**.

**Progression and ability terms (Bible §12–§13 rework):**
- "+1 to all six attributes" at awakening → **10 points to place** plus the first **choosing**; awakening takes a person from Delver Level 0 to **Delver Level 1**.
- the old "delver level" (= one attribute point) → **points** (one point = one attribute point); **Delver Level** now means **points ÷ 10**.
- old grade payouts (Tin–Platinum = 1–6 levels) → the **points** table: Tin 1, Copper 2, Iron 3, Silver 5, Gold 7, Platinum 10.
- old tier entry (delver level 20/60/120/230) → **Delver Level 5/14/22/36**.
- the **"three kinds"** of abilities → **four**, with **Movement** added.
- mundane competencies once called **"skills (1–10)"** → **mundane skills**, distinct from awakened **Skills**.
- magic domains **Force → Arcane · Vital → Life · Mind → Psionic**; **Space splits** → **Dimensional** (teleport/distance) and **Warding** (sealing/live-warding); the orb **"Vital Read" → "Life Read."**

**Rarity (reworked S30):**
- the old six-grade ladder **Common · Uncommon · Rare · Epic · Legendary · Mythic** → the **four-tier scarcity scale**: Common / Uncommon / Rare (each with Low/Mid/High graduations) / **Unique**. Rarity is *scarcity, not power.*
- **"Epic"** has no slot in the new scale → read an old "Epic" as **High Rare**, or as a **Unique power-tag**, per context.
- **Legendary / Mythic** are no longer ladder grades → they are **power-tags that ride only on Unique items** (see `essence_aspects_v1.md` §8).

**Intrinsic (within-game evolution):**
- **"Forceread"** (the Day-21 intrinsic) → evolved to **Deep Inspection** (Day 26). Read an old "Forceread" as Deep Inspection where it stands for the current intrinsic; keep the original name only when dating the original take or its evolution.

NPC dialogue recorded in old terms is remembered as having used the new ones.

**Retired and renamed files.** Older archives name files since folded in, renamed, or retired. The archives are write-once, so these names stay in their recaps as dated record; when one appears, read it as a pointer to where that thing lives now — do not open the old name.
- `dm_instructions.md`, `world_canon.md`, `world_canon-1.md`, `narration_style.md` → folded into **`game_bible.md`**.
- The session machinery, manifest, glossary, content index → **`gm_operations.md`** (a recap citing "Bible §24" or "Appendix A/B/C" points here).
- `bill_weaver_character.md`, `Bill_Weaver_Character_Sheet.*`, and the character-sheet *section of `campaign_state.md`* → the current sheet is **`bill_weaver_sheet.json`**.
- the **price book** section of `campaign_state.md` → **`pricing.json`**.
- the **crew profiles** (and `emberwaste_delve_team_prep.md`) → **`fortunes_folly_crew.json`** (stats) + the `npcs/` crew file (voice) + the arc files (narrative). *(`emberwaste_delve_team_prep.md` is retired/deleted — its delve was cleared in play.)*
- `wyatt_notes.md` and all the Wyatt-voice notebooks → retired Day 18; current truth is `campaign_state.md` + the JSONs. The in-fiction ciphered notebooks were removed from the fiction (S25) — do not reference them in narration.
- `hollow_reach_truth.md` (and any `_v2`) → **`hollow_reach_truth_v3.md`**.
- `living_world_truth_v1-1.md` → a stale duplicate of `living_world_truth_v1.md`; deleted.
- `special_foundation_delve_S20prep.md` → retired S21 (delve cleared in play).
- `day9_clarion_wire_announcement.md` → folded into **`pricing.json`** (the post-Day-9 telegraph rates).
- `Save_Point*.md` / `Session_*_SavePoint*.md` → working scaffolding; once applied at close, retired (§2, §3 step 9).

---

## Appendix C — Where things live (content index)

When a reference needs checking (§9; §1 step 6), this maps each file to what it holds.

**Tracked values (the authority layer — any current number):**
- **`bill_weaver_sheet.json`** — Bill's attributes, mundane skills, cultivation/abilities, gear, ammunition, money, banked cores/captures, and NPC warmth (`relationships`).
- **`fortunes_folly_crew.json`** — the four crew members' stats, gear, abilities, credits.
- **`pricing.json`** — every credit figure, value band, and the rarity/tier pricing model.

**Current narrative — the town, the people, the money picture, the plots:**
- **`campaign_state.md`** — story-so-far; live threads, contracts, deadlines, clocks; the NPC roster (with pointers to `npcs/` and to the sheet's warmth); the resume point. The first place to look for anything *current and narrative*. (Values are pointed-to, not held here.)

**NPC reference:**
- **`npcs/<name>.md`** — a recurring NPC's role, what they know about Bill, relationship texture, voice, and key exchanges.

**Rules and setting:**
- **`game_bible.md`** — the system and the world, incl. the warmth-band definitions.
- **`gm_operations.md`** (this file) — the protocols, the change-tag rule, the manifest, this index, the glossary.

**Closed history:**
- **`resolved_threads.md`** — every closed thread with its outcome and a pointer, plus the errata block.

**Worldbuilding catalogs (pull mid-scene):**
- `ability_orbs_v1.md`, `auras_v1.md`, `monster_categories_v1.md`, `dungeon_materials_v1.md`, `cultivation_body_forging_v1.md`, `magic_domains_v1.md`, `ability_framework_v1.md`, `essence_aspects_v1.md` (aspected essence, filtering, cores, weave-copying, and the rarity scale §8), `dungeon_economy_v1.md` (the tier × rarity pricing model behind `pricing.json`).

**DM-only (inform yourself; never reveal directly):**
- `living_world_truth_v1.md`, `mystery_anchors_v1.md`, `dm_directors_notes_v1.md`, `hollow_reach_truth_v3.md`, `system_engineer_truth_v1.md`, `delve_progression_truth_v1.md`, `system_cosmology_truth_v1.md`.

**Active location:**
- `infernal_dungeon_the_ashen_descent.md` — the current double-dungeon run, floor by floor.

**Dated history:**
- the current block's `Session_N.md` bodies and the closed-block arc files `sessions_01-05.md` … — write-once records. Don't re-read in full as routine.

**Map:**
- `Updated_Map.png`.
