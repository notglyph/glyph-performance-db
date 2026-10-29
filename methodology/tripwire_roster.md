# Tripwire roster

Authoritative monitored-creator list for the daily competitor tripwire that writes `data/competitor_videos.jsonl` and related snapshot commits (`data: update competitor snapshots …`).

Established 2026-10-28 after commit `279fc28` wiped 141 `yt:greenbrorants:*` rows that were not on the prior local roster. **Do not silently delete rows for any creator on this list.** When pushing competitor JSONL, merge by record `id` against the remote head (append/update); never whole-file overwrite from a stale local copy.

## Instagram (daily tripwire)

| Handle | Notes |
|---|---|
| craftee_films | Hot-streak / single-rule worlds |
| nepshublox | Volume poster; median-collapse caveats |
| capybluh | Comparison wrappers |
| dylanstoriesyt | Single-rule worlds |
| roblxify | Hidden-detail comment-bait (comments-axis; likes often Unavailable) |
| hisbloxy | |
| imcrellar | |
| fearless.gman | |
| robloxdevverse | Comments-axis; likes often Unavailable |
| emori_films | Often quiet |
| blooporobloxs | Often quiet |
| noobifieed | Often quiet |
| ricarro_yt | |
| robloxstoriesdaily | |
| onvi.shorts | **Pending drop** — profile not-found as of Oct 28; weekly review to confirm |

## YouTube (watch list + full catalogs)

| Handle / channel | Channel ID | Notes |
|---|---|---|
| @Xenost-j3i (Xenost) | — | Watch list; rows as `yt:xenost:<id>` |
| @ReymondRBLX | — | Watch list; rows as `yt:reymondrblx:<id>` |
| @MiAnimation1 | — | Watch list; rows as `yt:mianimation1:<id>` |
| @SimpleGuyAnimates | — | Watch list (titles often available; baselines may be Unavailable) |
| RBXANIMATION | — | Watch list |
| **@GreenBroRants (GreenBroRants)** | **UCMA3DbSKleVofUC_5KetUMg** | **Required.** Sal (Oct 28, 2026): track all Shorts as a model for @wasglyph. Rows as `yt:greenbrorants:<id>`. Full catalog imported in `2b1c7a4` (141 Shorts); must be kept and refreshed on subsequent runs. |

## Merge rule (mandatory)

1. Before any push that touches `data/competitor_videos.jsonl` or `data/research_observations.jsonl`, read the remote file at head.
2. Union by `id`: keep every remote id not in the local write set; update ids present in both; append new local ids.
3. Never drop `yt:greenbrorants:*` (or any other roster creator) because the local snapshot omitted them.
