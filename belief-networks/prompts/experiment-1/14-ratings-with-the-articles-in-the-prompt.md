# Experiment 1, step 14 of 18: Ratings with the articles in the prompt

Ratings and a network over the forty statements. Requests sent: 60. Models: Haiku 4.5. First and last request: 10 October 2026, 23:50 to 11 October 2026, 00:15 (Pacific time).

The request asks: “For each statement, say how strongly you agree or disagree with it, as an integer from -10 (completely disagree) to 10 (completely agree), where 0 means you neither agree nor disagree. If you cannot form a view on a statement, give null for it.”

## The template

`rate_after.txt`. The parts in braces are filled in for each request.

```text
{diet}Here are {n} statements.

{statements}

For each statement, say how strongly you agree or disagree with it, as an integer from -10 (completely disagree) to 10 (completely agree), where 0 means you neither agree nor disagree. If you cannot form a view on a statement, give null for it.

For each statement, also say whether most other people would agree with it: "yes", "no", or null if you cannot say.

Return JSON of the form {{"ratings": {{"b0": {{"stance": <integer or null>, "others_agree": "yes" | "no" | null}}, ...}}}} with every statement id.
```

## Requests as sent (2)

One request for each combination of article set, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Haiku 4.5 · Balanced set · 10 October 2026, 23:50</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (5852 words)

