# GM OPERATIONS — running the campaign

*The operational companion to `game_bible.md`. The Bible says what is true (rules and setting that change only by deliberate decision); this file says how to run and maintain the campaign session to session — the start and close protocols, the file manifest and reading guide, the glossary of renamed terms, and the content index. This file never overrides canon: where it touches a rule, `game_bible.md` wins. Read this file and the Bible together at the start of every session, alongside the current `campaign_state.md`.*

---

## 1. Start-of-session protocol

1. **Read `game_bible.md`, `gm_operations.md` (this file), and `campaign_state.md` in full.** Between them they hold the rules, the running machinery, the setting, and all current state (story-so-far, the sheet, money, reputations, threads, the town, prices, the resume point). The state doc's resume point and its "⚠ DM owed" block are the first things to honor.
2. **Read `dm_directors_notes_v1.md`** — the standing loops, scheduled beats, running clocks, and the most recent close-summary block (the `[S-N]` entry), which names exactly what is owed, spent, and carried into this session.
3. **Read the glossary (Appendix B) before narrating anything.** Old session files use retired terms; the glossary converts them on sight (for example "Iron rank" → an *officer* rank; "drummer" → traveling salesman; the old metal ranks → the new guild ranks; old progression terms → points / Delver Level). A retired term echoed back into narration is a continuity error — this read prevents it.
4. **Just-in-time entity pull (the rule that prevents mis-narration).** Before narrating any scene that turns on a **named NPC, location, item, deal, rank, or established fact**, pull that entity's current entry first — from `campaign_state.md` (the NPC list, threads, sheet, price book) and, if the entity is described only in older text, from the session file or `resolved_threads.md` via Appendix C. Do **not** narrate a named entity from memory or from a search fragment. If two passes of searching do not surface the entity, say so plainly rather than inventing a version. *(This is the discipline whose absence has produced mis-narration: a teacher's trade and an NPC's rank narrated from a stale impression instead of the current entry. One wrong pull corrupts continuity as badly as a contradiction; see §6, "When the player references canon you don't recognize.")*
5. **Pull a DM-only truth file, a catalog, or `mystery_anchors_v1.md` only as a scene approaches its subject** — not as routine. Consult `living_world_truth_v1.md` when Bill reads the newspaper, hears depot talk, or reaches toward the wider world.
6. **Read a `Session_N.md` only for a specific archived detail.** Do not re-read the session files in full each session — the story-so-far in `campaign_state.md` replaces that, and re-reading the dated records wastes context and re-teaches the old dense prose. For a *closed* thread's outcome, check `resolved_threads.md` first; it consolidates those with pointers, so you rarely have to open an archive.

---

## 2. End-of-session protocol (in order)

**STANDING CONVENTION — file delivery (rewrite-and-post; the player pushes).** The assistant cannot commit to the GitHub repo; the repo is the player's to write. Whenever the player asks to "update," "advance," or "fix" any game file — at session close or mid-session — this means: the assistant **rewrites the file (or a scoped update block) in full and POSTS it as a downloadable document, and the player replaces the file in GitHub.** Save points, authored canon, and new rules files are delivered the same way. The assistant never assumes a file is live in the repo until the player confirms the push. (Added S21.)

**Step 0 — Identify the changed files, and pull each in full before rewriting it (the gate).** Before writing anything, list every living file this session moved: always `campaign_state.md` and the new `Session_N.md`; plus `resolved_threads.md` if a thread closed or an archive needs errata; plus `living_world_truth_v1.md` and/or `dm_directors_notes_v1.md` if anything offstage or any plan/clock moved. **For each file you will rewrite or advance, read its current full text first** — a faithful rewrite is impossible from memory or from search fragments, and a partial rewrite silently drops standing content. If a file genuinely cannot be read whole, advance it with an explicit, scoped **update block** (named-section edits / moved clocks / a new close-summary entry) rather than a full rewrite, and say so. Never produce a "delta only because I didn't read it" rewrite of a file that needed reading.

