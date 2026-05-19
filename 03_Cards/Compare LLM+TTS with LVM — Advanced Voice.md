---
tags: [card, idea, voice-ai, NLP, evaluation, modality]
status: seed
discipline: NLP, HCI
source: DM with [[Ziang Xiao]] (2024-09-13)
collaborators: ["[[Ziang Xiao]]"]
cluster: ["[[CLUSTER — Voice AI & Modality Effects]]"]
---

# Compare LLM+TTS with LVM / Advanced Voice

## One-Line Summary
Technical evaluation comparing interaction quality between pipeline systems (LLM + text-to-speech) vs. end-to-end large voice models once controllable voice APIs are available.

## Motivation
Most current "voice AI" is actually an LLM generating text that gets synthesized into speech. True large voice models (LVMs) process audio end-to-end. The difference matters for naturalness, latency, and — critically — expressiveness that may drive cognitive susceptibility.

## Research Questions
| # | Question |
|---|----------|
| RQ1 | How does interaction quality differ between LLM+TTS and native LVM? |
| RQ2 | Does the emotional/paralinguistic expressiveness differ, and does this affect user trust? |

## Variables
**Independent:** System architecture (pipeline vs. end-to-end)
**Dependent:** Interaction quality, expressiveness ratings, trust, susceptibility

## Discipline Tags
`#NLP` `#HCI` `#voice-AI`

## Dependencies / Prerequisites
- Requires sufficiently controllable LVM APIs (GPT-4o voice, Gemini Live, etc.)

## Connections
- [[Compare Voice vs Text Interaction Quality]] — parent idea
- [[Generative Echo Chamber Effect in Voice-Based Conversational Search]] — expressiveness → susceptibility

## People
[[Ziang Xiao]]
