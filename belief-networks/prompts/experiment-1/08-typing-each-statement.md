# Experiment 1, step 8 of 18: Typing each statement

Writing and preparing the statements. Requests sent: 6. Models: Sonnet 5.5, Opus 5.5. First and last request: 10 October 2026, 23:36 to 11 October 2026, 00:06 (Pacific time).

The request asks: “For each statement, give two labels.”

## The template

`type_statements.txt`. The parts in braces are filled in for each request.

```text
Here are {n} statements.

{statements}

For each statement, give two labels.

"about": what the statement is about.
- "world": the world itself (events, quantities, causes, rules, what should be done).
- "text": an article as a piece of writing (its tone, emphasis, headline, what it includes or omits).
- "entity": how an article represents a person, group or institution.
- "between": how two or more articles relate to each other.

"content": what kind of claim it is.
- "event_state": factual; that something happened or is the case.
- "quantity": factual; a number, share, size or change in amount.
- "rule_status": factual; a law, policy, rule, official decision or formal status.
- "characterising": interpretive; describes the nature or character of something in terms that involve judgement.
- "causal": interpretive; that one thing causes, affects or explains another.
- "predictive": interpretive; what will or is likely to happen.
- "moral": evaluative; that something is good, bad, right, wrong, fair or unfair.
- "prescriptive": evaluative; what should or should not be done.
A factual claim can in principle be settled by evidence; an interpretive claim needs judgement beyond the evidence; an evaluative claim depends on values. Choose the single label that fits the main claim. Judge only the kind of claim, not whether it is true.

Return JSON of the form {{"labels": {{"b0": {{"about": "...", "content": "..."}}, ...}}}} with every statement id.
```

## Requests as sent (2)

One request for each combination of model, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Sonnet 5.5 · Both sets · 10 October 2026, 23:36</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1144 words)