```text
Over the past days you have read these news articles, in this order.

[Article A1: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A2: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A3: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]
[Article A6: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]




Here are 80 statements.

b0  Science scores do not tend to be lower for students using AI almost daily than for non-users.
b1  Across the OECD, around a fifth of 15-year-old students do not rely on AI chatbots almost daily for schoolwork.
b2  When AI is relied on heavily, weaker readers can't detect its mistakes and so forgo skill-building opportunities, reinforcing the problem in a loop.
b3  American 15-year-olds' PISA reading results have dropped to levels close to 25-year lows.
b4  More than half of US K-12 teachers fear AI makes it more difficult for students to learn to think critically.
b5  Even when socioeconomic status is taken into account, students who use AI chatbots almost daily do not get lower science scores than those who do not use them.
b6  Chatbots are sometimes wrong in the information they provide.
b7  Instruction in responsible AI use belongs in schools' teaching for students.
b8  With AI's help, students with disabilities can complete work they could not complete otherwise.
b9  Science scores are higher among students with moderate AI use for schoolwork (about monthly to once or twice a week) than among rare or near-daily users.
b10  Singapore is not evidence that classrooms can combine technology with a focus on early reading comprehension.
b11  Science scores tend to be lower for students using AI almost daily than for non-users.
b12  Whether students learn depends more on how they use AI than on whether they use it.
b13  What is mainly dangerous about AI is who holds power over it, rather than the technology as such.
b14  Metacognitive laziness in students results from outsourcing thinking to AI.
b15  No loop forms from heavy AI reliance whereby weaker readers can't detect AI mistakes and so forgo skill-building opportunities.
b16  Most US K-12 teachers expect AI to change education more than the internet or computers did.
b17  Almost 33% of European 12-to-17-year-olds use AI to have study tasks fully solved.
b18  Around half of undergraduates in the UK do not believe AI has enhanced their experience as students.
b19  The fraction of 15-year-olds classed as hasty readers did not come close to doubling from 2018 to 2025.
b20  Digital distractions in class help drive down student performance.
b21  Adopting generative AI leads to higher homework scores for students.
b22  PISA scores from China came from only four rich jurisdictions on its eastern coast.
b23  Trust between teachers and students is not being undermined by AI use.
b24  The adoption of generative AI led to an increase of about 18% in homework scores among Chinese students.
b25  If all 15-year-olds in the US reached at least basic PISA proficiency, the US economy would gain over $40 trillion across their careers.
b26  In response to AI, teachers are changing graded work into in-class or handwritten tasks.
b27  Digital distractions in class do not help drive down student performance.
b28  The adoption of generative AI did not reduce Chinese students' per-assignment time by about 30%.
b29  Whether students use AI matters at least as much for learning as how they use it.
b30  Long before AI came along, students were already cheating on their assignments.
b31  Singapore is evidence that classrooms can combine technology with a focus on early reading comprehension.
b32  Metacognitive laziness in students is not a result of outsourcing thinking to AI.
b33  Most OECD students (86%) have not used AI chatbots for even one schoolwork purpose.
b34  The existence of AI has not made take-home essays an insufficient method of assessing students.
b35  Delegating tasks to unstructured generative AI does not result in better performance while lacking actual learning improvements.
b36  American 15-year-olds' PISA reading results have not dropped to levels close to 25-year lows.
b37  When tasks are delegated to unstructured generative AI, performance improves without actual learning improvements.
b38  China's PISA results are representative of the country as a whole.
b39  Across the OECD, around a fifth of 15-year-old students rely on AI chatbots almost daily for schoolwork.
b40  The adoption of generative AI reduced Chinese students' per-assignment time by about 30%.
b41  The only parts of China that took part in PISA were wealthy eastern provinces.
b42  Most US K-12 teachers do not expect AI to change education more than the internet or computers did.
b43  Wealth, national or familial, predicts student performance less than it used to as technology has progressed.
b44  The adoption of generative AI did not lead to an increase of about 18% in homework scores among Chinese students.
b45  Among students today, abilities such as critical thinking and information evaluation are eroding in the age of AI.
b46  Adopting generative AI does not lead to higher homework scores for students.
b47  AI does not make it possible for students with disabilities to complete work they could not complete otherwise.
b48  Even when socioeconomic status is taken into account, students who use AI chatbots almost daily get lower science scores than those who do not use them.
b49  Among students today, abilities such as critical thinking and information evaluation are not eroding in the age of AI.
b50  Compared with the global average, students in China, Japan and South Korea say they are much less digitally distracted in science lessons.
b51  AI alone does not account for falling student test scores.
b52  Chatbots do not ever give out incorrect information.
b53  AI is not the reason teachers are changing graded work into in-class or handwritten tasks.
b54  Teaching students responsible AI use is not something schools should do.
b55  There is no association between moderate AI use for schoolwork (about monthly to once or twice a week) and higher science scores compared with rare or near-daily use.
b56  Around half of undergraduates in the UK believe AI has enhanced their experience as students.
b57  At least one schoolwork use of AI chatbots has been reported by most OECD students, at 86%.
b58  Half or fewer of US K-12 teachers fear AI makes it more difficult for students to learn to think critically.
b59  Some parts of China that took part in PISA were not wealthy eastern provinces.
b60  Before AI existed, students were not cheating on assignments.
b61  It is not the case that the main danger of AI is the concentration of power rather than the technology itself.
b62  If all 15-year-olds in the US reached at least basic PISA proficiency, the US economy would gain no more than $40 trillion across their careers.
b63  Students not using AI chatbots for schoolwork typically do not outscore students who do.
b64  Compared with the global average, students in China, Japan and South Korea do not say they are much less digitally distracted in science lessons.
b65  Among European 12-to-17-year-olds, many use AI to get tasks solved completely.
b66  With AI available, essays completed outside the classroom can no longer adequately serve as a means of assessing students.
b67  Among European 12-to-17-year-olds, hardly any use AI to get tasks solved completely.
b68  China's PISA results fail to be representative of the country as a whole.
b69  For most teachers who use AI for work, the weekly time saved is two hours or under.
b70  The number of Chinese jurisdictions that submitted scores to PISA was not limited to four wealthy eastern coastal ones.
b71  Students not using AI chatbots for schoolwork typically outscore students who do.
b72  The share of European 12-to-17-year-olds using AI to have study tasks fully solved is not nearly a third.
b73  Half or fewer of the teachers who use AI for work save two hours or less per week.
b74  Trust between teachers and students is being undermined by AI use.
b75  Chinese students adopting generative AI did not experience a roughly 20% decline in closed-book monthly exam scores over six months.
b76  Wealth, national or familial, predicts student performance no less than it used to as technology has progressed.
b77  Chinese students adopting generative AI experienced a roughly 20% decline in closed-book monthly exam scores over six months.
b78  Declines in student test scores have no cause other than AI.
b79  The fraction of 15-year-olds classed as hasty readers came close to doubling from 2018 to 2025.


For each statement, say how strongly you agree or disagree with it, as an integer from -10 (completely disagree) to 10 (completely agree), where 0 means you neither agree nor disagree. If you cannot form a view on a statement, give null for it.

For each statement, also say whether most other people would agree with it: "yes", "no", or null if you cannot say.

Return JSON of the form {"ratings": {"b0": {"stance": <integer or null>, "others_agree": "yes" | "no" | null}, ...}} with every statement id.
```

**The reply** (407 words)

