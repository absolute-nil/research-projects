---
tags: [card, idea, active-paper, multilingual, NLP, benchmark, geopolitical, narratives]
status: active
discipline: NLP, Computational Social Science
source: Grants/Narrative Bench + Meeting with [[Kenton]]
collaborators: ["[[Kenton]]", "[[Ziang Xiao]]"]
cluster: ["[[CLUSTER — Multilingual Narratives & Information Access]]"]
grant: Snorkel DaaS application
---

# NarrativeBench — Cross-Cultural Multilingual Information Seeking Benchmark

## One-Line Summary
First benchmark for evaluating multilingual LLMs on real-world cross-cultural information seeking, measuring whether models can bridge linguistic filter bubbles in geopolitical conflicts.

## Motivation
In conflicts like Israel-Palestine, India-Pakistan, and Russia-Ukraine, parallel information wars exist — Hebrew vs. Arabic, Hindi vs. Urdu, Ukrainian vs. Russian. Current multilingual LLMs actually *reinforce* linguistic silos (Faux Polyglot: 68% of retrieved docs in query language). No benchmark captures this. **NarrativeBench** fills that gap.

## Research Questions
| # | Question |
|---|----------|
| RQ1 | Can multilingual LLMs identify conflicting narratives across languages? |
| RQ2 | Do models overcome linguistic filter bubbles when queried in one language about cross-lingual topics? |
| RQ3 | Are models robust to confirmation-biased queries? |
| RQ4 | Do models provide consistent quality regardless of query language? |

## Target Capabilities
1. **Information conflict understanding** — reasoning over conflicting narratives
2. **Overcoming echo chambers** — surfacing multiple perspectives
3. **Overcoming linguistic filter bubbles** — cross-lingual source incorporation
4. **Confirmation bias robustness** — diverse views under confirmatory querying
5. **Language alignment** — answer in query language
6. **Cross-lingual consistency** — quality parity across query languages

## Tasks
- Narrative Identification
- Narrative Projection
- Narrative Exclusion
- Missing Narrative Identification

## Variables
**System variable:** LLM (various SOTA models)
**Query variable:** Query language, query framing (confirmatory vs. neutral)
**Primary outcome metric:** Information Parity (equal cognitive access to competing narratives, measured via Narrative-level Precision/Recall and Inclusion Rates)

## Dataset
- 50+ sources, 57 languages
- Organically occurring narrative flows
- Embedding-based classifiers validated against human experts
- Sentence-level narrative provenance annotation
- Geopolitical conflicts: Israel-Palestine, India-Pakistan, Russia-Ukraine, Qatar/UAE, Yemen, Maldives, CAR, DRC, Ethiopia, Korea-Japan, Greenland

## Discipline Tags
`#NLP` `#computational-social-science` `#multilingual` `#benchmark`

## Connections
- [[Topicality vs Multilinguality — Topical Bias Framework]] — framework for separating failure modes
- [[Biases in VLM Alignment on Geopolitical Topics]] — extends to vision-language
- [[Wikipedia as Ground Truth Causes Problems in Low-Resource Languages]] — evaluation pipeline critique
- [[Is Imperfect Better Than Nothing for Marginalized Communities]]
- [[CLUSTER — Misinformation & Cognitive Susceptibility]] — supply-side to demand-side link

## Related Work
- Faux Polyglot paper — 68% same-language retrieval finding
- Liu et al. (2024) ECBD framework
- [[Aligning Large Language Models with Diverse Political Viewpoints]]
- NarrativeBias / Wikipedia bias literature

## People
[[Kenton]], [[Ziang Xiao]]

## Grant Status
- Applied for Snorkel DaaS compute + expert annotation support
- LREC resource track mentioned as target venue
