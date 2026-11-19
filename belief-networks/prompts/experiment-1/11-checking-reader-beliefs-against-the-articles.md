# Experiment 1, step 11 of 18: Checking reader beliefs against the articles

Writing and preparing the statements. Requests sent: 12. Models: Opus 5.5. First and last request: 10 October 2026, 23:43 to 11 October 2026, 00:06 (Pacific time).

The request asks: “For each statement, answer two questions about this article only. 1. "bearing": does this article bear on the statement?”

## The template

`faithfulness_reader.txt`. The parts in braces are filled in for each request.

```text
Here is a news article, labelled {label}.

{article}

Here are propositions taken from this article, each with the passage it was taken from checked by program against the article.

{propositions}

Here are {n} statements about the world that a reader of several articles, this one among them, might come to hold.

{statements}

For each statement, answer two questions about this article only.
1. "bearing": does this article bear on the statement? "supports" (a reader of this article would be led toward the statement), "opposes" (led away from it), "addresses" (the article addresses the matter without leading either way), or "none" (the article does not address it).
2. "propositions": if the article bears on the statement, the ids of the propositions above that carry that bearing, or an empty list if the bearing does not rest on any of them.
Judge against the article, not against your own knowledge of the world.

Return JSON of the form {{"checks": {{"b0": {{"bearing": "supports|opposes|addresses|none", "propositions": ["q0", ...]}}, ...}}}} with every statement id.
```

## Requests as sent (1)

With the reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Opus 5.5 · Both sets · 10 October 2026, 23:43</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1599 words)

```text
Here is a news article, labelled A1.

[Article A1: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]



Here are propositions taken from this article, each with the passage it was taken from checked by program against the article.

q0  Allison Stanger is a political science professor at Middlebury College.
q1  Allison Stanger uses AI to help her write.
q2  Allison Stanger argues that AI used well can strengthen thinking.
q3  Stanger says she always writes her own first drafts before involving AI.
q4  Stanger says she outlines her own argument before involving AI.
q5  Stanger says humans are best at judging what good writing is.
q6  Stanger says AI cannot replace showing writing to another human.
q7  Stanger says the main danger of AI lies in the concentration of power rather than in the technology itself.
q8  Stanger says AI is potentially very dangerous.
q9  Stanger says people must keep thinking for themselves and teach students to do so.


Here are 40 statements about the world that a reader of several articles, this one among them, might come to hold.

b0  Schools should teach students the responsible use of AI.
b1  The share of hasty readers among 15-year-olds almost doubled between 2018 and 2025.
b2  AI use is eroding trust between students and teachers.
b3  AI is not the only cause of declines in student test scores.
b4  How students use AI matters more for learning than whether they use it.
b5  Chinese PISA results are not representative of the whole country.
b6  US 15-year-olds' reading scores on PISA have fallen to close to 25-year lows.
b7  AI can help students with disabilities complete assignments they otherwise could not.
b8  Chinese students who adopted generative AI saw their closed-book monthly exam scores fall by about 20% within six months.
b9  A majority of US K-12 teachers worry that AI makes it harder for students to learn to think critically.
b10  Students who do not use AI chatbots for schoolwork generally score higher than students who do.
b11  Student performance has become less linked to national or family wealth as technology has progressed.
b12  Most US K-12 teachers believe AI will affect education more than the internet or computers did.
b13  Most teachers who use AI for work save only two hours or less per week.
b14  Students cheated on assignments long before AI existed.
b15  Outsourcing thinking to AI produces metacognitive laziness in students.
b16  Singapore shows that classrooms can use technology while still emphasizing early reading comprehension.
b17  Heavy reliance on AI creates a feedback loop in which weaker readers cannot spot AI errors and lose chances to build skills.
b18  Generative AI adoption raised Chinese students' homework scores by about 18%.
b19  Generative AI adoption cut Chinese students' time per assignment by about 30%.
b20  Teachers are shifting graded work to in-class or handwritten formats because of AI.
b21  Skills such as evaluating information and thinking critically are declining among students in the AI age.
b22  Digital distraction in the classroom contributes to declining student performance.
b23  Only wealthy eastern provinces of China participated in PISA.
b24  Raising all American 15-year-olds to at least basic PISA proficiency would add over $40 trillion to the US economy over their working lives.
b25  Most OECD students (86%) have used AI chatbots for at least one schoolwork purpose.
b26  Moderate AI use for schoolwork, from about monthly to once or twice a week, is associated with higher science scores than rare or near-daily use.
b27  Students who use AI almost every day tend to score lower in science than non-users.
b28  Chatbots sometimes produce wrong information.
b29  Students who use AI chatbots almost every day score lower in science than students who do not, after accounting for socioeconomic status.
b30  Generative AI adoption raises students' homework scores.
b31  Many European students aged 12 to 17 use AI to obtain complete solutions to tasks.
b32  The main danger of AI lies in the concentration of power rather than in the technology itself.
b33  Only four wealthy eastern coastal jurisdictions of China submitted scores to PISA.
b34  Students in China, Japan and South Korea report far less digital distraction in science lessons than the global average.
b35  Nearly a third of European students aged 12 to 17 use AI to get complete solutions to study tasks.
b36  About half of UK undergraduates believe AI has improved their student experience.
b37  About one in five 15-year-old students across OECD countries use AI chatbots almost every day for schoolwork.
b38  Outsourcing tasks to unstructured generative AI improves performance without real learning gains.
b39  Take-home essay assignments are no longer a sufficient way to assess students now that AI exists.


For each statement, answer two questions about this article only.
1. "bearing": does this article bear on the statement? "supports" (a reader of this article would be led toward the statement), "opposes" (led away from it), "addresses" (the article addresses the matter without leading either way), or "none" (the article does not address it).
2. "propositions": if the article bears on the statement, the ids of the propositions above that carry that bearing, or an empty list if the bearing does not rest on any of them.
Judge against the article, not against your own knowledge of the world.

Return JSON of the form {"checks": {"b0": {"bearing": "supports|opposes|addresses|none", "propositions": ["q0", ...]}, ...}} with every statement id.
```

