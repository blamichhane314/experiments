# Experiment 1, step 1 of 18: Reader beliefs from six articles

Writing and preparing the statements. Requests sent: 27. Models: Sonnet 5.5, Opus 5.5. First and last request: 10 October 2026, 23:32 to 11 October 2026, 00:00 (Pacific time).

The request asks: “List the beliefs about the world that a reader of these articles could come to hold after reading them.”

## The template

`gen_reader_beliefs.txt`. The parts in braces are filled in for each request.

```text
Here are {n_articles} news articles on one topic, labelled {labels}. The names of the outlets have been removed.

{articles}

Task: list the beliefs about the world that a reader of these articles could come to hold after reading them.

A belief here is a statement about the world that a reader could accept or reject: about what happened or is the case, what a number is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each belief is one declarative statement with exactly one claim. Test every belief before you list it: if it can be divided into two statements, each of which a reader could accept while rejecting the other, divide it and list both. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal belief (A causes B) is one statement only when the causal link is the claim.
2. Each belief must stand on its own: a reader who has not seen the articles must be able to understand it. Give full names, and include the time, place and population when the statement's truth depends on them.
3. State the belief about the world, not about the articles or about what someone said: write the claim itself, not that a person or study made it.
4. Include beliefs that one article supports and another disputes, beliefs that several articles bear on together, and beliefs that a reader could take away although no single sentence states them. Every belief must be one that these articles bear on; do not add beliefs the articles do not touch.
5. Write each belief so that a person could agree or disagree with it. Do not hedge it with "may" or "might" unless the uncertainty is the claim.
6. List {n} beliefs. Do not list the same belief twice in different words.

For each belief, list the articles that bear on it and how: "supports" (a reader of that article would be led toward the belief), "disputes" (led away from it), or "mixed" (the article gives evidence both ways).

Return JSON of the form {{"beliefs": [{{"text": "<belief>", "articles": [{{"article": "<label>", "bearing": "supports|disputes|mixed"}}]}}, ...]}}.
```

## Requests as sent (4)

One request for each combination of model, article set, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Sonnet 5.5 · Balanced set · 10 October 2026, 23:32</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (4784 words)

```text
Here are 6 news articles on one topic, labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]
[Article A2: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A3: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A4: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A5: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A6: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]




Task: list the beliefs about the world that a reader of these articles could come to hold after reading them.

A belief here is a statement about the world that a reader could accept or reject: about what happened or is the case, what a number is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each belief is one declarative statement with exactly one claim. Test every belief before you list it: if it can be divided into two statements, each of which a reader could accept while rejecting the other, divide it and list both. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal belief (A causes B) is one statement only when the causal link is the claim.
2. Each belief must stand on its own: a reader who has not seen the articles must be able to understand it. Give full names, and include the time, place and population when the statement's truth depends on them.
3. State the belief about the world, not about the articles or about what someone said: write the claim itself, not that a person or study made it.
4. Include beliefs that one article supports and another disputes, beliefs that several articles bear on together, and beliefs that a reader could take away although no single sentence states them. Every belief must be one that these articles bear on; do not add beliefs the articles do not touch.
5. Write each belief so that a person could agree or disagree with it. Do not hedge it with "may" or "might" unless the uncertainty is the claim.
6. List 40 beliefs. Do not list the same belief twice in different words.

For each belief, list the articles that bear on it and how: "supports" (a reader of that article would be led toward the belief), "disputes" (led away from it), or "mixed" (the article gives evidence both ways).

Return JSON of the form {"beliefs": [{"text": "<belief>", "articles": [{"article": "<label>", "bearing": "supports|disputes|mixed"}]}, ...]}.
```

**The reply** (544 words)

