# SESSION 30 — Floor 1 of the Ashen Descent: The Smoldering Wastes, CLEARED

*Dated archive (`gm_operations.md` §3/§5). Day 28, Sunday, November 23, 1862 (in-fiction; the whole Descent runs on one delve-day). Outcome-and-event record; tracked values live in `bill_weaver_sheet.json` and `fortunes_folly_crew.json`. Closed events → `resolved_threads.md` (S30). DM ledger → `dm_directors_notes_v1.md` (S30 block).*

**ONE LINE:** The crew deposed the **Charred Warden** (Floor-1 boss) — Bill grabbed and **turned the dead prisoner's gaol-key to strip its fire-shield**, the crew ground the stripped boss down, and **Ember drank the freed soul-flood and then the Warden's core whole**. Bill spared/traded with the goblin **Snik**, the crew rested at a lit **Charred Chapel**, and Bill spent the lull on **Deep Inspection Lv.2**, **naming Ember**, his **first rune study**, the **living/spoken-binding** technique, and a full **crew + gun upgrade bench**. NEXT: descend to **Floor 2 — The Obsidian Caldera** (Broodmother Ignite).

---

## THE MECHANICS REVAMP (player-authored, this session)

The session opened by making combat **precise and player-visible**, and locking the tooling:

- **Dice:** all rolls route through the **dice_roller**. A faithful CLI port — `dice_roller.py` — was built (crypto-uniform via `os.urandom` rejection sampling, nat-20/nat-1, PF2e degrees of success: ≥DC+10 crit-success / ≥DC success / ≥DC−9 fail / else crit-fail; nat-20 +1 step, nat-1 −1 step) and the standing rule recorded as **`gm_operations.md` §10**. Calls state expression + modifier + DC before rolling; a result stands.
- **Visibility:** Bill's and the crew's numbers (AC, attack/dmg, DCs, HP, mana) show in **bold-bracket tags**; enemy AC/HP/saves/DCs stay **DM-side**, narrated in words. **Deep Inspection is the inward exception** that reads the hidden enemy layer for Bill (as his plates). Initiative = sorted once by **Speed**, held all fight. 5-second rounds.
- **Seam-shot rule changed:** the coil gun's bond-seam is now **+5 to the attack roll** (1d20 + 10 firearms + 5 seam, needs an active read), **not** the old auto-hit. The gun still "works perfectly" — no manufactured misses; the seam's only honest cost is wear/heat/entanglement.
- **Ability economy locked** (full model in `bill_weaver_sheet.json → abilities._ability_economy`): Deep Inspection cost = base (Sweep 1 / Tight 3 / Hard 6 / Full 12) × range-mult `1 + (ft/5)×0.1` (in-hand ×1) + 0.5 if moving + 1/rd/target held, −⅓ when Ember rides; thread/opposed = full × range + a 1d20+1 contest. Blueprint/drafting: holding is free, pay creation to seat + use to activate. Crafting Table: 5–10 / 15–30 / 60–120 bands. **Ember spends its own ME well**, not Bill's pool (except the larder fills the pool; an over-fielded construct on an empty well drains it).
- **A saves gap was found** and filled provisionally (Fort +5 / Ref +6 / Will +6 = level 2 + trained 2 + attr). **A real saves block is still owed.**

---

## THE CHARRED WARDEN (the boss fight)

