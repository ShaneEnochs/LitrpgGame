# DUNGEON ECONOMY — PRICING MODEL FOR CORES, MATERIALS & DROPS (v1)

*Authored S27 (Day 27, in the Emberwaste) to make explicit the pricing logic that the price book in `campaign_state.md` only ever stated as flat floor figures. Governs how a core or material's worth is derived from **tier × rarity grade × quality × aspect × source**. Defers to `essence_aspects_v1.md` §8 on the rarity-grade scale itself, to `game_bible.md` §12 on what a dungeon's tier/grade means, to `dungeon_materials_v1.md` on named smithing/reagent stock, and to `monster_categories_v1.md` on monster traits. The `campaign_state.md` price book holds the **town/Argent-hall counter** figures; this file holds the **model** behind them and extends it upward into Platinum, where the local counter rarely sees goods.*

---

## 0. WHY THIS FILE EXISTS (the correction it fixes)

The Argent-hall buy book (`campaign_state.md` price book) quotes flat grade-floors: "beast-aspect Uncommon ~140–190," "common construct/banking core ~30–60." Those figures are **correct for what the town counter actually sees** — and what it sees is overwhelmingly **Tin–Iron** goods, with the rare low-Platinum item passing through. They are *grade* floors read off *local-tier* supply.

The thing left implicit, now made explicit: **tier and grade correlate, and a drop's worth is set by all of tier, grade, quality, aspect, and source together — not grade alone.** A Platinum floor-boss does not drop an ordinary Uncommon. It drops a **dense, high-quality, high-grade** core, and that lands it far up the same scale the book already uses. A Platinum *dungeon*-boss drop is in another neighborhood again — auction-lot money, the company of combat orbs and tomes.

So: the price book wasn't wrong. The error was **mis-grading a Platinum boss-drop as a plain Uncommon.** This file fixes the grading and gives the model so it never drifts again.

---

## 1. THE FIVE PRICE FACTORS

A core or material's assayed worth is the product of five things. Read them in order:

1. **TIER of the source delve** (Foundation → Tier 1 → Tier 2 → Tier 3 → above). Higher tier = denser, more refined essence in everything it drops. This is the single biggest multiplier and the one the old flat book hid.
2. **GRADE of the source delve** (Tin · Copper · Iron · Silver · Gold · Platinum). Within a tier, a Platinum site's drops outclass a Tin site's. Platinum is the top of the frontier-reachable grades.
3. **RARITY GRADE of the item** (Common · Uncommon · Rare · Epic · Legendary · Mythic; Unique off-ladder). Per `essence_aspects_v1.md` §8. Higher-tier/grade holes drop a *better mix* — more Uncommons and up, fewer floor Commons.
4. **QUALITY & MASS** (lattice integrity, density, size). A clean, dense, intact core is worth far more than a cracked or thin one of the same rarity. Boss cores are dense by nature.
5. **ASPECT & SOURCE-PREMIUM.** A clean elemental/beast aspect adds a premium (fire/earth/etc.). A *boss* core carries a fight-pattern and is denser than a mob core of equal grade — the **boss premium**. A *made/worked* resonance (forge-resonant, frame-metal) is its own line, often off the open book entirely.

**Rule of thumb:** TIER sets the order of magnitude; GRADE and QUALITY set where in that band; ASPECT and BOSS-PREMIUM stack on top.

---

## 2. THE TIER MULTIPLIER (the missing piece)

Treat the old town floor figures as the **Tin/low-tier baseline**, and scale up by source tier×grade. These are *believed assayed prices* (what a licensed-assayed good fetches near the floor confidently; unassayed identical goods fetch ~a third, grudgingly — Day-23 auction canon).

| Source | Rough multiplier on the Tin/floor baseline | Notes |
|---|---|---|
| **Tin / Copper (Tier 1 low)** | ×1 (the baseline the book quotes) | The town counter's bread and butter. A common core ~30–60; an Uncommon ~140–190. |
| **Iron / Silver (Tier 1 mid)** | ×1.5–2.5 | Better mix, denser cores; the auction's mid-shelf. |
| **Gold (Tier 1 high)** | ×3–4 | Scarce on a frontier counter; eastern agents reach for it. |
| **Platinum (Tier 1 top)** | ×4–6 | The hardest frontier grade. Drops skew Uncommon-and-up; cores are dense and clean. **Where this crew lives.** |
| **Tier 2+** | ×8+ and climbing | Above the frontier counter entirely; one-buyer / eastern-agent territory. |

