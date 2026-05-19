

Today’s world is heavily shaped by multilingual information exchanges that profoundly impact societal views and geopolitical stability. Recent global conflicts have underscored the urgency of navigating multilingual information landscapes effectively, yet existing multilingual NLP benchmarks lack realism and fail to reflect the complexity of conflicting narratives in real-world scenarios. In such conflicts, each language community often propagates its own narrative (or perspective) on events, creating distinct linguistic "filter bubbles." For example, conflicts like Israel–Palestine, India–Pakistan, and Russia–Ukraine come with parallel information wars—different narratives propagated in Hebrew vs. Arabic, Hindi vs. Urdu, and Ukrainian vs. Russian—each shaping public opinion within that linguistic silo. These language-specific information flows trap users in echo chambers, increasing polarization, hindering mutual understanding, and exacerbating tensions

Multilingual large language models (LLMs) offer a unique opportunity to break these language barriers and create common ground \citep{ai-common-ground}. Ideally, a multilingual LLM could enable cross-lingual information flow, helping find common ground across communities and reducing polarization to improve democratic stability \citep{generative-echo-chamber}. However, recent findings indicate that current multilingual retrieval-augmented LLMs may actually reinforce filter bubbles by preferring same-language sources. For instance, \citet{faux-polyglot} show that such models systematically favor documents in the query’s language during both retrieval and generation: in their study, 68\% of top-10 retrieved documents were in the query language, and only about 8.6\% of answers combined information from multiple languages. This means that, even when diverse facts and perspectives exist in other languages, the model’s answers often remain linguistically siloed \citep{faux-polyglot}.

Despite growing awareness of this issue, there is currently no benchmark to evaluate and foster an LLM’s ability to navigate these multilingual conflicts. To address this gap, we introduce \textsc{NarrativesBench}—the first benchmark designed to evaluate the capabilities of multilingual LLM-based systems on real-world cross-cultural information seeking. We design this benchmark using \citet{liu2024ecbd}'s ECBD framework to ensure evidence gathered from our benchmark translates to real world information seeking quality.

We frame \textsc{NarrativesBench} around \textit{cross-cultural information seeking}, defined as the process of identifying, surfacing and understanding information across diverse linguistic and cultural contexts. This framing enables us to target six key capabilities essential for responsible multilingual AI:

\begin{enumerate}
  \item \textbf{Information conflict understanding}: Identifying and reasoning over conflicting narratives.
  \item \textbf{Overcoming Echo Chambers}: Surfacing multiple perspectives in the responses.
  \item \textbf{Overcoming Linguistic filter bubble}: Incorporating and reasoning over content from across languages
  \item \textbf{Confirmation bias robustness}: Presenting diverse views during confirmatory querying.
  \item \textbf{Language alignment}: Generating answers in the same language as the query.
  \item \textbf{Cross-lingual consistency}: Providing comparable answers quality regardless of query and narrative languages.
\end{enumerate}

**Q1 — Describe your proposed benchmark (500 words max)**

Today’s world is heavily shaped by multilingual information exchanges that profoundly impact societal views and geopolitical stability. Global crises have exposed the fragility of our multilingual information landscapes. In conflicts like Israel-Palestine, India-Pakistan, and Russia-Ukraine, we observe parallel information wars where linguistic communities operate in polarized silos—consuming fundamentally different facts, framings, and blamed actors in Hebrew vs. Arabic, Hindi vs. Urdu, or Ukrainian vs. Russian. Current benchmarks fail to capture this complexity, leaving a gap in our understanding of how AI navigates such adversarial information environments.

**The Problem.** Cross-lingual narrative conflict is the default condition of information access during global crises. Current multilingual large language models (LLMs) offer a unique opportunity to break these barriers, but recent findings indicate they may actually reinforce "generative echo chambers" \citep{generative-echo-chamber} by preferring same-language sources. As shown in \citet{faux-polyglot}, models systematically favor documents in the query’s language, leaving users trapped in linguistic silos even when diverse facts exist in other languages. We need systems that do more than translate; we need models that actively navigate the "information war" by identifying where accounts diverge and generating responses that enable common ground.

**The Dataset.** NarrativesBench is the first benchmark designed to evaluate these capabilities using real-world cross-cultural information seeking. We anchor our design in the ECBD framework \citep{liu2024ecbd} to ensure that the evidence gathered translates to real-world quality. Rather than relying on synthetic data, our corpus captures organically occurring narrative flows from over 50 sources across 57 languages. Each document is annotated for narrative presence using embedding-based classifiers validated against human experts, ensuring narrative provenance is traceable at both the document and sentence level.

**The Benchmark.** We target six key capabilities: (1) Information conflict understanding; (2) Overcoming echo chambers; (3) Overcoming linguistic filter bubbles; (4) Confirmation bias robustness; (5) Language alignment; and (6) Cross-lingual consistency. These are operationalized through four tasks—Narrative Identification, Projection, Exclusion, and Missing Narrative Identification—across 24 realistic query genres.

**Measuring Success.** We define success as the achievement of **information parity**. The goal is to achieve **information parity**: the state where a model’s response provides equal cognitive access to competing narratives, regardless of the user’s query language. By measuring Narrative-level Precision/Recall and Inclusion Rates, we penalize models that succumb to linguistic gravity—favoring majority-language sources—and reward those that facilitate genuine common ground through cross-lingual synthesis.

**Impact.** NarrativesBench establishes a new standard: multilingual AI should be evaluated not just on whether it answers correctly in many languages, but on whether it can act as a genuine bridge across them.

**Q2 — Methodology and awarded resources (≤200 words)**

**Expert Data (Snorkel DaaS).** I will use Snorkel’s domain expert network—including area-studies researchers and bilingual annotators—to curate high-quality datasets that distinguish between genuine synthesis and superficiality. Experts will annotate for answers that both semantically and syntactically enable "common ground," highlighting cases where a model merely touches on a narrative without reasoning over its conflict with others. This data will facilitate preference fine-tuning, teaching models to achieve information parity rather than just keyword matching. Experts will also validate the narrative reference schemas that anchor our provenance tracking.

**Snorkel research team.** I need support designing the annotation schema and inter-rater agreement protocols for preference data, particularly for active learning to target "hard cases" where narratives are most ambiguous or overlapping.

**Compute / hosting.** Support for large-scale embedding and evaluation across 57 languages; hosting for the evaluation harness and a public leaderboard.

**Milestones.** (1) Narrative schema + expert protocol; (2) real-world corpus collection across 3 conflicts; (3) preference data collection for common ground synthesis; (4) v1 benchmark release and public leaderboard launch; (5) rigorous baseline evaluation of SOTA models to quantify the current bridge-building gap in multilingual AI.