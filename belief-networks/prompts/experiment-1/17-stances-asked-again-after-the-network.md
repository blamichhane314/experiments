# Experiment 1, step 17 of 18: Stances, asked again after the network

Ratings and a network over the forty statements. Requests sent: 10. Models: Haiku 4.5. First and last request: 10 October 2026, 23:51 to 11 October 2026, 00:17 (Pacific time).

The request asks: “Give your current rating of every statement, as an integer from -10 (completely disagree) to 10 (completely agree), where 0 means you neither agree nor disagree. If you cannot form a view on a statement, give null for it.”

## The template

`net_stance_update.txt`. The parts in braces are filled in for each request.

```text
{diet}Here are {n} statements.

{statements}

Earlier you gave these ratings (-10 completely disagree to 10 completely agree, 0 neither, null where you could not form a view):
{previous}

Give your current rating of every statement, as an integer from -10 (completely disagree) to 10 (completely agree), where 0 means you neither agree nor disagree. If you cannot form a view on a statement, give null for it. You may keep or change any rating.

Return JSON of the form {{"stances": {{"b0": <integer or null>, "b1": <integer or null>, ...}}}} with every statement id.
```

## Requests as sent (2)

One request for each combination of article set, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Haiku 4.5 · Balanced set · 10 October 2026, 23:51</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (5924 words)

