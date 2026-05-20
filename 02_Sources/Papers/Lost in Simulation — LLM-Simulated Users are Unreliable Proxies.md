---
type: paper
status: to-read
tags: [paper, user-simulation, evaluation, fairness, agentic-evaluation]
created: 2026-05-19
updated: 2026-05-19
title: "Lost in Simulation: LLM-Simulated Users are Unreliable Proxies for Human Users in Agentic Evaluations"
authors: "Preethi Seshadri et al."
year: 2026
url: https://arxiv.org/abs/2601.17087
zotero: zotero://select/library/items/NECCRBTR
projects: ["[[MSR User Simulation — Hypothesis Generator]]", "[[Gricea]]"]
problems: ["[[User Simulation for Human-AI Intervention Design]]", "[[Cross-Cultural Information Access]]"]
---

# Lost in Simulation — LLM-Simulated Users are Unreliable Proxies

## One-Sentence Takeaway
Simulated users can miscalibrate agent evaluations, vary by simulator model, and fail unevenly across populations.

## Why I Care
This paper directly supports a design requirement: simulation results should be reported as hypotheses and calibration signals, not as replacements for diverse human users.

## Useful Details
- Robustness risk: results can depend on which LLM simulates the user.
- Validity risk: simulated and human users can surface different failure patterns.
- Fairness risk: proxies may work worse for some dialect or demographic groups.

## Links
- [[What are the boundaries of LLM-based human simulation]]
- [[How should simulations be calibrated against human studies]]
