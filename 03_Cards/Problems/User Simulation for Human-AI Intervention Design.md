---
type: problem
status: active
tags: [problem, user-simulation, hci, research-infrastructure]
created: 2026-05-19
updated: 2026-05-19
level: high
thesis_tracks:
  - "[[Track I — Human Behavior with AI]]"
  - "[[Track II — Conversational Agent Behavior in Complex Contexts]]"
  - "[[Track III — Democratized Information Governance]]"
projects:
  - "[[MSR User Simulation — Hypothesis Generator]]"
  - "[[Gricea]]"
organizations:
  - "[[Microsoft Research]]"
lenses:
  - "[[Simulation as hypothesis generator]]"
  - "[[Information Flows]]"
---

# User Simulation for Human-AI Intervention Design

## Problem
LLM-based user simulation is attractive because human studies are slow, expensive, and ethically constrained, but "realistic human simulation" is an unstable and underspecified goal. Human behavior changes across context, time, politics, technology, incentives, and interface affordances. Model behavior also changes.

## My Angle
Do not position simulation as a replacement for human users. Position it as a targeted hypothesis generator: create behavior simulators grounded in known undesirable information behaviors, test interface and agent affordances that push behavior toward desirable targets, then validate promising hypotheses with real humans.

The first concrete case is [[Multi-turn Collaboration Behavior Taxonomy]]: define desirable and undesirable collaboration through surveys/interviews, source conversations with those information flows, train a classifier, then use simulation to find interventions worth validating in [[Gricea]].

## Why This Belongs In The Thesis
This problem links [[Research Infrastructure for AI Studies]] to [[Biased Information Foraging and Echo Chambers]], [[Information Safety and Trust Calibration]], and [[Human Feedback and Power Dynamics]]. It gives [[Gricea]] a stronger role: a platform that can run both simulations and follow-up human studies.

## Core Tension
| Current field tendency | Better framing for this project |
|---|---|
| "Can we simulate humans realistically?" | "Can we use scoped simulations to generate useful intervention hypotheses?" |
| "Can simulation replace human evaluation?" | "Can simulation prioritize which human evaluations are worth running?" |
| "Can one simulator represent users generally?" | "Which behavior family and population boundary is this simulator valid for?" |
| "Does the simulated behavior look believable?" | "Does it predict or surface failures that matter for the next human study?" |

## Behavioral Targets
| Undesirable behavior | Desirable behavior |
|---|---|
| Not fact-checking | Source inspection and triangulation |
| Over-reliance | Calibrated trust |
| Confirmatory search | Exposure to relevant counterevidence |
| Low-quality feedback | Specific, actionable, context-rich feedback |
| Passive answer acceptance | Active questioning and repair |
| Premature compliance in collaboration | Clarification, assumption surfacing, and repair |
| Hallucinated common ground | Explicit shared-state checks |

## Open Questions
- [[What is the utility of LLM-based user simulation]]
- [[What are desirable and undesirable behaviors in multi-turn human-AI collaboration]]
- [[Can classifiers identify desirable and undesirable collaboration information flows]]
- [[Do we need to understand human behavior before predicting it]]
- [[When should simulation optimize for realism vs stress testing]]
- [[Can undesirable-behavior simulators generate intervention hypotheses]]
- [[How should simulations be calibrated against human studies]]
- [[What are the boundaries of LLM-based human simulation]]