````text
```json
{
  "ratings": {
    "b0": {"stance": -10, "others_agree": "no"},
    "b1": {"stance": -10, "others_agree": "no"},
    "b2": {"stance": 10, "others_agree": "yes"},
    "b3": {"stance": 10, "others_agree": "yes"},
    "b4": {"stance": 10, "others_agree": "yes"},
    "b5": {"stance": -10, "others_agree": "no"},
    "b6": {"stance": 10, "others_agree": "yes"},
    "b7": {"stance": 10, "others_agree": "yes"},
    "b8": {"stance": 10, "others_agree": "yes"},
    "b9": {"stance": 10, "others_agree": "yes"},
    "b10": {"stance": -10, "others_agree": "no"},
    "b11": {"stance": 10, "others_agree": "yes"},
    "b12": {"stance": 10, "others_agree": "yes"},
    "b13": {"stance": 10, "others_agree": "yes"},
    "b14": {"stance": 10, "others_agree": "yes"},
    "b15": {"stance": -10, "others_agree": "no"},
    "b16": {"stance": 10, "others_agree": "yes"},
    "b17": {"stance": 10, "others_agree": "yes"},
    "b18": {"stance": 10, "others_agree": "yes"},
    "b19": {"stance": -10, "others_agree": "no"},
    "b20": {"stance": 10, "others_agree": "yes"},
    "b21": {"stance": 10, "others_agree": "yes"},
    "b22": {"stance": 10, "others_agree": "yes"},
    "b23": {"stance": -10, "others_agree": "no"},
    "b24": {"stance": 10, "others_agree": "yes"},
    "b25": {"stance": 10, "others_agree": "yes"},
    "b26": {"stance": 10, "others_agree": "yes"},
    "b27": {"stance": -10, "others_agree": "no"},
    "b28": {"stance": -10, "others_agree": "no"},
    "b29": {"stance": -10, "others_agree": "no"},
    "b30": {"stance": 10, "others_agree": "yes"},
    "b31": {"stance": 10, "others_agree": "yes"},
    "b32": {"stance": -10, "others_agree": "no"},
    "b33": {"stance": -10, "others_agree": "no"},
    "b34": {"stance": -10, "others_agree": "no"},
    "b35": {"stance": 10, "others_agree": "yes"},
    "b36": {"stance": -10, "others_agree": "no"},
    "b37": {"stance": 10, "others_agree": "yes"},
    "b38": {"stance": -10, "others_agree": "no"},
    "b39": {"stance": 10, "others_agree": "yes"},
    "b40": {"stance": 10, "others_agree": "yes"},
    "b41": {"stance": 10, "others_agree": "yes"},
    "b42": {"stance": -10, "others_agree": "no"},
    "b43": {"stance": 10, "others_agree": "yes"},
    "b44": {"stance": -10, "others_agree": "no"},
    "b45": {"stance": 10, "others_agree": "yes"},
    "b46": {"stance": -10, "others_agree": "no"},
    "b47": {"stance": -10, "others_agree": "no"},
    "b48": {"stance": 10, "others_agree": "yes"},
    "b49": {"stance": -10, "others_agree": "no"},
    "b50": {"stance": 10, "others_agree": "yes"},
    "b51": {"stance": 10, "others_agree": "yes"},
    "b52": {"stance": -10, "others_agree": "no"},
    "b53": {"stance": -10, "others_agree": "no"},
    "b54": {"stance": -10, "others_agree": "no"},
    "b55": {"stance": -10, "others_agree": "no"},
    "b56": {"stance": 10, "others_agree": "yes"},
    "b57": {"stance": 10, "others_agree": "yes"},
    "b58": {"stance": -10, "others_agree": "no"},
    "b59": {"stance": -10, "others_agree": "no"},
    "b60": {"stance": -10, "others_agree": "no"},
    "b61": {"stance": -10, "others_agree": "no"},
    "b62": {"stance": -10, "others_agree": "no"},
    "b63": {"stance": -10, "others_agree": "no"},
    "b64": {"stance": -10, "others_agree": "no"},
    "b65": {"stance": 10, "others_agree": "yes"},
    "b66": {"stance": 10, "others_agree": "yes"},
    "b67": {"stance": -10, "others_agree": "no"},
    "b68": {"stance": 10, "others_agree": "yes"},
    "b69": {"stance": 10, "others_agree": "yes"},
    "b70": {"stance": -10, "others_agree": "no"},
    "b71": {"stance": 10, "others_agree": "yes"},
    "b72": {"stance": -10, "others_agree": "no"},
    "b73": {"stance": -10, "others_agree": "no"},
    "b74": {"stance": 10, "others_agree": "yes"},
    "b75": {"stance": -10, "others_agree": "no"},
    "b76": {"stance": -10, "others_agree": "no"},
    "b77": {"stance": 10, "others_agree": "yes"},
    "b78": {"stance": -10, "others_agree": "no"},
    "b79": {"stance": 10, "others_agree": "yes"}
  }
}
```
````

