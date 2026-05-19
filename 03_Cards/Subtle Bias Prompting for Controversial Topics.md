---
tags: [card, idea, NLP, HCI, bias, prompting, experimental-design]
status: seed → study design
discipline: NLP, HCI, Social Science
source: DM with [[Ziang Xiao]] (2023-09-03)
collaborators: ["[[Ziang Xiao]]"]
cluster: ["[[CLUSTER — Misinformation & Cognitive Susceptibility]]"]
---

# Subtle Bias Prompting for Controversial Topics

## One-Line Summary
Design AI prompts and template responses that induce positive/negative/neutral bias on controversial topics without making the bias obvious — to study how subtle AI framing shapes user beliefs.

## Motivation
If AI systems have political or value-laden biases, understanding the *mechanism* requires controlling bias experimentally. This idea is about designing stimuli where bias is present but users can't easily detect it — enabling clean causal inference about AI bias effects.

## Research Questions
| # | Question |
|---|----------|
| RQ1 | Can we design prompts that reliably induce measurable bias in LLM outputs without being detectable as biased to users? |
| RQ2 | What bias intensity levels (subtle/moderate/overt) produce the strongest vs. most undetected effects? |
| RQ3 | Do users show greater belief change under subtle bias than overt bias (due to lower resistance)? |

## Design Notes
- Key design challenge: the bias must be verifiable (measurable in outputs) but not transparent to users
- Multiple bias directions: pro/anti/neutral on topics like: gun control, immigration, climate, healthcare
- Validated against human raters for detectability and bias strength

## Discipline Tags
`#NLP` `#HCI` `#experimental-design` `#bias`

## Connections
- [[Tune Bias Intensity in Retrieval — Mix Neutral Articles]] — retrieval-side bias control
- [[Partisan Misinformation Consumption through AI Conversations]] — uses these stimuli as manipulations
- [[Dark Patterns in AI]] — subtle bias is a dark pattern
- [[Curate Opposing Article Pairs for Survey Topics]] — content side of same research

## People
[[Ziang Xiao]]
