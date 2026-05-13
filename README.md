# final_project_pm

Archive of the **IEOR 4733 final project** (Polson-Stern fair-value gap strategy on Kalshi NBA win-prob contracts) backed up from the old Dell laptop (`C:\Users\DELL\Desktop\final_project_pm`).

This repo currently holds the **Claude Code session artifacts** from that project — chat transcripts (`.jsonl`) and the Continuous Claude memory index. It does **not** contain the actual project source code (Beamer deck, paper, Python research code); those lived on the Dell and would need to be recovered separately if still available.

## Contents

```
final_project_pm/
├── README.md                # this file
├── .gitignore
├── memory/                  # Continuous Claude memory index — captures the project state at 2026-04-28
│   ├── MEMORY.md
│   ├── feedback_alpha_market_definition.md
│   ├── feedback_no_inprogress_in_slides.md
│   ├── project_ieor4733_deck_status.md
│   └── project_phase2a_top3_passes.md
└── <session-uuid>.jsonl     # Claude Code conversation transcript(s)
```

## What the memory files cover

Per `memory/MEMORY.md`:

- **`project_ieor4733_deck_status.md`** — 21-slide Polson-Stern Beamer deck status as of 2026-04-28; H1 rigor + higher-freq Kalshi adaptation pending.
- **`project_phase2a_top3_passes.md`** — V0 lineup-signal strategy state on branch `strategy/lineup_signal`; top-3 PPG cut passes (t = +2.42 at n=50); bimodal split between superstar reverters and mid-tier confirmers.
- **`feedback_alpha_market_definition.md`** — Correction on `α_market` definition (per-minute home-prob move WHILE on-court, not post-sub reaction).
- **`feedback_no_inprogress_in_slides.md`** — Keep in-progress experiments out of the 5-min deck; sweeps go in chat or paper roadmap.

## Session transcripts

The `.jsonl` files are Claude Code conversation logs (one per session). They mirror what was in the Drive backup folder `C--Users-DELL-Desktop-final-project-pm/`.

| Session UUID | Size | Captured |
|---|---:|---|
| `3b5c2738-e504-4a37-8abd-dfc9df035a4e` | 471 KB | ✅ |
| `54a2e222-5f04-45ef-a980-51122cf60aec` | 405 KB | ✅ |
| `736ddf85-9ea3-46da-a6c1-f6e246c56c60` | 454 KB | ✅ |
| `ad816e15-cf2d-4771-a20b-fe09d0682830` | 3.60 MB | ✅ |
| `d6ebdcc9-c84d-419a-b92d-0c3f20d9b73e` | 429 KB | ✅ |
| `dff23c01-7b44-4b73-95f7-5b5950dec4dc` | 1.76 MB | ✅ |
| `f711f97d-b896-4af0-bc40-0e99d1e82783` | 3.48 MB | ✅ |
| `8904d4c0-2a82-41b1-bcc5-1d3681586b04` | 7.31 MB | ⏳ pending |
| `a3cc2242-2dcb-4914-8fc8-56d2c24da44d` | 8.88 MB | ⏳ pending |
| `82b35adf-ec8c-490f-bd57-ecd56d661791` | 9.45 MB | ⏳ pending |

The 3 pending files exceed the MCP `download_file_content` size limit (~5 MB per call) and the tool consistently returns "session expired" for them. To recover them: open the Drive folder ([C--Users-DELL-Desktop-final-project-pm](https://drive.google.com/drive/folders/12FskG0hzNXpHiaZqe2ubuQ2wfdRtL99z)), download the 3 files manually via the browser, drop them into this directory, and commit.

## Relationship to the kalshi project

The kalshi repo (`C:\dev\projects\kalshi`) **ports the V4 mean-reversion strategy** out of this project. Its `CLAUDE.md` references this directory as the upstream source for `docs/CODE_STYLE.md` and the V4-v3 port (see `docs/strategies/v4_port_plan.md` in that repo).
