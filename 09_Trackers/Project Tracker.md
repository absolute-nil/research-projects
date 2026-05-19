---
type: tracker
status: active
tags: [tracker, project]
created: 2026-05-19
updated: 2026-05-19
---

# Project Tracker

## Status Legend
| Marker | Meaning | Use when |
|---|---|---|
| `:this_is_fine:` | IRB | Protocol, consent, or ethics review is the bottleneck |
| `:glitch_crab:` | Pre-registration | Study design or analysis plan needs locking |
| `:ziang-xiao:` | Need review | Needs advisor/collaborator review |
| `:claude:` | Experiments | Data collection, modeling, or system experiments are active |
| `:dart:` | Final Stage | Writing, rebuttal, camera-ready, or final polish |
| `:x:` | Didn't make it | Paused, rejected, scoped out, or archived |

## Active Projects
```dataview
TABLE tracker_status AS Status, stage AS Stage, thesis_track AS Track, next_milestone AS "Next Milestone", last_reviewed AS "Last Reviewed", deadline AS Deadline
FROM "01_Projects"
WHERE type = "project" AND status != "archived"
SORT last_reviewed DESC, file.mtime DESC
```

## By Thesis Track
```dataview
TABLE tracker_status AS Status, stage AS Stage, problems AS Problems, next_milestone AS "Next"
FROM "01_Projects"
WHERE type = "project" AND status != "archived"
GROUP BY thesis_track
```

## Projects Missing Tracker Fields
```dataview
TABLE stage, status, file.mtime
FROM "01_Projects"
WHERE type = "project" AND (!tracker_status OR !last_reviewed OR !next_milestone)
SORT file.mtime DESC
```