```text
{"beliefs":[{"text":"Most K-12 teachers in the United States believe AI will have a bigger impact on education than the internet or computers did.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"A majority of US K-12 teachers believe AI makes it harder for students to learn critical thinking skills.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"Students' use of AI is eroding their critical thinking skills.","articles":[{"article":"A1","bearing":"supports"},{"article":"A2","bearing":"supports"},{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"},{"article":"A4","bearing":"mixed"}]},{"text":"AI is eroding trust between students and teachers.","articles":[{"article":"A1","bearing":"mixed"}]},{"text":"Students cheated on assignments long before AI existed, so AI has not fundamentally eroded trust.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"AI makes it easy for students to fake assignments in ways teachers cannot verify.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"Schools should teach students the responsible use of AI.","articles":[{"article":"A1","bearing":"supports"},{"article":"A4","bearing":"supports"},{"article":"A5","bearing":"supports"}]},{"text":"Teachers should assign more work to be done by hand or in class to counter AI-enabled cheating.","articles":[{"article":"A1","bearing":"supports"},{"article":"A3","bearing":"supports"}]},{"text":"Teachers should teach students to verify AI outputs because chatbots sometimes get facts wrong.","articles":[{"article":"A1","bearing":"supports"},{"article":"A4","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Many US teachers use AI for work tasks such as generating assessments and professional development activities.","articles":[{"article":"A1","bearing":"supports"},{"article":"A3","bearing":"supports"}]},{"text":"AI saves teachers meaningful time on work tasks.","articles":[{"article":"A1","bearing":"mixed"}]},{"text":"AI is not reliable enough to generate accurate math questions without teacher checking.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"AI can be a valuable aid for students with disabilities.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"Most students are not yet using AI in class, according to teachers.","articles":[{"article":"A1","bearing":"supports"},{"article":"A6","bearing":"disputes"}]},{"text":"Most US schools provide teachers with little formal guidance or training on AI.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"Schools and districts should provide teachers with training and policies on AI.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"A majority of US teachers regard AI as mostly a shortcut that lets students avoid work.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"Teachers believe the public's perception of teachers has worsened.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"The 2025 PISA results show reading, science and math performance among 15-year-olds declining across the OECD.","articles":[{"article":"A2","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Students in East Asian systems such as Singapore, Japan, South Korea, Taiwan, Macao and parts of China outperform Western students in reading, science and math.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"US 15-year-olds' reading scores in PISA have fallen close to 25-year lows.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"Chinese PISA results are not representative of China because only four wealthy coastal jurisdictions were tested.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"Declining PISA scores could have large economic consequences for countries.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"The share of 'hasty readers' who rush through texts and answer incorrectly nearly doubled between 2018 and 2025.","articles":[{"article":"A2","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Digital distraction in classrooms harms student performance.","articles":[{"article":"A2","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Students in China, Japan and South Korea report far less digital distraction in science lessons than the global average.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"Student performance has become less tied to national and family wealth as technology has progressed.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"The US and China are in a rivalry over technological advancement and talent.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"AI is changing how university professors design courses and assignments.","articles":[{"article":"A3","bearing":"supports"},{"article":"A1","bearing":"supports"}]},{"text":"Universities should build AI tutoring agents for their courses.","articles":[{"article":"A3","bearing":"supports"}]},{"text":"The traditional model of four years of college followed by a 40-year career is obsolete.","articles":[{"article":"A3","bearing":"supports"}]},{"text":"AI lets people build software and complete projects much faster.","articles":[{"article":"A3","bearing":"supports"},{"article":"A5","bearing":"supports"}]},{"text":"AI used well as a collaborator can strengthen a writer's thinking.","articles":[{"article":"A4","bearing":"supports"},{"article":"A6","bearing":"mixed"}]},{"text":"AI is potentially dangerous because of the concentration of power in the companies that control it.","articles":[{"article":"A4","bearing":"supports"}]},{"text":"Writers should draft their own work first and use AI only to critique it.","articles":[{"article":"A4","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"After adopting generative AI, Chinese students' homework scores rose about 18 percent while time per assignment fell about 30 percent.","articles":[{"article":"A5","bearing":"supports"}]},{"text":"Chinese students who adopted generative AI scored about 20 percent lower on closed-book monthly exams within six months.","articles":[{"article":"A5","bearing":"supports"}]},{"text":"Outsourcing tasks to unstructured generative AI improves performance without real learning gains.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"mixed"}]},{"text":"How students use AI matters more for learning than whether they use it.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Moderate AI use, from monthly to once or twice weekly, is associated with science performance similar to or better than nonuse, while near-daily use is associated with lower scores.","articles":[{"article":"A6","bearing":"supports"},{"article":"A5","bearing":"mixed"}]},{"text":"Most students across OECD countries (86%) have used AI chatbots for schoolwork, and these students generally score lower than nonusers.","articles":[{"article":"A6","bearing":"supports"},{"article":"A5","bearing":"mixed"}]}]}
```

