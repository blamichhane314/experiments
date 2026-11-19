# Experiment 1, step 13 of 18: Rating what one article conveys about each statement

Ratings and a network over the forty statements. Requests sent: 120. Models: Haiku 4.5. First and last request: 10 October 2026, 23:49 to 11 October 2026, 00:14 (Pacific time).

The request asks: “For each statement, say what the writer's article conveys about it: not your own view, and not what you know from elsewhere, but what this article, as the writer wrote it, puts across to a reader. Give an integer from -10 (the article conveys firmly that the statement is false, or argues firmly against it) to 10 (the…”

## The template

`rate_attributed.txt`. The parts in braces are filled in for each request.

```text
A writer published the following news article.

"""
{headline}

{text}
"""

Here are {n} statements.

{statements}

For each statement, say what the writer's article conveys about it: not your own view, and not what you know from elsewhere, but what this article, as the writer wrote it, puts across to a reader. Give an integer from -10 (the article conveys firmly that the statement is false, or argues firmly against it) to 10 (the article conveys firmly that the statement is true, or argues firmly for it), where 0 means the article addresses the statement without taking either side. If the article does not address the statement, give null.

For each statement the article addresses, also say whose voice carries it: "writer" (the writer's own voice), "source" (a person, group or study the article cites), or "both".

Return JSON of the form {{"readings": {{"b0": {{"conveys": <integer or null>, "voice": "writer" | "source" | "both" | null}}, ...}}}} with every statement id.
```

## Requests as sent (2)

One request for each combination of article set, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Haiku 4.5 · Balanced set · 10 October 2026, 23:49</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (2261 words)

