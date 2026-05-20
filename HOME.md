---
type: home
tags:
  - home
cssclasses:
  - home
---

# Nikhil Sharma Research Vault

This vault is organized around projects, reusable cards, and source notes. Folders are only defaults for capture; the actual structure comes from wikilinks, backlinks, properties, tags, and Dataview.

## Start Here
- New idea: create in `03_Cards` with [[TPL — Concept & Idea]]
- New problem: create in `03_Cards/Problems` with [[TPL — Problem]]
- New lens: create in `03_Cards/Lenses` with [[TPL — Lens]]
- New research question: create in `03_Cards/Research_Questions` with [[TPL — Research Question]]
- New project: create a folder in `01_Projects` and add [[TPL — Project]]
- New study/evaluation/pseudocode: create it inside the relevant project folder
- New paper: import from Zotero into `02_Sources/Papers` with [[TPL — Paper Note]]
- New observation: create in `03_Cards/Observations` with [[TPL — Observation]]
- New organization: create in `04_Organizations` with [[TPL — Organization]]
- New rebuttal / revision / presentation: use `08_Writing`
- Daily scratchpad: use the Daily Note command

## Thesis Surface
- [[Overarching Thesis]]
- [[Thesis v2026-05-19]]
- [[Project Tracker]]
- [[Action Dashboard]]
- [[Software Feature Tracker]]
- [[Open Questions Dashboard]]
- [[Reading Channel Digest]]

## Active Projects
```dataview
TABLE tracker_status AS Status, stage, thesis_track AS Track, next_milestone AS "Next Milestone", deadline
FROM "01_Projects"
WHERE type = "project" AND status != "archived"
SORT last_reviewed DESC, deadline ASC, file.mtime DESC
```

## High-Level Problems
```dataview
TABLE status, projects, lenses
FROM "03_Cards/Problems"
WHERE type = "problem"
SORT file.name ASC
```

## Research Questions
```dataview
TABLE answer_status AS Answer, status, problem, project, projects, lenses
FROM "03_Cards/Research_Questions"
WHERE type = "research-question"
SORT status ASC, file.mtime DESC
```

## Open Questions
Use [[Open Questions Dashboard]] as the main question inbox.

## Project Components
```dataview
TABLE type, method, status, project
FROM "01_Projects"
WHERE contains(["study", "evaluation", "experiment", "pseudocode", "component", "software-feature"], type)
SORT file.mtime DESC
```

## Ideas To Revisit
```dataview
TABLE maturity, projects, themes, methods
FROM "03_Cards"
WHERE type = "card" AND (status = "seed" OR maturity = "seed")
SORT file.mtime DESC
LIMIT 25
```

## Recently Touched Sources
```dataview
TABLE authors, year, venue, read_status, projects
FROM "02_Sources/Papers"
WHERE type = "paper"
SORT file.mtime DESC
LIMIT 15
```

## Observations
```dataview
TABLE projects, people, organizations, themes
FROM "03_Cards/Observations"
WHERE type = "observation"
SORT file.mtime DESC
LIMIT 20
```

## Writing Pipeline
```dataview
TABLE status, project, venue, date
FROM "08_Writing"
WHERE contains(["writing", "presentation", "rebuttal", "paper-revision-workflow", "thesis-version", "cv"], type)
SORT file.mtime DESC
```

## People and Organizations
```dataview
TABLE type, institution, projects, themes
FROM "04_People" OR "04_Organizations"
WHERE type = "person" OR type = "organization"
SORT file.mtime DESC
```

## Open Tasks
```tasks
not done
sort by priority
sort by due
limit 30
```

## Research Graph Entry Points
Use these as graph filters, not as folder names.

`#project` `#problem` `#lens` `#research-question` `#paper` `#card` `#observation` `#person` `#organization` `#study` `#evaluation` `#experiment` `#pseudocode` `#software-feature` `#method/hci` `#method/nlp`

Key recurring terms should be links, for example `[[information seeking]]`, `[[voice AI]]`, `[[Cognitive Susceptibility in Voice AI]]`, `[[multilingual narratives]]`, `[[human-AI collaboration]]`.

## Guides
- [[Vault Operating Manual]]
- [[Zotero Workflow]]
- [[Tag and Link Conventions]]
- [[Research Index]]