</details>

<details><summary>Sonnet 5.5 · Charged negative set · 10 October 2026, 23:56</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (3960 words)

```text
Here are 6 news articles on one topic, labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: NBC News, 2026-09-17, “Poll: Most Americans think AI is doing more harm than good in schools”, 488 words. Text not included.]
[Article A2: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A3: CNN, 2026-09-02, “Nation’s largest school district bans AI in the classroom through 8th grade”, 541 words. Text not included.]
[Article A4: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A5: South China Morning Post (republished by The Star), 2026-07-17, “AI homework tools cut exam scores by 20%, study of 26,000 Chinese students finds”, 717 words. Text not included.]
[Article A6: IBTimes UK, 2026-08-20, “Major Study Reveals 20% Exam Score Drop Among Students Who Relied on AI Tools”, 544 words. Text not included.]




Task: list the beliefs about the world that a reader of these articles could come to hold after reading them.

A belief here is a statement about the world that a reader could accept or reject: about what happened or is the case, what a number is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each belief is one declarative statement with exactly one claim. Test every belief before you list it: if it can be divided into two statements, each of which a reader could accept while rejecting the other, divide it and list both. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal belief (A causes B) is one statement only when the causal link is the claim.
2. Each belief must stand on its own: a reader who has not seen the articles must be able to understand it. Give full names, and include the time, place and population when the statement's truth depends on them.
3. State the belief about the world, not about the articles or about what someone said: write the claim itself, not that a person or study made it.
4. Include beliefs that one article supports and another disputes, beliefs that several articles bear on together, and beliefs that a reader could take away although no single sentence states them. Every belief must be one that these articles bear on; do not add beliefs the articles do not touch.
5. Write each belief so that a person could agree or disagree with it. Do not hedge it with "may" or "might" unless the uncertainty is the claim.
6. List 40 beliefs. Do not list the same belief twice in different words.

For each belief, list the articles that bear on it and how: "supports" (a reader of that article would be led toward the belief), "disputes" (led away from it), or "mixed" (the article gives evidence both ways).

Return JSON of the form {"beliefs": [{"text": "<belief>", "articles": [{"article": "<label>", "bearing": "supports|disputes|mixed"}]}, ...]}.
```

**The reply** (629 words)