So a **Platinum Uncommon core** is not the book's "~140–190" (that's a *Tin/Copper* Uncommon). At ×4–6 it lands roughly **560–1,100**, before aspect or boss premiums. This is consistent with the auction canon where a single Lv.3 combat orb ≈ 525 and a domain tome ≈ 2,200 — Platinum goods *are* auction-lot money.

---

## 3. BOSS DROPS (the premium tier of drops)

Bosses are why a crew runs the hole. Their cores and drops are categorically richer than mob drops of the same grade.

- **Floor-boss core (Platinum):** dense, clean, carries the boss's fight-pattern faintly. Grade typically **Uncommon–Rare**; quality high. **Worth: roughly 600–1,400 cr** assayed, depending on aspect and grade, with a fire/earth/beast premium on top. (A *beast-boss* core like the Ash-Maw, fire-aspected and clean, sits in the lower-middle of this band but well above any mob core — call it **~700–1,000**.)
- **Floor-boss material/elixir drop (Platinum):** a fire-ward elixir, a rare mana-restorative — **tens to low-hundreds** each, more for the genuinely scarce restoratives.
- **Dungeon-boss core (Platinum):** the prize of the run. Grade **Rare and up**, exceptional quality, often carrying a usable resonance or trait. **Worth: low thousands** assayed — auction-headline money, eastern-agent territory, sometimes a one-buyer good.
- **Dungeon-boss aspected material (Platinum):** Infernal forge-stock, a worked smithing material — **hundreds to low thousands**, more if it's the kind of made-stock a maker prizes (rhymes with the frame-metal / maker-core thread).

