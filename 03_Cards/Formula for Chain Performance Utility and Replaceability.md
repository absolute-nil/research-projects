---
tags: [card, idea, economics, AI-replaceability, formal-model, HCI]
status: seed → formal model
discipline: Economics, HCI, Operations Research
source: Self-DM (2026-02-28)
cluster: ["[[CLUSTER — Human-AI Collaboration & Delegation]]"]
---

# Formula for Chain Performance, Utility, and Replaceability

## One-Line Summary
A formal model of task-chain performance quantifying AI replaceability as a function of: probability of successful execution, correction cost, and job/task coverage — enabling principled economic evaluation.

## Formal Model (Draft)

Let a task chain $T = \{t_1, t_2, ..., t_n\}$ where each task $t_i$ has:
- $p_i$ = probability of successful AI execution
- $c_i$ = cost of correcting an incorrect AI output for task $t_i$
- $u_i$ = utility of the task output

**Chain Performance:**
$$P_{chain} = \prod_{i=1}^{n} p_i$$

**Expected Replaceability Score:**
$$R = \sum_{i=1}^{n} \left[ p_i \cdot u_i - (1-p_i) \cdot c_i \right] \cdot \text{coverage}(t_i)$$

Where $\text{coverage}(t_i)$ = fraction of job description covered by task $t_i$.

## Key Cost Components (from Economics note)
- **Cost of writing prompt** for successful execution (task complexity × model capability)
- **Cost of evaluating AI output** (answer length, error type, human-in-loop needs)
- **Cost of correcting incorrect response** (can user fix it? or must they redo from scratch?)

## Research Questions
| # | Question |
|---|----------|
| RQ1 | Can this formula predict economic productivity gains from AI adoption? |
| RQ2 | How do we validate the formula against real-world economic outcomes? |
| RQ3 | How do task quality and prompt quality interact in the formula? |

## Discipline Tags
`#economics` `#formal-model` `#HCI` `#AI-evaluation`

## Connections
- [[Economics of AI Replaceability]] — parent note
- [[Compare Google Social Media Conversational Search and Deep Search]] — chain performance across search tasks
- [[People Accept Output from AI They Don't Want To]] — correction cost affects acceptance

## Related Work
- Brynjolfsson et al. on AI and productivity
- Acemoglu & Restrepo on task-based model of automation
- O*NET task descriptions as coverage input
