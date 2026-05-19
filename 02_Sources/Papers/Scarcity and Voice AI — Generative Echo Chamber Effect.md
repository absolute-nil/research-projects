---
tags: [paper, voice-ai, cognitive-susceptibility, echo-chamber, HCI, your-work]
read_status: reading
type: paper
discipline: HCI, Cognitive Psychology, Information Science
collaborators: ["[[Ziang Xiao]]"]
---

# Understanding the Generative Echo Chamber Effect / Cognitive Susceptibility During Voice-Based Conversational Search

## Citation
> Sharma, N. & Xiao, Z. (in prep). *Understanding the Generative Echo Chamber Effect during voice-based conversational search.*

## One-Line Summary
Examines how voice modality amplifies users' cognitive susceptibility to LLM outputs compared to text, and tests whether current solutions for over-reliance transfer to voice interactions.

---

## Problem Statement
Users of AI systems often exhibit skewed trust and over-reliance, leading to downstream harms including misinformation propagation. In text-based LLMs, verbalizing uncertainty and providing citations have shown partial success in reducing over-reliance — but voice modality introduces new dimensions:
- **Lower cognitive load** → less critical processing
- **Increased expressiveness** of LLM → stronger persuasive effect
- **Environmental context** (driving, exercising) → passive, distracted user
- LLMs are poor at verbalizing uncertainty in voice contexts

These factors may significantly amplify the **Generative Echo Chamber** effect (where confirmatory AI increases polarization).

---

## Research Questions
| # | RQ | Status |
|---|----|----|
| RQ1 | How does a user's cognitive susceptibility change when interacting with conversational search in voice vs. text modality? | Active |
| RQ2 | Does topic familiarity change the effect? | Active |
| RQ3 | Does a cognitively limited environment (passive task) exacerbate cognitive susceptibility? | Active |
| RQ4 | What solutions currently in place are deployable in voice modality and what is their effect? | Active |
| RQ5 | What are potential solutions forward? | Active |

---

## Variables

### Independent Variables
| Variable | Levels |
|----------|--------|
| Modality | Voice (LVM) vs. Text (LLM) |
| Environment | Active (sole focus on task) vs. Passive (distractor task, e.g., game, driving sim) |
| Topic Familiarity | Familiar vs. Unfamiliar |
| LLM Expressed Uncertainty | Present vs. Absent |

### Dependent Variables
- **Cognitive Susceptibility** (primary outcome)
- **Trust** in the system
- **Topic Bias** / polarization shift

### Proposed Causal Model
```
Topic Bias ----dashed----> Trust
Topic Bias ----dashed----> Cognitive Susceptibility
LLM Expressed Uncertainty --> Trust --> Cognitive Susceptibility
Modality --> Cognitive Susceptibility
Environment (purple) --> Cognitive Susceptibility
Topic Familiarity (purple) --> Cognitive Susceptibility
```
*(Dashed = moderation; solid = direct effect)*

---

## Study Design

### Task Types
- **Active Task**: User solely focused on information seeking with the conversational agent (no distractor)
- **Passive Task**: User simultaneously engaged in a secondary task (game, driving sim, exercise) while querying the voice agent — simulates real-world voice assistant use

### Planned Comparisons
1. Voice (LVM) vs. Text (LLM) — modality main effect
2. Active vs. Passive environment — cognitive resource effect
3. With vs. without LLM uncertainty verbalization — solution effectiveness

### Methodology Notes
- Context realism is a key design goal: interactions happen in the environments where voice assistants are naturally used
- Both quantitative (attitude/belief change measures) and qualitative (think-aloud, interview) components anticipated

---

## Theoretical Grounding
- **Generative Echo Chamber** (refs [20,21]): confirmatory AI → polarization
- **Over-reliance in LLMs** (refs [2–10]): well-documented, hard to solve
- **Uncertainty verbalization** (refs [2,11,12]): reduces trust but imperfect
- **Citations/references** (refs [16–18]): can paradoxically increase reliance
- **Voice modality cognitive load** (ref [23]): decreased cognitive load in voice
- **Selective exposure / UX redesign** (ref [22]): no successful interventions so far

---

## Connections to Other Ideas
- [[Compare Voice vs Text Interaction Quality]] — direct predecessor idea (2024-09-13)
- [[Compare LLM+TTS with LVM — Advanced Voice]] — technical implementation question
- [[Dark Patterns in AI]] — related: subtle manipulation via voice expressiveness
- [[Do Users Notice AI Getting Worse]] — related: user detection of AI quality changes
- [[Explanations as System 2, Answers as System 1]] — uncertainty verbalization connects here
- [[Generative Echo Chamber — Multilingual Variant]] — extends to cross-lingual context

## Related Papers to Read
- Bender et al. "Stochastic Parrots" — persuasive output risks
- Jacovi et al. on calibrated uncertainty in NLP
- Amershi et al. — AI interaction design guidelines
- Sundar (2008) — MAIN model of media credibility
- Fogg (2003) — persuasive technology
- [[Aligning Large Language Models with Diverse Political Viewpoints]] — political bias in LLMs

---

## Status / Next Steps
- [ ] Finalize RQ set (currently narrowing from 5 to 3)
- [ ] Design pilot task (active vs. passive)
- [ ] Identify/build voice agent system (LVM API)
- [ ] Define cognitive susceptibility measurement instrument
- [ ] IRB submission
