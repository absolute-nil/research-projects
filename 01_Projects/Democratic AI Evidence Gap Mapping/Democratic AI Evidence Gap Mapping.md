---
type: project
status: seed
stage: proposal
tracker_status: ":ziang-xiao:"
last_reviewed: 2026-05-19
next_milestone: "Define extraction schema and three public-concern examples"
tags: [project, method/hci, method/nlp, democratic-ai, public-deliberation, evidence-gap]
created: 2026-05-19
updated: 2026-05-19
aliases: [CIP Global Dialogues Evidence Gap Mapping, MSR Internship Draft]
collaborators: []
venue_target:
deadline:
methods: [hci, nlp, simulation, evidence-mapping]
themes: [democratic-ai, public-input, collective-intelligence, policy]
problems:
  - "[[Community-Based Auditing and Participatory Evaluation]]"
  - "[[Research Infrastructure for AI Studies]]"
lenses:
  - "[[Power Dynamics in Human-AI Systems]]"
  - "[[Information Flows]]"
thesis_track: "[[Track III — Democratized Information Governance]]"
source: https://docs.google.com/document/d/1hMVMK9RyuaIHGv_TSCZo1049Upm41EsV1Y-TC1NL-DU
---

# Democratic AI Evidence Gap Mapping

## Pitch
This project turns public deliberation data into empirical AI research questions, maps those questions against existing evidence, and uses Gricea to generate executable study designs or grounded simulations for understudied public concerns.

## Current Question
Can public concerns about AI be systematically translated into researchable questions, evidence-gap maps, and study designs that help researchers and policymakers prioritize what to study next?

## Research Questions
| ID | Question | Method | Status |
|---|---|---|---|
| RQ1 | How can open-ended public responses be converted into researchable HCI/AI questions? | NLP extraction + human validation | seed |
| RQ2 | Which public AI concerns are already supported by empirical evidence, partially studied, or understudied? | evidence mapping | seed |
| RQ3 | Can Gricea convert high-value public concerns into reproducible study designs? | system pipeline | seed |
| RQ4 | Can grounded simulations help prioritize human studies where evidence is missing? | simulation + calibration | seed |

## Claims
| Claim | Evidence needed | Linked notes |
|---|---|---|
| AI governance needs a translation layer between public deliberation and empirical research. | Examples from Global Dialogues mapped to RQs. | [[Public deliberation can become empirical research questions]] |
| Current AI evidence is fragmented and shaped by actors with the resources to run studies. | Evidence-gap map across public concerns. | [[AI systems need a living empirical evidence corpus]] |
| Gricea can make democratic AI research more actionable by generating study artifacts. | Demonstration on selected Global Dialogues concerns. | [[Gricea]] |

## Workstreams
- Data: [[Global Dialogues]] responses, demographic segments, tags, translations, summaries, votes, and pairwise preferences.
- Extraction: public concern, affected community, AI behavior, measurable outcome, studyable intervention.
- Evidence map: studied / partially studied / no clear evidence.
- Study generation: Gricea artifacts.
- Simulation: personas grounded in public response data.

## Related Terms
- [[democratic AI]]
- [[collective intelligence]]
- [[AI systems need a living empirical evidence corpus]]
- [[Public deliberation can become empirical research questions]]
- [[User behavior is affordance-dependent]]

## Organizations
- [[Center for an Informed Public]]
- [[Global Dialogues]]
- [[Microsoft Research]]

## Next Actions
- [ ] Add source docs or datasets for Global Dialogues.
- [ ] Define schema for extracted research questions.
- [ ] Identify first 3 public concern examples to convert into Gricea studies.

## Project Log
- 2026-05-19: Created from Google Doc draft material.
