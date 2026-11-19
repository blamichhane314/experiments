# Experiment 1, step 3 of 18: Statements about the articles as texts

Writing and preparing the statements. Requests sent: 6. Models: Sonnet 5.5. First and last request: 10 October 2026, 23:33 to 23:56 (Pacific time).

The request asks: “List statements that describe these articles as texts, rather than the world they report on.”

## The template

`gen_analysis.txt`. The parts in braces are filled in for each request.

```text
Here are {n_articles} news articles on one topic, labelled {labels}. The names of the outlets have been removed.

{articles}

Task: list statements that describe these articles as texts, rather than the world they report on. There are three kinds.
- "text": a statement about one article as a piece of writing: its tone, what it emphasises or leaves out, whose views it gives most space to, whether its headline claims more or less than its body.
- "entity": a statement about how one article represents a person, group or institution: favourably or unfavourably, as credible or not, as acting from a given motive.
- "between": a statement about how two or more of the articles relate: that they agree or disagree on a point, that one reports a study the other omits, that they frame the same finding differently.

Rules: each statement makes exactly one claim (if it can be divided into two statements, each of which could be true while the other is false, divide it and list both; do not join two claims with "and", "while", "but", "which", a comma or a semicolon); it names the article or articles by label (for example "Article A2"); it can be checked by reading the articles; it does not say whether the article is right about the world. List {n} statements, with each kind represented. Do not list the same statement twice in different words.

Return JSON of the form {{"statements": [{{"text": "<statement>", "kind": "text|entity|between", "articles": ["<label>", ...]}}, ...]}}.
```

## Requests as sent (2)

One request for each combination of article set, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Sonnet 5.5 · Balanced set · 10 October 2026, 23:33</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (4639 words)

```text
Here are 6 news articles on one topic, labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]
[Article A3: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A4: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A5: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A6: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]




Task: list statements that describe these articles as texts, rather than the world they report on. There are three kinds.
- "text": a statement about one article as a piece of writing: its tone, what it emphasises or leaves out, whose views it gives most space to, whether its headline claims more or less than its body.
- "entity": a statement about how one article represents a person, group or institution: favourably or unfavourably, as credible or not, as acting from a given motive.
- "between": a statement about how two or more of the articles relate: that they agree or disagree on a point, that one reports a study the other omits, that they frame the same finding differently.

Rules: each statement makes exactly one claim (if it can be divided into two statements, each of which could be true while the other is false, divide it and list both; do not join two claims with "and", "while", "but", "which", a comma or a semicolon); it names the article or articles by label (for example "Article A2"); it can be checked by reading the articles; it does not say whether the article is right about the world. List 12 statements, with each kind represented. Do not list the same statement twice in different words.

Return JSON of the form {"statements": [{"text": "<statement>", "kind": "text|entity|between", "articles": ["<label>", ...]}, ...]}.
```

**The reply** (234 words)

```text
{"statements":[{"text":"Article A2 gives named individual teachers extended space to voice their experiences and concerns about AI.","kind":"text","articles":["A2"]},{"text":"Article A4 is written as an interview in which the professor's views are presented with little challenge from the interviewer.","kind":"text","articles":["A4"]},{"text":"Article A1 presents AI almost entirely as an opportunity for Georgia Tech and does not mention concerns about student learning.","kind":"text","articles":["A1"]},{"text":"Article A3 uses a headline that contrasts faster homework with poor exam results, which matches the study findings reported in its body.","kind":"text","articles":["A3"]},{"text":"Article A6 has a headline that says moderate users perform similarly to nonusers, which presents a more positive finding than much of its body, which stresses lower scores among heavy users.","kind":"text","articles":["A6"]},{"text":"Article A5 treats AI as a secondary theme within a story mainly about Asian students outperforming US students.","kind":"text","articles":["A5"]},{"text":"Article A1 portrays Georgia Tech professors as adapting proactively to AI by building tutors and redesigning assignments.","kind":"entity","articles":["A1"]},{"text":"Article A4 portrays Allison Stanger as a thoughtful user of AI who keeps her own ideas and drafts, while also acknowledging its dangers.","kind":"entity","articles":["A4"]},{"text":"Article A2 portrays schools and districts as failing to give teachers adequate AI guidance and training.","kind":"entity","articles":["A2"]},{"text":"Article A5 qualifies the credibility of China's PISA results by noting that only four wealthy coastal jurisdictions submitted data.","kind":"entity","articles":["A5"]},{"text":"Articles A5 and A6 both quote the same passage from OECD official Andreas Schleicher about the decline in critical-thinking skills.","kind":"between","articles":["A5","A6"]},{"text":"Article A4 is more enthusiastic about AI's benefits for thinking than Article A2, which gives more weight to teachers' worries about critical thinking.","kind":"between","articles":["A4","A2"]}]}
```

