---
type: research-question
status: active
answer_status: unanswered
tags: [research-question, classifier, collaboration, information-flow]
created: 2026-05-19
updated: 2026-05-19
problem: "[[User Simulation for Human-AI Intervention Design]]"
project: "[[MSR User Simulation — Hypothesis Generator]]"
projects: ["[[MSR User Simulation — Hypothesis Generator]]", "[[Gricea]]"]
lenses: ["[[Simulation as hypothesis generator]]", "[[Information Flows]]", "[[Communicative Agency]]"]
methods: [annotation, classifier, conversation-analysis]
---

# Can classifiers identify desirable and undesirable collaboration information flows?

## Question
Can a classifier detect desirable and undesirable information-flow patterns in multi-turn human-AI collaboration conversations?

## Why It Matters
The classifier is the bridge between human-defined behavior taxonomies and simulation. It can help source examples, measure interventions, and evaluate whether a simulated or real conversation is moving toward better collaboration.

## Current Best Guess
A multi-label classifier may work if labels are anchored to observable turn or segment behaviors rather than vague holistic quality.

## How To Study It
- Collect or source multi-turn collaboration conversations.
- Label turn-level and segment-level behaviors from [[Multi-turn Collaboration Behavior Taxonomy]].
- Train and evaluate a classifier for desirable and undesirable information-flow patterns.
- Use classifier outputs to select simulator examples and evaluate intervention effects.

## Links
- Project: [[MSR User Simulation — Hypothesis Generator]]
- Feature: [[Feature — Simulation Harness for Behavioral Hypotheses]]
- Lens: [[Simulation as hypothesis generator]]

