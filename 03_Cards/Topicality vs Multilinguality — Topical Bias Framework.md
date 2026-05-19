---
tags: [card, idea, NLP, multilingual, bias, geopolitical, evaluation]
status: seed → developing
discipline: NLP, Computational Social Science
source: Self-DM (2025-11-12)
cluster: ["[[CLUSTER — Multilingual Narratives & Information Access]]"]
collaborators: ["[[Kenton]]"]
---

# Topicality vs Multilinguality — Topical Bias Framework

## One-Line Summary
A framework for disentangling whether a multilingual model fails to retrieve information because of **topical bias** (the topic is underrepresented in training) vs. **multilingual retrieval failure** (language-specific retrieval failure on well-covered topics).

## Motivation
When a multilingual model gives a poor answer on a geopolitical topic, it's unclear whether this is because: (a) the topic is underrepresented across all languages, or (b) the specific language's perspective is missing. This conflation leads to poor diagnostics and wrong interventions.

## Research Questions
| # | Question |
|---|----------|
| RQ1 | Can we design a test to separate topical bias from multilingual retrieval failure? |
| RQ2 | If all languages fail to retrieve an answer, is this evidence of topical bias? |
| RQ3 | How does topical bias distribute across geopolitical conflict topics? |

## Framework Logic
> *"If all these languages could not retrieve that answer then it's topical bias"*
- If model fails in **all** query languages → topical gap (topic not in training)
- If model succeeds in **some** languages but fails in others → multilingual retrieval failure
- This creates a diagnostic matrix for multilingual evaluation

## Variables
**Input:** Topic × language matrix of retrieval success/failure
**Output:** Topical bias score vs. multilingual retrieval bias score

## Discipline Tags
`#NLP` `#multilingual` `#evaluation` `#bias`

## Connections
- [[NarrativeBench — Cross-Cultural Multilingual Benchmark]] — framework needed for NarrativeBench diagnostics
- [[Biases in VLM Alignment on Geopolitical Topics]] — parallel framework for VLMs
- [[Wikipedia as Ground Truth Causes Problems in Low-Resource Languages]] — topicality = coverage = Wikipedia gap
- [[Fine-Grained Labels for Multilingual Models — User-Centered Taxonomy]] — finer labels needed

## Related Work
- Faux Polyglot paper
- Cross-lingual retrieval evaluation literature
- Barnett et al. on geographic bias in Wikipedia
