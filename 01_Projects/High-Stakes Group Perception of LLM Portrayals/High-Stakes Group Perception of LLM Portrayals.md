---
type: project
status: active
stage: design
tracker_status: ":ziang-xiao:"
health: yellow
priority: P1
last_reviewed: 2026-05-19
next_review: 2026-05-26
next_milestone: "Define high-stakes group inclusion rules and tractable topics"
next_action: "Draft inclusion/exclusion rules for high-stakes groups"
blockers: [ethics, topic-selection]
tags: [project, method/hci, method/nlp, narratives, stakeholder-feedback, llm-evaluation]
created: 2026-05-19
updated: 2026-05-19
aliases: [Perception of LLM Portrayal of Opinionated Issues by High-Stake Groups]
collaborators: []
venue_target:
deadline:
methods: [hci, evaluation, stakeholder-feedback]
themes: [narratives, representation, information-access, pluralism]
problems:
  - "[[Community-Based Auditing and Participatory Evaluation]]"
  - "[[Cross-Cultural Information Access]]"
lenses:
  - "[[Common Ground and Deliberation]]"
  - "[[Capability Labels and Taxonomies]]"
thesis_track: "[[Track II — Conversational Agent Behavior in Complex Contexts]]"
source: https://docs.google.com/document/d/1hMVMK9RyuaIHGv_TSCZo1049Upm41EsV1Y-TC1NL-DU
---

# High-Stakes Group Perception of LLM Portrayals

## Pitch
This project studies how people with different stakes in divisive issues judge LLM responses about those issues, and whether conditioning LLM outputs on stakeholder feedback improves perceived representativeness, diversity, satisfaction, and fairness.

## Current Question
How should LLMs portray opinionated, high-stakes issues when affected groups disagree about what counts as fair, representative, or satisfying information?

## Research Questions
| ID | Question | Method | Status |
|---|---|---|---|
| RQ1 | How do in-group members view information a chatbot presents to out-group members on divisive issues? | stakeholder study | seed |
| RQ2 | How do responses change when the model is conditioned on feedback from in-group members? | generation + evaluation | seed |
| RQ3 | Do in-group and out-group members react differently to feedback-conditioned outputs? | comparative evaluation | seed |

## Claims
| Claim | Evidence needed | Linked notes |
|---|---|---|
| Neutrality is underspecified for divisive issues. | Cases where groups disagree about valid perspectives. | [[Normative vs Descriptive Question Framing]] |
| Stakeholder satisfaction may reveal failures invisible to generic evaluation. | Ratings from directly affected groups. | [[High-stakes groups are evaluators of LLM portrayals]] |
| Feedback-conditioned outputs may improve representation but risk validating harmful perspectives. | Phase 1/2 comparison with explicit inclusion criteria. | [[What Should Information Assistants Do]] |

## Workstreams
- Study: [[Study — Stakeholder Perception of LLM Portrayals]]
- Topic set: abortion, Bangladesh protests, Israel/Gaza, Ukraine/Russia, China/Taiwan, Tibet, immigration, economic policy.
- Metric set: truthfulness, objectivity, representativeness, diversity, relevance, cognitive load, bias, clarity, change requests.
- Artifact: stakeholder-feedback chatbot arena.

## Related Terms
- [[NarrativeBench — Cross-Cultural Multilingual Benchmark]]
- [[Topicality vs Multilinguality — Topical Bias Framework]]
- [[Same Facts Different Narratives]]
- [[Normative vs Descriptive Question Framing]]
- [[Wikipedia as Ground Truth Causes Problems in Low-Resource Languages]]

## Next Actions
- [ ] Define "high-stakes group" inclusion rules.
- [ ] Decide which topics are ethically and practically tractable.
- [ ] Turn the topic table into a `Sources` or `Evaluation` note.

## Project Log
- 2026-05-19: Created from Google Doc draft material.
