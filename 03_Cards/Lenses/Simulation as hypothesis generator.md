---
type: lens
status: active
tags: [lens, user-simulation, hypothesis-generation]
created: 2026-05-19
updated: 2026-05-19
problems:
  - "[[User Simulation for Human-AI Intervention Design]]"
projects:
  - "[[MSR User Simulation — Hypothesis Generator]]"
  - "[[Gricea]]"
---

# Simulation as hypothesis generator

## Claim
The strongest use of LLM-based user simulation is not to prove how real users behave. It is to cheaply generate, compare, and prioritize hypotheses about which system designs might change behavior, before running expensive human studies.

## Pipeline
1. Identify a behavior family from literature or prior studies.
2. Build an undesirable-behavior simulator for a scoped context.
3. Define desirable target behavior and measurable movement.
4. Test interface or agent affordances against the simulator.
5. Treat successful simulated interventions as hypotheses.
6. Validate with humans in [[Gricea]].
7. Update the simulator from human-study misalignment.

## Guardrails
- A simulation result is never final evidence.
- Every simulator must state its population, context, behavior family, and invalid uses.
- Evaluation should report calibration against human data, not only believability.
- Simulations should include failure and fairness checks.

## Links
- [[LLM Human Simulation — Master Note]]
- [[User Simulation for Human-AI Intervention Design]]
- [[Feature — Simulation Harness for Behavioral Hypotheses]]