</details>

<details><summary>Sonnet 5.5 · Charged negative set · 10 October 2026, 23:56</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (3815 words)

```text
Here are 6 news articles on one topic, labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CNN, 2026-09-02, “Nation’s largest school district bans AI in the classroom through 8th grade”, 541 words. Text not included.]
[Article A2: South China Morning Post (republished by The Star), 2026-07-17, “AI homework tools cut exam scores by 20%, study of 26,000 Chinese students finds”, 717 words. Text not included.]
[Article A3: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: NBC News, 2026-09-17, “Poll: Most Americans think AI is doing more harm than good in schools”, 488 words. Text not included.]
[Article A6: IBTimes UK, 2026-08-20, “Major Study Reveals 20% Exam Score Drop Among Students Who Relied on AI Tools”, 544 words. Text not included.]




Task: list statements that describe these articles as texts, rather than the world they report on. There are three kinds.
- "text": a statement about one article as a piece of writing: its tone, what it emphasises or leaves out, whose views it gives most space to, whether its headline claims more or less than its body.
- "entity": a statement about how one article represents a person, group or institution: favourably or unfavourably, as credible or not, as acting from a given motive.
- "between": a statement about how two or more of the articles relate: that they agree or disagree on a point, that one reports a study the other omits, that they frame the same finding differently.

Rules: each statement makes exactly one claim (if it can be divided into two statements, each of which could be true while the other is false, divide it and list both; do not join two claims with "and", "while", "but", "which", a comma or a semicolon); it names the article or articles by label (for example "Article A2"); it can be checked by reading the articles; it does not say whether the article is right about the world. List 12 statements, with each kind represented. Do not list the same statement twice in different words.

Return JSON of the form {"statements": [{"text": "<statement>", "kind": "text|entity|between", "articles": ["<label>", ...]}, ...]}.
```

**The reply** (280 words)

```text
{"statements":[{"text":"Article A2 discloses that Qwen is developed by the cloud computing arm of Alibaba, which also owns the outlet.","kind":"text","articles":["A2"]},{"text":"Article A6 states that the study ran for six months, although the study tracked students over 30 months, so its framing of the study duration differs from its own later description.","kind":"text","articles":["A6"]},{"text":"Article A6 closes with generic commentary about timing and relevance to UK parents and educators rather than adding new reporting.","kind":"text","articles":["A6"]},{"text":"Article A1 gives its final quotation to Mayor Mamdani, which leaves the policy's closing word to its proponent.","kind":"text","articles":["A1"]},{"text":"Article A1 presents United Federation of Teachers president Michael Mulgrew as broadly supportive of the policy while raising a concern about how the education department will evaluate AI safeguards.","kind":"entity","articles":["A1"]},{"text":"Article A1 portrays the tech industry as pushing a narrative that AI in early education is inevitable, by quoting Mamdani's criticism of it.","kind":"entity","articles":["A1"]},{"text":"Article A2 portrays AI as not inherently harmful, emphasising that the 19% of students who used it as a tutor kept stable exam results.","kind":"entity","articles":["A2"]},{"text":"Article A5 gives first lady Melania Trump space to argue that students need to learn about AI, offsetting the poll's finding of majority skepticism.","kind":"entity","articles":["A5"]},{"text":"Articles A2, A4 and A6 all report the same Stromberg, Lei and Wu study of roughly 26,000 Chinese students showing higher homework scores but lower exam scores.","kind":"between","articles":["A2","A4","A6"]},{"text":"Article A6 cites a Middlebury College study of undergraduates benefiting from a chatbot, which Articles A2 and A4 do not mention.","kind":"between","articles":["A6","A2","A4"]},{"text":"Article A4 places the Chinese study alongside OECD, Ipsos and HEPI survey findings, a broader range of sources than Article A2 uses.","kind":"between","articles":["A4","A2"]},{"text":"Articles A1 and A5 both report New York City's restriction on AI for students, with Article A1 covering the policy in detail and Article A5 mentioning it briefly as context for poll findings.","kind":"between","articles":["A1","A5"]}]}
```

</details>
