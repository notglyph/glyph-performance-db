# Mission 003 — Operation Frame Zero: Study

*Status: IN PROGRESS (Oct 20, 2026). Access checkpoint passed; sample partially built; deep dives pending for most of the sample. Sections marked PENDING contain no findings — they fill as verified observations land. Access detail: `reports/mission_003_access_report.md`.*

## Sample status

| Block | Status |
|---|---|
| Access checkpoint (§3) | ✅ Complete — playback + captions Available; seek Partial; transcript tab Unavailable. |
| MiAnimation1 grid + records | ✅ 13 structured records with URLs/IDs added to `data/competitor_videos.jsonl` (12 most recent + the last-30 maximum). Baseline: median of 12 most recent = 582.5K views (rounded grid counts). Breakouts identified: 3.2M (5.5x), 2.6M (4.5x), 19M (~33x, age-unmatched — approximate). Matched comparisons on the same channel: 45K (0.08x), 54K (0.09x), 243K (0.42x), 260K (0.45x), 303K (0.52x). |
| Xenost / ReymondRBLX / GeyzeRBX grids | ⏳ In flight (browser capture running at first writing). |
| Glyph reference case (§8) | ✅ D.B. Cooper fully observed (frame zero, 0–3s, full story from captions). Record: `data/youtube_short_visual_observations.jsonl`. |
| Deep dives (frame-zero / 3s / story) for competitor sample | ⏳ Pending grid completion. |
| Winners-vs-losers counts (§7) | ⏳ Pending deep dives. Skeleton: `analysis/visual_hook_comparisons.md`. |
| Three first-frame experiments (§9) | ⏳ Drafted after the counts exist. (Mission 002's Experiment 1–3 in `reports/first_20_video_study.md` remain the standing tests meanwhile.) |

## §8 — Glyph application (verified portion)

**D.B. Cooper vs the swipe/body split.** Verified opening: cabin two-shot, question asked by narration, zero dilemma information visible at 0:00; premise lands ~2–3s by voice. Outcome: 71.3% stayed / 101.4% avg viewed. The split's most economical explanation now has a *seen* mechanism behind it: viewers deciding in the first second had nothing visual to decide *with*. The retention-oriented Glyph videos in our DB (Oxygen Mask 83.3% stayed; Escape Pod 79.1% with a 1.1% debate comment rate) put the dilemma's object and stakes on screen as the premise — the debate-oriented wins pair that with a choice viewers can argue about. D.B. Cooper had the argument (a genuine reversal story, verified from captions) but not the visible premise.

**Thumbnail ≠ frame zero (verified):** D.B. Cooper's feed thumbnail is a mid-video confrontation frame. Any packaging judgment made from thumbnails — ours or competitors' — must be re-based on playback.

## Method notes

- All view multiples in this mission are **view-based** (Mission 003 §2); IG engagement multiples from earlier missions are never mixed in.
- Grid view counts are rounded as displayed; multiples computed from them are labeled Calculated.
- Timestamps from playback are approximate (percentage seek); every record states its seek precision.
