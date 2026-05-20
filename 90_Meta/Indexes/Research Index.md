---
type: index
tags:
  - index
  - meta
---

# Research Index

## Cards by Maturity
```dataview
TABLE status, maturity, projects, themes, methods
FROM "03_Cards"
WHERE type = "card"
SORT maturity ASC, file.mtime DESC
```

## Problems
```dataview
TABLE status, thesis_tracks, projects, lenses
FROM "03_Cards/Problems"
WHERE type = "problem"
SORT file.name ASC
```

## Lenses
```dataview
TABLE status, problems, projects
FROM "03_Cards/Lenses"
WHERE type = "lens"
SORT file.name ASC
```

## Research Questions
```dataview
TABLE answer_status AS Answer, status, problem, project, projects, lenses
FROM "03_Cards/Research_Questions"
WHERE type = "research-question"
SORT status ASC, file.name ASC
```

## Papers by Project
```dataview
TABLE year, venue, read_status, projects
FROM "02_Sources/Papers"
WHERE type = "paper"
SORT year DESC
```

## Studies and Evaluations
```dataview
TABLE type, method, status, project
FROM "01_Projects"
WHERE contains(["study", "evaluation", "experiment", "software-feature"], type)
SORT file.mtime DESC
```

## Writing Artifacts
```dataview
TABLE status, project, venue, date
FROM "08_Writing"
WHERE contains(["writing", "presentation", "rebuttal", "cv", "paper-revision-workflow"], type)
SORT file.mtime DESC
```

## Unprocessed Imports
```dataview
LIST
FROM "00_Inbox"
SORT file.mtime DESC
```