```text
A writer published the following news article.

"""
[Article 1: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]


"""

Here are 90 statements.

b0  Stanger says the main danger of AI lies in the concentration of power rather than in the technology itself.
b1  AI use is not eroding trust between students and teachers.
b2  The share of hasty readers among 15-year-olds did not almost double between 2018 and 2025.
b3  Moderate AI use for schoolwork, from about monthly to once or twice a week, is associated with higher science scores than rare or near-daily use.
b4  Moderate AI use for schoolwork, from about monthly to once or twice a week, is not associated with higher science scores than rare or near-daily use.
b5  Take-home essay assignments are still a sufficient way to assess students even though AI exists.
b6  A majority of US K-12 teachers do not worry that AI makes it harder for students to learn to think critically.
b7  Far from half of UK undergraduates believe AI has improved their student experience.
b8  The share of hasty readers among 15-year-olds almost doubled between 2018 and 2025.
b9  Stanger says she always writes her own first drafts before involving AI.
b10  Students who use AI almost every day do not tend to score lower in science than non-users.
b11  AI can help students with disabilities complete assignments they otherwise could not.
b12  Outsourcing tasks to unstructured generative AI does not improve performance without real learning gains.
b13  It is not the case that most teachers who use AI for work save only two hours or less per week.
b14  Outsourcing thinking to AI produces metacognitive laziness in students.
b15  Stanger says AI is potentially very dangerous.
b16  Outsourcing thinking to AI does not produce metacognitive laziness in students.
b17  Students in China, Japan and South Korea report far less digital distraction in science lessons than the global average.
b18  Stanger says she outlines her own argument before involving AI.
b19  Only wealthy eastern provinces of China participated in PISA.
b20  Generative AI adoption does not raise students' homework scores.
b21  AI is not the only cause of declines in student test scores.
b22  Stanger says people must keep thinking for themselves and teach students to do so.
b23  Singapore shows that classrooms can use technology while still emphasizing early reading comprehension.
b24  Chinese students who adopted generative AI saw their closed-book monthly exam scores fall by about 20% within six months.
b25  Digital distraction in the classroom does not contribute to declining student performance.
b26  AI is the only cause of declines in student test scores.
b27  Chinese students who adopted generative AI did not see their closed-book monthly exam scores fall by about 20% within six months.
b28  About half of UK undergraduates believe AI has improved their student experience.
b29  Far from one in five 15-year-old students across OECD countries use AI chatbots almost every day for schoolwork.
b30  Students who do not use AI chatbots for schoolwork do not generally score higher than students who do.
b31  Few European students aged 12 to 17 use AI to obtain complete solutions to tasks.
b32  Students who use AI chatbots almost every day score lower in science than students who do not, after accounting for socioeconomic status.
b33  Most US K-12 teachers do not believe AI will affect education more than the internet or computers did.
b34  Skills such as evaluating information and thinking critically are declining among students in the AI age.
b35  Fewer than a third of European students aged 12 to 17 use AI to get complete solutions to study tasks.
b36  Chatbots sometimes produce wrong information.
b37  Many European students aged 12 to 17 use AI to obtain complete solutions to tasks.
b38  Teachers are shifting graded work to in-class or handwritten formats because of AI.
b39  Skills such as evaluating information and thinking critically are not declining among students in the AI age.
b40  The main danger of AI does not lie in the concentration of power rather than in the technology itself.
b41  Student performance has become less linked to national or family wealth as technology has progressed.
b42  Outsourcing tasks to unstructured generative AI improves performance without real learning gains.
b43  More than four wealthy eastern coastal jurisdictions of China submitted scores to PISA.
b44  A majority of US K-12 teachers worry that AI makes it harder for students to learn to think critically.
b45  AI cannot help students with disabilities complete assignments they otherwise could not.
b46  Most US K-12 teachers believe AI will affect education more than the internet or computers did.
b47  Generative AI adoption raised Chinese students' homework scores by about 18%.
b48  Allison Stanger uses AI to help her write.
b49  Chinese PISA results are representative of the whole country.
b50  Singapore does not show that classrooms can use technology while still emphasizing early reading comprehension.
b51  Generative AI adoption did not cut Chinese students' time per assignment by about 30%.
b52  Only four wealthy eastern coastal jurisdictions of China submitted scores to PISA.
b53  It is not the case that most OECD students (86%) have used AI chatbots for at least one schoolwork purpose.
b54  Stanger says humans are best at judging what good writing is.
b55  Generative AI adoption cut Chinese students' time per assignment by about 30%.
b56  Teachers are not shifting graded work to in-class or handwritten formats because of AI.
b57  It is not the case that only wealthy eastern provinces of China participated in PISA.
b58  Generative AI adoption did not raise Chinese students' homework scores by about 18%.
b59  About one in five 15-year-old students across OECD countries use AI chatbots almost every day for schoolwork.
b60  Heavy reliance on AI creates a feedback loop in which weaker readers cannot spot AI errors and lose chances to build skills.
b61  The main danger of AI lies in the concentration of power rather than in the technology itself.
b62  US 15-year-olds' reading scores on PISA have not fallen to close to 25-year lows.
b63  Students in China, Japan and South Korea do not report far less digital distraction in science lessons than the global average.
b64  Students cheated on assignments long before AI existed.
b65  Digital distraction in the classroom contributes to declining student performance.
b66  Schools should teach students the responsible use of AI.
b67  Student performance has not become less linked to national or family wealth as technology has progressed.
b68  Students who use AI almost every day tend to score lower in science than non-users.
b69  How students use AI does not matter more for learning than whether they use it.
b70  US 15-year-olds' reading scores on PISA have fallen to close to 25-year lows.
b71  Allison Stanger is a political science professor at Middlebury College.
b72  AI use is eroding trust between students and teachers.
b73  Students who use AI chatbots almost every day do not score lower in science than students who do not, after accounting for socioeconomic status.
b74  Most teachers who use AI for work save only two hours or less per week.
b75  Chinese PISA results are not representative of the whole country.
b76  Chatbots never produce wrong information.
b77  Take-home essay assignments are no longer a sufficient way to assess students now that AI exists.
b78  Schools should not teach students the responsible use of AI.
b79  Stanger says AI cannot replace showing writing to another human.
b80  Heavy reliance on AI does not create a feedback loop in which weaker readers cannot spot AI errors and lose chances to build skills.
b81  Nearly a third of European students aged 12 to 17 use AI to get complete solutions to study tasks.
b82  Raising all American 15-year-olds to at least basic PISA proficiency would not add over $40 trillion to the US economy over their working lives.
b83  Raising all American 15-year-olds to at least basic PISA proficiency would add over $40 trillion to the US economy over their working lives.
b84  Students who do not use AI chatbots for schoolwork generally score higher than students who do.
b85  Allison Stanger argues that AI used well can strengthen thinking.
b86  Most OECD students (86%) have used AI chatbots for at least one schoolwork purpose.
b87  Students did not cheat on assignments long before AI existed.
b88  How students use AI matters more for learning than whether they use it.
b89  Generative AI adoption raises students' homework scores.


For each statement, say what the writer's article conveys about it: not your own view, and not what you know from elsewhere, but what this article, as the writer wrote it, puts across to a reader. Give an integer from -10 (the article conveys firmly that the statement is false, or argues firmly against it) to 10 (the article conveys firmly that the statement is true, or argues firmly for it), where 0 means the article addresses the statement without taking either side. If the article does not address the statement, give null.

For each statement the article addresses, also say whose voice carries it: "writer" (the writer's own voice), "source" (a person, group or study the article cites), or "both".

Return JSON of the form {"readings": {"b0": {"conveys": <integer or null>, "voice": "writer" | "source" | "both" | null}, ...}} with every statement id.
```

