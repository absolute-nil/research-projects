---
type: reading-list
status: processed
tags: [source, reading-list, user-simulation, llm]
created: 2026-05-19
updated: 2026-05-19
url: https://github.com/Persdre/awesome-llm-human-simulation
projects:
  - "[[MSR User Simulation — Hypothesis Generator]]"
  - "[[Gricea]]"
problems:
  - "[[User Simulation for Human-AI Intervention Design]]"
---

# Awesome LLM-based Human Simulation — Source Map

## What This List Covers
The GitHub list organizes LLM-based human simulation across foundations, behavior simulation, LLM agents, bias and values, applications, evaluation, cognition and psychology, and social simulation.

## Useful Buckets For My Work
| Bucket                               | What it means for this vault                                                                              | Representative notes                                                                                                            |
| ------------------------------------ | --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Reliability / surveys                | Evidence that broad LLM-human simulation is not yet dependable enough as a substitute for humans.         | [[LLM-based Human Simulations Have Not Yet Been Reliable]], [[Lost in Simulation — LLM-Simulated Users are Unreliable Proxies]] |
| Grounded individual agents           | Simulation grounded in interviews, surveys, or self-reports.                                              | [[LLM Agents Grounded in Self-Reports Enable General-Purpose Simulation of Individuals]]                                        |
| Fine-tuned social-science predictors | Train on many human experiment responses to predict distributions under conditions.                       | [[Finetuning LLMs for Human Behavior Prediction in Social Science Experiments]]                                                 |
| Causal critique                      | Simulation treatments can alter unspecified context and create confounding.                               | [[The Challenge of Using LLMs to Simulate Human Behavior — Causal Inference Perspective]]                                       |
| Search / recommendation simulators   | Use LLM agents to generate query, click, recommendation, or shopping behavior.                            | [[BASES — Large-scale Web Search User Simulation]], [[How Reliable is Your Simulator]]                                          |
| Feedback simulation                  | Use model-based human feedback to lower the cost of feedback-method development.                          | [[AlpacaFarm — Simulation Framework for Human Feedback]]                                                                        |
| HCI synthetic personae               | Synthetic personas and data for piloting, design, and speculation, with authenticity and ethics concerns. | [[Challenges and Opportunities of LLM-Based Synthetic Personae and Data in HCI]]                                                |
| Intervention / training              | Use simulated practice partners for social skills and behavioral scaffolding.                             | [[Social Skill Training with Large Language Models]]                                                                            |

## Synthesis
The list is useful because it shows that "simulation" is not one thing. Papers use it for at least five different jobs:
- replacing or approximating human evaluation;
- generating synthetic training/evaluation data;
- modeling population or social dynamics;
- piloting designs before human studies;
- stress-testing edge cases or undesirable behavior.

For the MSR project, the strongest framing is not "make realistic humans." It is: use targeted simulators to generate hypotheses about which system affordances can move users from undesirable information behaviors toward desirable ones, then validate the hypotheses with humans through [[Gricea]].

## Zotero
See [[Zotero Import Queue — User Simulation]].

