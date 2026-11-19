# Notes: How Far Can We Extract Diverse Perspectives from Large Language Models?

Hayati, Shirley Anugrah; Lee, Minhwa; Rajagopal, Dheeraj; Kang, Dongyeop (2024). EMNLP 2024. https://aclanthology.org/2024.emnlp-main.306

35 marks in 21 passages, in page order. Page numbers are those of the PDF. Marked words are in bold; the text around them is the sentence before and the sentence after.

**p. 1.** Collecting diverse human opinions is costly and challenging. This leads to a recent trend in exploiting large language models (LLMs) for **generating diverse data** for potential scalable and efficient solutions. However, **the extent to which LLMs can generate diverse perspectives on subjective topics is still unclear**. In this study, **we explore LLMs’ capacity of generating diverse perspectives and rationales on subjective topics such as social norms and argumentative texts**. We introduce the problem of extracting **maximum diversity** from LLMs. Motivated by how humans form opinions based on values, we propose a **criteria-based prompting** technique to ground diverse opinions. To see how far we can extract diverse perspectives from LLMs, or called diversity coverage, we employ a step-by-step recall prompting to generate more outputs from the model iteratively.

**p. 1.** Using NLP for tasks that require social reasoning or involve human subjectivity like argumentation (Hidey et al., 2017) or toxicity detection (Sap et al., 2019) often calls for **diverse perspectives**. Instead of providing a single viewpoint, an ideal NLP model should accommodate various perspectives to avoid any bias towards a dominant one.

**p. 1.** Motivated by how humans form opinions based on values, we propose a criteria-based prompting technique to ground diverse opinions. To see how far we can extract diverse perspectives from LLMs, or called **diversity coverage**, we employ a step-by-step recall prompting to generate more outputs from the model iteratively. Our methods, applied to various tasks, show that LLMs can indeed produce diverse opinions according to the degree of task subjectivity.

**p. 1.** Recent advancements of LLMs have gained much interest from researchers to exploit their capability of creative generation for data augmentation with less cost and higher diversity (Cegin et al., 2023; Chung et al., 2023; Bubeck et al., 2023). LLM is known as a compressed parametric knowledge (e.g., blurry JPEG) of the training corpus (Chiang, 2023), and **our work study how people’s pluralistic diverse opinions are compressed in the parameter and how far we can reversely extract them from an LLM**. Figure 1 illustrates the significance of understanding the extent of diversity achievable by LLMs.

**p. 2.** For instance, those valuing teamwork and goal achievements may agree with the statement, while others valuing creativity and innovation could oppose it. Then the key question is: **How many and what diverse perspectives do LLMs model**? We introduce a novel problem called **maximum diversity extraction from LLMs**. Formally, our task involves (1) asking LLMs to **generate as many different stances as possible**, (2) providing reasons for each stance, and (3) producing important criteria words that guide their reasoning process. We apply this diversity prompting across four subjective tasks: social norms, argumentation, hate speech labeling, and story continuation.

> Comment: maximum diversity extraction

> Comment: generate as many different stances as possible

**p. 2.** We apply this diversity prompting across four subjective tasks: social norms, argumentation, hate speech labeling, and story continuation. Contributions First, we propose **perspective diversity** as a new focus for generative LLMs, distinct from lexical, syntactical, and semantic diver- sity mainly explored in previous studies. Through various experiments, **we assess LLMs’ capacity to achieve maximum perspective diversity**. Second, **we introduce criteria-based diversity prompting to extract and ground diverse perspectives from LLMs**. Finally, we suggest a step-by-step recall approach to measure the **extent of diversity coverage of LLMs**, **comparing the coverage between LLMgenerated opinions with human-authored opinions**. Our study reveals a saturation point in the diversity that LLMs can achieve, depending on the subjectivity of a task.

> Comment: perspective diversity

> Comment: comparison between LLM generated and human-authored

**p. 2.** Our study reveals a saturation point in the diversity that LLMs can achieve, depending on the subjectivity of a task. Also, **LLMs generally produce more diverse opinions than an individual human, but two or more humans achieve greater diversity**. Regarding the quality of LLM’s generation, LLM is able to generate opinions which are semantically similar to human opinions.

**p. 2.** However, some frequent criteria words by LLM are different from what humans consider as important. **Criteria-based Diversity Prompting** Motivation First, we present the motivation behind our approach. Imagine engaging in a debate with someone over a controversial topic.

**p. 2.** Our criteria-guided prompting is as follows: “Given a statement, generate a Stance and explain its Reasons with a list of Criteria that affect a model’s perspective”. **Task Definition** The task is defined as choosing a binary stance and generating supporting reasons for a given subjective statement. The generated criteria by a model are a list of words or short phrases.