**The reply** (457 words)

````text
```json
{
  "readings": {
    "b0": {"conveys": 10, "voice": "source"},
    "b1": {"conveys": null, "voice": null},
    "b2": {"conveys": null, "voice": null},
    "b3": {"conveys": null, "voice": null},
    "b4": {"conveys": null, "voice": null},
    "b5": {"conveys": null, "voice": null},
    "b6": {"conveys": null, "voice": null},
    "b7": {"conveys": null, "voice": null},
    "b8": {"conveys": null, "voice": null},
    "b9": {"conveys": 10, "voice": "source"},
    "b10": {"conveys": null, "voice": null},
    "b11": {"conveys": null, "voice": null},
    "b12": {"conveys": null, "voice": null},
    "b13": {"conveys": null, "voice": null},
    "b14": {"conveys": null, "voice": null},
    "b15": {"conveys": 10, "voice": "source"},
    "b16": {"conveys": null, "voice": null},
    "b17": {"conveys": null, "voice": null},
    "b18": {"conveys": 10, "voice": "source"},
    "b19": {"conveys": null, "voice": null},
    "b20": {"conveys": null, "voice": null},
    "b21": {"conveys": null, "voice": null},
    "b22": {"conveys": 10, "voice": "source"},
    "b23": {"conveys": null, "voice": null},
    "b24": {"conveys": null, "voice": null},
    "b25": {"conveys": null, "voice": null},
    "b26": {"conveys": null, "voice": null},
    "b27": {"conveys": null, "voice": null},
    "b28": {"conveys": null, "voice": null},
    "b29": {"conveys": null, "voice": null},
    "b30": {"conveys": null, "voice": null},
    "b31": {"conveys": null, "voice": null},
    "b32": {"conveys": null, "voice": null},
    "b33": {"conveys": null, "voice": null},
    "b34": {"conveys": null, "voice": null},
    "b35": {"conveys": null, "voice": null},
    "b36": {"conveys": null, "voice": null},
    "b37": {"conveys": null, "voice": null},
    "b38": {"conveys": null, "voice": null},
    "b39": {"conveys": null, "voice": null},
    "b40": {"conveys": -10, "voice": "source"},
    "b41": {"conveys": null, "voice": null},
    "b42": {"conveys": null, "voice": null},
    "b43": {"conveys": null, "voice": null},
    "b44": {"conveys": null, "voice": null},
    "b45": {"conveys": null, "voice": null},
    "b46": {"conveys": null, "voice": null},
    "b47": {"conveys": null, "voice": null},
    "b48": {"conveys": 10, "voice": "source"},
    "b49": {"conveys": null, "voice": null},
    "b50": {"conveys": null, "voice": null},
    "b51": {"conveys": null, "voice": null},
    "b52": {"conveys": null, "voice": null},
    "b53": {"conveys": null, "voice": null},
    "b54": {"conveys": 10, "voice": "source"},
    "b55": {"conveys": null, "voice": null},
    "b56": {"conveys": null, "voice": null},
    "b57": {"conveys": null, "voice": null},
    "b58": {"conveys": null, "voice": null},
    "b59": {"conveys": null, "voice": null},
    "b60": {"conveys": null, "voice": null},
    "b61": {"conveys": 10, "voice": "source"},
    "b62": {"conveys": null, "voice": null},
    "b63": {"conveys": null, "voice": null},
    "b64": {"conveys": null, "voice": null},
    "b65": {"conveys": null, "voice": null},
    "b66": {"conveys": null, "voice": null},
    "b67": {"conveys": null, "voice": null},
    "b68": {"conveys": null, "voice": null},
    "b69": {"conveys": null, "voice": null},
    "b70": {"conveys": null, "voice": null},
    "b71": {"conveys": 10, "voice": "both"},
    "b72": {"conveys": null, "voice": null},
    "b73": {"conveys": null, "voice": null},
    "b74": {"conveys": null, "voice": null},
    "b75": {"conveys": null, "voice": null},
    "b76": {"conveys": null, "voice": null},
    "b77": {"conveys": null, "voice": null},
    "b78": {"conveys": null, "voice": null},
    "b79": {"conveys": 10, "voice": "source"},
    "b80": {"conveys": null, "voice": null},
    "b81": {"conveys": null, "voice": null},
    "b82": {"conveys": null, "voice": null},
    "b83": {"conveys": null, "voice": null},
    "b84": {"conveys": null, "voice": null},
    "b85": {"conveys": 10, "voice": "both"},
    "b86": {"conveys": null, "voice": null},
    "b87": {"conveys": null, "voice": null},
    "b88": {"conveys": null, "voice": null},
    "b89": {"conveys": null, "voice": null}
  }
}
```
````

