---
type: research-question
status: active
tags: [research-question, user-simulation, red-teaming, evaluation]
created: 2026-05-19
updated: 2026-05-19
problem: "[[User Simulation for Human-AI Intervention Design]]"
project: "[[MSR User Simulation — Hypothesis Generator]]"
lenses: ["[[Simulation as hypothesis generator]]"]
methods: [framework, evaluation]
answer_status: partial
---

# When should simulation optimize for realism vs stress testing?

## Question
When should a simulator approximate likely user behavior, and when should it intentionally represent vulnerable, edge-case, or undesirable behavior?

## Current Best Guess
Realism matters when simulation is used as a proxy for human evaluation. Stress testing matters when the goal is to uncover failure modes or generate intervention hypotheses.

## How To Study It
- Define a matrix of simulation purposes: proxy evaluation, red teaming, hypothesis generation, design exploration.
- For each purpose, define success criteria and validation requirements.

## Links
- [[Lost in Simulation — LLM-Simulated Users are Unreliable Proxies]]
- [[User Simulation for Human-AI Intervention Design]]