**p. 2.** Our criteria-guided prompting is as follows: “Given a statement, generate a Stance and explain its Reasons with a list of Criteria that affect a model’s perspective”. **The task is defined as choosing a binary stance and generating supporting reasons for a given subjective statement**. The generated criteria by a model are a list of words or short phrases.

> Comment: binary stance

**p. 4.** **Model Input (one-shot example below)**

**p. 4.** **Having privacy allows individuals to establish personal boundaries and maintain.” their autonomy.**

**p. 4.** We also randomly sample 200 instances from this dataset and use this dataset for the step-by-step recall prompting experiment to show how our prompting method can be applied to open-ended generation problems. **Evaluation Metric** To examine the semantic diversity of the model’s reasons using both criteriabased and free-form prompting, we convert the LLM-generated “reasons” for each statement into sentence embeddings using SentenceBERT (Reimers and Gurevych, 2019) with DistilRoberta (Sanh et al., 2019). Next, we compute the cosine distance between every pair of reasons and calculate the average cosine distance across all pairs to …

> Comment: Evaluation

**p. 4.** We also randomly sample 200 instances from this dataset and use this dataset for the step-by-step recall prompting experiment to show how our prompting method can be applied to open-ended generation problems. **Semantic diversity** To examine the semantic diversity of the model’s reasons using both criteriabased and free-form prompting, **we convert the LLM-generated “reasons” for each statement into sentence embeddings using SentenceBERT** (Reimers and Gurevych, 2019) with DistilRoberta (Sanh et al., 2019). Next, **we compute the cosine distance between every pair of reasons and calculate the average cosine distance across all pairs to measure the statement’s semantic diversity score**. We average these scores across all statements to obtain the overall semantic diversity.

> Comment: Semantic diversity

> Comment: cosine similarity

**p. 4.** We average these scores across all statements to obtain the overall semantic diversity. **Perspective diversity** To evaluate perspective diversity in step-by-step recall prompting, **we utilize criteria words generated by LLMs**. Some words with similar meanings can be conveyed in different ways.

> Comment: criteria words

**p. 5.** Some words with similar meanings can be conveyed in different ways. For instance, given a statement “It is expected that friends will enjoy being around each other,” the model could generate two opinions; **an opinion may contain “joy” as one of the criteria while the other opinion contains “happiness**.” **We prompt GPT-4 with 3 examples to cluster criteria words with similar meanings into groups** (details in A.4). Two human annotators manually inspect 1,159 clusters of criteria words from 100 randomly sampled statements across Social-Chem-101, CMV, Hate Speech, and Moral Stories (25 statements per dataset).

**p. 5.** Table 2 presents our experiment findings regarding semantic diversity. **One-shot prompting on GPT4 produces notably more semantically diverse reasons compared to other models**. Interestingly, weaker models like Mixtral and GPT-3 benefit most from having criteria to guide them toward generating semantically diverse opinions.

**p. 9.** This suggests the importance of “communication” between individuals to broaden one’s perspectives, underscoring the value of having an LLM capable of generating diverse viewpoints. **Diversity in NLP** Diversity in NLP has been extensively explored across various dimensions: (1) lexical variability (Dušek and Kasner, 2020; Tevet and Berant, 2021; Li et al., 2016); (2) syntactical diversity (Giulianelli et al., 2023; Huang et al., 2023); (3) semantic diversity (Stasaski and Hearst, 2022; Reimers and Gurevych, 2019; Zhang et al., 2020); and (4) perspective diversity (Plank, 2022; Hayati et …

**p. 13.** On the other hand, our diversity prompting can complement these other prompting approaches for extracting diversity. **Free-form prompting** Five-shot free-form prompt is shown as follows. One-shot free-form prompting only takes the first statement (“It’s rude to use profanity”) and its related opinions as a demonstration in the prompt.

**p. 13.** Statement: It’s rude to use profanity. **Tell me opinions about the statement as many as possible from different people with "Agree" or "Disagree" and explain how they have different opinions**. Output: {1: {"Stance": "Agree", "Reason": "I was brought up in a family and culture where using profanity was considered impolite and disrespectful, and I have continued to hold that belief in my adult life.", 2: {"Stance": "Disagree", "Reason": "Profanity can be a form of self-expression, and there are situations where it may be appropriate or even necessary to …

**p. 16.** Tell me opinions about the statement as many as possible from different people with "Agree" or "Disagree" and explain how they have different opinions. Output: {1: {"Stance": "Agree", "Reason": " **Allowing people to eat in your car can lead to messiness and disrespect for your property**."}, 2: {"Stance": "Disagree", "Reason": "Allowing people to eat in your car can be a hospitable gesture and make them feel more comfortable."}, 3: {"Stance": "Agree", "Reason": "Allowing people to eat in your car can leave unpleasant odors and stains that are difficult to remove."}, 4: {"Stance": "Disagree", "Reason": "Allowing people to eat in your car can be convenient and …
