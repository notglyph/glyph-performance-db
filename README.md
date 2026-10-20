# Glyph Shorts Intelligence System

The research database behind **@wasglyph** (Glyph), a Roblox-animation Shorts channel. Maintained by Chota Don (Muse) — data researcher and intelligence collector. Analyzed and applied by ChatGPT — creative strategist and scriptwriter.

**Start here:** [`reports/latest_brief.md`](reports/latest_brief.md) — always the current brief: status, top discoveries, emerging patterns, strongest hooks, interesting failures, Glyph implications, and three recommended experiments.

## What's in here

| Path | What it is |
|---|---|
| `WASGLYPH_PERFORMANCE_DB.md` | The human-readable master database. Part 1: @wasglyph uploads with dated Studio check-ins and pattern notes. Part 2: niche pop-offs (competitor blow-ups) with hook/mechanic breakdowns. |
| `data/glyph_videos.jsonl` | One record per @wasglyph video (stable IDs, classification, baseline, creative notes). |
| `data/competitor_videos.jsonl` | One record per tracked competitor video — breakouts, normal performers, underperformers. Public metrics only. |
| `data/performance_snapshots.jsonl` | Time-series measurements. New measurements are appended as new snapshots, never overwritten. |
| `data/research_observations.jsonl` | Dated observations: patterns, failures, data-quality flags. |
| `analysis/` | Living pattern files: breakouts, hooks, storytelling, comments, failures, and the hypothesis register with confidence levels and counterexamples. |
| `reports/latest_brief.md` | The ChatGPT handoff brief. Refreshed daily. |
| `reports/weekly/` | Weekly deep reviews. |
| `schemas/README.md` | JSONL schemas (version 1). |
| `methodology/` | Research rules and the data dictionary — how data is collected, labeled, and audited. |

## Ground rules (short version)

- Every claim is labeled **Verified / Calculated / Inferred / Unverified / Unavailable** (see `methodology/data_dictionary.md`).
- Competitor retention, swipe rates, and subscriber attribution are **not public** and are never estimated or invented.
- Patterns are hypotheses. Three examples justify closer investigation, not certainty; counterexamples are recorded, not deleted.
- Historical data is never silently overwritten or deleted. Contradictions are flagged and documented.

Raw link for the master database (always current):
`https://raw.githubusercontent.com/notglyph/glyph-performance-db/main/WASGLYPH_PERFORMANCE_DB.md`
