---
tags: [card, idea, HCI, methodology, information-seeking, verification, NLP]
status: seed → methodology
discipline: HCI, Information Science, NLP
source: Self-DM (2025-07-30)
cluster: ["[[CLUSTER — Information Seeking Behavior & Search]]"]
---

# Fiction as a Verifiable Testbed for Information Seeking

## One-Line Summary
Use fictional universes with stable canon (Harry Potter, Star Wars, Lord of the Rings) as testbeds for claim verification and information-seeking studies — because the ground truth is fixed and verifiable.

## Motivation
Real-world information-seeking studies have a ground-truth problem: for contested topics, there's no objective truth to evaluate against. Fictional canon universes offer a closed-world assumption where facts are definitively true or false — enabling clean verification studies.

## Research Questions
| # | Question |
|---|----------|
| RQ1 | Can fictional domain tasks (verifying canon claims) serve as valid proxies for real-world information seeking? |
| RQ2 | Do users apply the same cognitive strategies when verifying fictional vs. real-world claims? |
| RQ3 | Do AI systems perform differently on in-canon vs. out-of-canon claims, and can users detect this? |

## Design Notes
- Each claim is its own entity with: (a) canon truth value, (b) source(s), (c) claim complexity
- Can sequence claims into a retrieval chain — train/test a language model on structured claims
- *"Do pilot in verifiable context"* — fictional domain as pilot before moving to real contested topics

## Discipline Tags
`#HCI` `#methodology` `#NLP` `#information-seeking`

## Connections
- [[Conversational Information Foraging]] — foraging strategies generalizable from fiction to real
- [[Web Search vs Parametric Knowledge Choice]] — fictional domain = perfect parametric knowledge test
- [[Do Users Notice AI Getting Worse]] — measure detection in verifiable domain

## Related Work
- Fan et al. (2019) — NarrativeQA and story comprehension
- Clark et al. on closed-world assumption in knowledge bases
