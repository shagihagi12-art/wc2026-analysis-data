# Methodology and limitations

## Scope

This is a dated group-stage research snapshot. It stores the fact layer separately from estimated outputs. It is not a betting model, an official forecast, or a real-time score service.

## G–L Monte Carlo scenario

The workbook’s G–L scenario uses 200,000 iterations with random seed `20260626`.

- Input: group-stage goals scored and conceded before the final matchday.
- Score generator: independent Poisson scoring model based on reduced attacking and defensive form.
- Venue treatment: neutral. Sales-side or display-side team order is **not** used as a home-advantage adjustment.
- Unmodelled factors: Elo, xG, squad availability, starting line-ups, tactical matchups, travel, weather, crowd, and actual home advantage.
- Exact standing ties requiring fair-play and FIFA-ranking criteria: randomly allocated for scenario purposes only. They must not be treated as official standings decisions.

## A–F validation archive

For A–F, the workbook reconstructs the final-matchday forecast inputs by withholding each final-matchday result. It then compares the reconstructed model output with the actual final group result.

This is a **retrospective validation exercise**. It is not evidence that the forecast was published before the corresponding kickoffs, and it should never be described that way.

## Japan team feature

The Japan section combines the known group outcome and official knockout route present in this snapshot with the same lightweight score-form framing. It is a route-limited probability indicator, not a full tournament forecast.

## Interpretation rules

- Treat match scores, standings, and scheduled cards as facts only for the stated snapshot time.
- Treat all probability values, likely finish positions, and route assessments as model outputs.
- When official tie-break information is required, check official records before declaring a final qualifier or bracket placement.
