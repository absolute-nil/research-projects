---
type: software-feature
status: seed
priority: P1
tags: [software-feature, gricea, study-authoring]
created: 2026-05-19
updated: 2026-05-19
last_reviewed: 2026-05-19
project: "[[Gricea]]"
objective: "Let researchers define study stages, conditions, tasks, and agent behavior without custom code."
problems: ["[[Research Infrastructure for AI Studies]]"]
research_questions: ["[[How do we scale manipulation of conversational agents for large-scale studies]]"]
constraints: [privacy, reproducibility, experimental-control]
---

# Feature — Study Flow Builder

## User Need
Researchers need to define conversational AI studies quickly while preserving condition assignment, consent, task order, and reproducibility.

## Requirements
- Define participant flow: consent, pre-survey, task, conversation, post-survey, debrief.
- Define experimental conditions and randomization.
- Attach agent instructions, retrieval settings, modality, and UI variants to conditions.
- Export a readable protocol.

## Open Questions
- [ ] What is the minimum viable schema for a study flow?
- [ ] Which fields must be locked before preregistration?
- [ ] How should the builder represent conversational interventions?

