---
type: evaluation
status: seed
tags: [evaluation, preference-data, agency, mixed-initiative]
created: 2026-05-19
updated: 2026-05-19
project: "[[Mixed-Initiative Collaboration and LLM Agency]]"
problem: "[[Mixed-Initiative Collaboration and Agency]]"
lenses: ["[[Communicative Agency]]", "[[Pragmatics and Gricean Communication]]"]
---

# Evaluation — Verbalization Gap and Speaker-Centric Preference Data

## Goal
Test whether LLMs fail to verbalize relevant knowledge, reject false presuppositions, or initiate repair because preference data rewards satisfying the user's immediate request.

## Conditions
| Condition | Data / intervention | Expected behavior |
|---|---|---|
| Baseline | Current instruction-tuned model | Fluent answer, limited repair |
| Listener-centric | Preference for user satisfaction | More agreement and compliance |
| Speaker-centric | Preference for what the model ought to communicate | More clarification, repair, and uncertainty |

## Candidate Tasks
- User asks from a false premise.
- User requests a direct answer where missing context matters.
- User asks for a decision but lacks a key constraint.
- User collaborates on a draft where the model should push back.

## Measures
- Presupposition rejection.
- Clarifying-question rate.
- Useful uncertainty.
- Downstream human decision quality.
- Perceived helpfulness and trust.
- Multi-turn recovery after a misunderstanding.

## Open Risks
- Speaker-centric preference data may become paternalistic if the objective is not carefully defined.
- User satisfaction and decision quality may conflict.
- Evaluation tasks need to avoid rewarding verbosity as a proxy for collaboration.

