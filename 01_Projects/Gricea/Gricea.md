---
type: project
status: active
stage: building
tracker_status: ":claude:"
last_reviewed: 2026-05-19
next_milestone: "Define study-flow schema, logging requirements, and platform evaluation"
tags: [project, method/hci, platform, open-science, conversational-ai]
created: 2026-05-19
updated: 2026-05-19
aliases: [Gricea Platform]
collaborators: []
venue_target:
deadline:
methods: [hci, platform, study-infrastructure]
themes: [conversational-ai, reproducibility, open-science, study-authoring]
problems:
  - "[[Research Infrastructure for AI Studies]]"
  - "[[Community-Based Auditing and Participatory Evaluation]]"
lenses:
  - "[[Information Flows]]"
  - "[[Power Dynamics in Human-AI Systems]]"
thesis_track: "[[Track III — Democratized Information Governance]]"
source: https://docs.google.com/document/d/1hMVMK9RyuaIHGv_TSCZo1049Upm41EsV1Y-TC1NL-DU
---

# Gricea

## Pitch
Gricea is a platform for designing, developing, deploying, and analyzing conversational AI studies. The core argument is that AI is changing too quickly for slow, one-off HCI study infrastructure; researchers need reusable, controlled, auditable infrastructure for studying how AI system design shapes human behavior.

## Current Question
How can Gricea lower the barrier for rigorous conversational AI studies while preserving experimental control, reproducibility, privacy, and fine-grained behavioral logging?

## Research Questions
| ID | Question | Method | Status |
|---|---|---|---|
| RQ1 | What kinds of conversational AI studies can be expressed through a configurable study-authoring platform? | platform evaluation | seed |
| RQ2 | Does visual study authoring reduce development time without reducing experimental rigor? | HCI study | seed |
| RQ3 | What logging, consent, and data controls are needed for production-quality conversational AI studies? | system design / governance | active |

## Claims
| Claim | Evidence needed | Linked notes |
|---|---|---|
| AI study infrastructure is a bottleneck for scientific progress on human-AI interaction. | Examples of slow, bespoke study development; time-to-study benchmarks. | [[AI systems need a living empirical evidence corpus]] |
| Researchers need controlled manipulation of model, system, and interface variables. | Taxonomy of study variables and examples expressible in Gricea. | [[Conversational Information Foraging]] |
| Open study protocols and shared data can improve cumulative science. | Governance model, privacy plan, and reusable protocol repository. | [[open science]] |

## Workstreams
- Platform: study flow, task flow, agent conditions, interface conditions, logging, deployment.
- Study authoring: visual builder for non-software researchers.
- Data infrastructure: fine-grained interaction logs, export formats, consent and privacy.
- Community layer: shared study protocols, designs, and data where ethically possible.
- Software features: [[Feature — Study Flow Builder]], [[Feature — Fine-Grained Interaction Logs]], [[Feature — Research Protocol Sharing]]
- Imported older notes: [[Notes — Gricea Imported Card]]

## Related Terms
- [[conversational AI]]
- [[human-AI interaction]]
- [[study authoring]]
- [[open science]]
- [[AI systems need a living empirical evidence corpus]]
- [[Public deliberation can become empirical research questions]]

## Literature Backbone
- [[Conversational Information Foraging]]
- [[User-Created AI Interfaces]]
- [[Human + AI vs AI + AI vs AI alone how does the task performance vary and what value do humans add]]

## Decisions
| Date | Decision | Rationale |
|---|---|---|
| 2026-05-19 | Keep Gricea as a project folder, not just a card. | It has platform, paper, study, and grant dimensions. |

## Next Actions
- [ ] Add current Gricea repository / deployment links.
- [ ] Create a [[Study — Gricea Platform Evaluation]] note when the evaluation design is clearer.
- [ ] Define privacy/security requirements for production study logging.

## Project Log
- 2026-05-19: Created from Google Doc draft material.
