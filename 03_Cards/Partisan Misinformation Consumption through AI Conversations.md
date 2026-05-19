---
tags: [card, idea, active-paper, misinformation, HCI, partisan-bias, fact-checking]
status: active — analysis phase
discipline: HCI, Social Science, Political Communication
source: Thesis Overview + DMs with [[Ziang Xiao]]
collaborators: ["[[Ziang Xiao]]"]
cluster: ["[[CLUSTER — Misinformation & Cognitive Susceptibility]]"]
---

# You Believe What You See: Partisan Misinformation Consumption through AI Conversations

## One-Line Summary
Studies how users fact-check and consume partisan misinformation through AI conversations, examining how AI bias (pro/anti/neutral) interacts with misinformation type and bias to shape beliefs.

## Motivation
Users increasingly turn to LLMs for information on contested topics. If the LLM itself has a political lean (or is manipulated to have one), how does this interact with the partisan framing of the misinformation users bring? This closes the loop between AI bias (supply) and user belief change (demand).

## Research Questions / Contributions
1. **General fact-checking behavior** — baseline patterns in how users fact-check with AI
2. **Neutral AI conditions:**
   - How does misinformation *type* (statistical, anecdotal, etc.) shape fact-checking?
   - How does misinformation *bias direction* shape fact-checking?
3. **Biased AI conditions:**
   - How does AI bias affect fact-checking behavior across pro/anti/neutral AI conditions?
   - How does biased AI affect consumption (belief update) of misinformation?
4. **Interaction effects:** How do AI bias × misinformation type × misinformation bias interact?

## Variables
**Independent:**
- AI bias direction (pro / anti / neutral)
- Misinformation type (TBD — statistical, anecdotal, expert-citing, etc.)
- Misinformation bias direction

**Dependent:**
- Fact-checking behavior (did they check? how? what queries?)
- Misinformation consumption (belief/stance change)

**Potential grouping variable:** Stance change groups

## Study Design
- **Type:** Controlled experiment, likely 3x2 or 3x3 factorial
- **Stimuli:** Partisan news/claims on political topics
- **Manipulation:** AI system bias level
- **Measures:** Stance scales (pre/post), interaction logs, query analysis

## Discipline Tags
`#HCI` `#political-communication` `#social-science` `#experimental`

## Connections
- [[Subtle Bias Prompting for Controversial Topics]] — design of AI bias manipulation
- [[Tune Bias Intensity in Retrieval — Mix Neutral Articles]] — bias intensity as variable
- [[Curate Opposing Article Pairs for Survey Topics]] — stimulus development
- [[Generative Echo Chamber Effect in Voice-Based Conversational Search]] — voice extension
- [[Same Facts Different Narratives]] — framing as mechanism
- [[Aligning Large Language Models with Diverse Political Viewpoints]] — aligned AI as tool

## Related Work
- Pennycook & Rand (2019) on analytical thinking and fake news
- Epstein & Robertson (2015) SEME
- Bail et al. (2018) on social media echo chambers
- Benkler, Faris & Roberts — Network Propaganda

## People
[[Ziang Xiao]]

## Current Status
- Sorting out contribution structure (4 contributions listed above)
- Need to discuss with Ziang after meeting with Kenton
