# Data Dictionary

## Verification labels

| Label | Meaning |
|---|---|
| **Verified** | Directly observed from an accessible source (Studio read, public page, the video itself). |
| **Calculated** | Mathematically derived from verified values (e.g., breakout multiplier, comment rate). |
| **Inferred** | Plausible interpretation, not directly established (e.g., "the loss is at the hook" from a metric split). |
| **Unverified** | Claimed or partially sourced, not yet confirmed. |
| **Unavailable** | Cannot currently be obtained (e.g., competitor retention; a gated Studio tab). |

Labels describe evidence quality, not truth. A Verified association is still not proof of causation.

## Metric definitions

- **Views** — public view count at collection time (competitors) or Studio count (Glyph; the two can differ slightly — source is always recorded).
- **Stayed to watch %** — Studio audience-retention headline for Shorts: share of viewers who stayed vs swiped away. Glyph only (owner-authorized). Competitor value: Unavailable.
- **Swiped away %** — 100 − stayed %.
- **Average % viewed** — Studio average percentage of the video watched; can exceed 100% when viewers rewatch.
- **AVD** — average view duration, seconds.
- **Net subs (video-attributed)** — Studio subscribers gained minus lost, attributed to the video. Glyph only.
- **Comment rate** — comments ÷ views × 100. A debate signal only alongside absolute volume; ~1%+ with high volume suggests a debate is firing (hypothesis, see `analysis/comment_patterns.md`).
- **Breakout multiplier** — observed views ÷ channel baseline views at a comparable age. For Instagram pop-offs logged before the JSONL system, the multiplier was computed on engagement (likes/comments vs the account's recent-post median) — those records say so in `baseline.method`.
- **Baseline** — a channel's recent typical performance, median preferred, with window and comparable-count recorded.

## Performance categories (exploratory)

| Category | Band |
|---|---|
| Breakout | ≥ 3x baseline |
| Notable | 2–3x |
| Typical | 0.75–1.25x |
| Underperformer | < 0.5x |
| Provisional | no trustworthy baseline |

## Confidence levels (patterns & hypotheses)

- **Low** — 1–2 independent examples, or strong confounders unexplored.
- **Moderate** — 3+ independent examples, consistent direction, counterexamples searched but the case isn't closed.
- **High** — many independent examples across creators/contexts, counterexamples examined and accounted for, plausible alternatives ruled out.

## Sources

- **YouTube Studio (owner-authorized, read-only)** — Glyph analytics. Access is session-based and intermittently gated by Google verification; gated reads are logged as failed checks, never worked around.
- **Public pages / platform clients** — competitor public metrics (views/likes/comments).
- **Comment samples** — mixed Top + Newest samples; sample size, method, and time always recorded; a sample never claims to represent the whole audience.
