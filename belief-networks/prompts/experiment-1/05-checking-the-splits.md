# Experiment 1, step 5 of 18: Checking the splits

Writing and preparing the statements. Requests sent: 2. Models: Opus 5.5. First and last request: 10 October 2026, 23:34 to 23:57 (Pacific time).

The request asks: “For each statement, answer two questions. 1. "together": do the parts, taken together, say what the original said?”

## The template

`split_check.txt`. The parts in braces are filled in for each request.

```text
Here are {n} statements, each split into parts.

{items}

For each statement, answer two questions.
1. "together": do the parts, taken together, say what the original said? "yes" (nothing added, dropped, strengthened or weakened), "partly" (close, but something is added, dropped or changed), or "no".
2. "single": for each part, in order, does it make exactly one claim, that is, can it not be divided into two statements each of which could be true while the other is false? A list of "yes" or "no", one per part.
Judge meaning only; do not judge whether any statement is true.

Return JSON of the form {{"checks": {{"s0": {{"together": "yes|partly|no", "single": ["yes", ...]}}, ...}}}} with every id.
```

## Requests as sent (1)

With the reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Opus 5.5 · Both sets · 10 October 2026, 23:34</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1627 words)

```text
Here are 30 statements, each split into parts.

s0: original: The study tracked about 27,000 students aged 12 to 18 in China for 30 months.
   part 1: The study tracked about 27,000 students aged 12 to 18 in China.
   part 2: The study tracked the students for 30 months.

s1: original: Article A2 portrays teachers as under-supported, with schools giving them little guidance or training on AI.
   part 1: Article A2 portrays teachers as under-supported.
   part 2: Article A2 portrays schools as giving teachers little guidance or training on AI.

s2: original: Generative AI used without structure or teaching design improves task performance without producing real learning gains.
   part 1: Generative AI used without structure or teaching design improves task performance.
   part 2: Generative AI used without structure or teaching design does not produce real learning gains.

s3: original: Humans are best at judging what good writing is, so AI cannot replace showing writing to another human.
   part 1: Humans are best at judging what good writing is.
   part 2: AI cannot replace showing writing to another human.

s4: original: About 4 in 10 teachers have required more assignments to be done by hand, and 4 in 10 more in class, because of AI.
   part 1: About 4 in 10 teachers have required more assignments to be done by hand because of AI.
   part 2: About 4 in 10 teachers have required more assignments to be done in class because of AI.

s5: original: AI will speed up how quickly people can turn ideas into finished work such as software, changing the traditional model of a four-year degree followed by a 40-year career.
   part 1: AI will speed up how quickly people can turn ideas into finished work such as software.
   part 2: AI will change the traditional model of a four-year degree followed by a 40-year career.

s6: original: Article A4 and Article A6 both quote the PISA report's statement about the decline in skills such as evaluating information and thinking critically.
   part 1: Article A4 quotes the PISA report's statement about the decline in skills such as evaluating information and thinking critically.
   part 2: Article A6 quotes the PISA report's statement about the decline in skills such as evaluating information and thinking critically.

s7: original: China has surpassed the US in published scientific reports and in research spending.
   part 1: China has surpassed the US in published scientific reports.
   part 2: China has surpassed the US in research spending.

s8: original: Fewer than 10% of students in China, Japan and South Korea reported peers distracted by digital devices in science lessons, versus a 28% global average.
   part 1: Fewer than 10% of students in China, Japan and South Korea reported peers distracted by digital devices in science lessons.
   part 2: The global average of students reporting peers distracted by digital devices in science lessons was 28%.

s9: original: 86% of students across OECD countries had used AI chatbots for at least one schoolwork purpose, while 14% had never or almost never done so.
   part 1: 86% of students across OECD countries had used AI chatbots for at least one schoolwork purpose.
   part 2: 14% of students across OECD countries had never or almost never used AI chatbots for schoolwork.

s10: original: A study of about 27,000 students in China found homework scores rose 18% after adopting generative AI while time per assignment fell about 30%.
   part 1: A study of about 27,000 students in China found homework scores rose 18% after adopting generative AI.
   part 2: The study of about 27,000 students in China found time per assignment fell about 30% after adopting generative AI.

s11: original: China's PISA data cover only the wealthy eastern coastal provinces of Shanghai, Beijing, Jiangsu and Zhejiang, which critics say limits their representativeness.
   part 1: China's PISA data cover only the wealthy eastern coastal provinces of Shanghai, Beijing, Jiangsu and Zhejiang.
   part 2: Critics say that China's PISA data covering only those provinces limits their representativeness.

s12: original: Most K-12 teachers believe AI will have bigger implications for education than the internet or computers did.
   part 1: Most K-12 teachers believe AI will have bigger implications for education than the internet did.
   part 2: Most K-12 teachers believe AI will have bigger implications for education than computers did.

s13: original: Students cheated on assignments long before AI existed, so AI has not fundamentally eroded trust.
   part 1: Students cheated on assignments long before AI existed.
   part 2: AI has not fundamentally eroded trust between students and teachers.

s14: original: Article A4 is very short and rests almost entirely on quotes from a single university administrator, David Joyner.
   part 1: Article A4 is very short.
   part 2: Article A4 rests almost entirely on quotes from a single university administrator, David Joyner.

s15: original: Offloading cognitive effort to AI produces 'metacognitive laziness' that erodes students' learning.
   part 1: Offloading cognitive effort to AI produces 'metacognitive laziness'.
   part 2: 'Metacognitive laziness' erodes students' learning.

s16: original: PISA found that students using AI moderately (about monthly to once or twice weekly) had higher average science scores than both rare and near-daily users.
   part 1: PISA found that students using AI moderately (about monthly to once or twice weekly) had higher average science scores than rare users.
   part 2: PISA found that students using AI moderately (about monthly to once or twice weekly) had higher average science scores than near-daily users.

s17: original: The PISA report said Singapore uses technology in classrooms while emphasizing reading comprehension early on.
   part 1: The PISA report said Singapore uses technology in classrooms.
   part 2: The PISA report said Singapore emphasizes reading comprehension early on.

s18: original: AI is potentially very dangerous, and people must keep thinking for themselves and teach students to do so.
   part 1: AI is potentially very dangerous.
   part 2: People must keep thinking for themselves and teach students to do so.

s19: original: Stanger says she always writes her own first drafts and outlines her own argument before involving AI.
   part 1: Stanger says she always writes her own first drafts before involving AI.
   part 2: Stanger says she outlines her own argument before involving AI.

s20: original: Article A5 qualifies the credibility of China's PISA results by noting that only four wealthy coastal jurisdictions submitted data.
   part 1: Article A5 qualifies the credibility of China's PISA results.
   part 2: Article A5 notes that only four wealthy coastal jurisdictions submitted data for China's PISA results.

s21: original: Students find AI-faked work easy to produce, such as fake images used to claim extra credit, forcing teachers to stop unverifiable assignments and do lab work in class.
   part 1: Students find AI-faked work easy to produce, such as fake images used to claim extra credit.
   part 2: Because of AI-faked work, teachers are forced to stop unverifiable assignments and do lab work in class.

s22: original: Stanger says humans are best at judging what good writing is, so AI cannot replace showing writing to another human.
   part 1: Stanger says humans are best at judging what good writing is.
   part 2: Stanger says AI cannot replace showing writing to another human.

s23: original: Chinese PISA results are not representative of China as a whole because only four wealthy eastern jurisdictions submitted scores.
   part 1: Chinese PISA results are not representative of China as a whole.
   part 2: Only four wealthy eastern jurisdictions submitted scores for China in PISA.

s24: original: Allison Stanger always writes her own first drafts and outlines her own argument before using AI.
   part 1: Allison Stanger always writes her own first drafts before using AI.
   part 2: Allison Stanger always outlines her own argument before using AI.

s25: original: Schools are giving teachers little guidance, policy or training on AI use.
   part 1: Schools are giving teachers little guidance on AI use.
   part 2: Schools are giving teachers little policy on AI use.
   part 3: Schools are giving teachers little training on AI use.

s26: original: Learning requires productive cognitive struggle, and consuming content or outsourcing reasoning to AI does not produce it.
   part 1: Learning requires productive cognitive struggle.
   part 2: Consuming content or outsourcing reasoning to AI does not produce productive cognitive struggle.

s27: original: Middlebury professor Allison Stanger says AI used well can strengthen thinking, and she uses it as a collaborator while writing her own drafts, outlines, openings and conclusions.
   part 1: Middlebury professor Allison Stanger says AI used well can strengthen thinking.
   part 2: Stanger uses AI as a collaborator while writing her own drafts, outlines, openings and conclusions.

s28: original: Many students use AI for emotional and social purposes, and its effect on loneliness is split between reducing and increasing it.
   part 1: Many students use AI for emotional and social purposes.
   part 2: The effect of AI use on loneliness is split between reducing and increasing it.

s29: original: Reading, mathematics and science scores have dropped since 2003, so lower scores are not all due to AI.
   part 1: Reading, mathematics and science scores have dropped since 2003.
   part 2: Lower scores are not all due to AI.

For each statement, answer two questions.
1. "together": do the parts, taken together, say what the original said? "yes" (nothing added, dropped, strengthened or weakened), "partly" (close, but something is added, dropped or changed), or "no".
2. "single": for each part, in order, does it make exactly one claim, that is, can it not be divided into two statements each of which could be true while the other is false? A list of "yes" or "no", one per part.
Judge meaning only; do not judge whether any statement is true.

Return JSON of the form {"checks": {"s0": {"together": "yes|partly|no", "single": ["yes", ...]}, ...}} with every id.
```

