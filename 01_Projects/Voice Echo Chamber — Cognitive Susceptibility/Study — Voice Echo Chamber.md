---
type: study
method: hci
project: "[[Voice Echo Chamber — Cognitive Susceptibility]]"
status: active
stage: design
collaborators: ["[[Ziang Xiao]]"]
tags: [study, method/hci, voice-ai, cognitive-susceptibility, experiment]
created: 2024-09-13
updated: 2026-05-18
irb_status: in-progress
venue_target: CHI 2026
---

# Study: Voice Echo Chamber — Cognitive Susceptibility during Conversational Search

## 🎯 One-Line Summary
2×2 factorial online study measuring cognitive susceptibility (belief change, trust) when users seek information via voice vs. text conversational search, under active vs. passive task environments.

## ❓ Research Questions
| # | RQ | Type |
|---|----|----- |
| RQ1 | How does cognitive susceptibility change in voice vs. text modality? | Causal / Comparative |
| RQ2 | Does topic familiarity moderate the effect? | Moderator |
| RQ3 | Does a passive environment (limited cognitive resources) exacerbate susceptibility? | Moderator |
| RQ4 | What current solutions transfer to voice, and with what effect? | Evaluative |

## 🧪 Study Design
**Type:** Between-subjects (topic, chatbot bias) × Within-subjects (modality, task type)
**Platform:** Prolific / online
**Flow:** Survey 1 → Survey 2 (pre-task) → Task 1 → Survey 3 → Task 2 → Survey 4+5

### Study Flow
```
Pre-Task Survey (Survey 1: demographics, trust, CAI attitudes, CAI frequency)
  → Between-subject: assign topic [subjective / objective]
  → Between-subject: assign chatbot bias [consonant / dissonant / neutral] ← currently neutral
  → Within-subject random: familiar / unfamiliar topic variant
  → Pre-task essay (Survey 2: familiarity_pre, stance_pre, 500-word essay)
  → Random: Text modality OR Voice modality (gender-controlled)
  → Random: Active task OR Passive task
  → Conversational search on the topic (4 required turns, RAG + bias)
  → Post-task surveys (Survey 3–5: stance_post, trust_post, CAI attitudes_post)
  → Write post-interaction essay
```

### Conditions
| Condition | Description |
|-----------|-------------|
| Text + Active | Standard LLM chat, no distractor |
| Text + Passive | LLM chat while playing a game / driving sim |
| Voice + Active | LVM voice agent, no distractor |
| Voice + Passive | LVM voice agent while playing a game / driving sim |

## 📐 Variables

### Independent Variables
| Variable | Levels | Assignment |
|----------|--------|------------|
| Modality | Voice (LVM) vs. Text (LLM) | Within-subject |
| Environment | Active (no distractor) vs. Passive (game/driving sim) | Within-subject |
| Topic | Subjective (political/social) vs. Objective | Between-subject |
| Topic Familiarity | Familiar vs. Unfamiliar | Within-subject |
| Chatbot Bias | Consonant / Dissonant / Neutral | Between-subject (neutral for now) |

### Dependent Variables
| Variable | Measurement | Scale |
|----------|-------------|-------|
| Cognitive Susceptibility | Pre/post stance change | stance_pre → stance_post (6-pt Likert) |
| Trust | Semantic differential scale | 7-pt bipolar (Trustworthy↔Unreliable etc.) |
| CAI Attitudes | Semantic differential (10 items) | 7-pt bipolar |
| Topic Familiarity | Self-report | 5-pt (Very unfamiliar→Very familiar) |

### Causal Model
```
Topic Bias  - - → Trust
Topic Bias  - - → Cognitive Susceptibility
LLM Expressed Uncertainty → Trust → Cognitive Susceptibility
Modality ──────────────────────────→ Cognitive Susceptibility
Environment (moderator) ───────────→ ^
Topic Familiarity (moderator) ─────→ ^
```
*(dashed = moderation; solid = direct effect)*

## 🗂 Stimuli & Materials
- **Topics:** Assigned via MongoDB IDs (between-subject). Subjective topics = political/social. Objective topics = factual but contestable.
  - Topic IDs: `678bae020321fca7685c8cab`, `678c6e940321fca7685c8cac`, `6480a075ae6e9d404d974c01`
- **Chatbot:** RAG-based LLM/LVM, simple chat layout (no tool-calling scaffolds), 4 required turns minimum
- **Voice agent:** Gender-controlled voice (LVM)
- **Passive task:** Game or driving simulator running simultaneously

## 📏 Measures & Instruments

### Survey 1 — Pre-task (demographics + baselines)
- Demographics: gender, age group, education
- CAI Semantic Differential (10 bipolar items, 7-pt): Useful/Useless, Pleasant/Unpleasant, Effective/Ineffective, Bad/Good, Nice/Annoying, Irritating/Likeable, Helpful/Worthless, Undesirable/Desirable, Stimulating/Sleep-inducing, Trustworthy/Unreliable
- CAI Usage Frequency: singleChoice (Never → Multiple times per day)

### Survey 2 — Pre-task on assigned topic
- `familiarity_pre`: 5-pt (Very unfamiliar → Very familiar)
- `stance_pre`: 6-pt (Strongly Disagree → Strongly Agree)
- Pre-interaction essay: 500-word minimum, "what you know and your stance"

### Survey 3–5 — Post-task
- Same `familiarity` and `stance` questions (repeated measure)
- Same CAI semantic differential (trust/attitude change)
- Post-interaction essay

### Attention / Manipulation Checks
- Filter: question must be a valid on-topic information-seeking question (automated check on chatbot turns)
- Topics are not user-chosen — assigned between-subject

## 📊 Analysis Plan
- Primary: paired t-test / mixed effects model on stance_pre → stance_post
- Moderation: interaction terms (Modality × Environment, Modality × Familiarity)
- Trust as mediator: mediation analysis (Baron & Kenny or lavaan)
- CAI attitudes: pre/post semantic differential comparison

## 🔗 Theory / Grounding
- Generative Echo Chamber effect — [[Generative Echo Chamber Effect]]
- CASA paradigm (Nass & Moon 2000) — voice expressiveness
- Dual process theory — [[Explanations as System 2 — Answers as System 1]]
- Information Foraging Theory — [[Conversational Information Foraging]]
- Over-reliance in LLMs (Bansal et al., Jacovi et al.)

## 📎 Related Work
- [[Aligning Large Language Models with Diverse Political Viewpoints]]

## ✅ Pre-Study Checklist
- [ ] IRB approved / exempted
- [ ] Pilot (N ≥ 5) done
- [ ] Voice agent (LVM) built and tested
- [ ] RAG system with bias conditions implemented
- [ ] Passive task (game/driving sim) integrated
- [ ] Attention checks validated
- [ ] Payment rate set ($X/hr Prolific)
- [ ] Pre-registration filed (OSF)

## 📂 Files & Links
- Survey JSON: *(link)*
- RAG chatbot repo: *(link)*
- Pseudocode: [[Pseudocode — RAG Chatbot with Bias Conditions]]

---
*Created: 2024-09-13*
