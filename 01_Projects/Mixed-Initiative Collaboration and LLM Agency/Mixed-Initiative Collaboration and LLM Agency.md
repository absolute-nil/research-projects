---
type: project
status: active
stage: seed
tracker_status: ":ziang-xiao:"
last_reviewed: 2026-05-19
next_milestone: "Narrow empirical hook and define first study"
tags: [project, method/nlp, method/hci, collaboration, agency, alignment]
created: 2026-05-19
updated: 2026-05-19
aliases: [Mixed-Initiative Collaboration, Missing Agency in LLMs]
collaborators: []
venue_target:
deadline:
methods: [preference-data, dialogue-evaluation, hci]
themes: [mixed-initiative, common-ground, agency, collaboration]
problems:
  - "[[Mixed-Initiative Collaboration and Agency]]"
  - "[[Information Safety and Trust Calibration]]"
lenses:
  - "[[Communicative Agency]]"
  - "[[Pragmatics and Gricean Communication]]"
  - "[[Common Ground and Deliberation]]"
thesis_track: "[[Track II — Conversational Agent Behavior in Complex Contexts]]"
source: "[[Mixed Initiative Collaboration — Source Notes]]"
---

# Mixed-Initiative Collaboration and LLM Agency

## Pitch
Current LLMs are strong at completing and delegating tasks, but weak at collaboration because they are trained to satisfy listener-centric preferences rather than to manage shared goals, repair, initiative, and common ground. This project asks whether speaker-centric preference data and collaboration-centered evaluations can recover communicative agency.

## Current Question
Can we operationally distinguish completion, delegation, and collaboration, then train or evaluate models for the behaviors needed for genuine mixed-initiative collaboration?

## Research Questions
| ID | Question | Method | Status |
|---|---|---|---|
| RQ1 | [[How do we distinguish completion delegation and collaboration]] | taxonomy + annotation | seed |
| RQ2 | [[Can speaker-centric preference data restore communicative agency]] | preference data + model evaluation | seed |
| RQ3 | Which model behaviors predict better human decisions rather than more satisfying immediate answers? | mixed-initiative tasks | seed |

## Core Claims
| Claim | Evidence needed | Linked notes |
|---|---|---|
| Collaboration is not the same as multi-turn task completion. | Taxonomy, examples, and annotator agreement. | [[Communicative Agency]] |
| Listener-centric preferences can discourage the model from rejecting presuppositions or initiating repair. | Preference pair analysis and counterfactual data. | [[Can speaker-centric preference data restore communicative agency]] |
| A useful collaborator should optimize for the human's eventual decision quality, not only immediate satisfaction. | User study or downstream task evaluation. | [[Common Ground and Deliberation]] |

## Workstreams
- Source synthesis: [[Mixed Initiative Collaboration — Source Notes]]
- Evaluation design: [[Evaluation — Verbalization Gap and Speaker-Centric Preference Data]]
- Related reading: [[Introspection Adapters — Training LLMs to Report Learned Behaviors]], [[LLMs Get Lost in Multi-Turn Conversations]]

## Next Actions
- [ ] Turn the completion/delegation/collaboration taxonomy into a coding rubric.
- [ ] Identify 2-3 datasets for extracting collaboration failures.
- [ ] Define one minimal experiment testing verbalization gap and presupposition rejection.

## Project Log
- 2026-05-19: Created from the mixed-initiative draft PDF and linked into the thesis problem map.