```text
Here are 57 statements.

b0  Allison Stanger is a political science professor at Middlebury College.
b1  Allison Stanger uses AI to help her write.
b2  Allison Stanger argues that AI used well can strengthen thinking.
b3  Stanger says she always writes her own first drafts before involving AI.
b4  Stanger says she outlines her own argument before involving AI.
b5  Stanger says humans are best at judging what good writing is.
b6  Stanger says AI cannot replace showing writing to another human.
b7  Stanger says the main danger of AI lies in the concentration of power rather than in the technology itself.
b8  Stanger says AI is potentially very dangerous.
b9  Stanger says people must keep thinking for themselves and teach students to do so.
b10  Reading, science and math performance among 15-year-olds declined globally in the 2025 PISA.
b11  Students in Beijing, Shanghai, Jiangsu, Zhejiang and Singapore were among the top performers in the 2025 PISA.
b12  Japan, South Korea, Macao and Taiwan were also in the top 10 across all three PISA subjects.
b13  US secondary students' reading scores in PISA fell close to 25-year lows.
b14  China's PISA data is criticised.
b15  Only four wealthy eastern coastal provinces and cities submitted scores for China's PISA data.
b16  China has surpassed the US in published scientific reports.
b17  China has surpassed the US in research spending.
b18  Andreas Schleicher says the most troubling trend is the decline in skills for evaluating information, connecting multiple sources and thinking critically about reading.
b19  The proportion of 'hasty readers' who rush through texts and answer incorrectly nearly doubled between 2018 and 2025.
b20  Fewer than 10% of students in China, Japan and South Korea reported peers being distracted by digital devices in science lessons.
b21  The global average of students reporting peers being distracted by digital devices in science lessons was 28%.
b22  The share of OECD students below baseline PISA performance rose to 20% in 2025 from 16% in 2022.
b23  A Stanford study cited in the PISA report estimates that basic aptitude for all 15-year-old Americans could add over $40 trillion to the US economy over their working lives.
b24  Singapore uses technology in classrooms.
b25  Singapore emphasizes reading comprehension early on.
b26  PISA found that students using AI moderately (about monthly to once or twice weekly) had higher average science scores than rare users.
b27  PISA found that students using AI moderately (about monthly to once or twice weekly) had higher average science scores than near-daily users.
b28  Students who used AI weekly to summarize reading or research performed about the same as AI nonusers after accounting for socioeconomic status.
b29  The OECD says the relationship between AI use and science performance may reflect who adopts AI and how, rather than a negative impact of AI.
b30  86% of students across OECD countries used AI chatbots for at least one schoolwork purpose.
b31  Students who do not use AI chatbots for schoolwork generally score higher than those who do.
b32  About one in five students use AI almost every day.
b33  Students who use AI almost every day tend to score lower in science than non-users, accounting for socioeconomic status.
b34  Reading, mathematics and science scores have dropped since 2003.
b35  Lower scores are not all due to AI.
b36  Weaker critical reading ability makes it harder for students to recognize incomplete or incorrect AI answers.
b37  Heavy reliance on AI reduces chances to develop critical reading skills.
b38  Nearly three in four K-12 teachers believe AI has bigger implications for education than the internet or computers.
b39  Nearly 8 in 10 polled teachers think schools should teach responsible use of AI.
b40  Six in 10 polled teachers have used AI themselves for work tasks.
b41  54% of polled teachers say AI makes it harder for students to learn critical thinking skills.
b42  55% of polled teachers think AI is mostly a shortcut for students to avoid work.
b43  Nearly 6 in 10 teachers say AI is eroding trust between students and teachers.
b44  About 4 in 10 teachers have required more assignments to be done by hand or in class because of AI.
b45  Among teachers using AI for work, 63% say it saves them two hours or less per week.
b46  About half of polled teachers say their school has offered no AI guidance or they are unsure what it is.
b47  Only about 4 in 10 polled teachers say their school offers AI training.
b48  Special education teacher Ellie Rodriguez says AI can help students with disabilities complete assignments they otherwise could not.
b49  A study of about 27,000 students in China found homework scores rose 18% after adopting generative AI.
b50  The study of about 27,000 students in China found time per assignment fell about 30% after adopting generative AI.
b51  The same students' scores on monthly closed-book exams without AI fell 20% within six months of adopting generative AI.
b52  The OECD's Digital Education Outlook 2026 found that where generative AI is neither built to teach nor used under structure, outsourcing tasks improves performance without real learning gains.
b53  In a survey of 7,000 European students aged 12–17, 31% said they use AI to provide complete solutions to tasks.
b54  In the HEPI/Kortext survey, 49% of UK undergraduates believe AI has improved their student experience.
b55  Georgia Tech professors are building AI tutor agents in response to AI.
b56  Georgia Tech professors are replacing long essays with in-class discussion in response to AI.


For each statement, give two labels.

"about": what the statement is about.
- "world": the world itself (events, quantities, causes, rules, what should be done).
- "text": an article as a piece of writing (its tone, emphasis, headline, what it includes or omits).
- "entity": how an article represents a person, group or institution.
- "between": how two or more articles relate to each other.

"content": what kind of claim it is.
- "event_state": factual; that something happened or is the case.
- "quantity": factual; a number, share, size or change in amount.
- "rule_status": factual; a law, policy, rule, official decision or formal status.
- "characterising": interpretive; describes the nature or character of something in terms that involve judgement.
- "causal": interpretive; that one thing causes, affects or explains another.
- "predictive": interpretive; what will or is likely to happen.
- "moral": evaluative; that something is good, bad, right, wrong, fair or unfair.
- "prescriptive": evaluative; what should or should not be done.
A factual claim can in principle be settled by evidence; an interpretive claim needs judgement beyond the evidence; an evaluative claim depends on values. Choose the single label that fits the main claim. Judge only the kind of claim, not whether it is true.

Return JSON of the form {"labels": {"b0": {"about": "...", "content": "..."}, ...}} with every statement id.
```

