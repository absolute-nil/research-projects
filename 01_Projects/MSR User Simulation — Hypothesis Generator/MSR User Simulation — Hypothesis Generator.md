---
type: project
status: active
stage: proposal
tracker_status: ":ziang-xiao:"
health: yellow
priority: P1
last_reviewed: 2026-05-19
next_review: 2026-05-26
next_milestone: Design survey/interview protocol and behavior taxonomy for multi-turn collaboration
next_action: Draft protocol to elicit desirable and undesirable multi-turn collaboration behaviors
blockers:
  - Need first-pass behavior taxonomy from surveys/interviews
  - Need corpus strategy for desirable/undesirable collaboration conversations
  - Need Zotero import for core simulation papers
tags:
  - project
  - user-simulation
  - msr
  - method/hci
  - method/nlp
  - gricea
  - collaboration
created: 2026-05-11
updated: 2026-05-19
aliases:
  - MSR Simulation Project
  - User Simulation Hypothesis Generator
collaborators:
  - "[[Ziang Xiao]]"
organizations:
  - "[[Microsoft Research]]"
venue_target: MSR summer project
deadline:
methods:
  - literature-review
  - simulation
  - hci-study
  - platform
themes:
  - user-simulation
  - hypothesis-generation
  - affordances
  - behavioral-intervention
  - multi-turn-collaboration
problems:
  - "[[User Simulation for Human-AI Intervention Design]]"
  - "[[Mixed-Initiative Collaboration and Agency]]"
  - "[[Research Infrastructure for AI Studies]]"
lenses:
  - "[[Simulation as hypothesis generator]]"
  - "[[Communicative Agency]]"
  - "[[Common Ground and Deliberation]]"
thesis_track: "[[Track II — Conversational Agent Behavior in Complex Contexts]]"
thesis_tracks:
  - "[[Track II — Conversational Agent Behavior in Complex Contexts]]"
  - "[[Track III — Democratized Information Governance]]"
---

# MSR User Simulation — Hypothesis Generator / Reverse red-teaming

## Pitch
One of the objectives of a simulation is to guide the development of affordances and model behavior to achieve better human-AI performance. The way current literature does this is through focusing on diversity and realism. However, as it has been acknowledge throughout the literature: human behavior is complex and non-deterministic. Human behavior is influenced by an array of social, economic and personal factors. This makes current simulation always a catchup game and low in utility to make any informed decisions. I pitch a different path to maximize the utility of simulation to guide affordances and model behavior given the constraints around achieving realistic human simulation.

Human behavior is a spectrum, the two extremes of this spectrum are 1) A human which always takes the cognitive shortcuts, gives complete agency to the model, does not fact-check, over-relies on the model, etc. and 2) A human which desirable behaviors such as always reviewing the code, retaining agency, etc. ***Note: The desirable behavior of humans under human-agent collaboration has not yet been defined and needs to be surveyed***

This framing allows us to frame the objective as: What affordances can shift the behavior of simulated users from undesirable towards desirable behaviors?

This can also enable auditing and red-teaming where we can look at the simulation of the undesireable behavior and investigate model performance.


~~This project asks whether simulation can generate useful hypotheses about multi-turn human-AI collaboration. The case study is to first learn what people consider desirable and undesirable human and Agent behaviors during multi-turn collaboration, then use real or sourced conversations to identify desirable and undesirable information flows, train a classifier over those flows, and use simulation to test which interface or assistant behaviors might move collaboration toward desirable patterns. Promising interventions are validated with human studies in [[Gricea]].~~

## Current Question
Can targeted user simulation help generate intervention hypotheses for improving multi-turn human-AI collaboration, without pretending to replace human participants?

## Tracker
| Status                     | Health | Priority | Last reviewed | Next milestone            |
| -------------------------- | ------ | -------- | ------------- | ------------------------- |
| `:ziang-xiao:` Need review | yellow | P1       | 2026-05-19    | survey/interview protocol |