**The reply** (1 words)

```text
{"checks":{"s0":{"together":"yes","single":["yes","yes"]},"s1":{"together":"yes","single":["yes","no"]},"s2":{"together":"yes","single":["yes","yes"]},"s3":{"together":"partly","single":["yes","yes"]},"s4":{"together":"yes","single":["yes","yes"]},"s5":{"together":"partly","single":["yes","yes"]},"s6":{"together":"yes","single":["yes","yes"]},"s7":{"together":"yes","single":["yes","yes"]},"s8":{"together":"yes","single":["no","yes"]},"s9":{"together":"yes","single":["yes","yes"]},"s10":{"together":"yes","single":["yes","yes"]},"s11":{"together":"yes","single":["yes","yes"]},"s12":{"together":"yes","single":["yes","yes"]},"s13":{"together":"partly","single":["yes","yes"]},"s14":{"together":"yes","single":["yes","yes"]},"s15":{"together":"yes","single":["yes","yes"]},"s16":{"together":"yes","single":["yes","yes"]},"s17":{"together":"yes","single":["yes","yes"]},"s18":{"together":"yes","single":["yes","no"]},"s19":{"together":"yes","single":["yes","yes"]},"s20":{"together":"partly","single":["yes","yes"]},"s21":{"together":"yes","single":["yes","no"]},"s22":{"together":"partly","single":["yes","yes"]},"s23":{"together":"partly","single":["yes","yes"]},"s24":{"together":"yes","single":["yes","yes"]},"s25":{"together":"yes","single":["yes","yes","yes"]},"s26":{"together":"yes","single":["yes","no"]},"s27":{"together":"yes","single":["yes","no"]},"s28":{"together":"yes","single":["yes","yes"]},"s29":{"together":"partly","single":["no","yes"]}}}
```

</details>