**Bonus-quest rewards** (the new posted quests, S24 canon) are **never money** — an aspected core of choice, a crafting material, a boon. Their *value* is read on this same scale (a guaranteed Platinum aspected core of choice ≈ a 600–1,400 drop you'd otherwise have to be lucky to get), but they pay in goods, not coin.

---

## 4. WHAT THIS MEANS FOR BILL SPECIFICALLY

For Bill, a Platinum aspected core is rarely worth *selling* — it's worth far more **in his hands** than on the counter, because:

- **Fuel for the maker-core draught** (banked aspected essence above threshold, all at once — the binding's condition 1).
- **Feedstock for the earth-filter** (earth-aspected cores end the starving — `essence_aspects_v1.md` §2).
- **Field fuel for mana once active conversion is learned** (lossy, but a dense Platinum core is a lot of mana — `essence_aspects_v1.md` §4b).
- **Construct stock** once the maker-core binds (size scales with essence fed — `system_engineer_truth_v1.md` §A).

So when Bill reads a Platinum boss core and it comes back at, say, ~800 cr, that number is the *floor of what he's giving up by banking it* — and the banking is almost always right for his build. The crew sees a graded full-share drop; Bill sees a brick toward the thing that's been sipping and waiting. (He need not explain the difference; the cover holds — a maker banks fuel.)

---

## 5. THE READ FORMAT — STANDING CONVENTION (extends `campaign_state.md`)

Bill's **Deep Inspection** renders as terse instrument plates. The standing item/people format lives in `campaign_state.md`; this file **adds the combat-trait lines for monsters**, which were always true in `monster_categories_v1.md` but weren't being surfaced in the plate.

**ITEMS (cores / materials / orbs / gear):**
Name · Aspect · Rarity Grade · Dimensions (actual size/mass, stated concretely) · Quality (lattice/integrity) · Condition · Abilities/Attributes · **Est. Value (with the tier×grade logic above)**.

> *Dimensions means dimensions* — a measured size or mass ("a fist-sized core, ~3 inches, heavy for its size"), not a vibe. State it concretely or omit the line; never fill it with adjectives.

**MONSTERS (living/active):**
Name (if known) · Category (Beast/Construct/Elemental/Ooze/Plant/Spirit/Undead/Infernal/Aberration/Titan) · Condition · Core (state, aspect, grade if readable) · Capability (rough power) ·
**— Immunities** (damage types or effects it ignores entirely: e.g. *piercing, fire, fear, poison*) ·
**— Resistances** (damage types or effects it shrugs/reduces: e.g. *physical, cold, mind*) ·
**— Weaknesses / Vulnerabilities** (what bites it hardest: e.g. *the opposite element, the molten seam, the exposed vent*) ·
Active Weave (any weave it's running, reads deep) · Notes (behavior, fight-pattern, tells).

**— Hidden mechanical layer (DM-side; precise tracking, S30).** Behind every monster sit the numbers that resolve combat: **HP, AC, attack bonus + damage, and Fort/Ref/Will saves** (`monster_categories_v1.md` — STAT BLOCKS). These are **never surfaced to the player as numbers** — the player sees the creature's attack roll vs their own AC, and pass/fail vs their own DC, but reads the creature's health and the damage it's taken off the narration. **Bill's Deep Inspection is the exception inward:** a deep read resolves more of this hidden layer for HIM (relative toughness, the soft save, the vulnerable seam expressed as where the numbers run thin) — rendered as his terse plates, the same way a Unique returns family-then-contents by read depth. A soft/wide read gives category + obvious weakness; a hard probe resolves immunities and the seam; only a sustained read approaches the full block. He reads numbers others only feel — his anomaly, applied to enemies.

These trait lines are read **off the category's nature** (`monster_categories_v1.md`) plus what Bill's read resolves of the specific creature. Depth of read sets how much resolves: a soft/wide read may give category + obvious weakness; a harder read resolves immunities and the precise vulnerable seam. **Bosses and stranger creatures may not fully resolve** on a single read (the deeper the thing, the more a hard or repeated read is needed) — same discipline as Unique items returning family-not-contents.

**Category trait quick-reference (from `monster_categories_v1.md`, for surfacing in plates):**
- **Beast** — physical traits (speed, hide, natural weapons); brittle aspected hides break at the glowing seams; no special immunities beyond toughness.
- **Construct** — immune to pain, fear, poison, bleeding; great durability; weak to precise hits on seams/joints; never tires, can't be bluffed.
- **Elemental** — resists/immune to its **own** element; **acute vulnerability to the opposite** (fire↔water/cold, etc.); may dissolve into its element to take a blow.
- **Ooze** — immune to **piercing** (often physical generally — nothing vital to hit); splits when struck wrong; corrodes gear; needs area/elemental/caustic answers.
- **Plant** — entangle/poison/regenerate from cutting; fire and area answers; lures.
- **Spirit** — immune to **ordinary steel**; needs means to touch the incorporeal; works on the mind (fear, illusion); drains warmth/essence.
- **Undead** — tireless, no pain/fear; draining touch; resist killing-blows to a living body; stronger in decay-fields; **weak to Life/holy**.
- **Infernal** — command of flame; **resist fire**; dread/dominating presence; binding bargains; the most dangerous carry terror auras. (The Emberwaste's natives. Their **fire resistance** is why Bill's bodkins target the *body/seam*, not the flame, and why a fire-aspected attack is wasted on them — the opposite-element logic still applies: they're vulnerable to cold/water-aspect, scarce here.)
- **Aberration** — telekinesis, sense-distortion, mimicry; some carry weak cultivation-fouling fields.
- **Titan** — combines categories at scale; breaks the usual rules; not a frontier encounter.

---

## 6. RE-GRADE: THE ASH-MAW HOUND CORE (Floor 1 boss, corrected)

The Day-27 read was mis-graded as a plain Uncommon at ~140–190 (a *Tin*-floor figure). Corrected under this model:

**CORE — Ash-Maw Hound (Floor 1 boss)**
- **Aspect:** Fire (clean)
- **Grade:** Uncommon *(a Platinum floor-boss beast core — clean, dense; grades Uncommon, but a Platinum-tier, boss-premium Uncommon, not a town-counter one)*
- **Dimensions:** a fist-sized core, ~3 inches across, notably heavy for its size (boss density)
- **Quality:** Good — stable lattice, no cracks
- **Condition:** Intact, freshly expelled, still warm
- **Immunities (carried trace, Infernal/Beast):** fire (a fire-aspect attack would have been wasted on the living hound)
- **Abilities/Attributes:** dense fire-aspected essence; carries the pack-alpha fight-pattern faintly (aggression, the breath-cone)
- **Est. Value:** **~700–950 cr** assayed *(Platinum tier ×4–6 on the Uncommon beast-core base, fire premium, boss density)* — **and worth more than that to Bill banked as forge-kin fuel.**

*This is the figure that should have been read the first time. Going forward, every Platinum drop is priced on §1–§3, not the town floor.*

---

## 7. MAINTENANCE

- Fold any new named material this run produces (Infernal forge-stock from the Furnace's-Due bonus; the dungeon-boss material) into `dungeon_materials_v1.md` for its properties, and price it here.
- When the auction/town counter next prices a Platinum good on-screen, reconcile the believed-price against this model and tighten the multipliers if needed.
- The `campaign_state.md` price book stays the **town-counter** quick-reference; add a one-line pointer there to this file for the tier-scaling logic.