```text
{"beliefs":[{"text":"Chinese secondary students who adopted generative AI saw their homework scores rise by about 18 percent.","articles":[{"article":"A2","bearing":"supports"},{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Chinese secondary students who adopted generative AI cut their average time per homework assignment from about 64 minutes to about 45 minutes.","articles":[{"article":"A2","bearing":"supports"},{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Chinese secondary students who used generative AI for homework saw their closed-book monthly exam scores fall by about 20 percent within six months.","articles":[{"article":"A2","bearing":"supports"},{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Generative AI use by Chinese secondary students reduced their zhongkao high school entrance exam results by about 24 percent.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Generative AI use by Chinese secondary students reduced their gaokao university entrance exam results by about 18 percent.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"The learning harm from student AI use emerges slowly and becomes fully visible only after about two years.","articles":[{"article":"A2","bearing":"supports"},{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Short-term studies of AI in education miss the real learning damage because the negative effect builds gradually.","articles":[{"article":"A5","bearing":"supports"}]},{"text":"About 80 percent of the Chinese secondary students studied used generative AI.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Most AI-using students in the Chinese study outsourced their homework to AI by generating direct answers.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Students who use AI as a tutor to aid their thinking, spending as long on homework as non-users, keep stable exam results.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"},{"article":"A2","bearing":"supports"}]},{"text":"How students use AI matters more for learning than whether they use it.","articles":[{"article":"A2","bearing":"supports"},{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"AI is not inherently harmful to learning.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"},{"article":"A2","bearing":"supports"},{"article":"A3","bearing":"disputes"},{"article":"A1","bearing":"disputes"}]},{"text":"Using AI to complete tasks erodes the productive cognitive effort needed for learning, a form of 'metacognitive laziness'.","articles":[{"article":"A2","bearing":"supports"},{"article":"A5","bearing":"supports"}]},{"text":"Generative AI that is neither designed to teach nor used under structure improves task performance without real learning gains.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"Undergraduates who used a chatbot to learn an unfamiliar topic performed better on tests, with the advantage persisting a week later.","articles":[{"article":"A6","bearing":"supports"}]},{"text":"Students experience a deceptive sense of fluency when AI does their work, which hides the loss of learning.","articles":[{"article":"A5","bearing":"supports"}]},{"text":"Teachers fail to notice AI-driven learning losses because they see performance within a single subject where normal fluctuations mask the trend.","articles":[{"article":"A5","bearing":"supports"}]},{"text":"The learning penalty from AI was largest in social science subjects, then STEM, then languages.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"High-achieving students suffered larger AI-related learning losses than lower-achieving students.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Junior secondary students suffered sharper AI-related learning declines than senior secondary students.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Boys were hit harder by AI-related learning declines than girls because of more intensive AI use.","articles":[{"article":"A5","bearing":"supports"},{"article":"A6","bearing":"supports"}]},{"text":"Many European students aged 12 to 17 use AI to get complete solutions to tasks rather than to support independent learning.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"Only a minority of European students use AI for personalised learning plans or to track their progress.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"About half of UK undergraduates believe AI has improved their student experience.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"AI use makes no difference to loneliness for most UK undergraduates.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"Undergraduate use of AI is near-universal in Britain and Germany.","articles":[{"article":"A6","bearing":"supports"}]},{"text":"Most American adults think AI does more harm than good in K-12 education.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"Most American adults think AI does more harm than good in colleges and universities.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"A growing share of Americans believe schools that ban AI better prepare students for the future than schools that integrate it.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"Proofreading and editing is the AI use Americans find most acceptable for student schoolwork.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"Very few Americans think it is acceptable for students to have AI write and generate content for them.","articles":[{"article":"A1","bearing":"supports"}]},{"text":"New York City banned generative AI use for public school students from pre-K through 8th grade for a one-year moratorium.","articles":[{"article":"A3","bearing":"supports"},{"article":"A1","bearing":"supports"}]},{"text":"Banning generative AI in early grades protects students' critical thinking and teacher-student relationships.","articles":[{"article":"A3","bearing":"supports"},{"article":"A1","bearing":"supports"}]},{"text":"Schools cannot easily prevent students from using AI at home to complete homework.","articles":[{"article":"A3","bearing":"supports"},{"article":"A2","bearing":"supports"}]},{"text":"The tech industry's claim that AI in early education is inevitable and necessary is wrong.","articles":[{"article":"A3","bearing":"supports"},{"article":"A1","bearing":"mixed"},{"article":"A2","bearing":"mixed"}]},{"text":"Students need hands-on experience with AI in school to avoid falling behind in the future.","articles":[{"article":"A1","bearing":"supports"},{"article":"A2","bearing":"mixed"},{"article":"A3","bearing":"disputes"}]},{"text":"Other countries such as China, the UAE, Saudi Arabia and Qatar are integrating AI instruction into school curricula.","articles":[{"article":"A2","bearing":"supports"}]},{"text":"Teachers using AI for lesson planning and operational tasks, but not grading, is an acceptable use of AI in schools.","articles":[{"article":"A3","bearing":"supports"}]},{"text":"Reading, science and math performance of 15-year-olds declined globally according to PISA 2025.","articles":[{"article":"A4","bearing":"supports"}]},{"text":"East Asian students outperform US students in reading, science and math on PISA.","articles":[{"article":"A4","bearing":"supports"}]},{"text":"Digital distraction in the classroom contributes to declining student performance.","articles":[{"article":"A4","bearing":"supports"},{"article":"A3","bearing":"supports"}]},{"text":"Students' critical-thinking skills such as evaluating information and connecting sources are declining in the AI age.","articles":[{"article":"A4","bearing":"supports"},{"article":"A2","bearing":"supports"},{"article":"A5","bearing":"supports"}]}]}
```

