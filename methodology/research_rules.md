# Research Rules

How the Glyph Shorts Intelligence System collects and judges evidence. Established Oct 20, 2026.

## Collection

1. **Four categories, not just hits.** Log breakouts, normal performers, underperformers, and emerging (fast-accelerating) videos. A pattern is only meaningful if it also gets checked against ordinary and unsuccessful videos.
2. **Compare like with like.** Videos are compared within the same channel at similar ages after publication. A 200K video from a 10K-baseline creator can matter more than a 2M video from a 5M-baseline creator.
3. **Record the benchmark.** Every classification names the baseline, the window, the number of comparable videos, and the method (median preferred). No baseline → classification is `provisional`, never fabricated.
4. **Breakout multiplier** = observed views ÷ channel baseline views. Exploratory bands: ≥3x strong breakout candidate; 2–3x notable; 0.75–1.25x typical; <0.5x underperformer candidate. These are research categories, not algorithm facts.
5. **Snapshots, not overwrites.** Every new measurement is a new snapshot with its own collection timestamp. History is preserved. Monitored creators: `methodology/tripwire_roster.md`. Competitor JSONL pushes must merge by record `id` against remote head (never whole-file overwrite from a stale local copy that omits roster creators such as @GreenBroRants).

## Accuracy

6. **Label everything:** Verified / Calculated / Inferred / Unverified / Unavailable (definitions in `data_dictionary.md`).
7. **Never invent.** No fabricated statistics, transcripts, timestamps, visuals, comments, or URLs. If a video wasn't watched, say so — no first-frame breakdown from a title or thumbnail.
8. **Competitor internals are not public.** Retention, swipe-away, and subscriber attribution for other channels are Unavailable. Never estimate them.
9. **Respect access controls.** No bypassing sign-in or verification gates. Failed checks are recorded as failed, with the reason.
10. **No secrets in the repo.** No passwords, tokens, API keys, or personal information. Ever.

## Patterns

11. **Patterns are hypotheses.** Each pattern file entry states: hypothesis, supporting examples (by video ID), counterexamples, sample size in *independent videos* (repeated check-ins of one video are one example), confounders, confidence (low/moderate/high + why), application to Glyph, and the next test.
12. **Three examples ≠ confirmed.** Three independent instances justify closer investigation. Promotion to high confidence requires more independent videos, a counterexample search, and ruling out obvious alternatives (creator size, topic, timing, length).
13. **Correlation is not causation.** A threshold associated with success does not establish that crossing it causes success.
14. **Contradictions are assets.** Conflicting records are flagged in place, investigated, and the correction documented. Nothing is silently deleted.

## First three seconds (highest creative priority)

15. For every video actually inspected, record: first frame contents, character count and action, immediately recognizable conflict, on-screen text, opening spoken line (only if accurately accessible), time-to-premise, curiosity gap, movement/camera attention draws, and why a viewer might stay. Uninspected videos get `Unavailable`, not a guess.

## Cadence

16. **Every 12h:** monitored creators checked; new uploads logged; snapshots updated; breakout candidates flagged; failures recorded.
17. **Daily:** `reports/latest_brief.md` refreshed; unusually strong/weak videos investigated; Glyph analytics updated when authorized access works.
18. **Weekly:** winners vs losers compared; hypotheses re-scored with counterexamples; three original creative experiments recommended; weekly report filed under `reports/weekly/`.
19. **Failed or skipped runs are marked as such.** A check that didn't happen is never written up as if it did.
