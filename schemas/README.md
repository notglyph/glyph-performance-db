# Schemas — version 1

All files in `data/` are JSONL: one valid JSON object per line, UTF-8. Numeric metrics are numbers; unavailable values are `null` (never `0`, never `""`, never an estimate). Timestamps are ISO 8601. Every record carries `source` and `verification` (see `methodology/data_dictionary.md` for the label definitions).

## Common video record (`glyph_videos.jsonl`, `competitor_videos.jsonl`)

| Field | Type | Notes |
|---|---|---|
| `id` | string | Stable permanent ID. `glyph:<slug>`, `ig:<creator>:<date>:<slug>`, or `yt:<video_id>` when the YouTube ID is known. Never reused. |
| `schema_version` | int | `1` |
| `platform` | string | `youtube` / `instagram` |
| `video_id` | string \| null | YouTube video ID when known; `null` otherwise. |
| `url` | string \| null | Direct URL when known. |
| `title` | string | Exact title as published. |
| `creator` | string | Channel/account handle. |
| `published_at` | string \| null | ISO date (with time/timezone when known). |
| `duration_sec` | number \| null | |
| `language` | string | e.g. `en` |
| `category` | string | `glyph` / `direct_competitor` / `adjacent` |
| `discovered_at` | string | ISO date the record was created. |
| `baseline` | object | `{typical_views, method, n_comparable}` — how the channel baseline was derived; values `null` when unavailable (classification is then `provisional`). |
| `classification` | string | `breakout` (≥3x) / `notable` (2–3x) / `typical` (0.75–1.25x) / `underperformer` (<0.5x) / `provisional`. Exploratory categories, not universal thresholds. |
| `breakout_multiplier` | number \| null | Observed performance ÷ baseline. |
| `creative` | object | Hook type, first-frame description, mechanic, beats — only what was actually inspected; otherwise `null` fields with a note. |
| `final_snapshot` | object | Latest known headline metrics (full history lives in `performance_snapshots.jsonl`). |

## `performance_snapshots.jsonl`

`video_ref` (joins to a video record `id`), `collected_at` (ISO), `age_hours`, `views`, `likes`, `comments`, `stayed_pct`, `swiped_pct`, `avd_sec`, `avg_pct_viewed`, `net_subs`, `source`, `verification`. Glyph-only fields (`stayed_pct`, `net_subs`, …) come from owner-authorized YouTube Studio reads; they are `null` for competitors because they are not public.

## `research_observations.jsonl`

`id` (`obs:<date>:<slug>`), `observed_at`, `type` (`pattern` / `failure` / `hook` / `comment_signal` / `data_quality`), `summary`, `evidence_refs` (video IDs or file references), `confidence` (`low` / `moderate` / `high`), `verification`.

## Change policy

Schema changes bump `schema_version` and are documented here with the date and reason. Existing lines are never rewritten to a new schema silently; a migration note is added instead.

## Schema adjustment — Oct 20, 2026 (Mission 002 audit, additive, backward-compatible)

Competitor records gained three optional fields; no existing field was renamed or removed:
- `breakout_multiplier_basis` (string) — states what the multiple measures. For all Instagram-sourced records: engagement (likes/comments vs creator recent-post median), **not views**. Read this before quoting any multiple.
- `grouped` (bool) + `group_note` — the record summarizes multiple posts; excluded from per-video comparisons until split.
- `metrics_complete` (bool) — false when neither likes nor comments were captured.
- `date_note` — preserves original source date text when `published_at` had to be nulled as non-ISO.