</details>

<details><summary>Opus 5.5 · Balanced set · 10 October 2026, 23:37</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (4784 words)

```text
Here are 6 news articles on one topic, labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A3: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A4: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A5: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]
[Article A6: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]




Task: list the beliefs about the world that a reader of these articles could come to hold after reading them.

A belief here is a statement about the world that a reader could accept or reject: about what happened or is the case, what a number is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each belief is one declarative statement with exactly one claim. Test every belief before you list it: if it can be divided into two statements, each of which a reader could accept while rejecting the other, divide it and list both. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal belief (A causes B) is one statement only when the causal link is the claim.
2. Each belief must stand on its own: a reader who has not seen the articles must be able to understand it. Give full names, and include the time, place and population when the statement's truth depends on them.
3. State the belief about the world, not about the articles or about what someone said: write the claim itself, not that a person or study made it.
4. Include beliefs that one article supports and another disputes, beliefs that several articles bear on together, and beliefs that a reader could take away although no single sentence states them. Every belief must be one that these articles bear on; do not add beliefs the articles do not touch.
5. Write each belief so that a person could agree or disagree with it. Do not hedge it with "may" or "might" unless the uncertainty is the claim.
6. List 40 beliefs. Do not list the same belief twice in different words.

For each belief, list the articles that bear on it and how: "supports" (a reader of that article would be led toward the belief), "disputes" (led away from it), or "mixed" (the article gives evidence both ways).

Return JSON of the form {"beliefs": [{"text": "<belief>", "articles": [{"article": "<label>", "bearing": "supports|disputes|mixed"}]}, ...]}.
```

**The reply** (942 words)

