---
tags: [card, idea, HCI, framing, narrative, misinformation, social-science]
status: seed → developing
discipline: HCI, Communication, Social Science
source: Self-DM (2025-06-30)
cluster: ["[[CLUSTER — Misinformation & Cognitive Susceptibility]]", "[[CLUSTER — Multilingual Narratives & Information Access]]"]
---

# Same Facts, Different Narratives

## One-Line Summary
Study on framing diversity: given identical facts about an event, how differently do people (or AI systems) construct the story or narrative frame?

## Motivation
Framing is one of the most powerful forces in political communication — the same facts can support radically different narratives. Understanding the space of possible narratives from a fixed factual base is foundational to understanding AI-mediated information flows and the Generative Echo Chamber.

## Research Questions
| # | Question |
|---|----------|
| RQ1 | Given identical factual premises, how much variance exists in human narrative construction? |
| RQ2 | Do AI systems exhibit systematic framing biases when given the same facts? |
| RQ3 | Does the framing produced by AI influence the narrative users adopt? |
| RQ4 | Can cross-lingual narrative diversity (from [[NarrativeBench — Cross-Cultural Multilingual Benchmark]]) be explained by factual vs. framing differences? |

## Variables
**Independent:** Facts provided (controlled), AI system condition (biased/neutral)
**Dependent:** Narrative frame adopted, polarization change, fact recall
**Unit of analysis:** Paragraph/document narrative; user belief stance

## Study Design
- **Task:** Give participants the same set of facts; ask them to write or rate narratives
- **AI condition:** AI generates narratives from same facts — measure framing diversity
- **Measurement:** Frame analysis, stance classification, linguistic framing features (Entman 1993)

## Discipline Tags
`#social-science` `#communication` `#framing` `#HCI`

## Connections
- [[Partisan Misinformation Consumption through AI Conversations]] — framing as mechanism of bias
- [[NarrativeBench — Cross-Cultural Multilingual Benchmark]] — cross-lingual framing differences
- [[Normative vs Descriptive Question Framing]] — framing at question level
- [[Subtle Bias Prompting for Controversial Topics]] — design of biased framing

## Related Work
- Entman (1993) — Framing: Toward Clarification of a Fractured Paradigm
- Chong & Druckman (2007) — Framing Theory
- Card et al. (2015) — Media Frames Corpus
