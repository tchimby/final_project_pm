---
name: keep in-progress experiments out of the deck
description: when polishing the IEOR 4733 deck, do not surface live experiment results — only what is settled
type: feedback
originSessionId: 8904d4c0-2a82-41b1-bcc5-1d3681586b04
---
When editing the IEOR 4733 presentation deck (`presentation_assets/slides.tex`),
do NOT add slides or claims about in-progress / exploratory experiments
(e.g., σ-aggregator sweeps, Polymarket-only and cross-venue Options B/C
backtests, recede-threshold sweeps). Those go in the conversation and the
roadmap section of the paper, not on slides.

**Why:** User said "no mention of our current experiment in" when I'd been
about to insert the cross-venue Options B+C results into the deck. The deck
should present the settled headline result + roadmap; new sweeps live in
§5 of the paper or the conversation, not in the 5-min talk.

**How to apply:** Default to keeping unsettled numbers out of the deck.
If a script produces a fresh sweep result, surface it in chat or in a
roadmap bullet — never auto-insert into a slide. Only put numbers on
slides that have been promoted to "this is the headline" by the user.
