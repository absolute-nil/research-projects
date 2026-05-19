---
tags: [card, idea, NLP, multilingual, Wikipedia, evaluation, low-resource]
status: seed
discipline: NLP, Computational Linguistics
source: Self-DM (2025-11-05)
cluster: ["[[CLUSTER — Multilingual Narratives & Information Access]]"]
---

# Wikipedia as Ground Truth Causes Problems in Low-Resource Languages

## One-Line Summary
Critique and research direction on fact-checking and NLP evaluation pipelines that over-rely on Wikipedia — particularly harmful for low-resource language communities where Wikipedia coverage is sparse or biased.

## Motivation
Wikipedia is used as ground truth in: fact-checking datasets, NLP training data, retrieval corpora, and evaluation benchmarks. But Wikipedia's coverage is deeply unequal — low-resource languages have far fewer articles, on different topics, often translated from English rather than reflecting local knowledge. Using it as ground truth systematically disadvantages these communities.

## Research Questions
| # | Question |
|---|----------|
| RQ1 | How does Wikipedia coverage inequality map onto NLP benchmark performance gaps across languages? |
| RQ2 | What alternative ground truth sources can replace Wikipedia for low-resource evaluation? |
| RQ3 | Does Wikipedia's English-language bias produce factual errors in low-resource language contexts? |

## Discipline Tags
`#NLP` `#multilingual` `#low-resource` `#evaluation`

## Connections
- [[NarrativeBench — Cross-Cultural Multilingual Benchmark]] — NarrativeBench must avoid Wikipedia-only ground truth
- [[Topicality vs Multilinguality — Topical Bias Framework]] — Wikipedia gap = topical gap
- [[Is Imperfect Better Than Nothing for Marginalized Communities]] — systemic question about AI equity

## Related Work
- Hovy & Yang (2021) on data statements
- Blasi et al. (2022) on unequal NLP
- Barnett et al. on geographic bias in Wikipedia