</details>

<details><summary>Haiku 4.5 · Charged negative set · 11 October 2026, 00:13</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (2077 words)

```text
A writer published the following news article.

"""
[Article 1: NBC News, 2026-09-17, “Poll: Most Americans think AI is doing more harm than good in schools”, 488 words. Text not included.]


"""

Here are 88 statements.

b0  Restricting AI in early education protects students' critical thinking.
b1  56% of US adults believe a school that prohibits AI will better prepare students for the future than one that integrates it.
b2  AI use makes no difference to loneliness for most UK undergraduates.
b3  Top-performing students did not lose more from AI use than lower-achieving students.
b4  Outsourcing tasks to AI reduces the productive cognitive effort that real learning requires.
b5  Using a chatbot to learn an unfamiliar topic did not improve undergraduates' test performance.
b6  Heavy student use of generative AI did not lower Chinese students' gaokao university entrance exam results by about 18%.
b7  It is not the case that about half of UK undergraduates believe AI has improved their student experience.
b8  Generative AI is inherently harmful to learning.
b9  Students who use AI as a tutor while spending about as long on homework as non-users do not suffer little or no loss in exam performance.
b10  Teaching students about AI and giving them hands-on experience is needed so the United States does not fall behind.
b11  Digital distraction in the classroom harms student performance.
b12  Social science subjects did not suffer the largest exam declines among AI-using Chinese students, followed by STEM and then languages.
b13  Generative AI is not inherently harmful to learning.
b14  AI use among UK undergraduates is not near-universal at 94%.
b15  Restricting AI in early education protects teacher-student relationships.
b16  It is not the case that a majority of American adults think AI does more harm than good in K-12 education.
b17  Outsourcing tasks to AI does not reduce the productive cognitive effort that real learning requires.
b18  About 80% of students in the Chinese study reported using generative AI.
b19  The advantage of using a chatbot to learn an unfamiliar topic did not persist a week later.
b20  The tech industry's claim that AI in early education is inevitable and necessary is wrong.
b21  In the poll, only 7% of adults said it is OK for AI to write and generate content.
b22  About half of UK undergraduates believe AI has improved their student experience.
b23  AI use among UK undergraduates is near-universal, at 94%.
b24  A majority of American adults, about 53 percent, think AI does more harm than good in K-12 education.
b25  A majority of American adults think AI does more harm than good in K-12 education.
b26  Proofreading and editing is the AI use Americans most often consider acceptable for school assignments.
b27  Evidence from short-term studies does not understate AI's long-term damage to learning.
b28  Using a chatbot to learn an unfamiliar topic improved undergraduates' test performance.
b29  Los Angeles Unified School District is not restricting student access to generative AI platforms.
b30  Very few Americans think it is acceptable for students to have AI write and generate their schoolwork.
b31  It is not the case that very few Americans think it is acceptable for students to have AI write and generate their schoolwork.
b32  New York City is banning generative AI use for public school students from 2K through 8th grade for a one-year moratorium.
b33  Boys were hit harder by AI-related learning declines than girls because of more intensive AI use.
b34  Boys were hurt more by AI use than girls.
b35  Teachers and students are slow to notice AI's learning harm because AI-completed work feels fluent and productive.
b36  The effect of generative AI on learning depends on how students use it.
b37  AI use among German undergraduates is not near-universal at 93%.
b38  The New York City ban on generative AI use for students from pre-kindergarten through 8th grade is not a one-year moratorium.
b39  Generative AI use raised the homework scores of Chinese secondary students by about 18 percent.
b40  Evidence from short-term studies understates AI's long-term damage to learning.
b41  AI use among German undergraduates is near-universal, at 93%.
b42  Students who use AI as a tutor while spending about as long on homework as non-users suffer little or no loss in exam performance.
b43  The advantage of using a chatbot to learn an unfamiliar topic persisted a week later.
b44  The poll found 27% of US adults believe AI does more good than harm in K-12 education.
b45  Generative AI use did not raise the homework scores of Chinese secondary students by about 18 percent.
b46  Even without structure or instructional design, generative AI can produce real learning gains.
b47  Heavy student use of generative AI lowered Chinese students' results on the zhongkao high school entrance exam by about 24%.
b48  The learning harm from student AI use accumulates slowly.
b49  Heavy student use of generative AI did not lower Chinese students' results on the zhongkao high school entrance exam by about 24%.
b50  Social science subjects suffered the largest exam declines among AI-using Chinese students, followed by STEM and then languages.
b51  The effect of generative AI on learning does not depend on how students use it.
b52  Without structure or instructional design, generative AI does not produce real learning gains.
b53  Younger secondary students lose more from AI use than older ones because of looser oversight.
b54  The learning harm from student AI use does not accumulate slowly.
b55  Top-performing students lost more from AI use than lower-achieving students.
b56  Schools can easily prevent students from using AI at home to complete homework.
b57  Generative AI use cut the time Chinese secondary students spent per homework assignment from about 64 minutes to about 45 minutes.
b58  Without structure or instructional design, generative AI improves task performance.
b59  Younger secondary students lose more from AI use than older ones.
b60  Younger secondary students do not lose more from AI use than older ones because of looser oversight.
b61  The learning harm from student AI use does not take about two years to fully show up.
b62  In the poll, 49% of adults said AI proofreading and editing is acceptable for student assignments.
b63  Los Angeles Unified School District is restricting student access to generative AI platforms.
b64  The learning harm from student AI use takes about two years to fully show up.
b65  Heavy student use of generative AI lowered Chinese students' gaokao university entrance exam results by about 18%.
b66  Schools cannot easily prevent students from using AI at home to complete homework.
b67  Boys were not hurt more by AI use than girls.
b68  Teachers and students are not slow to notice AI's learning harm because AI-completed work feels fluent and productive.
b69  Generative AI use did not cut the time Chinese secondary students spent per homework assignment from about 64 minutes to about 45 minutes.
b70  Within six months of adopting generative AI, Chinese secondary students' monthly closed-book exam scores fell by about 20% relative to non-users.
b71  Within six months of adopting generative AI, Chinese secondary students' monthly closed-book exam scores did not fall by about 20% relative to non-users.
b72  It is not the case that a majority of American adults, about 53 percent, think AI does more harm than good in K-12 education.
b73  First lady Melania Trump said young students need to learn about AI and get hands-on experience so the United States can lead.
b74  The Decision Desk/SurveyMonkey poll found 53% of US adults believe AI does more harm than good in K-12 education.
b75  The tech industry's claim that AI in early education is inevitable and necessary is not wrong.
b76  The New York City ban on generative AI use for students from pre-kindergarten through 8th grade is a one-year moratorium.
b77  That figure is up 9 points from June 2025.
b78  Younger secondary students do not lose more from AI use than older ones.
b79  Not about 80% of students in the Chinese study reported using generative AI.
b80  Restricting AI in early education does not protect students' critical thinking.
b81  AI use makes a difference to loneliness for most UK undergraduates.
b82  Restricting AI in early education does not protect teacher-student relationships.
b83  Digital distraction in the classroom does not harm student performance.
b84  Without structure or instructional design, generative AI does not improve task performance.
b85  Proofreading and editing is not the AI use Americans most often consider acceptable for school assignments.
b86  Teaching students about AI and giving them hands-on experience is not needed so the United States does not fall behind.
b87  Boys were not hit harder by AI-related learning declines than girls because of more intensive AI use.


For each statement, say what the writer's article conveys about it: not your own view, and not what you know from elsewhere, but what this article, as the writer wrote it, puts across to a reader. Give an integer from -10 (the article conveys firmly that the statement is false, or argues firmly against it) to 10 (the article conveys firmly that the statement is true, or argues firmly for it), where 0 means the article addresses the statement without taking either side. If the article does not address the statement, give null.

For each statement the article addresses, also say whose voice carries it: "writer" (the writer's own voice), "source" (a person, group or study the article cites), or "both".

Return JSON of the form {"readings": {"b0": {"conveys": <integer or null>, "voice": "writer" | "source" | "both" | null}, ...}} with every statement id.
```

