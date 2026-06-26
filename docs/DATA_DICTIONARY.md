# Data dictionary

## `2026-06-26_WC2026_OfficialState.csv`

| Column | Meaning |
| --- | --- |
| `snapshot_at_jst` | Snapshot timestamp in Japan Standard Time. |
| `group` | Group letter, A–L. |
| `rank_now` | Rank in the snapshot. |
| `rank_status` | Whether the rank was final at the snapshot. |
| `group_status` | Whether the group was complete at the snapshot. |
| `team_code` | Three-letter team code used in this project. |
| `team_ja`, `team_en` | Japanese and English team names. |
| `played` to `points` | Group-stage record fields. |
| `next_opponent_code`, `next_opponent`, `next_kickoff_jst` | Next match fields where applicable. |
| `source_status`, `source_reference` | Capture provenance retained from the source snapshot. |

## `2026-06-26_WC2026_MatchFacts.csv`

| Column | Meaning |
| --- | --- |
| `snapshot_at_jst` | Snapshot timestamp in Japan Standard Time. |
| `match_id` | Match identifier retained from the capture source. |
| `group` | Group letter, A–L. |
| `kickoff_jst` | Kickoff in Japan Standard Time. |
| `home_code`, `home_team_ja`, `away_code`, `away_team_ja` | Participating teams as recorded in this snapshot. These labels are not used for a home-advantage model. |
| `home_score`, `away_score` | Score where completed. |
| `status` | Match state at the snapshot. |
| `source_status`, `source_reference` | Capture provenance. |
| `official_match_center` | Official Match Centre landing-page reference. |

## `2026-06-26_WC2026_BestThird_Tracker.csv`

| Column | Meaning |
| --- | --- |
| `snapshot_at_jst` | Snapshot timestamp in Japan Standard Time. |
| `rank_now` | Provisional third-place rank in the snapshot. |
| `group`, `team_code`, `team_ja` | Group and team identifiers. |
| `played`, `points`, `goal_difference`, `goals_for` | Third-place comparison values available at the snapshot. |
| `group_status`, `third_status` | Completion and qualification context. |
| `ranking_note` | Explicit note on the provisional ranking and tie-break limits. |