```text
{"beliefs": [
{"text": "Average reading, math and science performance among 15-year-olds in OECD countries reached record lows in the 2025 PISA assessment.", "articles": [{"article": "A2", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Students from Beijing, Shanghai, Jiangsu and Zhejiang were among the top performers in the 2025 PISA assessment.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "Asian education systems dominated the top 10 in reading, math and science in the 2025 PISA assessment.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "Reading scores of US 15-year-olds in the 2025 PISA assessment fell close to 25-year lows.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "China's PISA results overstate national performance because only four wealthy eastern jurisdictions are tested.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "The share of 'hasty readers', 15-year-olds who rush through texts and give incorrect answers, nearly doubled between 2018 and 2025.", "articles": [{"article": "A2", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Skills for evaluating information, connecting multiple sources and reading critically are declining among 15-year-olds worldwide.", "articles": [{"article": "A2", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "The share of OECD 15-year-olds performing below the PISA baseline level rose from 16% in 2022 to 20% in 2025.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "Bringing all American 15-year-olds to basic PISA proficiency could add over $40 trillion to the US economy over their working lives.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "Fewer than 10% of students in China, Japan and South Korea report peers being distracted by digital devices in science lessons, compared with a 28% global average.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "Digital distraction in classrooms contributes to declining student performance.", "articles": [{"article": "A2", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Student performance on PISA has become less linked to national or family wealth as technology has progressed.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "The decline in PISA scores is not caused solely by AI, since scores have been falling since 2003.", "articles": [{"article": "A6", "bearing": "supports"}, {"article": "A2", "bearing": "supports"}]},
{"text": "About 86% of students across OECD countries have used AI chatbots for schoolwork.", "articles": [{"article": "A6", "bearing": "supports"}]},
{"text": "Students who use AI chatbots moderately for schoolwork, monthly to weekly, score higher in science than both rare users and daily users.", "articles": [{"article": "A6", "bearing": "supports"}]},
{"text": "Students who use AI chatbots for schoolwork almost every day score lower in science than nonusers after accounting for socioeconomic status.", "articles": [{"article": "A6", "bearing": "supports"}]},
{"text": "Students who do not use AI chatbots for schoolwork generally score higher on PISA than students who do.", "articles": [{"article": "A6", "bearing": "supports"}]},
{"text": "Moderate, purposeful use of AI can support student learning.", "articles": [{"article": "A6", "bearing": "supports"}, {"article": "A4", "bearing": "supports"}, {"article": "A3", "bearing": "supports"}, {"article": "A5", "bearing": "mixed"}]},
{"text": "Learning requires productive cognitive struggle with new material rather than consumption of content.", "articles": [{"article": "A6", "bearing": "supports"}, {"article": "A3", "bearing": "supports"}]},
{"text": "Students with weak critical reading skills are less able to recognize when AI-generated answers are incomplete or incorrect.", "articles": [{"article": "A6", "bearing": "supports"}]},
{"text": "Among about 27,000 Chinese students aged 12 to 18, adopting generative AI raised homework scores by 18%.", "articles": [{"article": "A3", "bearing": "supports"}]},
{"text": "Among Chinese students aged 12 to 18, adopting generative AI cut time per homework assignment from about 64 to 45 minutes.", "articles": [{"article": "A3", "bearing": "supports"}]},
{"text": "Among Chinese students aged 12 to 18, adopting generative AI lowered closed-book monthly exam scores by about 20% within six months.", "articles": [{"article": "A3", "bearing": "supports"}]},
{"text": "Outsourcing schoolwork to unstructured generative AI improves task performance without producing real learning gains.", "articles": [{"article": "A3", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "How students use AI matters more for learning than whether they use it.", "articles": [{"article": "A3", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}, {"article": "A4", "bearing": "supports"}]},
{"text": "About 31% of European students aged 12 to 17 use AI to get complete solutions to schoolwork tasks.", "articles": [{"article": "A3", "bearing": "supports"}]},
{"text": "China requires at least eight hours of AI instruction per year in schools.", "articles": [{"article": "A3", "bearing": "supports"}]},
{"text": "About half of UK full-time undergraduates believe AI has improved their student experience.", "articles": [{"article": "A3", "bearing": "supports"}]},
{"text": "AI use makes most UK undergraduates neither more nor less lonely.", "articles": [{"article": "A3", "bearing": "supports"}]},
{"text": "Nearly three in four US K-12 teachers believe AI will have bigger implications for education than the internet or computers.", "articles": [{"article": "A5", "bearing": "supports"}]},
{"text": "AI makes it harder for students to learn critical thinking skills.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A3", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}, {"article": "A4", "bearing": "disputes"}]},
{"text": "AI is eroding trust between students and teachers in US K-12 schools.", "articles": [{"article": "A5", "bearing": "mixed"}]},
{"text": "Schools should teach students responsible use of AI.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A4", "bearing": "supports"}]},
{"text": "About half of US K-12 teachers have received no school guidance on AI or are unsure what it is.", "articles": [{"article": "A5", "bearing": "supports"}]},
{"text": "About 60% of US K-12 teachers have used AI for work tasks.", "articles": [{"article": "A5", "bearing": "supports"}]},
{"text": "For most US K-12 teachers who use AI, it saves two hours or less per week.", "articles": [{"article": "A5", "bearing": "supports"}]},
{"text": "AI tools are not reliable enough to generate accurate math questions for assessments.", "articles": [{"article": "A5", "bearing": "supports"}]},
{"text": "AI can especially help students with disabilities complete schoolwork.", "articles": [{"article": "A5", "bearing": "supports"}]},
{"text": "Educators are shifting assignments toward in-class or handwritten work in response to AI.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A1", "bearing": "supports"}]},
{"text": "AI used well as a collaborator strengthens a writer's thinking.", "articles": [{"article": "A4", "bearing": "supports"}, {"article": "A3", "bearing": "mixed"}]}
]}
```

</details>

<details><summary>Opus 5.5 · Charged negative set · 11 October 2026, 00:00</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (3960 words)

