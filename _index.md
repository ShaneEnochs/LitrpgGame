# NPCs — index & convention

*One file per recurring NPC (or coherent group). These files own each NPC's **voice, knowledge-of-Bill, relationship texture, and key exchanges** — the durable, qualitative side. They do **not** hold the warmth number: that lives in `bill_weaver_sheet.json` → `relationships`, read against the band definitions in `game_bible.md`. Crew mechanical stats live in `fortunes_folly_crew.json`. Hidden NPC agendas stay in the DM truth files, not here — these files are player-facing.*

## Roster
- `pearce.md` — assayer, partner (knows the read is unique; not the System)
- `calloway.md` — lawyer, counsel (holds the true name)
- `doss.md` — guild 1st Lieutenant, covert ally
- `the_gunsmith.md` — Main Stretch; building partner
- `pickering.md` — Oregon Clarion; patron (holds the true name)
- `hessler.md` — guild cage; warm insider
- `tasker.md` — sundries dealer; first customer
- `pem.md` — street-kid info-broker; the Day-1 loot-share (converted) + the pending Compact
- `mrs_maddox.md` — ally/gatekeeper; children's-trust trustee
- `the_firm.md` — Tatch, Min, Cobb, Holt, the sisters, Bess, Charlie, Eli
- `fortunes_folly.md` — the crew (Myles, Charles, Jason, Julie); stats in the crew JSON
- `the_mission.md` — Father Lessard, Sister Beatrice, Sister Agnes, Esther, Ada (the "John" side)
- `the_dunmore_brothers.md` — alliance; + Rusk (protected)

## Maintenance (per gm_operations.md §3 close-out, step 5)
At session close, for each NPC engaged: append the key exchange (dated, session-ref'd; key beats, not a transcript) and update the relationship texture if it shifted. The warmth *number* is updated in the sheet (close-out step 2), surfaced during play by the change-tag.

## Status
Built in migration Phase 2 from `campaign_state.md`'s NPC section, the crew JSON, and targeted archive reads. Verbatim dialogue and earlier exchanges are appended during the Phase-4 archive consolidation, when every session body is read. Dormant/one-off NPCs (Crane, Dell, Marguerite, Arrowood, Hollis Vane & Tom, Dr. Arrowood, the licensed guild assayer, etc.) stay in the arc narrative until they re-enter play and earn a file.
