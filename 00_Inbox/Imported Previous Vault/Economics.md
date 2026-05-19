---
tags: [thesis, economics, AI-replaceability]
related_idea: "[[Formula for Chain Performance Utility and Replaceability]]"
cluster: "[[CLUSTER — Human-AI Collaboration & Delegation]]"
home: "[[HOME]]"
---

**Questions Economics people are interested in:**  

- **Macro-economic trends**: How does deployment of AI in a field impact the economic activity happening in that field
- **Micro-economic trends**:
    - Can AI replace a human in a particular job?
    - What are the productivity gains of incorporating AI in a job
    - What are the costs of incorporating AI in a job

  
  
**Metrics we have right now:**  

- **NLP**:
    - Linguistic capabilities of models
    - Fundamental reasoning capabilities
    - Multilingual capabilities
    - Summarization capabilities
    - Semantic similarity...
- **HCI**
    - Controlled studies that study how AI influences human reliance, trust, etc.
    - Simulation: Study how AI interacts with other agents and how it can follow normative structures
    - Controlled studies looking at different systems and scaffolds impact on tasks
- **Economics evaluation**:
    - Look at O-NET and evaluate how well AI can do a task given inputs and expected output. **(What rishi is working on)**

  
  
**AI integration:**  

- Can AI assist the human?
- Can AI collaborate with the human?
- **Can AI replace the human? - we focus on this**

  
  
**(constraint) What is the AI we are talking about here?**  

- **Foundational model can do it by itself - we focus on this**
- Foundational model with tool calls
- Orchestration of AI agents (An AI system)

  
  
**(Research direction 1):** Given we have HCI and NLP evaluations what is the gap in predicting actual economic impact?  

- Survey HCI and NLP papers
- Find the gaps that exist that prevent the metrics from having predictive powers for economics variables

  
  
**(Research direction 2):**  

- Still have to find the gaps in evaluation: but here I think there are a few metrics missing and we can focus on building them:
    - **Cost of writing a prompt for successful execution** given task complexity and model performance for that task complexity
    - **Cost of evaluating an AI output** for a given task complexity. It can be a composite of length of answer, number of steps that human is not in the loop, the type of errors that might occur (easy to catch or hard to catch)
    - **Cost of correcting an incorrect AI response:** For that task and given the AI capabilities, how difficult it is to correct the AI or give feedback, is it easier to abandon the task and do it yourself, etc?

  
  
**Open questions:**  

- How do we validate the metrics? Given we are looking for predictive power in downstream economics variables like productivity, etc.
- One way is to look at historical data (like how SAT is evaluated for its predictive power) but we will not have this data since we don't have historical data and the rapid pace AI models keep changing. Maybe we rely on simulation?

Notion of task quality can be very complex

we need to have a good measure for task quality for having these metrics

aren't these all connected? the models output will change based on the quality of the prompt -> estimate of the cost to write that prompt that I give to the LLM

