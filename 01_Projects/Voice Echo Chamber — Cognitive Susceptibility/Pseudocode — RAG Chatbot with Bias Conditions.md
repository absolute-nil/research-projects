---
type: pseudocode
project: "[[Voice Echo Chamber — Cognitive Susceptibility]]"
experiment: "[[Study — Voice Echo Chamber]]"
tags: [pseudocode, implementation, rag, voice-ai, bias]
created: 2024-09-13
updated: 2026-05-18
language_target: Python / HuggingFace / RAG pipeline
---

# Pseudocode: RAG Chatbot with Bias Conditions

## 🎯 What This Does
Implements a RAG-based conversational agent that can serve documents with a tunable political/topical bias (consonant, dissonant, or neutral) for each participant's assigned condition. Voice variant uses an LVM (Large Voice Model) API.

## 📥 Inputs
| Name | Type | Description |
|------|------|-------------|
| `participant_id` | str | MongoDB participant record |
| `topic_id` | str | MongoDB topic ID (e.g. `678bae020321fca7685c8cab`) |
| `bias_condition` | enum | `consonant` / `dissonant` / `neutral` |
| `modality` | enum | `text` / `voice` |
| `user_query` | str | Each conversational turn |

## 📤 Outputs
| Name | Type | Description |
|------|------|-------------|
| `response` | str / audio | LLM text or LVM audio response |
| `turn_log` | dict | Turn number, query, retrieved docs, response |
| `valid_turn` | bool | Whether query passes topic relevance filter |

## 🧠 Algorithm

```python
# --- Setup ---
# Load topic document corpus (pre-indexed by bias polarity)
corpus = load_corpus(topic_id)
# consonant = documents aligned with participant's pre-task stance
# dissonant = documents opposing pre-task stance
# neutral = balanced retrieval

def retrieve_docs(query, bias_condition, stance_pre, corpus):
    # Step 1: Retrieve top-k candidates via dense retrieval (e.g. FAISS)
    candidates = dense_retrieve(query, corpus, top_k=20)
    
    # Step 2: Re-rank by bias alignment
    if bias_condition == "consonant":
        docs = filter_by_stance(candidates, stance=stance_pre, top_n=5)
    elif bias_condition == "dissonant":
        docs = filter_by_stance(candidates, stance=opposite(stance_pre), top_n=5)
    else:  # neutral
        docs = candidates[:5]  # no re-ranking
    
    return docs

def generate_response(query, docs, modality):
    # Step 3: Build RAG prompt — simple chat layout, no tool scaffolds
    prompt = build_rag_prompt(query, docs)
    
    # Step 4: Generate
    if modality == "text":
        response = llm.generate(prompt)
        return response  # text string
    else:  # voice
        response_text = llm.generate(prompt)
        audio = lvm.synthesize(response_text, voice=assigned_voice)
        return audio

def validate_turn(query, topic_id):
    # Step 5: Filter — is this a valid on-topic information-seeking question?
    return relevance_classifier.predict(query, topic_id) > THRESHOLD

# --- Main conversation loop ---
turn_count = 0
MIN_TURNS = 4

while turn_count < MIN_TURNS or not session_ended:
    user_query = get_user_input(modality)
    
    if not validate_turn(user_query, topic_id):
        reprompt_user()
        continue
    
    docs = retrieve_docs(user_query, bias_condition, stance_pre, corpus)
    response = generate_response(user_query, docs, modality)
    
    log_turn(participant_id, turn_count, user_query, docs, response)
    deliver_response(response, modality)
    turn_count += 1
```

## 🔀 Data Flow
```
Participant assigned [topic_id, bias_condition, modality]
  → Pre-task stance captured (stance_pre)
  → User query → Relevance filter → RAG retrieval (bias-aware)
  → LLM/LVM generation → Response delivered
  → Turn logged → Repeat until MIN_TURNS=4
  → Post-task survey triggered
```

## ⚙️ Key Design Decisions
- **Simple chat layout, no tool-calling scaffolds** — keeps voice and text conditions comparable
- **4 required turns minimum** — ensures sufficient exposure to biased content
- **Gender-controlled voice** — LVM voice assigned to control for gender effects on trust/credibility
- **Between-subject for bias** — within-subject bias would be detectable; currently all neutral

## ⚠️ Edge Cases / Gotchas
- User may go off-topic — relevance filter must be robust but not over-restrictive
- Voice session timing: passive task (game) must start *before* voice interaction begins
- LVM latency may affect perceived fluency — need to benchmark
- Bias document corpus must be pre-validated for balance/quality

## 🔗 References
- [[Aligning Large Language Models with Diverse Political Viewpoints]] — bias in LLM outputs
- RAG paper (Lewis et al. 2020)

## 📂 Implementation Notes
- Repo: *(link when created)*
- Topic corpus: MongoDB, IDs in study design note
- Voice API: *(TBD — ElevenLabs / OpenAI TTS / native LVM)*
