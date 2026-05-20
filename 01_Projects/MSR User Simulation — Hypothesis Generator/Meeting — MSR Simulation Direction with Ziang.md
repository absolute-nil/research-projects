---
type: meeting
tags: [meeting, user-simulation, msr]
created: 2026-05-19
updated: 2026-05-19
date: 2026-05-19
project: "[[MSR User Simulation — Hypothesis Generator]]"
attendees:
  - "[[Nikhil Sharma]]"
  - "[[Ziang Xiao]]"
organizations:
  - "[[Microsoft Research]]"
---

# Meeting — MSR Simulation Direction with Ziang

## Purpose
Clarify what user simulation is for, whether realism is the right objective, and whether the MSR project can be framed around simulation as a hypothesis generator for human-AI intervention design.

## Notes
- Nikhil's starting concern: human and model behavior both change, so "realistic" or "general" simulation is a weak objective.
- Nikhil's preferred direction: use simulation to represent known undesirable behavior families, then test interface or LLM affordances that move behavior toward desirable targets.
- Ziang's counterpoint: changing behavior is not a reason to reject simulation; behavioral science is already about prediction under changing conditions.
- Ziang's useful reframing: simulation can have utility without perfect prediction.
- Ziang's concrete utilities:
  - improve model quality;
  - identify usability issues;
  - offer policy-design insights;
  - reduce the cost of repeated human evaluation.
- Ziang's distinction: targeting vulnerable or failure behaviors is closer to red teaming/persona teaming than general user simulation.
- Shared convergence: the effective affordance found in simulation should be treated as a hypothesis for a human study.

## Decisions
- Frame the MSR project as hypothesis generation, not as proof that the simulation community is wrong.
- Connect the project to [[Gricea]] because Gricea can run the human validation loop after simulation screening.
- Avoid claiming that simulations represent all users or fully realistic behavior.

## Action Items
- [ ] Write a concise pitch: "simulation as hypothesis generator for behavioral interventions."
- [ ] Read and import the papers in [[Zotero Import Queue — User Simulation]].
- [ ] Decide whether the first behavior family is not fact-checking, over-reliance, or confirmatory search.
- [ ] Create a Gricea feature note for simulation harness support.

## Links
- Project: [[MSR User Simulation — Hypothesis Generator]]
- People: [[Ziang Xiao]]
- Organization: [[Microsoft Research]]
- Master note: [[LLM Human Simulation — Master Note]]
- Lens: [[Simulation as hypothesis generator]]

