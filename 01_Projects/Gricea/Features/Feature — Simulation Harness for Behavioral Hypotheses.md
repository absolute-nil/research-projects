---
type: software-feature
status: seed
priority: P1
tags: [software-feature, gricea, user-simulation, behavioral-intervention]
created: 2026-05-19
updated: 2026-05-19
last_reviewed: 2026-05-19
project: "[[Gricea]]"
objective: "Run scoped user simulators as hypothesis generators, then connect simulation results to human-study validation."
problems:
  - "[[User Simulation for Human-AI Intervention Design]]"
  - "[[Research Infrastructure for AI Studies]]"
research_questions:
  - "[[Can undesirable-behavior simulators generate intervention hypotheses]]"
  - "[[How should simulations be calibrated against human studies]]"
constraints: [privacy, calibration, reproducibility, simulator-drift]
---

# Feature — Simulation Harness for Behavioral Hypotheses

## User / Research Need
Researchers need a way to test many candidate interface and LLM-behavior interventions cheaply before running human studies, while keeping clear boundaries around what simulation can and cannot claim.

## Requirements
- Define simulator profile, behavior family, grounding evidence, and invalid uses.
- Run a simulator across multiple intervention conditions.
- Log prompts, model versions, simulator outputs, intervention settings, and outcome metrics.
- Compare simulator outputs with human-study results from Gricea.
- Produce a calibration report before simulator reuse.

## Acceptance Criteria
- [ ] A study can define an undesirable behavior simulator.
- [ ] The same intervention conditions can be run in simulation and human-study modes.
- [ ] Outputs can be compared at outcome and trace levels.
- [ ] Simulator results are labeled as hypotheses until human validation is attached.

## Open Questions
- [ ] Should simulator definitions live in project notes, Gricea config, or both?
- [ ] How many simulator models are needed for robustness checks?
- [ ] Which behavior metrics are general enough to reuse?