```text
Over the past days you have read these news articles, in this order.

[Article A1: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]
[Article A2: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]
[Article A3: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A4: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A5: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A6: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]




Here are 80 statements.

b0  Chatbots sometimes produce wrong information.
b1  Far from half of UK undergraduates believe AI has improved their student experience.
b2  Chatbots never produce wrong information.
b3  Teachers are shifting graded work to in-class or handwritten formats because of AI.
b4  Raising all American 15-year-olds to at least basic PISA proficiency would not add over $40 trillion to the US economy over their working lives.
b5  Few European students aged 12 to 17 use AI to obtain complete solutions to tasks.
b6  It is not the case that most OECD students (86%) have used AI chatbots for at least one schoolwork purpose.
b7  Schools should teach students the responsible use of AI.
b8  Chinese PISA results are not representative of the whole country.
b9  US 15-year-olds' reading scores on PISA have fallen to close to 25-year lows.
b10  AI is not the only cause of declines in student test scores.
b11  Students who do not use AI chatbots for schoolwork generally score higher than students who do.
b12  Generative AI adoption does not raise students' homework scores.
b13  Students who use AI almost every day do not tend to score lower in science than non-users.
b14  Student performance has become less linked to national or family wealth as technology has progressed.
b15  The share of hasty readers among 15-year-olds almost doubled between 2018 and 2025.
b16  Generative AI adoption cut Chinese students' time per assignment by about 30%.
b17  AI use is eroding trust between students and teachers.
b18  Nearly a third of European students aged 12 to 17 use AI to get complete solutions to study tasks.
b19  Skills such as evaluating information and thinking critically are declining among students in the AI age.
b20  Many European students aged 12 to 17 use AI to obtain complete solutions to tasks.
b21  AI use is not eroding trust between students and teachers.
b22  The share of hasty readers among 15-year-olds did not almost double between 2018 and 2025.
b23  Students in China, Japan and South Korea do not report far less digital distraction in science lessons than the global average.
b24  Students in China, Japan and South Korea report far less digital distraction in science lessons than the global average.
b25  Students cheated on assignments long before AI existed.
b26  US 15-year-olds' reading scores on PISA have not fallen to close to 25-year lows.
b27  Students who use AI chatbots almost every day score lower in science than students who do not, after accounting for socioeconomic status.
b28  It is not the case that most teachers who use AI for work save only two hours or less per week.
b29  Take-home essay assignments are still a sufficient way to assess students even though AI exists.
b30  Outsourcing thinking to AI produces metacognitive laziness in students.
b31  Students who use AI almost every day tend to score lower in science than non-users.
b32  Only wealthy eastern provinces of China participated in PISA.
b33  Digital distraction in the classroom does not contribute to declining student performance.
b34  AI can help students with disabilities complete assignments they otherwise could not.
b35  Most teachers who use AI for work save only two hours or less per week.
b36  Generative AI adoption did not cut Chinese students' time per assignment by about 30%.
b37  Students did not cheat on assignments long before AI existed.
b38  Outsourcing tasks to unstructured generative AI does not improve performance without real learning gains.
b39  Students who use AI chatbots almost every day do not score lower in science than students who do not, after accounting for socioeconomic status.
b40  Student performance has not become less linked to national or family wealth as technology has progressed.
b41  Singapore does not show that classrooms can use technology while still emphasizing early reading comprehension.
b42  How students use AI does not matter more for learning than whether they use it.
b43  Fewer than a third of European students aged 12 to 17 use AI to get complete solutions to study tasks.
b44  Singapore shows that classrooms can use technology while still emphasizing early reading comprehension.
b45  Moderate AI use for schoolwork, from about monthly to once or twice a week, is not associated with higher science scores than rare or near-daily use.
b46  Generative AI adoption raised Chinese students' homework scores by about 18%.
b47  A majority of US K-12 teachers worry that AI makes it harder for students to learn to think critically.
b48  AI is the only cause of declines in student test scores.
b49  Chinese students who adopted generative AI saw their closed-book monthly exam scores fall by about 20% within six months.
b50  Chinese PISA results are representative of the whole country.
b51  Heavy reliance on AI does not create a feedback loop in which weaker readers cannot spot AI errors and lose chances to build skills.
b52  Generative AI adoption did not raise Chinese students' homework scores by about 18%.
b53  Only four wealthy eastern coastal jurisdictions of China submitted scores to PISA.
b54  The main danger of AI does not lie in the concentration of power rather than in the technology itself.
b55  Moderate AI use for schoolwork, from about monthly to once or twice a week, is associated with higher science scores than rare or near-daily use.
b56  How students use AI matters more for learning than whether they use it.
b57  About one in five 15-year-old students across OECD countries use AI chatbots almost every day for schoolwork.
b58  It is not the case that only wealthy eastern provinces of China participated in PISA.
b59  Teachers are not shifting graded work to in-class or handwritten formats because of AI.
b60  Digital distraction in the classroom contributes to declining student performance.
b61  A majority of US K-12 teachers do not worry that AI makes it harder for students to learn to think critically.
b62  Raising all American 15-year-olds to at least basic PISA proficiency would add over $40 trillion to the US economy over their working lives.
b63  AI cannot help students with disabilities complete assignments they otherwise could not.
b64  Chinese students who adopted generative AI did not see their closed-book monthly exam scores fall by about 20% within six months.
b65  Far from one in five 15-year-old students across OECD countries use AI chatbots almost every day for schoolwork.
b66  More than four wealthy eastern coastal jurisdictions of China submitted scores to PISA.
b67  The main danger of AI lies in the concentration of power rather than in the technology itself.
b68  Heavy reliance on AI creates a feedback loop in which weaker readers cannot spot AI errors and lose chances to build skills.
b69  Schools should not teach students the responsible use of AI.
b70  Generative AI adoption raises students' homework scores.
b71  Skills such as evaluating information and thinking critically are not declining among students in the AI age.
b72  About half of UK undergraduates believe AI has improved their student experience.
b73  Most US K-12 teachers do not believe AI will affect education more than the internet or computers did.
b74  Students who do not use AI chatbots for schoolwork do not generally score higher than students who do.
b75  Take-home essay assignments are no longer a sufficient way to assess students now that AI exists.
b76  Most OECD students (86%) have used AI chatbots for at least one schoolwork purpose.
b77  Most US K-12 teachers believe AI will affect education more than the internet or computers did.
b78  Outsourcing thinking to AI does not produce metacognitive laziness in students.
b79  Outsourcing tasks to unstructured generative AI improves performance without real learning gains.


Earlier you gave these ratings (-10 completely disagree to 10 completely agree, 0 neither, null where you could not form a view):
b0  10
b1  10
b2  -10
b3  8
b4  -10
b5  -8
b6  -10
b7  9
b8  9
b9  10
b10  10
b11  10
b12  -10
b13  -10
b14  7
b15  10
b16  10
b17  9
b18  9
b19  10
b20  9
b21  -9
b22  -10
b23  -10
b24  10
b25  10
b26  -10
b27  10
b28  -10
b29  -9
b30  9
b31  10
b32  9
b33  -10
b34  9
b35  9
b36  -10
b37  -10
b38  -9
b39  -10
b40  -7
b41  -10
b42  -10
b43  -9
b44  10
b45  -10
b46  10
b47  10
b48  -10
b49  10
b50  -9
b51  -10
b52  -10
b53  9
b54  -9
b55  10
b56  10
b57  10
b58  -10
b59  -8
b60  10
b61  -10
b62  10
b63  -9
b64  -10
b65  -10
b66  -8
b67  9
b68  10
b69  -9
b70  10
b71  -10
b72  10
b73  -10
b74  -10
b75  9
b76  10
b77  10
b78  -9
b79  -10


Give your current rating of every statement, as an integer from -10 (completely disagree) to 10 (completely agree), where 0 means you neither agree nor disagree. If you cannot form a view on a statement, give null for it. You may keep or change any rating.

Return JSON of the form {"stances": {"b0": <integer or null>, "b1": <integer or null>, ...}} with every statement id.
```

