---
tags: [card, idea, NLP, information-retrieval, search, diversity, redundancy]
status: seed → developing
discipline: NLP, Information Retrieval, HCI
source: Self-DM (2025-04-14; 2025-04-18)
cluster: ["[[CLUSTER — Information Seeking Behavior & Search]]"]
---

# Retrieval by Information Gain / Redundancy Removal

## One-Line Summary
An information retrieval paradigm that iteratively removes documents with high semantic overlap to maximize novelty and diversity in search results — users browse a page, then the system removes highly similar pages from the results.

## Motivation
Standard search returns ranked results that are often redundant. If a user has read one article, articles that largely repeat the same content add little value. An information-gain-based retrieval system would maximize the marginal information per result shown.

## Two Design Ideas
1. **Google search with GPT variant:** After viewing a page, use LLM to identify and remove semantically similar results from the remaining list
2. **Benchmark-based version:** Multilingual retrieval with information gain as the ranking criterion (from 2025-04-18 note)

## Research Questions
| # | Question |
|---|----------|
| RQ1 | Does information-gain-based retrieval improve user task performance vs. relevance-ranked retrieval? |
| RQ2 | Does diversity in search results reduce confirmation bias? |
| RQ3 | How do we measure "information gain" from a user's perspective? |

## Discipline Tags
`#NLP` `#information-retrieval` `#HCI`

## Connections
- [[Tune Bias Intensity in Retrieval — Mix Neutral Articles]] — diversity via neutral mixing
- [[Limit Search Results to 2-3 Documents]] — scarcity + diversity as complementary
- [[Web Search vs Parametric Knowledge Choice]] — retrieval design affects tool choice
- [[NarrativeBench — Cross-Cultural Multilingual Benchmark]] — cross-lingual information gain metric

## Related Work
- Carbonell & Goldstein (1998) — Maximal Marginal Relevance (MMR)
- Dang & Croft (2010) on diversity in search
