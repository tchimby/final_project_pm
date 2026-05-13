---
name: alpha_market should mirror alpha_basketball
description: User correction on what alpha_market measures — per-minute home_prob move while player is on court, NOT 60s-after-sub reactions
type: feedback
originSessionId: a3cc2242-2dcb-4914-8fc8-56d2c24da44d
---
α_market is the **per-minute home_prob move while the player is on the court**,
summed across stints in each game and causally rolled across prior in-season
games. Direct parallel to α_basketball.

I initially built it as "60-second price reaction after each substitution
event" — that's a different signal. The user corrected this and we refactored
(`e0b779e` on `strategy/lineup_signal`).

**Why:** The whole point of having α_basketball and α_market as a pair is that
their **difference** Ҕα = α_basketball − α_market measures per-player
mispricing in directly comparable units (per-minute rates, oriented to the
player's team). Post-sub reaction windows can't be subtracted from per-minute
basketball production — different units, different time scales.

**How to apply:** When extending or building parallel signals, preserve the
"per-minute, while-on-court, summed-over-stints" structure unless explicitly
asked otherwise. If the user asks for a "post-event reaction" signal, that's
a separate module, not this one.