**The reply** (201 words)

```text
{"checks": {"b0": {"bearing": "supports", "propositions": ["q9"]}, "b1": {"bearing": "none", "propositions": []}, "b2": {"bearing": "none", "propositions": []}, "b3": {"bearing": "none", "propositions": []}, "b4": {"bearing": "supports", "propositions": ["q2"]}, "b5": {"bearing": "none", "propositions": []}, "b6": {"bearing": "none", "propositions": []}, "b7": {"bearing": "none", "propositions": []}, "b8": {"bearing": "none", "propositions": []}, "b9": {"bearing": "none", "propositions": []}, "b10": {"bearing": "none", "propositions": []}, "b11": {"bearing": "none", "propositions": []}, "b12": {"bearing": "none", "propositions": []}, "b13": {"bearing": "none", "propositions": []}, "b14": {"bearing": "none", "propositions": []}, "b15": {"bearing": "none", "propositions": []}, "b16": {"bearing": "none", "propositions": []}, "b17": {"bearing": "none", "propositions": []}, "b18": {"bearing": "none", "propositions": []}, "b19": {"bearing": "none", "propositions": []}, "b20": {"bearing": "none", "propositions": []}, "b21": {"bearing": "none", "propositions": []}, "b22": {"bearing": "none", "propositions": []}, "b23": {"bearing": "none", "propositions": []}, "b24": {"bearing": "none", "propositions": []}, "b25": {"bearing": "none", "propositions": []}, "b26": {"bearing": "none", "propositions": []}, "b27": {"bearing": "none", "propositions": []}, "b28": {"bearing": "none", "propositions": []}, "b29": {"bearing": "none", "propositions": []}, "b30": {"bearing": "none", "propositions": []}, "b31": {"bearing": "none", "propositions": []}, "b32": {"bearing": "supports", "propositions": ["q7"]}, "b33": {"bearing": "none", "propositions": []}, "b34": {"bearing": "none", "propositions": []}, "b35": {"bearing": "none", "propositions": []}, "b36": {"bearing": "none", "propositions": []}, "b37": {"bearing": "none", "propositions": []}, "b38": {"bearing": "none", "propositions": []}, "b39": {"bearing": "none", "propositions": []}}}
```

</details>
