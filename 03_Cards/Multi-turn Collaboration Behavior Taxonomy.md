---
type: card
status: active
tags: [card, collaboration, taxonomy, user-simulation]
created: 2026-05-19
updated: 2026-05-19
projects:
  - "[[MSR User Simulation — Hypothesis Generator]]"
  - "[[Mixed-Initiative Collaboration and LLM Agency]]"
problems:
  - "[[Mixed-Initiative Collaboration and Agency]]"
  - "[[User Simulation for Human-AI Intervention Design]]"
lenses:
  - "[[Communicative Agency]]"
  - "[[Common Ground and Deliberation]]"
---

# Multi-turn Collaboration Behavior Taxonomy

## Purpose
Define the behavior space for studying desirable and undesirable information flows in multi-turn human-AI collaboration.

## Collaboration Boundary
- Completion: one-shot artifact generation.
- Single-turn delegation: one-shot task execution.
- Multi-turn delegation: repeated task execution where the user still owns goals and success criteria.
- Multi-turn collaboration: joint management of goals, constraints, shared context, initiative, repair, and evolving plans.

## Desirable Collaboration Behaviors
| Behavior | What it looks like |
|---|---|
| Goal alignment | The model checks whether it understands the user's actual objective. |
| Constraint elicitation | The model asks for missing constraints before committing to a path. |
| Assumption surfacing | The model marks assumptions and asks whether they hold. |
| Repair | The model notices misunderstanding, drift, or contradiction and helps recover. |
| Productive pushback | The model rejects false premises or poor plans when needed. |
| Evidence grounding | Claims are tied to sources, reasons, or inspectable evidence. |
| Calibrated initiative | The model takes initiative when useful but does not seize control. |
| Decision trace | The conversation leaves a record of decisions, tradeoffs, and unresolved issues. |

## Undesirable Collaboration Behaviors
| Behavior | What it looks like |
|---|---|
| Premature compliance | The model answers before clarifying a fragile task. |
| Sycophancy | The model validates the user's framing even when it is weak or false. |
| Goal drift | The conversation moves away from the user's actual objective without acknowledgment. |
| Hidden assumptions | The model relies on unstated constraints or invented context. |
| Hallucinated common ground | The model acts as if agreement or shared understanding exists when it does not. |
| Overconfident synthesis | The model compresses uncertainty into a confident answer. |
| Passive user acceptance | The user stops questioning, verifying, or steering. |
| Missing repair | The model fails to recover after confusion, contradiction, or correction. |

## Measurement Ideas
- Turn-level labels for clarification, repair, pushback, assumption surfacing, grounding, and initiative.
- Segment-level labels for desirable or undesirable information flow.
- Conversation-level outcome: better decision, better artifact, better understanding, or calibrated trust.

## Links
- [[What are desirable and undesirable behaviors in multi-turn human-AI collaboration]]
- [[Can classifiers identify desirable and undesirable collaboration information flows]]
- [[MSR User Simulation — Hypothesis Generator]]