**The reply** (167 words)

````text
```json
{
  "stances": {
    "b0": 10,
    "b1": 10,
    "b2": -10,
    "b3": 8,
    "b4": -10,
    "b5": -8,
    "b6": -10,
    "b7": 9,
    "b8": 9,
    "b9": 10,
    "b10": 10,
    "b11": 10,
    "b12": -10,
    "b13": -10,
    "b14": 7,
    "b15": 10,
    "b16": 10,
    "b17": 9,
    "b18": 9,
    "b19": 10,
    "b20": 9,
    "b21": -9,
    "b22": -10,
    "b23": -10,
    "b24": 10,
    "b25": 10,
    "b26": -10,
    "b27": 10,
    "b28": -10,
    "b29": -9,
    "b30": 9,
    "b31": 10,
    "b32": 9,
    "b33": -10,
    "b34": 9,
    "b35": 9,
    "b36": -10,
    "b37": -10,
    "b38": -9,
    "b39": -10,
    "b40": -7,
    "b41": -10,
    "b42": -10,
    "b43": -9,
    "b44": 10,
    "b45": -10,
    "b46": 10,
    "b47": 10,
    "b48": -10,
    "b49": 10,
    "b50": -9,
    "b51": -10,
    "b52": -10,
    "b53": 9,
    "b54": -9,
    "b55": 10,
    "b56": 10,
    "b57": 10,
    "b58": -10,
    "b59": -8,
    "b60": 10,
    "b61": -10,
    "b62": 10,
    "b63": -9,
    "b64": -10,
    "b65": -10,
    "b66": -8,
    "b67": 9,
    "b68": 10,
    "b69": -9,
    "b70": 10,
    "b71": -10,
    "b72": 10,
    "b73": -10,
    "b74": -10,
    "b75": 9,
    "b76": 10,
    "b77": 10,
    "b78": -9,
    "b79": -10
  }
}
```
````

</details>

<details><summary>Haiku 4.5 · Charged negative set · 11 October 2026, 00:16</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (5093 words)

