# MAGIC DOMAINS AND ATTUNEMENT — worldbuilding catalog (v1)

*This subsystem slots in beside the other catalogs. It elaborates `game_bible.md` §13 (cultivation, essence, mana, magic) and §14 (magic law) and never overrides them; current state would live in `campaign_state.md` as usual. It governs **tome spellcasting only** — the cast-magic track — and leaves auras, ability orbs, the essence/mana split, runecraft, and spiritual pressure as already written. Voice follows §2: plain and literal.*

---

## 1. The idea

Magic effects fall into a small number of natural **domains** — recurring patterns in how mana shapes into a result. Every awakened caster has an **affinity** that opens one domain to them fully, sometimes a second with real effort, and closes the rest off to a degree that runs from hard to impossible. This is why no caster does everything, why casters specialize, why a domain you lack is a person you have to hire, and why a party covers ground a lone caster never can.

Two things are separate and both true. The domains are a real fact of how mana works. The human **map** of the domains is twelve years old, regional, and disputed — assayers' and researchers' working models, not a federal standard like the tier/grade ladder. Folk casters just know "I'm good with fire and force, useless with the healing books." Eastern researchers draw fancier charts and argue about them. That gap is the period texture and a standing research thread.

---

## 2. What this changes, and what it leaves alone

**Changes** the one thing in current canon: under §13, anyone with a magic build could learn any tome. Now a **tome is keyed to a domain**, and learning a tome outside your affinity runs from costly to unusable.

**Leaves alone:**
- The essence/mana split, mana from Intellect, recovery, overcasting risk — all §13, untouched.
- **Ability orbs stay outside the gate.** An awakened person still uses an orb by feel (§13); orbs grant non-magical abilities off mana and don't belong to a domain. This keeps orbs as the "anyone can get power from loot" track.
- **Auras stay outside the gate.** An aura is the core's own pressure-field shaped (§13); it's found as loot and works off the core, not learned as domain spellcraft. An aura may carry a domain *flavor* but doesn't require affinity to use.
- **Runecraft stays a material craft** (the Runecraft skill, §6; `dungeon_materials_v1.md`). Domain affinity can *help* a runecrafter, per §4, but inscribing runes into material is still its own trade.
- Licensing, assay, and the gray-to-black market (§14) all continue — domains give them sharper teeth (§6 below).

The point of holding the gate to tomes is that the trained-caster identity becomes specialized and legible, while the loot tracks (orbs, auras) stay open to everyone. That preserves the distinctions §13 already draws.

---

## 3. The domains (the working assayer taxonomy)

A working set of nine. Treat the names as regional slang, not settled terms — an eastern paper and a frontier assayer may call the same domain different things.

- **Life.** Absolute control over biology and living tissue: healing, accelerated growth, forced mutations, shape-shifting. The healer's domain, valuable out of all proportion to its tome count because a party lives or dies on it. Respected and watched at once; the bright end (knitting flesh, fighting infection) is welcome anywhere, and the dark end (forced mutation, flesh-twisting, the deliberate ruin of a body) is heavily restricted and fast to draw attention.

- **Transmutation.** Manipulation and alteration of inanimate physical substance: shaping earth, forging metals, changing states of matter. The trades' domain — steady commercial demand in smithing, building, and refining, and the one domain whose value is mostly peaceful. Lightly watched; its native crime is not violence but assay fraud and counterfeiting, passing transmuted stock as the real thing.

- **Arcane.** Mastery over raw, volatile energy: fire, lightning, pure concussive force. The common combat magic — the widest affinity, the cheapest and most-traded tomes, the domain a plain delver most often holds. Most tolerated by the law because it is everywhere and obvious; a man throwing fire hides nothing.

- **Dimensional.** Bending of physical space and gravity: teleportation, portal creation, telekinetic movement. Rare, precious, and slow to learn, and the most valuable and registered domain there is — a Dimensional tome is a small fortune. It interlocks with runecraft and with how the arches and dungeon interiors behave (§11), which is part of why the USBD tracks it so closely.

