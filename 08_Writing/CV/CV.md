---
type: cv
status: active
tags: [cv, writing]
created: 2026-05-19
updated: 2026-05-19
---

# CV

## Maintenance Rule
Keep the canonical CV document elsewhere if needed, but use this note as the linked research CV index. Each entry can link to the project, paper, talk, award, or service record it came from.

## Publications
```dataview
TABLE venue, year, projects
FROM "02_Sources/My Publications" OR "02_Sources/Papers"
WHERE contains(tags, "publication") OR type = "paper"
SORT year DESC
```

## Projects
```dataview
TABLE stage, tracker_status, venue_target, deadline
FROM "01_Projects"
WHERE type = "project"
SORT file.mtime DESC
```

## Presentations
```dataview
TABLE project, venue, date, status
FROM "08_Writing/Presentations"
WHERE type = "presentation"
SORT date DESC
```

## Awards / Fellowships
- [[Nikhil Fellowships Research Statement]]

