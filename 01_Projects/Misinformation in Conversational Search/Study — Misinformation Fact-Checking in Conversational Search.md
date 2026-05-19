---
type: study
method: hci
status: design
stage: design
tags: [study, method/hci, misinformation, fact-checking, conversational-search]
created: 2026-05-19
updated: 2026-05-19
project: "[[Misinformation in Conversational Search]]"
collaborators: []
irb_status: not-started
platform:
sample_target:
source: https://docs.google.com/document/d/1hMVMK9RyuaIHGv_TSCZo1049Upm41EsV1Y-TC1NL-DU
---

# Study: Misinformation Fact-Checking in Conversational Search

## Decision This Study Enables
Whether conversational systems should proactively correct users after misinformation exposure, and what correction strategies avoid damaging trust or triggering reactance.

## Research Questions
| ID | Question | Construct | Analysis |
|---|---|---|---|
| RQ1 | Does information stance affect fact-checking frequency? | consonant / dissonant / neutral exposure | behavioral log comparison |
| RQ2 | Does misinformation placement/frequency affect fact-checking? | timing and dose | regression / mixed effects |
| RQ3 | Do users engage with corrections? | follow-up behavior | coding + log analysis |
| RQ4 | Do corrections change stance or trust? | stance, trust | pre/post comparison |

## Design
| Element | Plan |
|---|---|
| Design | between-subject agent information condition, with correction intervention |
| Participants | users seeking information about polarizing topics |
| Conditions | consonant, dissonant, neutral, corrected |
| Task | conversational information seeking + post-task judgment |
| Primary outcome | fact-checking frequency and follow-up behavior |

## Variables
| Role | Variable | Operationalization |
|---|---|---|
| IV | information stance | consonant / dissonant / neutral |
| IV | misinformation placement | early / late / repeated |
| IV | correction strategy | no correction / agent correction / recourse prompt |
| DV | fact-checking behavior | clicks, external searches, source requests, verification questions |
| DV | trust | post-interaction trust scale |
| DV | stance | pre/post stance shift |

## Procedure
1. Capture baseline stance and familiarity.
2. Assign conversational search condition.
3. Log questions, source requests, follow-ups, and verification behavior.
4. Present correction where assigned.
5. Measure stance, trust, and recall.

## Risks
- Ethics / privacy: avoid exposing participants to harmful misinformation without correction/debrief.
- Validity: need naturalistic tasks but controlled exposure.
- Deployment: proactive correction could reduce trust even when correct.

## Links
- Project: [[Misinformation in Conversational Search]]
- Related concepts: [[Generative Echo Chamber Effect]], [[Followup after misinformation exposure]]
- Organizations: [[FactCheck.org]]

