---
type: tracker
status: active
tags: [tracker, project]
created: 2026-05-19
updated: 2026-05-19
---

# Project Tracker

## Source Of Truth
Each project note owns its own status. Update these fields first:

| Field | Meaning |
|---|---|
| `tracker_status` | Emoji marker for lifecycle status |
| `health` | green / yellow / red |
| `priority` | P0 / P1 / P2 / P3 |
| `next_action` | One concrete next action, not a vague milestone |
| `next_milestone` | The next meaningful project checkpoint |
| `blockers` | Current blocker list |
| `last_reviewed` / `next_review` | Review cadence |

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
TABLE tracker_status AS Status, health AS Health, priority AS Priority, stage AS Stage, next_action AS "Next Action", blockers AS Blockers, next_review AS "Next Review"
FROM "01_Projects"
WHERE type = "project" AND status != "archived"
SORT priority ASC, health DESC, next_review ASC
```

## Red / Yellow Projects
```dataview
TABLE tracker_status AS Status, priority AS Priority, next_action AS "Next Action", blockers AS Blockers, next_milestone AS "Next Milestone"
FROM "01_Projects"
WHERE type = "project" AND status != "archived" AND (health = "red" OR health = "yellow")
SORT priority ASC, next_review ASC
```

## By Stage
```dataview
TABLE tracker_status AS Status, health AS Health, priority AS Priority, next_action AS "Next Action"
FROM "01_Projects"
WHERE type = "project" AND status != "archived"
GROUP BY stage
SORT stage ASC
```

## By Thesis Track
```dataview
TABLE tracker_status AS Status, health AS Health, priority AS Priority, stage AS Stage, problems AS Problems, next_action AS "Next Action"
FROM "01_Projects"
WHERE type = "project" AND status != "archived"
GROUP BY thesis_track
```

## Projects Missing Tracker Fields
```dataview
TABLE stage, status, tracker_status, health, priority, next_action, last_reviewed, next_review
FROM "01_Projects"
WHERE type = "project" AND (!tracker_status OR !health OR !priority OR !next_action OR !last_reviewed OR !next_review OR !next_milestone)
SORT file.mtime DESC
```

## Stale Reviews
```dataview
TABLE tracker_status AS Status, health AS Health, priority AS Priority, last_reviewed AS "Last Reviewed", next_review AS "Next Review", next_action AS "Next Action"
FROM "01_Projects"
WHERE type = "project" AND status != "archived" AND next_review AND next_review < date(today)
SORT next_review ASC
```

## Project Open Questions
```dataview
TABLE answer_status AS Answer, status, project, projects, problem
FROM "03_Cards/Research_Questions"
WHERE type = "research-question" AND answer_status != "answered"
SORT project ASC, file.mtime DESC
```
