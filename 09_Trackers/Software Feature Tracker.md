---
type: tracker
status: active
tags: [tracker, software, feature]
created: 2026-05-19
updated: 2026-05-19
---

# Software Feature Tracker

## Open Features
```dataview
TABLE project, status, priority, objective, constraints, last_reviewed
FROM "01_Projects"
WHERE type = "software-feature" AND status != "done"
SORT priority ASC, last_reviewed DESC
```

## Decisions
```dataview
TABLE project, decision_date, decision, rationale
FROM "01_Projects"
WHERE type = "software-decision"
SORT decision_date DESC
```

