# Mission 003 — Access Report

*Oct 20, 2026. Mandatory checkpoint (Mission 003 §3), executed before sample analysis. Test subjects: "The D.B. Cooper Dilemma.." (@wasglyph, `x_amXwtRcG4`) via direct browser playback + thumbnail endpoints; MiAnimation1 channel grid.*

## Capability classification

| Capability | Status | Evidence |
|---|---|---|
| Direct playback (motion + audio) | **Available** | The Short plays in the browser with moving animation and audible narration; pause works (button + keyboard); reload restarts from 0:00. No sign-in wall, age gate, or bot check encountered. |
| Frame-zero observation | **Available** | Earliest frames observable on load/reload. First verified frame-zero captured for `x_amXwtRcG4` (see `data/youtube_short_visual_observations.jsonl`). |
| Second-accurate seeking | **Partially available** | The Shorts seek slider is percentage-based with no per-second readout. Scrubbing is coarse; all second-level timestamps in this mission are approximations converted from percentages against runtime, and are labeled as such. |
| Spoken audio | **Available** | Narration audible; auto-generated captions readable during playback and sufficient to verify the spoken hook verbatim. |
| Transcript panel | **Unavailable** | Shorts expose no transcript tab (player menu offers captions only). The public timedtext endpoint returned no track list. Captions during playback are the working route. |
| Public metadata | **Available** | Title, views, likes, comments, upload date readable on the video page; channel grids show per-video view counts (rounded as displayed — always labeled). |
| Thumbnail frames | **Available, with a verified caveat** | `i.ytimg.com/vi/<id>/oardefault.jpg` returns the full 1080×1920 feed thumbnail. **Verified on `x_amXwtRcG4`: the thumbnail is a later confrontation frame, NOT frame zero** (creator-selected). Thumbnails are evidence about the *feed-facing frame*, never about 0:00, and are labeled accordingly in every record. |

## Consequence for the mission

The visual study can proceed: frame-zero and first-3-seconds analysis will rest on **direct playback observation + captions**, with approximate timestamps. No observation in Mission 003 comes from a thumbnail or a title.

## First verified finding (Glyph's own video, feeds the study's §8)

D.B. Cooper's actual opening (verified): a two-character cabin two-shot; the narration opens with a question ("Would you trust your best friend with your life?"), but **no dilemma object, danger, or choice is visible at 0:00** — the premise arrives by voice over ~2–3s. Full record: `data/youtube_short_visual_observations.jsonl`.
