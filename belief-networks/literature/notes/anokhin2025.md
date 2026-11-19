# Notes: AriGraph: Learning Knowledge Graph World Models with Episodic Memory for LLM Agents

Anokhin, Petr; Semenov, Nikita; Sorokin, Artyom; Evseev, Dmitry; Kravchenko, Andrey; Burtsev, Mikhail; Burnaev, Evgeny (2025). IJCAI 2025. https://www.ijcai.org/proceedings/2025/2

3 marks in 3 passages, in page order. Page numbers are those of the PDF. Marked words are in bold; the text around them is the sentence before and the sentence after.

**p. 1.** Current LLM-based agents process past experiences using a full history of observations, summarization, retrieval augmentation. However, **these unstructured memory representations do not facilitate the reasoning and planning essential for complex decision-making**. In our study, we introduce AriGraph, a novel method wherein the agent constructs and updates a memory graph that integrates semantic and episodic memories while exploring the environment.

**p. 2.** For evaluation of proposed methods we set up experiments to study two research questions. **RQ1. Can LLM based agents learn useful structured world model from scratch via interaction with an environment? RQ2. Does structured knowledge representation improve retrieval of relevant facts from memory and enable effective exploration**? We evaluated our agent in complex interactive tasks in Textworld and NetHack environments [Côté et al., 2018; Küttler et al., 2020].

**p. 2.** Although AriGraph was originally designed for an agent interacting with the environment, it also demonstrates competitive performance on multi-hop question answering tasks. **Memory graph structure**. AriGraph world model G = (Vs, Es, Ve, Ee) consists of semantic (Vs, Es) and episodic memory (Ve, Ee) vertices and edges (see Figure 2).
