---
tags: [card, idea, NLP, RAG, bias, experimental-design, retrieval]
status: seed
discipline: NLP, HCI
source: DM with [[Ziang Xiao]] (2023-09-03)
collaborators: ["[[Ziang Xiao]]"]
cluster: ["[[CLUSTER — Misinformation & Cognitive Susceptibility]]", "[[CLUSTER — Information Seeking Behavior & Search]]"]
---

# Tune Bias Intensity in Retrieval — Mix Neutral Articles

## One-Line Summary
Experimental design idea: adjust bias strength in RAG systems by mixing neutral or opposing-perspective articles into the retrieval corpus alongside biased sources.

## Motivation
Rather than binary (biased/unbiased) retrieval conditions, this approach enables continuous control over bias intensity by manipulating the *ratio* of biased:neutral:opposing documents retrieved. This creates a more ecologically valid and precise experimental design.

## Design Notes
- **Bias intensity dial:** % of biased articles in retrieved set (0%, 25%, 50%, 75%, 100%)
- **Direction:** unidirectional bias vs. mixed bias vs. opposing bias in same set
- Can test whether *any* neutral exposure is enough to reduce bias effects

## Connections
- [[Subtle Bias Prompting for Controversial Topics]] — prompt-level complement
- [[Limit Search Results to 2-3 Documents]] — quantity × bias ratio interaction
- [[Curate Opposing Article Pairs for Survey Topics]] — article curation for this

## People
[[Ziang Xiao]]
