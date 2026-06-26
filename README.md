# WC2026 Analysis Data

An independent, timestamped data snapshot and analysis workbook for the 2026 World Cup group stage.

> **Snapshot:** 2026-06-26 19:16 JST  
> **Release:** `v2026.06.26`  
> **Project status:** A–F groups complete; G–L were still before their final matchday at this snapshot.

This repository separates **facts** from **model outputs**. It is not affiliated with, endorsed by, or produced by FIFA or any tournament organiser.

## What is included

| Path | Contents |
| --- | --- |
| `data/2026-06-26_WC2026_OfficialState.csv` | Current group table for all 48 teams, including snapshot time and next match fields. |
| `data/2026-06-26_WC2026_MatchFacts.csv` | Results and scheduled matches in the snapshot. |
| `data/2026-06-26_WC2026_BestThird_Tracker.csv` | Provisional ranking of third-placed teams. |
| `workbook/2026-06-26_WC2026_公開版_現況と再構成検証.xlsx` | Japanese workbook: group focus sheets, G–L Monte Carlo outputs, Japan feature, and A–F validation archive. |
| `docs/2026-06-26_WC2026_MODEL_SPEC.md` | Input-layer specification, tie-break treatment, and update workflow. |
| `docs/DATA_DICTIONARY.md` | Column definitions for the CSV files. |
| `docs/METHODOLOGY.md` | Model boundary and limitations. |

## Facts vs. estimates

### Facts in this release

- Match scores and match status present in the CSV snapshot
- Group points, goal difference, goals scored, and the current standing in that snapshot
- Scheduled final-match cards and kickoff fields present in the data
- The 2026 competition's group-ranking and best-third-place comparison sequence described in the model specification

### Model outputs in this release

- G–L finishing-position and Round-of-32 probabilities
- Best-third-place scenario distributions
- Japan's Round-of-16 / quarter-final route-limited probability indicators
- A–F group-stage validation tables

Model outputs are estimates only. They are not official forecasts, betting advice, or a guarantee of any outcome.

## Important integrity note: A–F archive

The A–F validation materials are **retrospectively reconstructed** from information that was available before each group’s final matchday. They are not records of forecasts actually published before kickoff. This distinction is visible in the workbook and must be retained in any downstream use or quotation.

## Sources and verification

Each CSV retains `snapshot_at_jst`, `source_status`, and `source_reference` fields. The match table also keeps the official Match Centre landing-page URL.

Before using the dataset for a current claim, verify changed facts directly against the official tournament Match Centre and regulations. This release is a dated research snapshot, not a live feed.

- FIFA Match Centre: https://www.fifa.com/en/tournaments/mens/worldcup/canadamexicousa2026/match-center
- Competition regulations: https://digitalhub.fifa.com/m/636f5c9c6f29771f/original/FWC2026_regulations_EN.pdf

## Update policy

1. Publish a new date-stamped data snapshot; do not overwrite an earlier release.
2. Recalculate `OfficialState` and the third-place tracker after every completed final-match window.
3. Resolve any standings tie requiring fair-play or ranking criteria from official records before marking it final.
4. Recompute model outputs only after the fact layer has been frozen for the new timestamp.
5. Record changes in `CHANGELOG.md`.

## Use and attribution

See `LICENSE.md` and `docs/PUBLICATION_POLICY.md`. The project’s original workbook structure, Japanese explanatory text, and model outputs are shared under CC BY 4.0. No rights are granted over third-party names, marks, visual assets, or source-platform content.
