---
name: Phase 2a passes at top-3 scorers; mispricing tracks recognition tier
description: V0 lineup-signal strategy state as of 2026-04-25 — basketball signal passes when filtered to top-3 PPG per team; superstar reverters vs mid-tier confirmers
type: project
originSessionId: a3cc2242-2dcb-4914-8fc8-56d2c24da44d
---
V0 lineup-signal status (branch: `strategy/lineup_signal`, head: `47c3bf2`):

* Universe-wide α_basketball: t = +1.44 at n=50, weakens to +1.26 at n=200.
* **Top-3 scorers per team** (causal PPG rank): t = **+2.42** at n=50 (PASSES
  +2.0 bar), weakens to +1.89 at n=200.
* α_market is dead in both universe and top-3 cuts.
* Within top-3, results are bimodal by recognition tier: superstars (Durant,
  K. Leonard, Booker, Adebayo, Sengun, Powell, Ingram) **revert** —
  market over-reacts to their subs; mid-tier stars (Ball, Markkanen, Mobley,
  Giddey, M. Bridges, McCollum, Butler III, Pritchard, Claxton, Kuzma)
  **confirm** — market under-reacts.

**Why:** This is the operational handle for the project's mispricing
hypothesis. The split correlates with media recognition more than basketball
stats — the market mediates information flow more aggressively for high-
recognition players, leaving mid-tier alpha under-priced.

**How to apply:** When suggesting next moves on this branch, the
highest-information experiment is a **train/test watchlist split**: build
the WITH/AGAINST lists from a training slice and re-test on a held-out
slice. If the same player rosters work, signal is real. If they collapse,
it was overfit to small samples (~47 trades/player avg). The handoff
`thoughts/shared/handoffs/2026-04-25c_phase2a_topn_basketball_passes.md`
ranks the three next moves; train/test split is move 1, cost-adjusted PnL
is move 2 (mandatory per CLAUDE.md hard-constraint #2), shorter hold
windows is move 3.

A "first-50-games-stronger" pattern shows up in EVERY basketball run
(small-sample t-stat decays at n=200). Either an early-season regime
effect or first-window luck — diagnostic deferred.