**The reply** (1 words)

```text
{"labels":{"b0":{"about":"entity","content":"event_state"},"b1":{"about":"entity","content":"event_state"},"b2":{"about":"entity","content":"causal"},"b3":{"about":"entity","content":"event_state"},"b4":{"about":"entity","content":"event_state"},"b5":{"about":"entity","content":"characterising"},"b6":{"about":"entity","content":"causal"},"b7":{"about":"entity","content":"causal"},"b8":{"about":"entity","content":"characterising"},"b9":{"about":"entity","content":"prescriptive"},"b10":{"about":"world","content":"event_state"},"b11":{"about":"world","content":"event_state"},"b12":{"about":"world","content":"event_state"},"b13":{"about":"world","content":"quantity"},"b14":{"about":"world","content":"event_state"},"b15":{"about":"world","content":"event_state"},"b16":{"about":"world","content":"quantity"},"b17":{"about":"world","content":"quantity"},"b18":{"about":"entity","content":"characterising"},"b19":{"about":"world","content":"quantity"},"b20":{"about":"world","content":"quantity"},"b21":{"about":"world","content":"quantity"},"b22":{"about":"world","content":"quantity"},"b23":{"about":"world","content":"quantity"},"b24":{"about":"world","content":"event_state"},"b25":{"about":"world","content":"event_state"},"b26":{"about":"world","content":"event_state"},"b27":{"about":"world","content":"event_state"},"b28":{"about":"world","content":"event_state"},"b29":{"about":"entity","content":"causal"},"b30":{"about":"world","content":"quantity"},"b31":{"about":"world","content":"event_state"},"b32":{"about":"world","content":"quantity"},"b33":{"about":"world","content":"event_state"},"b34":{"about":"world","content":"event_state"},"b35":{"about":"world","content":"causal"},"b36":{"about":"world","content":"causal"},"b37":{"about":"world","content":"causal"},"b38":{"about":"world","content":"quantity"},"b39":{"about":"world","content":"quantity"},"b40":{"about":"world","content":"quantity"},"b41":{"about":"world","content":"quantity"},"b42":{"about":"world","content":"quantity"},"b43":{"about":"world","content":"quantity"},"b44":{"about":"world","content":"quantity"},"b45":{"about":"world","content":"quantity"},"b46":{"about":"world","content":"quantity"},"b47":{"about":"world","content":"quantity"},"b48":{"about":"entity","content":"causal"},"b49":{"about":"world","content":"quantity"},"b50":{"about":"world","content":"quantity"},"b51":{"about":"world","content":"quantity"},"b52":{"about":"entity","content":"causal"},"b53":{"about":"world","content":"quantity"},"b54":{"about":"world","content":"quantity"},"b55":{"about":"world","content":"event_state"},"b56":{"about":"world","content":"event_state"}}}
```

</details>

<details><summary>Opus 5.5 · Both sets · 10 October 2026, 23:42</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (2834 words)

