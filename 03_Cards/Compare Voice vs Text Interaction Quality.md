---
tags: [card, idea, voice-ai, modality, HCI, NLP]
status: seed → developed
discipline: HCI, NLP
source: DM with [[Ziang Xiao]] (2024-09-13)
collaborators: ["[[Ziang Xiao]]"]
cluster: ["[[CLUSTER — Voice AI & Modality Effects]]"]
---

# Compare Voice vs Text Interaction Quality

## One-Line Summary
Systematic comparison of interaction quality across text LLMs, TTS-augmented LLMs, and native large voice models (LVMs) — focusing on output quality, user experience, and behavioral differences.

## Motivation
As voice-capable AI systems become more sophisticated, it's unclear whether the *quality* of interactions (in terms of information quality, user satisfaction, cognitive load) differs meaningfully across modalities. This is a prerequisite for understanding voice-specific harms.

## Research Questions
| # | Question |
|---|----------|
| RQ1 | Does information quality differ between text, TTS+LLM, and LVM interactions? |
| RQ2 | Does interaction quality (fluency, coherence, satisfaction) differ? |
| RQ3 | Do behavioral patterns (query reformulation, follow-up questions, abandonment) differ? |

## Variables
**Independent:** System type (text LLM / LLM+TTS / LVM)
**Dependent:** Information quality, interaction quality, user satisfaction, behavioral metrics

## Study Design
- **Type:** Comparative user study
- **Note:** Advanced voice APIs need to be sufficiently controllable before this is feasible
- **Prerequisite:** Access to LVM APIs with parity in task coverage

## Discipline Tags
`#HCI` `#NLP` `#evaluation`

## Connections
- [[Generative Echo Chamber Effect in Voice-Based Conversational Search]] — builds directly on this
- [[Compare LLM+TTS with LVM — Advanced Voice]] — more specific technical version
- [[Web Search vs Parametric Knowledge Choice]] — task-type effects generalize

## Related Work
- Cowan et al. on voice assistant mental models
- Porcheron et al. (2018) on voice in context
