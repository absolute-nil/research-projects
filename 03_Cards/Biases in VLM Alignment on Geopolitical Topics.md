---
tags: [card, idea, NLP, VLM, bias, geopolitical, multimodal]
status: seed
discipline: NLP, Computational Social Science
source: Self-DM (2025-11-10)
collaborators: ["[[Kenton]]"]
cluster: ["[[CLUSTER — Multilingual Narratives & Information Access]]"]
---

# Biases in VLM Alignment on Geopolitical Sensitive Topics

## One-Line Summary
Study how Vision-Language Models (VLMs) exhibit alignment failures and biases when processing geopolitically sensitive topics — images, captions, and cross-modal reasoning about contested events.

## Motivation
LLM biases on text are increasingly documented, but VLMs add a new dimension: the image itself carries cultural and geopolitical framing. A photo of a conflict can be captioned very differently depending on perspective. How do VLMs align with or resist these framings?

## Research Questions
| #   | Question                                                                                              |
| --- | ----------------------------------------------------------------------------------------------------- |
| RQ1 | Do VLMs exhibit systematic biases when captioning or reasoning about images of geopolitical conflict? |
| RQ2 | Do biases vary by language of query?                                                                  |
| RQ3 | Do VLMs apply different "perspectives" to the same image depending on prompt language?                |
| RQ4 | How do VLM alignment decisions interact with training data geography and language?                    |

## Variables
**Input:** Image (from conflict zone) × query language × prompt framing
**Dependent:** Caption content, perspective alignment score, narrative framing

## Study Design
- Collect images from geopolitical conflict events with known narrative contexts (e.g., pro-X vs. pro-Y framings)
- Probe VLMs (GPT-4V, Gemini, LLaVA, etc.) with the same images in different query languages
- Code outputs for narrative alignment using the [[Topicality vs Multilinguality — Topical Bias Framework]]

## Discipline Tags
`#NLP` `#VLM` `#multimodal` `#geopolitical`

## Connections
- [[NarrativeBench — Cross-Cultural Multilingual Benchmark]] — VLM extension of NarrativeBench
- [[Topicality vs Multilinguality — Topical Bias Framework]] — apply diagnostic framework
- [[Aligning Large Language Models with Diverse Political Viewpoints]] — text analog

## People
[[Kenton]]