## Research Questions
| ID  | Question                                                                               | Method                             | Status     |
| --- | -------------------------------------------------------------------------------------- | ---------------------------------- | ---------- |
| RQ1 | [[What are desirable and undesirable behaviors in multi-turn human-AI collaboration]]  | survey + interview                 | unanswered |
| RQ2 | [[Can classifiers identify desirable and undesirable collaboration information flows]] | conversation labeling + classifier | unanswered |
| RQ3 | [[Can undesirable-behavior simulators generate intervention hypotheses]]               | simulation + human validation      | unanswered |
| RQ4 | [[How should simulations be calibrated against human studies]]                         | Gricea study                       | partial    |
| RQ5 | [[What are the boundaries of LLM-based human simulation]]                              | framework                          | partial    |

## Collaboration Definitions
These definitions are inherited from [[Mixed-Initiative Collaboration and LLM Agency]], [[Communicative Agency]], and [[delegation vs collaboration]].

- Single-turn completion: the model fills in or produces an artifact in response to one request. The user owns the goal, context, and evaluation criteria.
- Single-turn delegation: the user gives the model a bounded task to perform once. The model may execute well or poorly, but it does not jointly manage goals over time.
- Multi-turn delegation: the user and model go back and forth to complete a user-owned task. The model may ask clarifying questions, but initiative, goals, and success criteria remain primarily user-directed.
- Multi-turn collaboration: the human and model jointly manage goals, context, constraints, initiative, repair, and evolving plans. A collaborator can ask clarifying questions, surface missing assumptions, reject false premises, push back, preserve common ground, and optimize for the human's eventual decision or artifact quality rather than immediate satisfaction.

## Current Simulation Literature Motivation
The current LLM-human-simulation literature tends to optimize for several utilities: reducing the cost of human evaluation, scaling synthetic behavior traces, predicting human responses, simulating individuals or populations, and generating feedback or interaction data. [[AlpacaFarm — Simulation Framework for Human Feedback]] uses simulation to speed iteration on feedback-learning methods. [[BASES — Large-scale Web Search User Simulation]] uses LLM agents to scale web-search behavior simulation. [[LLM Agents Grounded in Self-Reports Enable General-Purpose Simulation of Individuals]] pushes toward more realistic individual agents grounded in self-reports. [[Finetuning LLMs for Human Behavior Prediction in Social Science Experiments]] optimizes for predicting human responses in social-science settings. At the same time, [[Lost in Simulation — LLM-Simulated Users are Unreliable Proxies]] and [[LLM-based Human Simulations Have Not Yet Been Reliable]] warn that LLM-simulated users are not reliable general proxies for real humans, while [[The Challenge of Using LLMs to Simulate Human Behavior — Causal Inference Perspective]] highlights causal-validity problems when simulated context changes with the prompt.

## Why That Does Not Optimize For My Utility
My utility is not generic realism, broad population prediction, or replacing human studies. I want simulation to help decide which collaborative affordances are worth testing with humans. Optimizing for believability or average proxy accuracy can miss the question I actually care about: which concrete assistant behaviors, interface designs, or conversational scaffolds move a user from an undesirable collaboration pattern to a desirable one? If simulation is used as final evidence, the validity burden is too high and often unclear. If simulation is used as a hypothesis generator, the burden becomes more tractable: it only needs to help prioritize candidate interventions that will later be tested with real users.

## Proposed Case Study
Study desirable and undesirable behaviors in multi-turn collaboration.

1. Survey and interview people about collaboration with AI:
   - what counts as a useful collaborator;
   - what counts as a harmful, shallow, or misleading collaborator;
   - when users want the model to take initiative;
   - when users want pushback, clarification, repair, or refusal;
   - what behaviors make users over-delegate, disengage, or accept poor reasoning.