```text
Here are 6 news articles on one topic, labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CNN, 2026-09-02, “Nation’s largest school district bans AI in the classroom through 8th grade”, 541 words. Text not included.]
[Article A2: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A3: NBC News, 2026-09-17, “Poll: Most Americans think AI is doing more harm than good in schools”, 488 words. Text not included.]
[Article A4: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A5: IBTimes UK, 2026-08-20, “Major Study Reveals 20% Exam Score Drop Among Students Who Relied on AI Tools”, 544 words. Text not included.]
[Article A6: South China Morning Post (republished by The Star), 2026-07-17, “AI homework tools cut exam scores by 20%, study of 26,000 Chinese students finds”, 717 words. Text not included.]




Task: list the beliefs about the world that a reader of these articles could come to hold after reading them.

A belief here is a statement about the world that a reader could accept or reject: about what happened or is the case, what a number is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each belief is one declarative statement with exactly one claim. Test every belief before you list it: if it can be divided into two statements, each of which a reader could accept while rejecting the other, divide it and list both. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal belief (A causes B) is one statement only when the causal link is the claim.
2. Each belief must stand on its own: a reader who has not seen the articles must be able to understand it. Give full names, and include the time, place and population when the statement's truth depends on them.
3. State the belief about the world, not about the articles or about what someone said: write the claim itself, not that a person or study made it.
4. Include beliefs that one article supports and another disputes, beliefs that several articles bear on together, and beliefs that a reader could take away although no single sentence states them. Every belief must be one that these articles bear on; do not add beliefs the articles do not touch.
5. Write each belief so that a person could agree or disagree with it. Do not hedge it with "may" or "might" unless the uncertainty is the claim.
6. List 40 beliefs. Do not list the same belief twice in different words.

For each belief, list the articles that bear on it and how: "supports" (a reader of that article would be led toward the belief), "disputes" (led away from it), or "mixed" (the article gives evidence both ways).

Return JSON of the form {"beliefs": [{"text": "<belief>", "articles": [{"article": "<label>", "bearing": "supports|disputes|mixed"}]}, ...]}.
```

**The reply** (1035 words)

