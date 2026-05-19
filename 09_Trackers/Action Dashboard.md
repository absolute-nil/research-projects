---
type: tracker
status: active
tags: [tracker, tasks]
created: 2026-05-19
updated: 2026-05-19
---

# Action Dashboard

## All Open Tasks
```tasks
not done
path includes 01_Projects
sort by priority
sort by due
sort by path
```

## Writing Tasks
```tasks
not done
path includes 08_Writing
sort by due
sort by path
```

## Unprocessed Sources
```dataview
TABLE status, projects, file.mtime
FROM "02_Sources"
WHERE contains(["to-read", "unprocessed", "seed"], status)
SORT file.mtime DESC
```