**Setup.** The crew held the gate-line; a hex battle-map was rendered. Bill read the Warden full-bore from outside the gates (Deep Inspection Lv.1): a fire-shielded furnace-construct, **heavy fire-shield blunts ~⅓ of all incoming damage** (crew steel included) until broken; resists fire (hellfire still bites); soft spot is its **dodge** (heavy/slow); telegraphed **hammer sweep**; drops a **fire-cage** on the most important target (it'd want Charles); the dead prisoner's key was read as the **shield's off-switch**.

**The key / Prisoner's Vengeance.** Bill first ruled "leave the key unless we hit a door we can't pass," then committed — **snuck across open ground** (untrained Stealth, a real gamble; failed the approach → the Warden roused), **grabbed the key** (took a 12-dmg clipping smash, woke the boss, floor sealed), and mid-fight **drove the key into the shield-binding seam and turned it** (two clean Crafting/Engineering checks). The shield **severed**; the keystone pulled, blowing the warded cell open and freeing a **soul-flood** that fell on the Warden. Bill failed a Reflex save vs the shield-collapse backlash (**10 fire dmg**; 22 total on the fight, healed).

**The grind.** Shield down = full damage. The crew worked it across ~5 rounds: Myles's taunt **crit-locked** it (a nat-1 boss save), Jason carved it (incl. a crit), Julie's force, the freed souls tearing at it, and Bill's **seam-delivered, charged Hell Grenade detonated from inside** (a clean inside-out blast that spared Jason on a Reflex save and seared the clinging souls). The Warden rolled **three nat-1s** (taunt save, opening smash, death-throe) and never landed a meaningful blow on the crew.

**The kill — drunk dry.** With the Warden helpless at the brink, Bill had Ember **drink the soul-flood first** (a primed conduit; the safe timing, before they could turn on the living — bulk drunk, a thin remnant scattered), then **drink the Warden's core whole** (the drink WAS the kill). **Banked: ~240 ME + the Warden pattern.** Ember's well is now vast (flood + Warden core).

**Floor 1 — CLEARED.** Quest "Breach the Ash" complete. Soul-Coins (the Warden's drop / the dungeon-natives' currency) banked. Nobody on the crew bled; Bill took 22, healed.

---

## SNIK THE GOBLIN (a loose end, tied off)

The fleeing Floor-1 coal-goblin (a **dungeon-native**, not a delver-observer — a continuity wrinkle was caught and corrected in play) was found cowering on a hoard. Bill's wide Lv.2 array lit up its stash; a closer read identified the prize. Bill spoke to it (it understood broken trade-Common), and **traded the inert Imp-Prince husk** (a crown jewel to a hoarder, useless to Bill) **for a Ghost Touch rune + a Ghost Oil + scavenged cores**, let Snik keep its coin and life, took its **sworn oath** (read genuine-but-flighty), and got **true-but-vague Floor-2 intel** (rising fire that drowns the paths; thin obsidian bridges; a "mother" that **pulls** rather than chases). Bill cowed it with a full-bore read ("I will see you"). Snik stays put.

---

## THE CHAPEL REST (the lull) — what Bill built

The crew lit a **Charred Chapel** (first internal rest point; HP/mana topped, conditions cleared). In the safe fire:

- **DEEP INSPECTION Lv.1 → Lv.2** (the long-flagged premium-reps level): deeper hidden-layer/boss resolution (reads enemy numbers others only feel), cheaper distance reads, and a **native efficient array mode** (hold a whole fight bottomed for almost nothing). *(The big delve-payout attribute points are NOT paid mid-run — they land at the threshold on EXIT after Floor 5. Banked, owed, single-entry.)* Class still Lv.2; Lv.3 banking.
- **EMBER — named.** Bill named the bound maker-core **"Ember"** (built wide for any gender; its first held word). A long, unhurried **communion** on the rune-language: Ember showed Bill how it *hears* essence as a spoken language (vs Bill's *reading* it as structure); the two grammars are halves of one thing. The voice is **one step nearer**.
- **First RUNE study.** Bill read the Ghost Touch rune to the grain (matter / inscription / essence), **stored the pattern**, and the Drafting pane's rune category began to surface. Inventing an original rune-language is now a reachable frontier (needs more studied runes/grammar + binding-capable substrate + the craft of inscription), with Ember as the fluent teacher.
- **LIVING / SPOKEN bindings — learned.** Instead of etching a static rune, Ember **speaks** a weave live, bond-fed, and Bill seats it. The lesson generalized off the communion.
- **The bench — crew + gun upgrades** (off the Warden's binding-trained **maul-iron** + Emberwaste **drake-scales** + the smithing nodule + Ember's well). Five builds, rolled:
  - **Jason — "Shearing Edge"** (success): fire-aspect re-pointed to a web/chitin shearer — the anchor-line killer.
  - **Myles — "Rooted"** (failed first, **reworked** to success as a *living bond-fed* anchor) on a **drake-faced** (fire-resistant) shield: **can't be pulled.** The keystone answer to the Broodmother's pull.
  - **Julie — "Open Throat"** (**critical success** — exceptional): focus turned amplifier, cheaper *and* harder casts, with headroom.
  - **Charles — "Long Lantern"** (success): reaching, slightly cheaper heals — stretches the crew's mana clock.
  - **Bill — drake-scale vest** (success): light fire-resistant underplate.
  - **The gun:** instead of etching, Bill **spoke ghost-touch onto the coil gun** (bind check, success) — every round now harms the incorporeal on Ember's word, bypassing "guns hate enchantment." Kept the physical rune + oil (templates). Test-shot vaporized a remnant soul.

**★ The bond is now LOAD-BEARING.** Ember holds four standing bond-fed threads off its well — the wide sweep, the larder, **Myles's root**, and **the gun's ghost-touch**. Powerful, and a single rich seam: cut or overtax the bond and Myles loses his root and the gun loses its edge against the dead. The gun-bond **entanglement deepened**. Specialty forge-stock is now **low** (the rune-language frontier waits for more substrate).

---

## DELTAS (full values in the JSON authority layer)

- **Class:** System Engineer **Lv.2** (Lv.3 banking). **Deep Inspection Lv.2.**
- **Delver Level:** still **2** (the delve-payout is banked for exit; DL = points ÷ 10).
- **Maker-core:** **named "Ember"**; well **vast** (flood + Warden core); 4 standing bond-fed threads; bond load-bearing. New captures: Warden pattern, hungry-dead/soul pattern, smoke-wisp pattern, **spirit-containment ward** (study), Ghost Touch rune (stored), rune-grammar (begun).
- **Gun:** spoken **ghost-touch** live; **seam = +5** (not auto). Hellfire rounds recovered/regrown (~38); ~86 bodkins.
- **Gear:** drake-scale vest (worn); Ghost Touch rune + Ghost Oil kept; Warden maul-iron + drake-scales **mostly spent** on the upgrades; Soul-Coins banked. Imp-Prince husk **traded away** to Snik.
- **HP/mana:** topped at the Chapel (40/40, 210/210).
- **Provisional saves:** Fort +5 / Ref +6 / Will +6 (a real block still owed).
- **Mundane ticks flagged for next clean audit:** a Shooting-under-threat tick (carried from S29) + a first **Stealth** seed (the open-ground crossing).

---

## RESUME POINT

**Descend the stairs to FLOOR 2 of the ASHEN DESCENT — "The Obsidian Caldera."** Run from `infernal_dungeon_the_ashen_descent.md`: lava lakes + razor **obsidian bridges** + steam vents; the **Magma Tides** event (lava rises on a warning rumble, submerges the bridges); mobs Brimstone Slime / Lava Beetle / Flame-Weaver Spider / Screaming Bat / Blood-Tick / Ashen Ghoul; elites Magma Elemental + Spitting Drake; side-quest **Alchemist's Greed**; **boss: BROODMOTHER IGNITE** — a gargantuan spider on a magma web over a drop, **pulls** the party toward the edge, spawns flaming spiders without end; **kill condition = burn her anchor-webs to drop her into the lava.** Snik's warning matches. The crew is **kitted for exactly this floor.**

**SINGLE-ENTRY — a wipe is final; no resupply, no retreat to town.** Win condition: **depose Azazel, the Ashen Sovereign (Floor 5).** Charred Chapels work for recovery inside the run.

**Live edges:** the bond is now load-bearing (the floor's whole danger is *pulling* — and Myles's anti-pull root rides the bond); the gun-bond entanglement is deeper; charging skills under boss-load is still the failure-edge; specialty forge-stock is low.

---

## DM HOLDS (do not resolve — see `dm_directors_notes_v1.md` S30)

The Examine:Self wrong-shaped void stays **unsolved** (no Severn-Falls / Rebecca / cosmology proper nouns in Bill's narration). The soul-prison's deeper *who/why* stays a hook (mechanism given, reason withheld). The freed souls drunk into Ember sit "strange" — a quiet clue thread. The dead delver whose ghost-gear Snik hoarded vs. "first crew on record" is a deliberate loose thread. Keep the curriculum unrevealed; reveal by doing.