</details>

<details><summary>Haiku 4.5 · Charged negative set · 11 October 2026, 00:15</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (5036 words)

```text
Over the past days you have read these news articles, in this order.

[Article A1: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A2: NBC News, 2026-09-17, “Poll: Most Americans think AI is doing more harm than good in schools”, 488 words. Text not included.]
[Article A3: CNN, 2026-09-02, “Nation’s largest school district bans AI in the classroom through 8th grade”, 541 words. Text not included.]
[Article A4: IBTimes UK, 2026-08-20, “Major Study Reveals 20% Exam Score Drop Among Students Who Relied on AI Tools”, 544 words. Text not included.]
[Article A5: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A6: South China Morning Post (republished by The Star), 2026-07-17, “AI homework tools cut exam scores by 20%, study of 26,000 Chinese students finds”, 717 words. Text not included.]




Here are 80 statements.

b0  The share of German undergraduates using AI is not 93% and is not near-universal.
b1  Chinese secondary students' homework scores did not rise by roughly 18 percent through their use of generative AI.
b2  Chinese secondary students' time per homework assignment did not fall from roughly 64 minutes to roughly 45 minutes as a result of generative AI use.
b3  Student performance suffers because of digital distraction in the classroom.
b4  Of all AI uses for school assignments, Americans do not most frequently deem proofreading and editing acceptable.
b5  Chinese students who used generative AI heavily scored about 18% lower on the gaokao university entrance exam as a result.
b6  For most UK undergraduates, using AI changes how lonely they feel.
b7  Among AI-using Chinese students, the exam declines were not ordered as biggest in social sciences, then STEM, then languages.
b8  Limiting AI in early education safeguards the relationships between teachers and students.
b9  Generative AI by its nature damages learning.
b10  Student AI use harms learning gradually, with the damage building up over time.
b11  AI-related learning declines affected boys more than girls because boys used AI more intensively.
b12  How students use generative AI does not determine its effect on learning.
b13  When tasks are handed off to AI, the productive cognitive effort that genuine learning depends on is diminished.
b14  Chinese secondary students' time per homework assignment fell from roughly 64 minutes to roughly 45 minutes because of generative AI use.
b15  Limiting AI in early education does not safeguard students' critical thinking.
b16  Chinese students who used generative AI heavily did not see their gaokao university entrance exam results fall by about 18%.
b17  The share of UK undergraduates who think AI has made their student experience better is not roughly 50%.
b18  Teachers and students notice AI's learning harm promptly, and the fluency of AI-completed work is not the reason for any delay.
b19  Short-term studies underestimate how much AI harms learning over the long term.
b20  Chinese students who used generative AI heavily scored about 24% lower on the zhongkao high school entrance exam as a result.
b21  Of all AI uses for school assignments, Americans most frequently deem proofreading and editing acceptable.
b22  Most American adults believe AI does more harm than good in K-12 education.
b23  Almost all German undergraduates, 93% of them, use AI.
b24  Almost all UK undergraduates, 94% of them, use AI.
b25  Because oversight is looser, younger secondary students suffer greater losses from AI use than older ones.
b26  Short-term studies do not underestimate how much AI harms learning over the long term.
b27  The share of UK undergraduates using AI is not 94% and is not near-universal.
b28  Among AI-using Chinese students, exam declines were biggest in social sciences, next biggest in STEM, and smallest in languages.
b29  Generative AI fails to boost task performance when no structure or instructional design is provided.
b30  Secondary students who are younger suffer greater losses from using AI than older secondary students do.
b31  Students at the top of the achievement distribution were not hurt more by AI use than lower-achieving students were.
b32  Older secondary students lose at least as much from AI use as younger ones.
b33  Generative AI only yields genuine learning gains when it is accompanied by structure and instructional design.
b34  The United States can avoid falling behind without teaching students about AI and giving them hands-on experience.
b35  It takes roughly two years for the learning harm from student AI use to become fully apparent.
b36  Chinese secondary students who adopted generative AI did not see their monthly closed-book exam scores drop roughly 20% compared with non-users within six months.
b37  New York City's prohibition on generative AI for pre-K through 8th grade students is not a moratorium lasting one year.
b38  AI use harmed boys more than it harmed girls.
b39  Undergraduates who used a chatbot to learn an unfamiliar topic performed better on tests.
b40  Chinese secondary students who adopted generative AI saw their monthly closed-book exam scores drop roughly 20% compared with non-users within six months.
b41  It is easy for schools to stop students from using AI at home to do their homework.
b42  Chinese secondary students' homework scores rose by roughly 18 percent through their use of generative AI.
b43  How students use generative AI determines its effect on learning.
b44  The tech industry is mistaken to claim that AI in early education is inevitable and necessary.
b45  Undergraduates who used a chatbot to learn an unfamiliar topic did not perform better on tests.
b46  Roughly four in five students in the Chinese study said they used generative AI.
b47  For the United States not to fall behind, students need to be taught about AI and given hands-on experience with it.
b48  Because AI-completed work feels fluent and productive, teachers and students take a long time to recognize AI's harm to learning.
b49  AI use did not harm boys more than it harmed girls.
b50  The share of students in the Chinese study who reported using generative AI was not about 80%.
b51  Students at the top of the achievement distribution were hurt more by AI use than lower-achieving students were.
b52  Americans adults who think AI does more harm than good in K-12 education, at about 53 percent, do not form a majority.
b53  Handing tasks off to AI leaves intact the productive cognitive effort that genuine learning depends on.
b54  A week later, learners who had used a chatbot to study an unfamiliar topic no longer held their advantage.
b55  Only a small number of Americans consider it acceptable for students to have AI write and generate their schoolwork.
b56  Chinese students who used generative AI heavily did not see their zhongkao high school entrance exam results fall by about 24%.
b57  Generative AI does not by its nature damage learning.
b58  It is hard for schools to stop students from using AI at home to do their homework.
b59  Limiting AI in early education does not safeguard the relationships between teachers and students.
b60  Exam performance suffers little or not at all for students who use AI as a tutor and spend roughly as much time on homework as non-users.
b61  Student AI use harms learning quickly rather than gradually, or the damage does not build up slowly.
b62  The Los Angeles Unified School District is limiting students' access to generative AI platforms.
b63  It does not take roughly two years for the learning harm from student AI use to become fully apparent.
b64  Generative AI boosts task performance even when no structure or instructional design is provided.
b65  New York City's prohibition on generative AI for pre-K through 8th grade students is a moratorium lasting one year.
b66  Roughly 50% of undergraduates in the UK think AI has made their student experience better.
b67  Looser oversight does not cause younger secondary students to lose more from AI use than older ones.
b68  A substantial number of Americans think it is acceptable for students to have AI write and generate their schoolwork.
b69  The Los Angeles Unified School District is not limiting students' access to generative AI platforms.
b70  Generative AI can deliver real learning gains even when it lacks structure and instructional design.
b71  Exam performance suffers substantially for students who use AI as a tutor and spend roughly as much time on homework as non-users.
b72  About 53 percent of American adults, a majority, believe AI causes more harm than benefit in K-12 education.
b73  Student performance does not suffer because of digital distraction in the classroom.
b74  For most UK undergraduates, using AI does not change how lonely they feel.
b75  The tech industry is right to claim that AI in early education is inevitable and necessary.
b76  AI-related learning declines did not affect boys more than girls because of more intensive AI use.
b77  A week later, learners who had used a chatbot to study an unfamiliar topic still held their advantage.
b78  Half or fewer of American adults think AI does more harm than good in K-12 education.
b79  Limiting AI in early education safeguards students' critical thinking.


For each statement, say how strongly you agree or disagree with it, as an integer from -10 (completely disagree) to 10 (completely agree), where 0 means you neither agree nor disagree. If you cannot form a view on a statement, give null for it.

For each statement, also say whether most other people would agree with it: "yes", "no", or null if you cannot say.

Return JSON of the form {"ratings": {"b0": {"stance": <integer or null>, "others_agree": "yes" | "no" | null}, ...}} with every statement id.
```