- **Psionic.** Direct manipulation of the brain and perception: telepathy, mind control, memory alteration, sensory illusions. The most legally dangerous domain by far — compulsion especially, because a man who can bend a will can do anything and prove nothing. Restricted or banned in most jurisdictions; an open Psionic affinity on a record is enough to keep a person watched whether or not they ever cast.

- **Spirit.** Interaction with the ethereal essence of life beyond the physical body: astral projection, communication with the dead, soul-binding. This is where the Church keeps its hard suspicion (§14 names Spirit, Undead, and Infernal as its concern). The benign end is respected; the necromantic edge — the dead, the lingering, what won't stay down — is restricted near everywhere and is contraband worth real money.

- **Summoning.** Piercing the veil of reality: calling extraplanar creatures, conjuring physical objects from nothing, banishing targets into pocket dimensions. Heavily watched by Church and USBD both for the extraplanar traffic it opens; the calling end draws the hardest scrutiny, while the banishment end is valued guild work against monsters and demons.

- **Divination.** Reading and rewriting the cosmic script: foreseeing the future, remote viewing, probability manipulation. Niche and contested — gambling houses ban it outright, market-fraud statutes reach it, scrying makes it an espionage and privacy problem, and the courts have not settled what a foreseen act means in law. Prized by those who can use it, distrusted by everyone it is pointed at.

- **Warding.** Enforcement of magical boundaries and rules: dispelling, impenetrable shields, trapping magical entities. The seal-works domain, directly load-bearing for dungeon containment law — a USBD-certified warder is a real and respectable trade, commercially large, the people the law leans on to keep a sealed mouth sealed.

**No separate holy domain.** The Church's consecrated rites, blessings, and exorcisms are not their own kind of magic. Where they do something real, it reads as Spirit-work; the rest is institutional authority, not domain magic. The Church's stake in the magic system lives in its jurisdiction over the dark end of Spirit and the traffic of Summoning (§6), not in a power of its own.

---

## 4. Affinity — how access actually works

- Each caster has a **primary** domain they cast at full strength. Some have a **secondary** they can reach with real study, at a lower ceiling and a higher mana cost. The rest are **closed**: a tome in a closed domain is near-unusable, and forcing a single weak effect from one costs heavily and courts backlash (the overcasting risks in §13 — exhaustion, injury, spell failure, worse).
- **No clean percentage.** The ceiling falls off with distance from the primary rather than at a fixed line. A strong primary, a capped secondary, a steep drop after that.
- **Set at awakening,** alongside class assignment and the 10-point choosing (§13). It correlates with class without being identical — a healer-class leans Life, an enchanter or crafting-class leans Transmutation or Warding, a plain delver most often Arcane — and it carries a flavor of the settle-by-struggle pattern (how the core opened, what the person was doing when it did). Whether affinity can ever shift after that is rumored and best left as no, with the rumor itself as bait.
- **Affinity pairs with intrinsics.** Domain says *what magic a caster can reach*; an intrinsic discipline (`ability_framework_v1.md`) says *how deep they have driven it*. An Arcane discipline amplifies a caster's Arcane spells; a Life discipline, their healing. The two systems reinforce — access is one axis, trained depth the other — and a caster with a strong primary and no intrinsic behind it is broad and shallow.
- **Adjacency is disputed on purpose.** The eastern working model holds some domains as neighboring and easier to hold together — schools variously argue Arcane with Dimensional, Life with Spirit, Psionic with Divination, Transmutation with Warding — and some as opposed and rarely held at once. But schools draw the map differently, documented exceptions exist, and no one has proven the geometry. Don't treat it as solved; the argument is the texture, and charting it correctly is the kind of thing a researcher would chase (and Bill could outpace them at, per §8).

---

## 5. Reading and discovering affinity

