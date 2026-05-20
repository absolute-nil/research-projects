---
type: paper
status: to-read
tags: [paper, user-simulation, causal-inference, validity]
created: 2026-05-19
updated: 2026-05-19
title: "The Challenge of Using LLMs to Simulate Human Behavior: A Causal Inference Perspective"
authors: "George Gui and Olivier Toubia"
year: 2023
url: https://arxiv.org/abs/2312.15524
projects: ["[[MSR User Simulation — Hypothesis Generator]]"]
problems: ["[[User Simulation for Human-AI Intervention Design]]"]
---

# The Challenge of Using LLMs to Simulate Human Behavior — Causal Inference Perspective

## One-Sentence Takeaway
LLM-simulated experiments can confound the intended treatment with unstated context because the simulated person and environment are constructed from the full prompt.

## Why I Care
This gives a rigorous validity critique for simulation-based intervention testing. If the prompt changes the world, the treatment effect is ambiguous.

## Design Implication
The MSR project should explicitly define the source of variation: the undesirable behavior simulator is not a real person; it is a targeted behavioral model used to generate candidate interventions.

## Links
- [[How should simulations be calibrated against human studies]]
- [[When should simulation optimize for realism vs stress testing]]