```text
Here are 176 statements.

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
b40  Schools should not teach students the responsible use of AI.
b41  The share of hasty readers among 15-year-olds did not almost double between 2018 and 2025.
b42  AI use is not eroding trust between students and teachers.
b43  AI is the only cause of declines in student test scores.
b44  How students use AI does not matter more for learning than whether they use it.
b45  Chinese PISA results are representative of the whole country.
b46  US 15-year-olds' reading scores on PISA have not fallen to close to 25-year lows.
b47  AI cannot help students with disabilities complete assignments they otherwise could not.
b48  Chinese students who adopted generative AI did not see their closed-book monthly exam scores fall by about 20% within six months.
b49  A majority of US K-12 teachers do not worry that AI makes it harder for students to learn to think critically.
b50  Students who do not use AI chatbots for schoolwork do not generally score higher than students who do.
b51  Student performance has not become less linked to national or family wealth as technology has progressed.
b52  Most US K-12 teachers do not believe AI will affect education more than the internet or computers did.
b53  It is not the case that most teachers who use AI for work save only two hours or less per week.
b54  Students did not cheat on assignments long before AI existed.
b55  Outsourcing thinking to AI does not produce metacognitive laziness in students.
b56  Singapore does not show that classrooms can use technology while still emphasizing early reading comprehension.
b57  Heavy reliance on AI does not create a feedback loop in which weaker readers cannot spot AI errors and lose chances to build skills.
b58  Generative AI adoption did not raise Chinese students' homework scores by about 18%.
b59  Generative AI adoption did not cut Chinese students' time per assignment by about 30%.
b60  Teachers are not shifting graded work to in-class or handwritten formats because of AI.
b61  Skills such as evaluating information and thinking critically are not declining among students in the AI age.
b62  Digital distraction in the classroom does not contribute to declining student performance.
b63  It is not the case that only wealthy eastern provinces of China participated in PISA.
b64  Raising all American 15-year-olds to at least basic PISA proficiency would not add over $40 trillion to the US economy over their working lives.
b65  It is not the case that most OECD students (86%) have used AI chatbots for at least one schoolwork purpose.
b66  Moderate AI use for schoolwork, from about monthly to once or twice a week, is not associated with higher science scores than rare or near-daily use.
b67  Students who use AI almost every day do not tend to score lower in science than non-users.
b68  Chatbots never produce wrong information.
b69  Students who use AI chatbots almost every day do not score lower in science than students who do not, after accounting for socioeconomic status.
b70  Generative AI adoption does not raise students' homework scores.
b71  Few European students aged 12 to 17 use AI to obtain complete solutions to tasks.
b72  The main danger of AI does not lie in the concentration of power rather than in the technology itself.
b73  More than four wealthy eastern coastal jurisdictions of China submitted scores to PISA.
b74  Students in China, Japan and South Korea do not report far less digital distraction in science lessons than the global average.
b75  Fewer than a third of European students aged 12 to 17 use AI to get complete solutions to study tasks.
b76  Far from half of UK undergraduates believe AI has improved their student experience.
b77  Far from one in five 15-year-old students across OECD countries use AI chatbots almost every day for schoolwork.
b78  Outsourcing tasks to unstructured generative AI does not improve performance without real learning gains.
b79  Take-home essay assignments are still a sufficient way to assess students even though AI exists.
b80  Allison Stanger is a political science professor at Middlebury College.
b81  Allison Stanger uses AI to help her write.
b82  Stanger says she always writes her own first drafts before involving AI.
b83  Stanger says she outlines her own argument before involving AI.
b84  Reading, science and math performance among 15-year-olds declined globally in the 2025 PISA.
b85  Students in Beijing, Shanghai, Jiangsu, Zhejiang and Singapore were among the top performers in the 2025 PISA.
b86  Japan, South Korea, Macao and Taiwan were also in the top 10 across all three PISA subjects.
b87  US secondary students' reading scores in PISA fell close to 25-year lows.
b88  China's PISA data is criticised.
b89  Only four wealthy eastern coastal provinces and cities submitted scores for China's PISA data.
b90  China has surpassed the US in published scientific reports.
b91  China has surpassed the US in research spending.
b92  Allison Stanger is not a political science professor at Middlebury College.
b93  Allison Stanger does not use AI to help her write.
b94  Stanger does not say she always writes her own first drafts before involving AI.
b95  Stanger does not say she outlines her own argument before involving AI.
b96  Reading, science and math performance among 15-year-olds did not decline globally in the 2025 PISA.
b97  Students in Beijing, Shanghai, Jiangsu, Zhejiang and Singapore were not among the top performers in the 2025 PISA.
b98  Japan, South Korea, Macao and Taiwan were not also in the top 10 across all three PISA subjects.
b99  US secondary students' reading scores in PISA did not fall close to 25-year lows.
b100  China's PISA data is not criticised.
b101  More than four wealthy eastern coastal provinces and cities submitted scores for China's PISA data.
b102  China has not surpassed the US in published scientific reports.
b103  China has not surpassed the US in research spending.
b104  Article A2 gives named individual teachers extended space to voice their experiences and concerns about AI.
b105  Article A4 is written as an interview in which the professor's views are presented with little challenge from the interviewer.
b106  Article A1 presents AI almost entirely as an opportunity for Georgia Tech.
b107  Article A1 does not mention concerns about student learning.
b108  Article A3 uses a headline that contrasts faster homework with poor exam results.
b109  Article A3's headline matches the study findings reported in its body.
b110  Article A6 has a headline that says moderate users perform similarly to nonusers.
b111  Article A6's headline presents a more positive finding than much of its body, which stresses lower scores among heavy users.
b112  Article A5 treats AI as a secondary theme within a story mainly about Asian students outperforming US students.
b113  Article A1 portrays Georgia Tech professors as adapting proactively to AI by building tutors.
b114  Article A1 portrays Georgia Tech professors as adapting proactively to AI by redesigning assignments.
b115  Article A4 portrays Allison Stanger as a thoughtful user of AI who keeps her own ideas and drafts.
b116  Article A4 portrays Allison Stanger as acknowledging AI's dangers.
b117  Article A2 portrays schools and districts as failing to give teachers adequate AI guidance.
b118  Article A2 portrays schools and districts as failing to give teachers adequate AI training.
b119  Article A5 qualifies the credibility of China's PISA results.
b120  Article A5 notes that only four wealthy coastal jurisdictions submitted data for China's PISA results.
b121  Article A5 quotes a passage from OECD official Andreas Schleicher about the decline in critical-thinking skills.
b122  Article A6 quotes the same passage from OECD official Andreas Schleicher about the decline in critical-thinking skills.
b123  Article A4 is more enthusiastic about AI's benefits for thinking than Article A2.
b124  Article A2 gives more weight to teachers' worries about critical thinking than Article A4.
b125  Article A2 gives most of its space to quotations from individual classroom teachers.
b126  Article A5 is written as an interview in which the professor's views are presented with little challenge.
b127  Article A5 contains one question about creativity that challenges the professor's views.
b128  The headline of Article A4 suggests a more positive finding than the opening sentences of the body of Article A4.
b129  The opening sentences of the body of Article A4 lead with declining scores.
b130  Article A6 is framed mainly around a US–China rivalry.
b131  AI is a secondary theme in Article A6.
b132  Article A1 relies on a single university official as its only named source.
b133  Article A1 presents Georgia Tech and its faculty as adapting constructively to AI.
b134  Article A5 portrays Allison Stanger as an enthusiastic user of AI.
b135  Article A5 portrays Allison Stanger as self-aware in her use of AI.
b136  Article A5 portrays Allison Stanger as keeping control of her own writing.
b137  Article A2 portrays teachers as under-supported.
b138  Article A2 portrays schools as giving teachers little guidance or training on AI.
b139  Article A6 notes criticism of China's PISA data.
b140  The criticism noted in Article A6 is that only wealthy coastal regions were tested.
b141  Article A3 cites OECD research in support of the point that how students use AI matters.
b142  Article A4 cites OECD research in support of the point that how students use AI matters.
b143  Article A4 quotes the PISA report's statement about the decline in skills such as evaluating information and thinking critically.
b144  Article A6 quotes the PISA report's statement about the decline in skills such as evaluating information and thinking critically.
b145  Article A1 describes teachers moving assessment away from take-home work toward in-class work.
b146  Article A2 describes teachers moving assessment away from take-home work toward in-class work.
b147  Article A2 reports survey figures on teachers moving assessment away from take-home work toward in-class work.
b148  Article A1 does not report survey figures on teachers moving assessment away from take-home work toward in-class work.
b149  Article A1 gives most of its space to the views of individual K-12 teachers, quoted by name and school.
b150  Article A1 gives space to poll figures alongside the views of individual K-12 teachers.
b151  Article A2 opens with a framing of Asia versus the US as a competition.
b152  Article A2 ties the test results to a technological rivalry between the US and China.
b153  Article A4 is very short.
b154  Article A4 rests almost entirely on quotes from a single university administrator, David Joyner.
b155  Article A5's headline highlights a Goldilocks effect for moderate AI use.
b156  Article A5's body says students who do not use AI chatbots generally score higher than those who do.
b157  Article A6 is a transcript of a radio interview.
b158  In Article A6, the host's questions are mostly open-ended prompts.
b159  In Article A6, the guest's answers are largely favourable to AI.
b160  Article A2 presents the Chinese PISA data as open to criticism.
b161  Article A2 notes that only four wealthy coastal jurisdictions submitted scores.
b162  Article A6 presents Allison Stanger as a credible, thoughtful AI user.
b163  Article A6 lets Allison Stanger describe AI as miraculous.
b164  Article A6 lets Allison Stanger acknowledge the dangers of AI.
b165  Article A1 portrays teachers as under-supported.
b166  Article A1 quotes teachers as lacking training from their schools and districts.
b167  Article A1 quotes teachers as lacking guidance from their schools and districts.
b168  Article A4 portrays Georgia Tech professors as adapting proactively to AI.
b169  Article A4 portrays Georgia Tech professors as building tutor agents.
b170  Article A4 portrays Georgia Tech professors as replacing essays with class discussion.
b171  Articles A2 and A5 both quote the same passage from the OECD's Andreas Schleicher about the decline in skills for evaluating information.
b172  Article A3 reports that heavy or unstructured AI use is linked to weaker learning outcomes.
b173  Article A5 reports that heavy or unstructured AI use is linked to weaker learning outcomes.
b174  Article A1 relies on teacher survey data.
b175  Article A3 relies on a tracking study of student exam performance in China.


For each statement, give two labels.

"about": what the statement is about.
- "world": the world itself (events, quantities, causes, rules, what should be done).
- "text": an article as a piece of writing (its tone, emphasis, headline, what it includes or omits).
- "entity": how an article represents a person, group or institution.
- "between": how two or more articles relate to each other.

"content": what kind of claim it is.
- "event_state": factual; that something happened or is the case.
- "quantity": factual; a number, share, size or change in amount.
- "rule_status": factual; a law, policy, rule, official decision or formal status.
- "characterising": interpretive; describes the nature or character of something in terms that involve judgement.
- "causal": interpretive; that one thing causes, affects or explains another.
- "predictive": interpretive; what will or is likely to happen.
- "moral": evaluative; that something is good, bad, right, wrong, fair or unfair.
- "prescriptive": evaluative; what should or should not be done.
A factual claim can in principle be settled by evidence; an interpretive claim needs judgement beyond the evidence; an evaluative claim depends on values. Choose the single label that fits the main claim. Judge only the kind of claim, not whether it is true.

Return JSON of the form {"labels": {"b0": {"about": "...", "content": "..."}, ...}} with every statement id.
```