- A caster feels their **primary** roughly from first real contact with tomes — the right book "wants to be read," the wrong one stays inert.
- A **precise** read needs a specialist assay, an added and costlier service beyond the standard 300 cr core assay (§14). That assay makes a record, charges a fee, and becomes a licensing data point — another reason to ride to Saint Orison's licensing office, another line on a person's file.
- A restricted-domain affinity on the record — Psionic, the necromantic edge of Spirit, or an open Summoning affinity — draws USBD and Church interest on its own, before the person has cast a thing. This is a clean, grounded source of legal pressure that doesn't require catching anyone in the act.

---

## 6. The economy and law of domains

- **Tome value turns on domain rarity and legality,** not power alone. An Arcane tome is ordinary depot stock. A Transmutation tome trades steadily on commercial demand. A Life tome sells high because parties need healers. A Warding tome holds steady guild demand off the seal-works trade. A Dimensional tome is a small fortune. A Summoning tome is rare and watched. A Divination tome is niche and pricey. A Psionic tome, or a necromantic Spirit tome, is contraband the Hollow Road moves and the USBD wants burned.
- **Licensing maps cleanly onto domains** (§14): Arcane lightly watched and most tolerated; Transmutation lightly watched, its crime commercial; Life respected and watched, its dark edge restricted; Warding a certified, respectable trade; Dimensional valuable and registered; Summoning watched by Church and USBD both; Divination niche and legally contested; Psionic and the necromantic edge of Spirit heavily restricted. A license isn't just "magic, yes/no," it's domain-by-domain, and a man permitted for Arcane has no standing to be carrying a Psionic tome.
- It deepens the factions already on the board. The Church (§18) gets a concrete jurisdiction in the dark end of Spirit and the traffic of Summoning. The USBD gets a registry worth enforcing and a certified warder trade to run. The Hollow Road gets a clear high-value cargo. None of it is new machinery — it's the existing law and trade, given domains to sort by.

---

## 7. Why this earns its place in a solo game

Mage Tank used a hard magic cap to force a party. You don't need that, and shouldn't import it. The domains do useful work for a single protagonist on their own:

- They give the casters **around** Bill real identity and rivalry — every NPC caster is now someone with a domain, a ceiling, and a thing they can't do — without adding one rule to the table.
- They make **hired specialists matter.** The domains Bill can't touch are exactly the people he has to pay, trust, or do without: the healer, the warder, the one who can read a sealed arch. A lone engineer can't cover a spectrum, and now the gaps have names.
- They give whatever Bill's own path makes of magic a **shape and a limit** instead of open-ended access, which fits the campaign's whole stance that builds concentrate and delvers diverge (§12, §21).

---

## 8. Bill — handle in play, don't fix it here

The attunement system is first of all the **world's** — it governs the casters Bill meets, hires, fights, and competes with. Whether and how Bill himself sits under domain affinity is a question his particular awakening answers, and his Engineer path (§21) may stand in a different relation to magic than a tome-caster does. Leave that to play rather than nailing it down on the page. If anything, the disputed adjacency map (§4) is the sort of problem his strengths are built to crack — let that be something he can discover, not something the file pre-decides.

---

## 9. Decisions — settled and still open

The domain list is settled; the rest stay deliberately open as standing forks and research threads:

- **The domain list and names — settled.** The nine adopted are Life, Transmutation, Arcane, Dimensional, Psionic, Spirit, Summoning, Divination, Warding (regional name variants still vary in play). This is canon.
- **The adjacency map — open.** Whether to fix one true geometry behind the scenes (a DM-only answer, the way the minor mysteries are anchored) or to leave it genuinely open even to you. The in-world argument among schools stands either way (§4).
- **Whether the USBD ever standardizes it,** the way it standardized tiers and grades — a natural "news from the faster East" beat if and when the East reaches the territory. Open.
- **Whether affinity can shift.** Cleanest answer is no; the rumor that it can is good bait either way.
- **Retrofit.** Whether any caster NPCs already established in `campaign_state.md` need a domain assigned now, or get one the next time they're onstage.