2. Build a behavior taxonomy:
   - desirable flows: goal alignment, clarification, repair, assumption surfacing, uncertainty handling, evidence grounding, alternative exploration, decision trace, calibrated initiative;
   - undesirable flows: premature compliance, sycophancy, goal drift, hidden assumptions, overconfident synthesis, hallucinated common ground, passive user acceptance, missing repair, shallow agreement.
3. Source or collect multi-turn conversations:
   - public conversation datasets where allowed;
   - Gricea-collected collaboration tasks;
   - staged tasks with consenting participants;
   - synthetic examples only as bootstrapping data, clearly separated from human data.
4. Label information flows:
   - turns where goals are negotiated;
   - turns where assumptions are surfaced or hidden;
   - turns where the model takes initiative;
   - turns where the user accepts, questions, corrects, or delegates;
   - turns where collaboration improves or degrades.
5. Train a classifier:
   - multi-label classifier for desirable/undesirable collaboration information flows;
   - use it to find conversation segments, build simulator behaviors, and evaluate interventions.
6. Run simulation:
   - instantiate undesirable collaboration patterns;
   - test model/interface affordances that should shift behavior;
   - rank interventions as hypotheses.
7. Validate in [[Gricea]]:
   - run human studies on the strongest simulated interventions;
   - compare simulator predictions to human behavior;
   - update the simulator boundary and classifier.

## Claims
| Claim                                                                                        | Evidence needed                                                        | Linked notes                                                                                           |
| -------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Multi-turn collaboration is behaviorally distinct from completion and delegation.            | Survey/interview definitions, coding rubric, conversation examples.    | [[What are desirable and undesirable behaviors in multi-turn human-AI collaboration]]                  |
| Desirable and undesirable collaboration can be operationalized as information-flow patterns. | Human labels over multi-turn conversations and classifier performance. | [[Can classifiers identify desirable and undesirable collaboration information flows]]                 |
| Simulation is useful if it generates intervention hypotheses that survive human validation.  | Simulator-to-human transfer study in [[Gricea]].                       | [[Simulation as hypothesis generator]], [[How should simulations be calibrated against human studies]] |

**Meeting Notes**:
*Observed behaviors* -> what are current simulations doing -> how are they replicating this behavior -> prompting based approach to 

- What are the known user behaviors? 
- Log analysis -> out of these known phenomenon what are observable (wild chat or swe chat)
- Chat vs Agentic formats
- **What are the behaviors that stakeholders want from human-agent collaboration?** What are good patterns that we want to observe. 
- Targeted simulation -> How do these agentic environments reacting to these known phenomena
  
## Workstreams
- Literature synthesis: [[LLM Human Simulation — Master Note]]
- Meeting evidence: [[Meeting — MSR Simulation Direction with Ziang]]
- Gricea integration: [[Feature — Simulation Harness for Behavioral Hypotheses]]
- Zotero queue: [[Zotero Import Queue — User Simulation]]
- Collaboration taxonomy: [[Multi-turn Collaboration Behavior Taxonomy]]

## Open Questions
- [ ] Which collaboration context should be first: writing, research planning, coding, information seeking, or policy/design decision-making?
- [ ] Should the first classifier operate at turn, segment, or whole-conversation level?
- [ ] What public conversation datasets can be used ethically and legally?
- [ ] What minimum human-label quality is needed before simulator training?

## Next Actions
- [ ] Draft survey/interview protocol for desirable and undesirable multi-turn collaboration behaviors.
- [ ] Draft the annotation schema for collaboration information flows.
- [ ] Identify candidate conversation datasets and Gricea task designs.
- [ ] Import unchecked papers in [[Zotero Import Queue — User Simulation]].

## Project Log
- 2026-05-19: Created from Ziang discussion and literature scan of [[Awesome LLM-based Human Simulation — Source Map]].
- 2026-05-19: Consolidated standalone pitch into this canonical project note and shifted case study to multi-turn collaboration behavior.

