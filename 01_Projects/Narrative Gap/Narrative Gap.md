---
type: project
status: active
stage: writing
tracker_status: ":dart:"
last_reviewed: 2026-05-19
next_milestone: "Link final paper, benchmark repo, and conflict-specific source notes"
tags: [project, method/nlp, benchmark, narratives, multilingual, geopolitical-conflict]
created: 2026-05-19
updated: 2026-05-19
aliases: [NarrativeBench, Narrative Gap]
collaborators: []
venue_target:
deadline:
methods: [nlp, benchmark, multilingual-evaluation]
themes: [narratives, multilinguality, information-access, geopolitical-conflict]
problems:
  - "[[Cross-Cultural Information Access]]"
lenses:
  - "[[Capability Labels and Taxonomies]]"
  - "[[Information Flows]]"
thesis_track: "[[Track II — Conversational Agent Behavior in Complex Contexts]]"
source: https://docs.google.com/document/d/1hMVMK9RyuaIHGv_TSCZo1049Upm41EsV1Y-TC1NL-DU
---

# Narrative Gap

## Pitch
Narrative Gap studies whether AI systems can help people navigate diverse multilingual narratives around conflicts and high-stakes events, especially where information access is fragmented by language, geography, and political context.

## Current Question
How can benchmarks and model evaluations capture whether AI systems represent plural, cross-cultural, multilingual narratives rather than collapsing them into dominant-source summaries?

## Research Questions
| ID | Question | Method | Status |
|---|---|---|---|
| RQ1 | How do models represent different regional narratives for the same conflict or event? | benchmark evaluation | active |
| RQ2 | Which languages and regions are underrepresented or distorted? | multilingual evaluation | active |
| RQ3 | Can models support common ground without erasing disagreement? | qualitative + automatic eval | seed |

## Claims
| Claim | Evidence needed | Linked notes |
|---|---|---|
| Multilingual AI systems can reproduce geopolitical and language-access silos. | Model comparison across conflicts, regions, and languages. | [[NarrativeBench — Cross-Cultural Multilingual Benchmark]] |
| Ground-truth framing is weak for contested narratives. | Examples where Wikipedia or dominant-language sources flatten disagreement. | [[Wikipedia as Ground Truth Causes Problems in Low-Resource Languages]] |
| Users need agency to explore perspectives beyond their local information environment. | User-facing task design and evaluation. | [[Same Facts Different Narratives]] |

## Workstreams
- Benchmark: conflict/topic coverage, languages, regions, capability taxonomy.
- Source material: Nagorno-Karabakh / Artsakh materials and other conflict narratives.
- Paper: [[NEURIPS_NARRATIVE_GAP.pdf]]
- Related project: [[High-Stakes Group Perception of LLM Portrayals]]

## Related Terms
- [[NarrativeBench — Cross-Cultural Multilingual Benchmark]]
- [[Topicality vs Multilinguality — Topical Bias Framework]]
- [[Same Facts Different Narratives]]
- [[Biases in VLM Alignment on Geopolitical Topics]]

## Next Actions
- [ ] Link final paper PDF and any benchmark repo.
- [ ] Convert conflict-specific source material into source notes, not project notes.
- [x] Add related papers from Zotero. ✅ 2026-05-18

## Project Log
- 2026-05-19: Created from Google Doc draft material and existing publication context.