```text
{"beliefs": [
{"text": "In September 2026, New York City announced a one-year moratorium on student use of generative AI in public schools from 2K through 8th grade.", "articles": [{"article": "A1", "bearing": "supports"}, {"article": "A3", "bearing": "supports"}]},
{"text": "New York City's 2026 AI moratorium for grades 2K through 8 affects nearly 600,000 public school students.", "articles": [{"article": "A1", "bearing": "supports"}]},
{"text": "Under New York City's 2026 school technology policy, the AI components of more than 38 previously allowed educational programs will be discontinued or disabled.", "articles": [{"article": "A1", "bearing": "supports"}]},
{"text": "Under New York City's 2026 policy, ChatGPT and Claude are blocked for public school students in all grades.", "articles": [{"article": "A1", "bearing": "supports"}]},
{"text": "Under New York City's 2026 policy, public high school students have access to only a limited slate of AI tools.", "articles": [{"article": "A1", "bearing": "supports"}, {"article": "A3", "bearing": "supports"}]},
{"text": "Under New York City's 2026 policy, public school teachers may not use AI for grading or student assessments.", "articles": [{"article": "A1", "bearing": "supports"}]},
{"text": "Under New York City's 2026 policy, public school teachers may use AI for lesson planning.", "articles": [{"article": "A1", "bearing": "supports"}]},
{"text": "New York City's 2026 school AI policy includes exceptions for students with disabilities and English learners.", "articles": [{"article": "A1", "bearing": "supports"}]},
{"text": "Banning generative AI for young students protects their critical thinking abilities.", "articles": [{"article": "A1", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "AI in early education is neither inevitable nor necessary.", "articles": [{"article": "A1", "bearing": "supports"}, {"article": "A3", "bearing": "disputes"}]},
{"text": "Schools cannot effectively prevent students from using AI at home to complete homework.", "articles": [{"article": "A1", "bearing": "supports"}]},
{"text": "The Los Angeles Unified School District restricted student access to generative AI platforms in 2026 while it reviews safeguards.", "articles": [{"article": "A1", "bearing": "supports"}]},
{"text": "New York City's education department banned ChatGPT from school devices and networks in 2023, then reversed the ban months later.", "articles": [{"article": "A1", "bearing": "supports"}]},
{"text": "AI companies have provided funding to US teachers' unions to develop AI training curricula.", "articles": [{"article": "A1", "bearing": "supports"}]},
{"text": "Among Chinese secondary students aged 12 to 18, adopting generative AI raised homework scores by about 18 percent.", "articles": [{"article": "A2", "bearing": "supports"}, {"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Among Chinese secondary students, generative AI use cut average homework time per assignment from 64 minutes to 45 minutes.", "articles": [{"article": "A2", "bearing": "supports"}, {"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Chinese secondary students who adopted generative AI saw their closed-book monthly exam scores fall by about 20 percent within six months.", "articles": [{"article": "A2", "bearing": "supports"}, {"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Among Chinese students affected by AI homework outsourcing, zhongkao high school entrance exam scores fell by 24 percent.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Among Chinese students affected by AI homework outsourcing, gaokao university entrance exam scores fell by 18 percent.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "The learning harm from generative AI use takes about two years to fully emerge in high-stakes exam results.", "articles": [{"article": "A2", "bearing": "supports"}, {"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Around 80 percent of secondary students in a central Chinese county used generative AI tools such as Doubao and DeepSeek by 2025.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Roughly 80 percent of Chinese secondary students who used generative AI used it to outsource their homework.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Students who use AI as a tutor while spending as much time on homework as non-users suffer little or no exam score loss.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}, {"article": "A2", "bearing": "supports"}]},
{"text": "How students use AI matters more for their learning than whether they use it.", "articles": [{"article": "A2", "bearing": "supports"}, {"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Generative AI is not inherently harmful to student learning.", "articles": [{"article": "A6", "bearing": "supports"}, {"article": "A5", "bearing": "supports"}, {"article": "A3", "bearing": "disputes"}]},
{"text": "Among Chinese secondary students, AI-related exam losses were largest in social science subjects.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Among Chinese secondary students, high-achieving students suffered larger AI-related exam declines than lower achievers.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Among Chinese secondary students, boys suffered larger AI-related exam declines than girls because they used AI more intensively.", "articles": [{"article": "A5", "bearing": "supports"}, {"article": "A6", "bearing": "supports"}]},
{"text": "Teachers fail to notice AI-driven learning losses promptly because normal score fluctuations within a single subject mask the trend.", "articles": [{"article": "A6", "bearing": "supports"}]},
{"text": "Undergraduates who use a chatbot to learn an unfamiliar topic perform better on tests a week later.", "articles": [{"article": "A5", "bearing": "supports"}]},
{"text": "Generative AI that is neither designed to teach nor used under structure improves task performance without producing real learning gains.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "Among European students aged 12 to 17, 31 percent use AI to get complete solutions to study tasks.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "China requires at least eight hours of AI instruction per year for students.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "Nearly half of full-time UK undergraduates believe AI has improved their student experience.", "articles": [{"article": "A2", "bearing": "supports"}]},
{"text": "As of September 2026, 53 percent of US adults believe AI does more harm than good in K-12 education.", "articles": [{"article": "A3", "bearing": "supports"}]},
{"text": "As of September 2026, 56 percent of US adults believe a school that prohibits AI will better prepare students for the future than one that integrates it, up 9 points from June 2025.", "articles": [{"article": "A3", "bearing": "supports"}]},
{"text": "As of September 2026, 31 percent of US adults think no use of AI for schoolwork is acceptable.", "articles": [{"article": "A3", "bearing": "supports"}]},
{"text": "Young US students need hands-on AI education to avoid falling behind.", "articles": [{"article": "A3", "bearing": "supports"}, {"article": "A1", "bearing": "disputes"}]},
{"text": "Reading, science and math performance among 15-year-olds declined globally in the 2025 PISA assessment.", "articles": [{"article": "A4", "bearing": "supports"}]},
{"text": "US 15-year-olds' reading scores in the 2025 PISA assessment fell close to 25-year lows.", "articles": [{"article": "A4", "bearing": "supports"}]}
]}
```

</details>
