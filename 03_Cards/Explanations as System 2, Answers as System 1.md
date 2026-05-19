---
tags: [card, idea, HCI, dual-process, cognitive-psychology, explanation, AI-design]
status: seed → developing
discipline: HCI, Cognitive Psychology
source: Self-DM (2026-02-23)
cluster: ["[[CLUSTER — Misinformation & Cognitive Susceptibility]]", "[[CLUSTER — Human-AI Collaboration & Delegation]]"]
---

# Explanations as System 2, Answers as System 1

## One-Line Summary
Empirical study on whether AI explanations engage System 2 (deliberative) thinking while direct answers trigger System 1 (intuitive) processing — and how this shapes user reliance and belief change.

## Motivation
Dual-process theory (Kahneman) distinguishes fast intuitive thinking (System 1) from slow deliberative reasoning (System 2). AI answers, especially in voice, may be consumed as System 1 responses. But explanations may force System 2 engagement. If true, this has major design implications for reducing over-reliance.

## Research Questions
| # | Question |
|---|----------|
| RQ1 | Do AI explanations (vs. direct answers) elicit more deliberative reasoning in users? |
| RQ2 | Does the framing of information as "explanation" vs. "answer" change user compliance and belief change? |
| RQ3 | Does the effect vary by modality (voice vs. text)? |
| RQ4 | Can explanation design mitigate the Generative Echo Chamber effect? |

## Variables
**Independent:** Response type (answer only / answer + explanation / explanation only), Modality
**Dependent:** Reasoning quality (think-aloud coding), belief change, trust, time spent
**Theoretical framework:** Kahneman (2011) Dual Process Theory

## Study Design
- **Type:** Experiment with think-aloud
- **Stimuli:** Contested factual/political topics
- **Conditions:** Direct answer vs. explanation-first vs. explanation-after

## Discipline Tags
`#HCI` `#cognitive-psychology` `#dual-process`

## Connections
- [[Generative Echo Chamber Effect in Voice-Based Conversational Search]] — explanation as intervention
- [[Dark Patterns in AI]] — explanation absence as dark pattern
- [[Partisan Misinformation Consumption through AI Conversations]] — explanation effects on fact-checking
- [[Adaptive Assistance Calibrated to User Knowledge]] — calibrate explanation depth

## Related Work
- Kahneman (2011) *Thinking, Fast and Slow*
- Springer et al. (2019) on XAI user trust
- Lombrozo (2006) on explanatory reasoning