**The reply** (447 words)

````text
```json
{
  "readings": {
    "b0": {"conveys": null, "voice": null},
    "b1": {"conveys": 10, "voice": "writer"},
    "b2": {"conveys": null, "voice": null},
    "b3": {"conveys": null, "voice": null},
    "b4": {"conveys": null, "voice": null},
    "b5": {"conveys": null, "voice": null},
    "b6": {"conveys": null, "voice": null},
    "b7": {"conveys": null, "voice": null},
    "b8": {"conveys": null, "voice": null},
    "b9": {"conveys": null, "voice": null},
    "b10": {"conveys": 10, "voice": "source"},
    "b11": {"conveys": null, "voice": null},
    "b12": {"conveys": null, "voice": null},
    "b13": {"conveys": null, "voice": null},
    "b14": {"conveys": null, "voice": null},
    "b15": {"conveys": null, "voice": null},
    "b16": {"conveys": -10, "voice": "writer"},
    "b17": {"conveys": null, "voice": null},
    "b18": {"conveys": null, "voice": null},
    "b19": {"conveys": null, "voice": null},
    "b20": {"conveys": null, "voice": null},
    "b21": {"conveys": 10, "voice": "writer"},
    "b22": {"conveys": null, "voice": null},
    "b23": {"conveys": null, "voice": null},
    "b24": {"conveys": 10, "voice": "writer"},
    "b25": {"conveys": 10, "voice": "writer"},
    "b26": {"conveys": 10, "voice": "writer"},
    "b27": {"conveys": null, "voice": null},
    "b28": {"conveys": null, "voice": null},
    "b29": {"conveys": null, "voice": null},
    "b30": {"conveys": 10, "voice": "writer"},
    "b31": {"conveys": -10, "voice": "writer"},
    "b32": {"conveys": 10, "voice": "writer"},
    "b33": {"conveys": null, "voice": null},
    "b34": {"conveys": null, "voice": null},
    "b35": {"conveys": null, "voice": null},
    "b36": {"conveys": null, "voice": null},
    "b37": {"conveys": null, "voice": null},
    "b38": {"conveys": -10, "voice": "writer"},
    "b39": {"conveys": null, "voice": null},
    "b40": {"conveys": null, "voice": null},
    "b41": {"conveys": null, "voice": null},
    "b42": {"conveys": null, "voice": null},
    "b43": {"conveys": null, "voice": null},
    "b44": {"conveys": 10, "voice": "writer"},
    "b45": {"conveys": null, "voice": null},
    "b46": {"conveys": null, "voice": null},
    "b47": {"conveys": null, "voice": null},
    "b48": {"conveys": null, "voice": null},
    "b49": {"conveys": null, "voice": null},
    "b50": {"conveys": null, "voice": null},
    "b51": {"conveys": null, "voice": null},
    "b52": {"conveys": null, "voice": null},
    "b53": {"conveys": null, "voice": null},
    "b54": {"conveys": null, "voice": null},
    "b55": {"conveys": null, "voice": null},
    "b56": {"conveys": null, "voice": null},
    "b57": {"conveys": null, "voice": null},
    "b58": {"conveys": null, "voice": null},
    "b59": {"conveys": null, "voice": null},
    "b60": {"conveys": null, "voice": null},
    "b61": {"conveys": null, "voice": null},
    "b62": {"conveys": 10, "voice": "writer"},
    "b63": {"conveys": null, "voice": null},
    "b64": {"conveys": null, "voice": null},
    "b65": {"conveys": null, "voice": null},
    "b66": {"conveys": null, "voice": null},
    "b67": {"conveys": null, "voice": null},
    "b68": {"conveys": null, "voice": null},
    "b69": {"conveys": null, "voice": null},
    "b70": {"conveys": null, "voice": null},
    "b71": {"conveys": null, "voice": null},
    "b72": {"conveys": -10, "voice": "writer"},
    "b73": {"conveys": 10, "voice": "source"},
    "b74": {"conveys": 10, "voice": "writer"},
    "b75": {"conveys": null, "voice": null},
    "b76": {"conveys": 10, "voice": "writer"},
    "b77": {"conveys": 10, "voice": "writer"},
    "b78": {"conveys": null, "voice": null},
    "b79": {"conveys": null, "voice": null},
    "b80": {"conveys": null, "voice": null},
    "b81": {"conveys": null, "voice": null},
    "b82": {"conveys": null, "voice": null},
    "b83": {"conveys": null, "voice": null},
    "b84": {"conveys": null, "voice": null},
    "b85": {"conveys": -10, "voice": "writer"},
    "b86": {"conveys": -10, "voice": "source"},
    "b87": {"conveys": null, "voice": null}
  }
}
```
````

</details>
