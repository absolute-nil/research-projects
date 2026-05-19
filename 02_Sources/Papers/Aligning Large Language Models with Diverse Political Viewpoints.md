---
tags: [paper, political-bias, LLM, alignment, NLP]
type: paper
authors: ["Röttger et al."]
venue: Unknown (likely ACL/EMNLP/NAACL)
year: ~2023
---

# Aligning Large Language Models with Diverse Political Viewpoints

## Citation
> Röttger et al. (2023). *Aligning Large Language Models with Diverse Political Viewpoints.* [Venue TBD]

## Summary
LLMs like ChatGPT exhibit systematic political biases — when queried about political information, they often take normative stances. This paper aligns LLMs with diverse political viewpoints using 100,000 comments from Swiss parliamentary candidates. The aligned models generate more accurate, multi-perspective political viewpoints compared to commercial models. They also propose a procedure for generating balanced summaries of multiple viewpoints.

## Key Contributions
1. Empirically documents political bias in LLMs (ChatGPT)
2. Fine-tuning on Swiss parliamentary candidate comments for political diversity
3. Balanced overview generation procedure for summarizing competing viewpoints

## Relevance to Your Research
- **Direct relevance** to [[Partisan Misinformation Consumption through AI Conversations]] — biased AI conditions
- **Direct relevance** to [[NarrativeBench — Cross-Cultural Multilingual Benchmark]] — political viewpoints across languages
- Motivates the need to study how biased AI outputs influence users (connects to [[Generative Echo Chamber Effect in Voice-Based Conversational Search]])
- Raises question: if models can be aligned to political diversity, can users detect this alignment or are they still susceptible? → connects to [[Do Users Notice AI Getting Worse]] and [[Dark Patterns in AI]]

## Connected Ideas
- [[Generative Echo Chamber Effect in Voice-Based Conversational Search]]
- [[Partisan Misinformation Consumption through AI Conversations]]
- [[Same Facts Different Narratives]]
- [[Normative vs Descriptive Question Framing]]

## Notes
- Swiss political system used as testbed — good external validity question for US/global contexts
- "Balanced overview" procedure is a direct analog to what NarrativeBench tries to evaluate