**The reply** (1 words)

```text
{"labels":{"b0":{"about":"world","content":"prescriptive"},"b1":{"about":"world","content":"quantity"},"b2":{"about":"world","content":"causal"},"b3":{"about":"world","content":"causal"},"b4":{"about":"world","content":"causal"},"b5":{"about":"world","content":"characterising"},"b6":{"about":"world","content":"quantity"},"b7":{"about":"world","content":"causal"},"b8":{"about":"world","content":"quantity"},"b9":{"about":"world","content":"quantity"},"b10":{"about":"world","content":"quantity"},"b11":{"about":"world","content":"event_state"},"b12":{"about":"world","content":"quantity"},"b13":{"about":"world","content":"quantity"},"b14":{"about":"world","content":"event_state"},"b15":{"about":"world","content":"causal"},"b16":{"about":"world","content":"characterising"},"b17":{"about":"world","content":"causal"},"b18":{"about":"world","content":"quantity"},"b19":{"about":"world","content":"quantity"},"b20":{"about":"world","content":"event_state"},"b21":{"about":"world","content":"event_state"},"b22":{"about":"world","content":"causal"},"b23":{"about":"world","content":"event_state"},"b24":{"about":"world","content":"predictive"},"b25":{"about":"world","content":"quantity"},"b26":{"about":"world","content":"quantity"},"b27":{"about":"world","content":"quantity"},"b28":{"about":"world","content":"event_state"},"b29":{"about":"world","content":"quantity"},"b30":{"about":"world","content":"causal"},"b31":{"about":"world","content":"quantity"},"b32":{"about":"world","content":"characterising"},"b33":{"about":"world","content":"quantity"},"b34":{"about":"world","content":"quantity"},"b35":{"about":"world","content":"quantity"},"b36":{"about":"world","content":"quantity"},"b37":{"about":"world","content":"quantity"},"b38":{"about":"world","content":"causal"},"b39":{"about":"world","content":"characterising"},"b40":{"about":"world","content":"prescriptive"},"b41":{"about":"world","content":"quantity"},"b42":{"about":"world","content":"causal"},"b43":{"about":"world","content":"causal"},"b44":{"about":"world","content":"causal"},"b45":{"about":"world","content":"characterising"},"b46":{"about":"world","content":"quantity"},"b47":{"about":"world","content":"causal"},"b48":{"about":"world","content":"quantity"},"b49":{"about":"world","content":"quantity"},"b50":{"about":"world","content":"quantity"},"b51":{"about":"world","content":"event_state"},"b52":{"about":"world","content":"quantity"},"b53":{"about":"world","content":"quantity"},"b54":{"about":"world","content":"event_state"},"b55":{"about":"world","content":"causal"},"b56":{"about":"world","content":"characterising"},"b57":{"about":"world","content":"causal"},"b58":{"about":"world","content":"quantity"},"b59":{"about":"world","content":"quantity"},"b60":{"about":"world","content":"event_state"},"b61":{"about":"world","content":"event_state"},"b62":{"about":"world","content":"causal"},"b63":{"about":"world","content":"event_state"},"b64":{"about":"world","content":"predictive"},"b65":{"about":"world","content":"quantity"},"b66":{"about":"world","content":"quantity"},"b67":{"about":"world","content":"quantity"},"b68":{"about":"world","content":"event_state"},"b69":{"about":"world","content":"quantity"},"b70":{"about":"world","content":"causal"},"b71":{"about":"world","content":"quantity"},"b72":{"about":"world","content":"characterising"},"b73":{"about":"world","content":"quantity"},"b74":{"about":"world","content":"quantity"},"b75":{"about":"world","content":"quantity"},"b76":{"about":"world","content":"quantity"},"b77":{"about":"world","content":"quantity"},"b78":{"about":"world","content":"causal"},"b79":{"about":"world","content":"characterising"},"b80":{"about":"world","content":"event_state"},"b81":{"about":"world","content":"event_state"},"b82":{"about":"world","content":"event_state"},"b83":{"about":"world","content":"event_state"},"b84":{"about":"world","content":"quantity"},"b85":{"about":"world","content":"event_state"},"b86":{"about":"world","content":"event_state"},"b87":{"about":"world","content":"quantity"},"b88":{"about":"world","content":"event_state"},"b89":{"about":"world","content":"quantity"},"b90":{"about":"world","content":"quantity"},"b91":{"about":"world","content":"quantity"},"b92":{"about":"world","content":"event_state"},"b93":{"about":"world","content":"event_state"},"b94":{"about":"world","content":"event_state"},"b95":{"about":"world","content":"event_state"},"b96":{"about":"world","content":"quantity"},"b97":{"about":"world","content":"event_state"},"b98":{"about":"world","content":"event_state"},"b99":{"about":"world","content":"quantity"},"b100":{"about":"world","content":"event_state"},"b101":{"about":"world","content":"quantity"},"b102":{"about":"world","content":"quantity"},"b103":{"about":"world","content":"quantity"},"b104":{"about":"text","content":"characterising"},"b105":{"about":"text","content":"characterising"},"b106":{"about":"text","content":"characterising"},"b107":{"about":"text","content":"event_state"},"b108":{"about":"text","content":"event_state"},"b109":{"about":"text","content":"characterising"},"b110":{"about":"text","content":"event_state"},"b111":{"about":"text","content":"characterising"},"b112":{"about":"text","content":"characterising"},"b113":{"about":"entity","content":"characterising"},"b114":{"about":"entity","content":"characterising"},"b115":{"about":"entity","content":"characterising"},"b116":{"about":"entity","content":"characterising"},"b117":{"about":"entity","content":"characterising"},"b118":{"about":"entity","content":"characterising"},"b119":{"about":"text","content":"characterising"},"b120":{"about":"text","content":"event_state"},"b121":{"about":"text","content":"event_state"},"b122":{"about":"between","content":"event_state"},"b123":{"about":"between","content":"characterising"},"b124":{"about":"between","content":"characterising"},"b125":{"about":"text","content":"characterising"},"b126":{"about":"text","content":"characterising"},"b127":{"about":"text","content":"event_state"},"b128":{"about":"text","content":"characterising"},"b129":{"about":"text","content":"event_state"},"b130":{"about":"text","content":"characterising"},"b131":{"about":"text","content":"characterising"},"b132":{"about":"text","content":"event_state"},"b133":{"about":"entity","content":"characterising"},"b134":{"about":"entity","content":"characterising"},"b135":{"about":"entity","content":"characterising"},"b136":{"about":"entity","content":"characterising"},"b137":{"about":"entity","content":"characterising"},"b138":{"about":"entity","content":"characterising"},"b139":{"about":"text","content":"event_state"},"b140":{"about":"text","content":"event_state"},"b141":{"about":"text","content":"event_state"},"b142":{"about":"text","content":"event_state"},"b143":{"about":"text","content":"event_state"},"b144":{"about":"text","content":"event_state"},"b145":{"about":"text","content":"event_state"},"b146":{"about":"text","content":"event_state"},"b147":{"about":"text","content":"event_state"},"b148":{"about":"text","content":"event_state"},"b149":{"about":"text","content":"characterising"},"b150":{"about":"text","content":"event_state"},"b151":{"about":"text","content":"characterising"},"b152":{"about":"text","content":"characterising"},"b153":{"about":"text","content":"characterising"},"b154":{"about":"text","content":"characterising"},"b155":{"about":"text","content":"event_state"},"b156":{"about":"text","content":"event_state"},"b157":{"about":"text","content":"event_state"},"b158":{"about":"text","content":"characterising"},"b159":{"about":"text","content":"characterising"},"b160":{"about":"text","content":"characterising"},"b161":{"about":"text","content":"event_state"},"b162":{"about":"entity","content":"characterising"},"b163":{"about":"entity","content":"event_state"},"b164":{"about":"entity","content":"event_state"},"b165":{"about":"entity","content":"characterising"},"b166":{"about":"entity","content":"event_state"},"b167":{"about":"entity","content":"event_state"},"b168":{"about":"entity","content":"characterising"},"b169":{"about":"entity","content":"event_state"},"b170":{"about":"entity","content":"event_state"},"b171":{"about":"between","content":"event_state"},"b172":{"about":"text","content":"event_state"},"b173":{"about":"text","content":"event_state"},"b174":{"about":"text","content":"event_state"},"b175":{"about":"text","content":"event_state"}}}
```

</details>