1. **Reconcile money and consumables to one current figure.** Settle the day's pocket, tab, ammunition, and any debts to a single audit line. This is what kills the recurring coin-correction problem — do it every session.
2. **Write a new `Session_N.md`** — the dated, write-once archive of what happened this session (the recap contents in §3 below). Created once; **never edited afterward** (corrections to a past archive go in `resolved_threads.md`'s errata block — see step 4 — never back into the archive).
3. **Rewrite `campaign_state.md` in place — every session, without exception.** Refresh the story-so-far, update the sheet to current values, prune *resolved* threads (and only resolved ones — see "resolved vs. compressed" in §4), demote inactive contacts to a short dormant line, reset the resume point and the "⚠ DM owed" block. Rewrite, do not append, so the file stays about the same length session over session. **The state doc is never allowed to lag the latest session** — if a thing was true in play this session, it is current here at close. (The Day-11 failure that prompted this rule: a companion record was updated and the state doc was left a session behind, so it carried stale money and a flattened agreement into the next session. Do not repeat it.)
4. **Move resolved threads to `resolved_threads.md`.** In the same motion as the prune in step 3, every genuinely-closed thread leaves the state doc and lands here with its outcome — what it was, how it resolved, the session it closed in, and a one-line pointer to the `Session_N.md` holding the full detail. Outcome-only; do not re-narrate. This file is the consolidated answer to "whatever happened with X?" so history is found in one place without opening archives. It also holds an **errata block**: corrections to write-once archives (a wrong figure, a stale standing balance recorded in a past `Session_N.md`) are noted here, never edited into the archive itself, so the immutable record stays immutable and the correction still lives in one known place.
5. **Run the skill/attribute audit against `game_bible.md` §§3, 5, 6, 12** and apply ticks to the sheet in step 3. State each award and each held gate with its reason; bank gains that are earned but gated on a future event (for example a subskill bump that lands when a designed thing is actually fabricated). No within-band attribute tick without real training in play; no growth past 20 and no points without an open core.
6. **Advance `living_world_truth_v1.md` if anything offstage moved** — small and caused, with the reason logged. Most sessions little moves; breakthroughs are rare. In the same pass, **advance `dm_directors_notes_v1.md`:** mark spent beats SPENT with the session number, move the clocks, prune overtaken plans, append a new `[S-N]` close-summary block, and (post-awakening) log every System ruling and price in its rulings ledger. Per Step 0, read each file (or produce a scoped update block) before advancing it.
7. **Tell the player exactly what to do in the project:** add the new session file; replace `campaign_state.md` and any other living file that moved; append to `resolved_threads.md`; leave everything else. Name every file touched and every file deliberately left alone.

---

## 3. The recap contents

The recap (in the session file and reflected in the state doc): location; date or rough time; health, wounds, fatigue, conditions, mana; credits and debts; ammunition; weapons, armor, meaningful inventory; companions, hirelings, allies, rivals, enemies; active quests, contracts, bounties, obligations; known factions and current reputation; important NPCs; clues, rumors, mysteries, unresolved threads; consequences in motion; next obvious options.

---

## 4. The rules that keep it lean — and keep it true

- **One current value per fact.** The session file holds history; the state doc holds now; `resolved_threads.md` holds closed outcomes; nothing lives in two of them at once.
- **Rewrite, never append.** Prune on every update — but prune correctly (below).
- **Resolved vs. compressed — the rule that stops live threads from being flattened.** Pruning a *resolved* thread and shortening a *live* one are different operations, and confusing them is how a real agreement gets lost. A **resolved** thread is genuinely closed — it *leaves* the state doc and moves to `resolved_threads.md` with its outcome. A **live or pending** thread *stays* in the state doc and may be written shorter, but **its status tag and its pointer may never be dropped.** Shortening a live fact is not the same as the fact being settled. (The failure this prevents: a pending two-outfit alliance was pruned down to one line about a sub-detail, as though shortening it had resolved it, and the live agreement vanished from the records for several sessions.)
- **Status-and-pointer discipline.** Every live thread in the state doc carries (a) a **status tag** when it isn't obvious — *live / pending / standing-indefinitely* — and (b) a **pointer** to where its full record lives (a `Session_N.md`, or `resolved_threads.md`). The few load-bearing items — standing agreements, protections, open forks — also carry a short **"do not compress"** flag. This is what lets the state doc stay lean (the line is short; the detail is pointed-to, not copied in) without a fact being misread as smaller than it is. Narrative history does *not* go in the state doc — that is what the archives and `resolved_threads.md` are for; the state doc carries the current value, its status, and a pointer, nothing more.
- **Closed-event vs. standing-thing.** Only genuinely-closed *events* go to `resolved_threads.md`. A thing that *happened* but remains operative — a standing protection, a live relationship condition, an open fork inside an otherwise-finished event — stays live in the state doc even though its triggering event is in the past. (Examples that must stay live: a poison-pill account that still publishes on a death; a trustee's standing condition that still governs the relationship; an awakening fork that remains open and unspent after the assay that recorded it closed.)

### Filename discipline (this stops version sprawl)

- The living files always keep the **same filename** — `campaign_state.md`, never `_v5`. Replacing them in the project leaves no duplicate behind.
- The **only** file that increments is the session archive: `Session_10.md`, `Session_11.md`, and so on, each a distinct dated record.
- No `-1` copies, no version numbers on the living files. If a duplicate ever appears in the project, delete the older one — overlapping copies are how a superseded fact gets surfaced by mistake.

### What never changes at session end

`game_bible.md`, `gm_operations.md` (this file), the four mystery truth files (`hollow_reach_truth_v3`, `system_engineer_truth_v1`, `delve_progression_truth_v1`, `system_cosmology_truth_v1`), and the seven catalogs move only when a rule or the world is deliberately changed — never as part of normal play. The exceptions are `living_world_truth_v1.md` and `dm_directors_notes_v1.md`, which are built to be advanced at session close (see §2 step 6). `mystery_anchors_v1.md` sits with the static files: it changes only when a new mystery's answer must be fixed, never as part of normal play.

---

## 5. The character sheet

The character sheet lives **inside `campaign_state.md`** as a section, not as a separate file. It is rewritten in place with the rest of the state doc every session (§2 step 3), and the skill/attribute audit (§2 step 5) applies its ticks there. There is no standalone sheet file; older references to `Bill_Weaver_Character_Sheet.*` are retired (Appendix B).

---

## 6. Continuity

Maintain continuity carefully — names, places, injuries, promises, debts, inventory, faction reactions, relationship changes. If uncertain about a past fact, say so and make the smallest reasonable assumption or ask. Do not casually retcon established facts.

**When the player references canon you don't recognize.** If the player speaks as though something is already established — a name, person, place, item, rule, event, debt, or relationship — and you don't recognize it, do not contradict it, brush it aside, or invent a version on the spot. First do a thorough reading of the file or files most likely to hold it, using the content index in Appendix C to choose where to look, and read enough to actually find it rather than skimming. Only after checking: if it is there, treat it as canon and continue; if it is genuinely in none of the files, say so plainly and either ask the player or make the smallest reasonable assumption and note it, so a new fact gets established cleanly instead of guessed. Treating a real established fact as unknown corrupts continuity as badly as contradicting one. (This is the same discipline the start-of-session just-in-time entity pull enforces — see §1 step 4.)

**Precedence when records conflict:** `game_bible.md` first, then `campaign_state.md` for current state, then `resolved_threads.md` for the outcome of a closed thread, then the most recent session file. Older session files are dated history and do not override newer state. Where a write-once archive is known to contain an error, the correction lives in `resolved_threads.md`'s errata block and wins over the archive's wrong figure — the archive is left intact as the dated record, but the errata note is authoritative on that specific point. `gm_operations.md` governs procedure but never overrides canon.

---

## Appendix A — Companion files and when to read them

**Project manifest — the project should contain exactly these files, and nothing else.** Anything in the project not on this list is superseded cruft: delete it (Appendix B says what each retired file became). A duplicate or a version-suffixed copy of a living file is the main way a stale fact resurfaces — there is only ever one current copy, under the canonical name.
- **Rules & setting (static):** `game_bible.md`; `gm_operations.md` (this file); the seven catalogs (`ability_orbs_v1`, `auras_v1`, `monster_categories_v1`, `cultivation_body_forging_v1`, `dungeon_materials_v1`, `magic_domains_v1`, `ability_framework_v1`); `essence_aspects_v1` (added S21 — aspected essence, filtering, banking, cores, essence-touched craft, weave-copying); the four truth files (`hollow_reach_truth_v3`, `system_engineer_truth_v1`, `delve_progression_truth_v1`, `system_cosmology_truth_v1`); `mystery_anchors_v1`. *(`special_foundation_delve_S20prep.md` is RETIRED as of S21 — its delve was cleared in play; delete it.)*
- **Living (rewritten or advanced at session close):** `campaign_state.md` (which contains the character sheet), `resolved_threads.md`, `living_world_truth_v1.md`, `dm_directors_notes_v1.md`.
- **Dated history (write-once):** `Session_1.md` through the latest session file.
- **Map:** `Updated_Map.png`.
- **Optional:** the current session's close-out working sheet may sit in the project until applied; once its deltas are folded into `campaign_state.md` and `resolved_threads.md`, delete it.

Read every session, with `game_bible.md`:
- **`campaign_state.md`** — all live state: story-so-far, character sheet, money, reputations, active threads and clocks, the New Abilene map, prices, resume point.
- **`gm_operations.md`** (this file) — the session protocols, manifest, glossary, and content index.
- **`resolved_threads.md`** — the consolidated archive of genuinely-closed threads with their outcomes, plus the errata block correcting known write-once-archive errors. Consulted (not necessarily read in full each time) as the one place to answer "whatever happened with X?" without digging through session files; rewritten/appended at session close as threads resolve.
- **`dm_directors_notes_v1.md`** — the DM's living plan: standing session loops, scheduled beats, near-term escalations, the post-awakening System rulings ledger, and the idea bench. Read at session start; advanced at session close.

DM-only, read as the story approaches their subjects (never reveal directly):
- **`hollow_reach_truth_v3.md`** — the central mystery.
- **`system_engineer_truth_v1.md`** — Bill's anomalous awakening; dormant until the core opens.
- **`delve_progression_truth_v1.md`** — the hidden layer beneath Bible §12.
- **`system_cosmology_truth_v1.md`** — the cross-world cosmology behind the curriculum (why the dungeons exist, who built them, the other worlds). Final-architecture; defers to the three files above; the deepest spoiler in the campaign.
- **`living_world_truth_v1.md`** — the offstage world tracker (living; advanced at session close). Its public items surface when Bill reads the *Clarion* or hears the town; never read aloud as itself.
- **`mystery_anchors_v1.md`** — fixed DM-only answers to the minor mysteries in the threads list, so clues stay solvable and improvisation can't drift. Defers to the four truth files on their subjects; read when a scene approaches an anchored item.

Reference, pull when a scene needs them:
- **`ability_orbs_v1.md`**, **`auras_v1.md`**, **`monster_categories_v1.md`**, **`cultivation_body_forging_v1.md`**, **`dungeon_materials_v1.md`**, **`magic_domains_v1.md`**, **`ability_framework_v1.md`**.

Dated history (write-once; do not re-read in full — the current "story so far" in `campaign_state.md` replaces them):
- **`Session_1.md`** through the latest session file.

---

## Appendix B — Glossary of renamed and retired terms (for reading old session files)

Old session files used earlier names since corrected. When reading them, convert:
- "The Veyrish Territories" / "Veyrish Territory" → **Oregon Territory.**
- "The Meridian States" → **the East** ("Meridian" survives only in the *Meridian Rail Combine*, a company name).
- *Veyrish Clarion* → ***Oregon Clarion***.
- "Bureau of Thaumaturgic Licensure" → **U.S. Bureau of Delving (USBD).**
- "Order of Saint Veyr" → **the Catholic Church** (the New Abilene mission is Catholic; Sister Beatrice is a nun there).
- All dollar/cent amounts → **credits** (1¢ = 1 cr).
- The "~10 years" timeline in Session 2 → **twelve years** (Appearance 1850, now 1862); everything else in that session's corrections still stands.
- "drummer" → **traveling salesman** in narration (characters may still say "drummer" in dialogue).
- Old metal license ranks → new guild ranks (Bible §19): **Bronze → Rookie; Iron → Member; Silver → Senior Member; Gold → an officer rank (Captain by default).** Provisional is unchanged. An NPC described as an *officer* who held an old metal rank (e.g. "Officer Doss, Iron rank") converts to an **officer** rank, not the rank-and-file equivalent — Doss is a **1st Lieutenant**. The old **Black Seal** is now the **sealed warrant** — a special authority, not a rank.

**Progression and ability terms (renamed in the Bible §12–§13 rework; convert when reading older session text):**
- "+1 to all six attributes" at awakening → **10 points to place** plus the first **choosing**; awakening now takes a person from Delver Level 0 to **Delver Level 1**.
- the old "delver level" (= one attribute point) → **points** (one point = one attribute point). The term **Delver Level** now means **points ÷ 10** — the completion-record milestone that gates tier entry.
- old grade payouts (Tin–Platinum = 1/2/3/4/5/6 levels per completion) → the **points** table: Tin 1, Copper 2, Iron 3, Silver 5, Gold 7, Platinum 10.
- old tier entry requirements (delver level 20 / 60 / 120 / 230) → **Delver Level 5 / 14 / 22 / 36**.
- the **"three kinds"** of abilities (actives, passives, intrinsics) → **four**, with the **Movement** category added.
- mundane competencies once called **"skills (1–10)"** → **mundane skills**, to separate them from the awakened **Skills** layer (Active, Passive, Movement, Intrinsic).
- magic domains **Force → Arcane · Vital → Life · Mind → Psionic**. **Space splits**: its teleport-and-distance work → **Dimensional**, its sealing and live-warding work → **Warding**. **Spirit** keeps its name. **Transmutation, Summoning, Divination,** and **Warding** are new domains with no old equivalent.
- the ability orb **"Vital Read" → "Life Read."**

NPC dialogue recorded in old terms is remembered as having used the new ones.

**Retired and renamed files (for reading old session bodies).** Older session files name files that have since been folded in, renamed, retired, or consolidated. The archives are write-once, so these names stay in their recaps as dated record; when one appears, read it as a pointer to where that thing lives now — do not open the old name, it should no longer exist in the project.
- `dm_instructions.md`, `world_canon.md`, `world_canon-1.md`, `narration_style.md` → all folded into **`game_bible.md`** (the voice and narration rules are now §2).
- The session-structure machinery, the file manifest, the glossary, and the content index → **moved out of `game_bible.md` (§24 + appendices) into `gm_operations.md`** (Day 18). A recap that cites "Bible §24" or "Appendix A/B/C" points to the matching section of `gm_operations.md` now.
- `bill_weaver_character.md`, `Bill_Weaver_Character_Sheet.docx` / `_v2` / `_v3` / `_v4` → the current sheet is the character-sheet section of **`campaign_state.md`**. (A recap that logs a sheet change — e.g. "updated to v3; Presence 8→9" — stays as the dated audit trail of when each gain landed.)
- `wyatt_notes.md`, `wyatt_notes-1.md`, the four-way split (`wyatt_people.md` / `wyatt_places.md` / `wyatt_ledger.md` / `wyatt_board.md`), and the two consolidated notebooks **`wyatt_people_places.md`** / **`wyatt_ledger_board.md`** → **all RETIRED Day 18.** Current truth lives in **`campaign_state.md`**; these files duplicated it in Bill's first-person voice and are no longer maintained. The notebooks still exist *in the fiction* (Bill keeps two ciphered books in the upstairs window casing), but no project file tracks them; if a scene opens a notebook, render its content on the spot from `campaign_state.md`. When an old session recap names a notebook, read it as a pointer to `campaign_state.md`.
- `hollow_reach_truth.md` (and any `_v2`) → **`hollow_reach_truth_v3.md`**.
- `day9_clarion_wire_announcement.md` → folded into the price book in **`campaign_state.md`** (the post-Day-9 telegraph rates).
- `Save_Point*.md`, `Session_*_SavePoint*.md`, and the per-session close-out sheets → working scaffolding; once applied, their content lives in **`campaign_state.md`** and **`resolved_threads.md`**.

---

## Appendix C — Where things live (content index)

When a reference needs checking (see §6, "When the player references canon you don't recognize," and §1 step 4), this maps each file to the kinds of things it holds. Read the file or files listed for the kind of thing in question.

**Current state — Bill, the town, the people, the money, the plots:**
- **`campaign_state.md`** — the first place to look for almost anything *current*. Bill's character sheet (attributes, skills, conditions, mana, gear, ammunition); the running money ledger and established prices; his reputations and legal status; active threads, contracts, deadlines, and clocks; the New Abilene street map and its named locals; the important-NPC list with current relationships; the teaching ledger; and the story-so-far. If the player references a person, place, deal, debt, item, business, or plot thread as established, check here first.

**Rules and setting — things that don't change session to session:**
- **`game_bible.md`** — the system and the world: voice and table conventions, attributes and skills, health and combat, the history and timeline, geography, how dungeons work, delve growth (tiers, grades, payouts), cultivation/essence/mana/magic, magic law, firearms and technology, economy and currency, factions, guild rank, peoples, progression, reputation.
- **`gm_operations.md`** (this file) — how to run and maintain the campaign: the start/close session protocols, the recap contents, the lean-and-true record rules, filename discipline, continuity and precedence, the file manifest, this content index, and the glossary.

**Closed history — the outcomes of threads no longer live:**
- **`resolved_threads.md`** — every genuinely-closed thread with its outcome and a pointer to the `Session_N.md` that holds the full detail, plus the errata block for known write-once-archive errors. Check here when the player references a past *resolved* matter (a finished job, a settled debt, a closed decision) and the state doc no longer carries it because it was correctly pruned. Live and pending threads are NOT here — those stay in `campaign_state.md`.

**Worldbuilding catalogs — specific entries to pull mid-scene:**
- **`ability_orbs_v1.md`** — specific ability orbs: what each does, its mana cost, rarity, legal status.
- **`auras_v1.md`** — specific auras: effects, costs, legal and registration status.
- **`monster_categories_v1.md`** — the monster categories (Beast through Titan): traits, behavior, examples.
- **`dungeon_materials_v1.md`** — dungeon-derived materials (relic steel, deep iron, ghostwood, starfall glass, and kin): properties and uses.
- **`cultivation_body_forging_v1.md`** — the cultivation detail file: cores, the eight inner gates, the outer core, how gates open, Intellect and mana, and spiritual pressure.
- **`magic_domains_v1.md`** — the nine magic domains (Life, Transmutation, Arcane, Dimensional, Psionic, Spirit, Summoning, Divination, Warding), how affinity gates which spells a caster can learn, and the domain economy and licensing. Pull when a caster's reach, a tome's value, or a domain-keyed restriction is in question.
- **`ability_framework_v1.md`** — how a delver's Skills sort into four categories (Active with the Intellect-scaled seated kit, Passive including auras, Movement with its one-seated rule, and Intrinsic with evolutions), how the choosing offers Skills and how declined options lock, and how Skills crystallize into orbs with seating requirements. Pull when a build, a loadout, the choosing, or an intrinsic's growth is in question.

**DM-only — read to inform yourself; never reveal directly:**
- **`living_world_truth_v1.md`** — the offstage world: the wider frontier and the East, the Bureau, Saint Orison, Bill's father, scarce science, the cell's outward footprint, and the newspaper items Bill can read. Check here for anything happening away from Bill.
- **`mystery_anchors_v1.md`** — the fixed answer behind any minor mystery the threads list carries (who, what, why — and how it can be discovered).
- **`dm_directors_notes_v1.md`** — what the DM has planned: loops, beats, clocks, pacing yardsticks, the rulings and price ledger, banked ideas.
- **`hollow_reach_truth_v3.md`** — the central mystery.
- **`system_engineer_truth_v1.md`** — Bill's anomalous awakening and his System (how his delver window differs from everyone else's).
- **`delve_progression_truth_v1.md`** — the hidden mechanics beneath Bible §12.
- **`system_cosmology_truth_v1.md`** — the origin and purpose of the whole dungeon system, how it differs across worlds, and what Special Delves and the sinks truly are. Check here for anything touching the deep 'why' behind the dungeons.

**Dated history:**
- **`Session_1.md`** through the latest session file — write-once records of past sessions. Check a session file when the player references a specific past event and `campaign_state.md` doesn't carry the detail. Do not re-read them in full as routine.

**Map:**
- **`Updated_Map.png`** — the current New Abilene / region map image.