```text
Over the past days you have read these news articles, in this order.

[Article A1: South China Morning Post (republished by The Star), 2026-07-17, “AI homework tools cut exam scores by 20%, study of 26,000 Chinese students finds”, 717 words. Text not included.]
[Article A2: CNN, 2026-09-02, “Nation’s largest school district bans AI in the classroom through 8th grade”, 541 words. Text not included.]
[Article A3: NBC News, 2026-09-17, “Poll: Most Americans think AI is doing more harm than good in schools”, 488 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A6: IBTimes UK, 2026-08-20, “Major Study Reveals 20% Exam Score Drop Among Students Who Relied on AI Tools”, 544 words. Text not included.]




Here are 80 statements.

b0  Restricting AI in early education does not protect teacher-student relationships.
b1  Without structure or instructional design, generative AI improves task performance.
b2  It is not the case that about half of UK undergraduates believe AI has improved their student experience.
b3  Heavy student use of generative AI did not lower Chinese students' results on the zhongkao high school entrance exam by about 24%.
b4  Social science subjects did not suffer the largest exam declines among AI-using Chinese students, followed by STEM and then languages.
b5  Without structure or instructional design, generative AI does not produce real learning gains.
b6  Heavy student use of generative AI did not lower Chinese students' gaokao university entrance exam results by about 18%.
b7  The advantage of using a chatbot to learn an unfamiliar topic did not persist a week later.
b8  Evidence from short-term studies does not understate AI's long-term damage to learning.
b9  Heavy student use of generative AI lowered Chinese students' gaokao university entrance exam results by about 18%.
b10  Teachers and students are not slow to notice AI's learning harm because AI-completed work feels fluent and productive.
b11  Younger secondary students lose more from AI use than older ones.
b12  Not about 80% of students in the Chinese study reported using generative AI.
b13  The learning harm from student AI use does not accumulate slowly.
b14  Top-performing students did not lose more from AI use than lower-achieving students.
b15  The New York City ban on generative AI use for students from pre-kindergarten through 8th grade is not a one-year moratorium.
b16  AI use among UK undergraduates is not near-universal at 94%.
b17  Digital distraction in the classroom does not harm student performance.
b18  Younger secondary students do not lose more from AI use than older ones.
b19  Proofreading and editing is the AI use Americans most often consider acceptable for school assignments.
b20  AI use among UK undergraduates is near-universal, at 94%.
b21  Generative AI use raised the homework scores of Chinese secondary students by about 18 percent.
b22  The advantage of using a chatbot to learn an unfamiliar topic persisted a week later.
b23  Teachers and students are slow to notice AI's learning harm because AI-completed work feels fluent and productive.
b24  AI use among German undergraduates is near-universal, at 93%.
b25  Even without structure or instructional design, generative AI can produce real learning gains.
b26  The tech industry's claim that AI in early education is inevitable and necessary is wrong.
b27  Generative AI use did not cut the time Chinese secondary students spent per homework assignment from about 64 minutes to about 45 minutes.
b28  Using a chatbot to learn an unfamiliar topic improved undergraduates' test performance.
b29  Top-performing students lost more from AI use than lower-achieving students.
b30  About 80% of students in the Chinese study reported using generative AI.
b31  The effect of generative AI on learning depends on how students use it.
b32  Outsourcing tasks to AI does not reduce the productive cognitive effort that real learning requires.
b33  It is not the case that a majority of American adults, about 53 percent, think AI does more harm than good in K-12 education.
b34  AI use makes no difference to loneliness for most UK undergraduates.
b35  Heavy student use of generative AI lowered Chinese students' results on the zhongkao high school entrance exam by about 24%.
b36  Generative AI use cut the time Chinese secondary students spent per homework assignment from about 64 minutes to about 45 minutes.
b37  Without structure or instructional design, generative AI does not improve task performance.
b38  It is not the case that a majority of American adults think AI does more harm than good in K-12 education.
b39  Evidence from short-term studies understates AI's long-term damage to learning.
b40  The learning harm from student AI use takes about two years to fully show up.
b41  Generative AI is inherently harmful to learning.
b42  Very few Americans think it is acceptable for students to have AI write and generate their schoolwork.
b43  Digital distraction in the classroom harms student performance.
b44  Restricting AI in early education protects students' critical thinking.
b45  The New York City ban on generative AI use for students from pre-kindergarten through 8th grade is a one-year moratorium.
b46  Generative AI is not inherently harmful to learning.
b47  About half of UK undergraduates believe AI has improved their student experience.
b48  Restricting AI in early education does not protect students' critical thinking.
b49  Students who use AI as a tutor while spending about as long on homework as non-users do not suffer little or no loss in exam performance.
b50  Social science subjects suffered the largest exam declines among AI-using Chinese students, followed by STEM and then languages.
b51  Boys were hit harder by AI-related learning declines than girls because of more intensive AI use.
b52  The effect of generative AI on learning does not depend on how students use it.
b53  Proofreading and editing is not the AI use Americans most often consider acceptable for school assignments.
b54  Within six months of adopting generative AI, Chinese secondary students' monthly closed-book exam scores fell by about 20% relative to non-users.
b55  Los Angeles Unified School District is not restricting student access to generative AI platforms.
b56  Teaching students about AI and giving them hands-on experience is needed so the United States does not fall behind.
b57  Schools cannot easily prevent students from using AI at home to complete homework.
b58  A majority of American adults, about 53 percent, think AI does more harm than good in K-12 education.
b59  AI use makes a difference to loneliness for most UK undergraduates.
b60  Students who use AI as a tutor while spending about as long on homework as non-users suffer little or no loss in exam performance.
b61  Outsourcing tasks to AI reduces the productive cognitive effort that real learning requires.
b62  The tech industry's claim that AI in early education is inevitable and necessary is not wrong.
b63  Using a chatbot to learn an unfamiliar topic did not improve undergraduates' test performance.
b64  Boys were not hurt more by AI use than girls.
b65  Boys were not hit harder by AI-related learning declines than girls because of more intensive AI use.
b66  The learning harm from student AI use accumulates slowly.
b67  Los Angeles Unified School District is restricting student access to generative AI platforms.
b68  Teaching students about AI and giving them hands-on experience is not needed so the United States does not fall behind.
b69  Younger secondary students lose more from AI use than older ones because of looser oversight.
b70  Younger secondary students do not lose more from AI use than older ones because of looser oversight.
b71  AI use among German undergraduates is not near-universal at 93%.
b72  Generative AI use did not raise the homework scores of Chinese secondary students by about 18 percent.
b73  It is not the case that very few Americans think it is acceptable for students to have AI write and generate their schoolwork.
b74  Restricting AI in early education protects teacher-student relationships.
b75  Schools can easily prevent students from using AI at home to complete homework.
b76  Boys were hurt more by AI use than girls.
b77  A majority of American adults think AI does more harm than good in K-12 education.
b78  The learning harm from student AI use does not take about two years to fully show up.
b79  Within six months of adopting generative AI, Chinese secondary students' monthly closed-book exam scores did not fall by about 20% relative to non-users.


Earlier you gave these ratings (-10 completely disagree to 10 completely agree, 0 neither, null where you could not form a view):
b0  -8
b1  -9
b2  -8
b3  -9
b4  -9
b5  9
b6  -9
b7  -9
b8  -9
b9  9
b10  8
b11  9
b12  -9
b13  -9
b14  -9
b15  -9
b16  -9
b17  -9
b18  -9
b19  8
b20  9
b21  9
b22  9
b23  8
b24  9
b25  -8
b26  8
b27  -9
b28  9
b29  9
b30  9
b31  9
b32  -9
b33  -9
b34  7
b35  9
b36  9
b37  -9
b38  -9
b39  9
b40  9
b41  -7
b42  8
b43  9
b44  8
b45  9
b46  9
b47  8
b48  -8
b49  -9
b50  9
b51  9
b52  -9
b53  -8
b54  9
b55  -9
b56  7
b57  9
b58  9
b59  -7
b60  9
b61  9
b62  -8
b63  -9
b64  -9
b65  -9
b66  9
b67  9
b68  -7
b69  9
b70  -9
b71  -9
b72  -9
b73  -8
b74  8
b75  -9
b76  9
b77  9
b78  -9
b79  -9


Give your current rating of every statement, as an integer from -10 (completely disagree) to 10 (completely agree), where 0 means you neither agree nor disagree. If you cannot form a view on a statement, give null for it. You may keep or change any rating.

Return JSON of the form {"stances": {"b0": <integer or null>, "b1": <integer or null>, ...}} with every statement id.
```

