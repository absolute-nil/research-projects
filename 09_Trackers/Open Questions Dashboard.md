---
type: tracker
status: active
tags: [tracker, research-question]
created: 2026-05-19
updated: 2026-05-19
---

# Open Questions Dashboard

## Where To Put Questions
Put open unanswered questions in `03_Cards/Research_Questions` using [[TPL — Research Question]].

Use a project page only for very local tactical questions. If a question could matter to more than one project, make it a research-question note and link it back to projects, problems, and lenses.

## Unanswered Questions
```dataview
TABLE status, project, projects, problem, lenses, methods
FROM "03_Cards/Research_Questions"
WHERE type = "research-question" AND answer_status = "unanswered"
SORT file.mtime DESC
```

## Partially Answered Questions
```dataview
TABLE status, project, projects, problem, lenses, methods
FROM "03_Cards/Research_Questions"
WHERE type = "research-question" AND answer_status = "partial"
SORT file.mtime DESC
```

## By Problem
```dataview
TABLE answer_status AS Answer, status, project, projects, methods
FROM "03_Cards/Research_Questions"
WHERE type = "research-question" AND answer_status != "answered"
GROUP BY problem
```