**The reply** (407 words)

````text
```json
{
  "ratings": {
    "b0": {"stance": 10, "others_agree": "no"},
    "b1": {"stance": -10, "others_agree": "no"},
    "b2": {"stance": -10, "others_agree": "no"},
    "b3": {"stance": -8, "others_agree": "no"},
    "b4": {"stance": -10, "others_agree": "no"},
    "b5": {"stance": 9, "others_agree": "yes"},
    "b6": {"stance": -10, "others_agree": "no"},
    "b7": {"stance": -10, "others_agree": "no"},
    "b8": {"stance": 8, "others_agree": "yes"},
    "b9": {"stance": -9, "others_agree": "no"},
    "b10": {"stance": 10, "others_agree": "yes"},
    "b11": {"stance": 9, "others_agree": "yes"},
    "b12": {"stance": -10, "others_agree": "no"},
    "b13": {"stance": 10, "others_agree": "yes"},
    "b14": {"stance": 10, "others_agree": "yes"},
    "b15": {"stance": -10, "others_agree": "no"},
    "b16": {"stance": -10, "others_agree": "no"},
    "b17": {"stance": -10, "others_agree": "no"},
    "b18": {"stance": -10, "others_agree": "no"},
    "b19": {"stance": 10, "others_agree": "yes"},
    "b20": {"stance": 10, "others_agree": "yes"},
    "b21": {"stance": 10, "others_agree": "yes"},
    "b22": {"stance": 9, "others_agree": "yes"},
    "b23": {"stance": 10, "others_agree": "yes"},
    "b24": {"stance": 10, "others_agree": "yes"},
    "b25": {"stance": 10, "others_agree": "yes"},
    "b26": {"stance": -10, "others_agree": "no"},
    "b27": {"stance": -10, "others_agree": "no"},
    "b28": {"stance": 10, "others_agree": "yes"},
    "b29": {"stance": 10, "others_agree": "yes"},
    "b30": {"stance": 10, "others_agree": "yes"},
    "b31": {"stance": -10, "others_agree": "no"},
    "b32": {"stance": -9, "others_agree": "no"},
    "b33": {"stance": 9, "others_agree": "yes"},
    "b34": {"stance": -9, "others_agree": "no"},
    "b35": {"stance": 10, "others_agree": "yes"},
    "b36": {"stance": -10, "others_agree": "no"},
    "b37": {"stance": -10, "others_agree": "no"},
    "b38": {"stance": 10, "others_agree": "yes"},
    "b39": {"stance": 9, "others_agree": "yes"},
    "b40": {"stance": 10, "others_agree": "yes"},
    "b41": {"stance": -10, "others_agree": "no"},
    "b42": {"stance": 10, "others_agree": "yes"},
    "b43": {"stance": 10, "others_agree": "yes"},
    "b44": {"stance": 8, "others_agree": "yes"},
    "b45": {"stance": -10, "others_agree": "no"},
    "b46": {"stance": 10, "others_agree": "yes"},
    "b47": {"stance": 8, "others_agree": "yes"},
    "b48": {"stance": 10, "others_agree": "yes"},
    "b49": {"stance": -10, "others_agree": "no"},
    "b50": {"stance": -10, "others_agree": "no"},
    "b51": {"stance": 10, "others_agree": "yes"},
    "b52": {"stance": -10, "others_agree": "no"},
    "b53": {"stance": -10, "others_agree": "no"},
    "b54": {"stance": -10, "others_agree": "no"},
    "b55": {"stance": 10, "others_agree": "yes"},
    "b56": {"stance": -10, "others_agree": "no"},
    "b57": {"stance": -9, "others_agree": "no"},
    "b58": {"stance": 10, "others_agree": "yes"},
    "b59": {"stance": -10, "others_agree": "no"},
    "b60": {"stance": 10, "others_agree": "yes"},
    "b61": {"stance": -10, "others_agree": "no"},
    "b62": {"stance": 9, "others_agree": "yes"},
    "b63": {"stance": -10, "others_agree": "no"},
    "b64": {"stance": -10, "others_agree": "no"},
    "b65": {"stance": 10, "others_agree": "yes"},
    "b66": {"stance": 9, "others_agree": "yes"},
    "b67": {"stance": -10, "others_agree": "no"},
    "b68": {"stance": -10, "others_agree": "no"},
    "b69": {"stance": -10, "others_agree": "no"},
    "b70": {"stance": -8, "others_agree": "no"},
    "b71": {"stance": -10, "others_agree": "no"},
    "b72": {"stance": 10, "others_agree": "yes"},
    "b73": {"stance": -10, "others_agree": "no"},
    "b74": {"stance": 10, "others_agree": "yes"},
    "b75": {"stance": -8, "others_agree": "no"},
    "b76": {"stance": -10, "others_agree": "no"},
    "b77": {"stance": 9, "others_agree": "yes"},
    "b78": {"stance": -10, "others_agree": "no"},
    "b79": {"stance": 9, "others_agree": "yes"}
  }
}
```
````

</details>