**The reply** (167 words)

````text
```json
{
  "stances": {
    "b0": -8,
    "b1": -9,
    "b2": -8,
    "b3": -9,
    "b4": -9,
    "b5": 9,
    "b6": -9,
    "b7": -9,
    "b8": -9,
    "b9": 9,
    "b10": 8,
    "b11": 9,
    "b12": -9,
    "b13": -9,
    "b14": -9,
    "b15": -9,
    "b16": -9,
    "b17": -9,
    "b18": -9,
    "b19": 8,
    "b20": 9,
    "b21": 9,
    "b22": 9,
    "b23": 8,
    "b24": 9,
    "b25": -8,
    "b26": 8,
    "b27": -9,
    "b28": 9,
    "b29": 9,
    "b30": 9,
    "b31": 9,
    "b32": -9,
    "b33": -9,
    "b34": 7,
    "b35": 9,
    "b36": 9,
    "b37": -9,
    "b38": -9,
    "b39": 9,
    "b40": 9,
    "b41": -7,
    "b42": 8,
    "b43": 9,
    "b44": 8,
    "b45": 9,
    "b46": 9,
    "b47": 8,
    "b48": -8,
    "b49": -9,
    "b50": 9,
    "b51": 9,
    "b52": -9,
    "b53": -8,
    "b54": 9,
    "b55": -9,
    "b56": 7,
    "b57": 9,
    "b58": 9,
    "b59": -7,
    "b60": 9,
    "b61": 9,
    "b62": -8,
    "b63": -9,
    "b64": -9,
    "b65": -9,
    "b66": 9,
    "b67": 9,
    "b68": -7,
    "b69": 9,
    "b70": -9,
    "b71": -9,
    "b72": -9,
    "b73": -8,
    "b74": 8,
    "b75": -9,
    "b76": 9,
    "b77": 9,
    "b78": -9,
    "b79": -9
  }
}
```
````

</details>
