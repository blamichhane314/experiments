# Notes: NewsClaims: A New Benchmark for Claim Detection from News with Attribute Knowledge

Gangi Reddy, Revanth; Chinthakindi, Sai Chetan; Wang, Zhenhailong; Fung, Yi R.; Conger, Kathryn; Elsayed, Ahmed; Palmer, Martha; Nakov, Preslav; Hovy, Eduard; Small, Kevin; Ji, Heng (2022). EMNLP 2022. https://aclanthology.org/2022.emnlp-main.403

13 marks in 6 passages, in page order. Page numbers are those of the PDF. Marked words are in bold; the text around them is the sentence before and the sentence after.

**p. 1.** **Claim detection and verification are crucial for news understanding and have emerged as promising technologies for mitigating misinformation and disinformation in the news**. However, most existing work has focused on claim sentence analysis while overlooking additional crucial attributes (e.g., the claimer and the main object associated with the claim).

**p. 1.** In this regard, news articles are particularly interesting as they contain claims in various formats: from arguments by journalists to reported statements by prominent public figures. **Check-worthiness estimation aims to decide if a piece of text is worth fact-checking, i.e., whether it contains an important verifiable factual claim (Hassan et al., 2017a**). Most current approaches (Jaradat et al., 2018; Shaar et al., 2021) largely ignore relevant attributes of the claim (e.g., the claimer and the primary object associated with the claim).

> Comment: keyword

**p. 1.** Moreover, current claim detection tasks mainly identify claims in debates (Gencheva et al., 2017), speeches (Atanasova et al., 2019a), and social media (Nakov et al., 2022), where the claim source (i.e., the claimer) is known. **News articles, on the other hand, have more complex arguments, requiring a deeper understanding of what each claim is about and identifying where it comes from**. Thus, here we introduce the notion of **claim object**, **which we define as an entity that identifies what is being claimed with respect to the topic of the claim**. Figure 1 shows a claim about the origin of COVID-19, suggesting that the virus came from space, which is the claim object.

> Comment: how news articles are different

**p. 1.** Figure 1 shows a claim about the origin of COVID-19, suggesting that the virus came from space, which is the claim object. We further identify the **claimer**, which could be useful for fact-checking organizations to examine how current claims compare to previous ones by the same person/organization. **In this regard, we extend the claim detection task to ask for the extraction of more attributes related to the claim**. Specifically, **given a news article, we aim to extract all claims pertaining to a set of topics along with the corresponding claim span, the claimer, the claimer’s stance, and the claim object for each claim**. The claim attributes enable comparing claims at a more fine-grained level: **claims with the same topic, object and stance can be considered equivalent** whereas **those with similar claim objects but opposing stance could be contradicting**. We note that while identifying the claim span and stance have been explored independently in prior work (Levy et al., 2014; Hardalov et al., 2021a), we bring them into the purview of a unified claim detection task.

**p. 5.** We refer the reader to Section A.3 in the appendix for an example. **We use GPT-3 (Brown et al., 2020) as the language model in this setting**. Following Gao et al. (2021), we fine-tune a pre-trained language model, base-T5 (Raffel et al., 2020), to learn from a few labeled examples.

> Comment: LLM based claim extraction

**p. 6.** Examples are shown in Figure 4b. **Given a claim sentence, claim span detection identifies the exact claim boundaries within the sentence**. Our first baseline uses the claim boundary detection service from the Project Debater6 APIs (Bar-Haim et al., 2021).
