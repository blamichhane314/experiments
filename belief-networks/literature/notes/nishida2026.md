# Notes: Beyond Retrieval: Structuring Evolving and Inconsistent External Knowledge with Proposition Relations for RAG

Nishida, Noriki; Cheng, Fei; Matsumoto, Yuji (2026). EMNLP 2026. https://aclanthology.org/2026.emnlp-main.294

15 marks in 13 passages, in page order. Page numbers are those of the PDF. Marked words are in bold; the text around them is the sentence before and the sentence after.

**p. 1.** Beyond Retrieval: Structuring Evolving and Inconsistent External Knowledge with **Proposition** Relations for RAG

**p. 1.** For example, Ge et al. (2025) showed that temporally organizing multi-session dialogues as timelines improves memory retrieval and reasoning. Li et al. (2025) decomposed documents into **propositions** (Chen et al., 2024; Liu et al., 2025) and dynamically labeled their truthfulness. However, these methods organize knowledge as collections of facts, without explicitly modeling rich relations between them.

**p. 1.** This distinction is important because temporal validity and misinformation are not properties of isolated propositions alone. In this paper, **we aim to continually organize evolving and inconsistent external knowledge bases through relations between propositions**. Our goal is to examine whether part of the burden of integrating such knowledge can be shifted from inference-time reasoning to pre-retrieval knowledge organization.

**p. 2.** Our goal is to examine whether part of the burden of integrating such knowledge can be shifted from inference-time reasoning to pre-retrieval knowledge organization. Our core hypothesis is that **explicit inter-proposition relations** help LLMs integrate evidence and resolve temporal updates, contradictions, and misinformation. Specifically, we propose Proposition-Structured RAG (ProStructRAG), which represents external knowledge as a set of timestamped propositions and structures it through inter-proposition relations.

> Comment: explicit inter-proposition relationships

**p. 3.** **A proposition is a concise, self-contained mention of a fact, used as the minimal knowledge unit in ProStruct-RAG**. Context-dependent expressions such as pronouns are replaced with their corresponding entities so that each proposition can be interpreted independently.

**p. 4.** **Relation** Definition updates A temporal update relation where the subject partially or fully updates the object. The subject represents a newer state, while the object represents previously valid information that has since been updated.

**p. 4.** The prompt template used for proposition extraction is provided in Appendix A. **Inter-Proposition Relation Extraction** Existing methods often assign factuality labels to propositions independently.

**p. 4.** The prompt templates used for interproposition relation classification and refinement are provided in Appendix A. **Proposition graph construction**. We construct a proposition graph G = (V, E), where each node v ∈ V is a proposition and each directed edge e ∈ E is an inter-proposition relation from a subject to an object proposition.

**p. 4.** **At inference time, given a question, we retrieve relevant knowledge from the proposition graph as a relational structure**. The goal is to retrieve not only question-relevant propositions, but also their relations to other propositions, such as updates, contradictions, and support.

> Comment: use proposition graph at inference time

**p. 5.** These benchmarks require models to answer questions whose correct answers can change with the target time; thus, models must not only retrieve relevant knowledge, but also interpret how it evolves over time. Specifically, we use the following datasets: (1) **CLARKNews** (Li et al., 2025) is a temporal QA benchmark constructed from real web articles. We use only QA pairs whose answer changes at least three times for the same question text, and remove cases with multiple correct answers at the same time point.

**p. 15.** **Table 6: Example of temporally ordered propositions generated for Event E1 (The Blue Luminite Energy Crisis**) in the Asteria dataset. The asterisk indicates that the propositions are fake information.

**p. 17.** The trade-off is therefore between inferencetime flexibility and reusable precomputed structure: ProStruct-RAG incurs offline construction and maintenance costs, but reuses the resulting graph across queries. **Information Sufficiency of Propositions**. **Propositions extracted by LLMs are designed to be concise abstractions of source documents**. **A key question is whether this abstraction retains sufficient information for accurate question answering**. Because a document does not have a uniquely defined ground-truth proposition decomposition, this analysis does not directly measure intrinsic extraction accuracy or completeness.

**p. 17.** When only a single document is added, the added context may not contain enough complementary evidence to offset this additional noise. **With two documents, the model may have access to a broader set of supporting details, which can occasionally compensate for information omitted from the proposition subgraph**. Nevertheless, the gain is small and not systematic.
