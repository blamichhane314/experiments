# Experiment 8, prompt test, step 2 of 7: Propositions: six articles, each asked for

Propositions of an article. Requests sent: 10. Models: Haiku 4.5, GPT-4o, Sonnet 5.5. First and last request: 16 October 2026, 12:47 to 14:29 (Pacific time).

The request asks: “For each article, list the propositions about the world that it contains.”

## The template

`props_Ball.txt`. The parts in braces are filled in for each request.

```text
The following {n_articles} news articles are labelled {labels}. The names of the outlets have been removed.

{articles}

Task: for each article, list the propositions about the world that it contains.

A proposition is a single claim about the world that an article states or reports: what happened or is the case, what a number is, what a rule or status is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each proposition contains exactly one claim. Test every proposition before you list it: if it can be divided into two statements, each of which could be true while the other is false, divide it and list both. Two numbers, two findings, a finding and a second finding about its size or timing, or a fact and a comment on it are two claims. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal claim (A causes B) is one proposition only when the causal link is the claim.
2. Each proposition must stand on its own: a reader who has not seen the article must be able to understand it. Resolve pronouns, give full names, and include the time, place and population when the claim's truth depends on them. Add nothing else.
3. State the proposition as a claim about the world, not about the article. When an article reports a claim made by a person or a study, state the claim itself and record the source in "relation" and "source"; do not write "the article says".
4. Keep the article's meaning. Do not strengthen, weaken, generalise or soften the claim.
5. Leave out rhetorical flourishes, questions, and claims whose meaning cannot be resolved from the article.
6. Each proposition must come from the article it is listed under. Copy, character for character, the shortest passage of that article that states it ("span"). The passage must be one continuous stretch of the article, with every word, letter and punctuation mark exactly as in the article: do not change a word, do not shorten it with "...", and do not join passages from different places. Copy the passage as it stands even where the proposition itself resolves a pronoun or gives a full name.
7. List every proposition the article contains. Do not list the same proposition twice in different words.

For each proposition, give "relation": "asserts" (the article states it in its own voice), "reports" (the article reports a person, group or study saying it), or "hedges" (the article states it with doubt or qualification), and "source": who makes the claim (a person, group or study as named in the article, or "the article" when it is the article's own voice).

Return JSON of the form {{"articles": [{{"article": "<label>", "propositions": [{{"text": "<proposition>", "span": "<exact passage>", "relation": "asserts|reports|hedges", "source": "<who>"}}, ...]}}, ...]}}, with one entry in "articles" for each article you were asked about.
```

## Requests as sent (6)

One request for each combination of model, round, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>GPT-4o, temperature 0 · Round 1 · 16 October 2026, 12:51</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (4846 words)

```text
The following 6 news articles are labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A3: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A6: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]




Task: for each article, list the propositions about the world that it contains.

A proposition is a single claim about the world that an article states or reports: what happened or is the case, what a number is, what a rule or status is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each proposition contains exactly one claim. Test every proposition before you list it: if it can be divided into two statements, each of which could be true while the other is false, divide it and list both. Two numbers, two findings, a finding and a second finding about its size or timing, or a fact and a comment on it are two claims. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal claim (A causes B) is one proposition only when the causal link is the claim.
2. Each proposition must stand on its own: a reader who has not seen the article must be able to understand it. Resolve pronouns, give full names, and include the time, place and population when the claim's truth depends on them. Add nothing else.
3. State the proposition as a claim about the world, not about the article. When an article reports a claim made by a person or a study, state the claim itself and record the source in "relation" and "source"; do not write "the article says".
4. Keep the article's meaning. Do not strengthen, weaken, generalise or soften the claim.
5. Leave out rhetorical flourishes, questions, and claims whose meaning cannot be resolved from the article.
6. Each proposition must come from the article it is listed under. Copy, character for character, the shortest passage of that article that states it ("span").
7. List every proposition the article contains. Do not list the same proposition twice in different words.

For each proposition, give "relation": "asserts" (the article states it in its own voice), "reports" (the article reports a person, group or study saying it), or "hedges" (the article states it with doubt or qualification), and "source": who makes the claim (a person, group or study as named in the article, or "the article" when it is the article's own voice).

Return JSON of the form {"articles": [{"article": "<label>", "propositions": [{"text": "<proposition>", "span": "<exact passage>", "relation": "asserts|reports|hedges", "source": "<who>"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (7614 words)

```text
{"articles":[{"article":"A1","propositions":[{"text":"Georgia Tech is welcoming its incoming freshman class to campus this week.","span":"[passage of 12 words]","relation":"asserts","source":"the article"},{"text":"Georgia Tech is known for its computer science, engineering and other STEM programs.","span":"[passage of 13 words]","relation":"asserts","source":"the article"},{"text":"Artificial intelligence is changing STEM industries and how Georgia Tech approaches its curriculum.","span":"[passage of 17 words]","relation":"asserts","source":"the article"},{"text":"David Joyner is Georgia Tech's interim vice provost for AI in education.","span":"[passage of 26 words]","relation":"asserts","source":"the article"},{"text":"Nearly 15,000 students at Georgia Tech are majoring in or minoring in AI-related fields, including computer science.","span":"[passage of 26 words]","relation":"reports","source":"David Joyner"},{"text":"Georgia Tech recognizes that AI is changing STEM industries.","span":"[passage of 11 words]","relation":"reports","source":"David Joyner"},{"text":"Some professors at Georgia Tech are building their own AI agents that serve as tutors for classes.","span":"[passage of 17 words]","relation":"reports","source":"David Joyner"},{"text":"Plenty of faculty at Georgia Tech are reacting to AI by changing their teaching methods.","span":"[passage of 40 words]","relation":"reports","source":"David Joyner"},{"text":"AI can help students complete some tasks more quickly.","span":"[passage of 12 words]","relation":"reports","source":"David Joyner"},{"text":"The old model of going to college for four years and then having a 40-year career has been dead for a while.","span":"[passage of 26 words]","relation":"reports","source":"David Joyner"},{"text":"AI plays a role in giving us a new tool to help us go through a process faster.","span":"[passage of 19 words]","relation":"reports","source":"David Joyner"},{"text":"AI means that we're not going to spend some time formulating an idea, spend three weeks building our software, and then encounter the next big challenge.","span":"[passage of 25 words]","relation":"reports","source":"David Joyner"},{"text":"We're going to formulate the idea and have AI help us write the software.","span":"[passage of 15 words]","relation":"reports","source":"David Joyner"}]},{"article":"A2","propositions":[{"text":"High-school students across Asia are pulling ahead of their Western peers in reading, science, and math performance.","span":"[passage of 32 words]","relation":"asserts","source":"the article"},{"text":"Reading, science, and math performance among 15-year-olds has continued a decline globally across the board.","span":"[passage of 39 words]","relation":"asserts","source":"the article"},{"text":"The 2025 Programme for International Student Assessment was released this week by the Organisation for Economic Co-operation and Development.","span":"[passage of 39 words]","relation":"asserts","source":"the article"},{"text":"Students in the Chinese cities of Beijing and Shanghai, Chinese provinces Jiangsu and Zhejiang, and the city-state of Singapore were among last year’s top performers in reading, science, and math.","span":"[passage of 26 words]","relation":"asserts","source":"the article"},{"text":"Japan and South Korea were in the Asia-dominated top 10 across all three subjects.","span":"[passage of 29 words]","relation":"asserts","source":"the article"},{"text":"The semi-autonomous Chinese city of Macao and the self-governing democracy of Taiwan were in the Asia-dominated top 10 across all three subjects.","span":"[passage of 29 words]","relation":"asserts","source":"the article"},{"text":"Secondary students in the US saw their reading scores fall close to 25-year lows.","span":"[passage of 50 words]","relation":"asserts","source":"the article"},{"text":"China has surpassed the US in published scientific reports as well as research spending.","span":"[passage of 23 words]","relation":"asserts","source":"the article"},{"text":"Both the US and China exceeded $1 trillion in research spending in 2024.","span":"[passage of 23 words]","relation":"asserts","source":"the article"},{"text":"The growing adoption of AI could significantly impact secondary education.","span":"[passage of 15 words]","relation":"reports","source":"the PISA report"},{"text":"The decline in skills that matter most in the AI age is most troubling.","span":"[passage of 42 words]","relation":"reports","source":"Andreas Schleicher"},{"text":"In a world increasingly flooded with information, students are less likely to think deeply and separate signal from noise.","span":"[passage of 20 words]","relation":"reports","source":"Andreas Schleicher"},{"text":"China’s data for the PISA tests is not without critics.","span":"[passage of 36 words]","relation":"asserts","source":"the article"},{"text":"The testing has shown a continued drop in US scores over the last decade.","span":"[passage of 19 words]","relation":"asserts","source":"the article"},{"text":"Student performance has become less linked with national or family wealth as technology has progressed.","span":"[passage of 19 words]","relation":"reports","source":"the latest report"},{"text":"It is difficult to determine the exact correlation between the rise of digital tools and test performance.","span":"[passage of 29 words]","relation":"asserts","source":"the article"},{"text":"Higher digital distraction in the classroom is a challenge identified by the study.","span":"[passage of 29 words]","relation":"asserts","source":"the article"},{"text":"Fewer than 10% of students from China, Japan, and South Korea reported that their peers were distracted by digital devices during science lessons.","span":"[passage of 30 words]","relation":"asserts","source":"the article"},{"text":"The global average of students distracted by digital devices during science lessons is 28%.","span":"[passage of 30 words]","relation":"asserts","source":"the article"},{"text":"Singapore used technology in its classrooms but also emphasized reading comprehension early on.","span":"[passage of 26 words]","relation":"reports","source":"the report"},{"text":"The proportion of “hasty readers” nearly doubled between 2018 and 2025.","span":"[passage of 25 words]","relation":"reports","source":"the report"},{"text":"The average performance among OECD countries in science, reading, and math has reached record lows.","span":"[passage of 27 words]","relation":"asserts","source":"the article"},{"text":"Performance meeting a basic level aptitude in PISA among all 15-year-old Americans could add over $40 trillion to the US economy over their working lives.","span":"[passage of 34 words]","relation":"reports","source":"a Stanford University study"},{"text":"The percentage of OECD students below the baseline performance increased last year to 20% from 16% in 2022.","span":"[passage of 19 words]","relation":"asserts","source":"the article"}]},{"article":"A3","propositions":[{"text":"AI has led to a decline in multiple student skills as well as a drop in test scores.","span":"[passage of 46 words]","relation":"reports","source":"the OECD’s latest Program for International Student Assessment (PISA)"},{"text":"Moderate use of AI is associated with stronger performance in certain subjects compared to limited or daily use.","span":"[passage of 46 words]","relation":"reports","source":"the OECD’s latest Program for International Student Assessment (PISA)"},{"text":"Students who used AI moderately recorded higher average science scores than both students who rarely used AI and those who used it almost every day.","span":"[passage of 38 words]","relation":"asserts","source":"the article"},{"text":"The advantage of moderate AI use was especially clear when students used AI to summarize assigned reading or conduct preliminary research on a new topic.","span":"[passage of 21 words]","relation":"asserts","source":"the article"},{"text":"Students who reported using AI weekly for summarizing or research tended to perform at about the same level as AI nonusers after accounting for socioeconomic status.","span":"[passage of 25 words]","relation":"asserts","source":"the article"},{"text":"Students who used AI almost every day and students who rarely used it tended to have lower scores.","span":"[passage of 19 words]","relation":"asserts","source":"the article"},{"text":"These relationships do not necessarily imply a negative impact of AI use on science performance.","span":"[passage of 33 words]","relation":"reports","source":"the study"},{"text":"Moderate and intentional use of AI for schoolwork and learning may be positively related to student performance.","span":"[passage of 21 words]","relation":"reports","source":"the study"},{"text":"Digital tools can support learning when used purposefully and in moderation.","span":"[passage of 34 words]","relation":"reports","source":"the OECD"},{"text":"Excessive or unguided use of digital tools can contribute to distraction and shallower engagement.","span":"[passage of 34 words]","relation":"reports","source":"the OECD"},{"text":"Learning does not occur through the consumption of content but as a productive cognitive struggle of the mind with new material.","span":"[passage of 41 words]","relation":"reports","source":"the findings"},{"text":"Reading, mathematics, and science scores have dropped since 2003.","span":"[passage of 22 words]","relation":"reports","source":"PISA"},{"text":"86% of students across OECD countries had used AI chatbots for at least one of the schoolwork purposes examined in the assessment.","span":"[passage of 46 words]","relation":"asserts","source":"the article"},{"text":"14% of students across OECD countries said they had never or almost never used AI for any of the schoolwork purposes examined in the assessment.","span":"[passage of 46 words]","relation":"asserts","source":"the article"},{"text":"About one in five students reported using AI almost every day.","span":"[passage of 11 words]","relation":"asserts","source":"the article"},{"text":"Students who reported using AI almost every day tended to score lower in science than students who did not, accounting for socioeconomic status.","span":"[passage of 17 words]","relation":"asserts","source":"the article"},{"text":"The weaker a student’s ability to read critically, the harder it may be to recognize when an AI-generated answer is incomplete or incorrect.","span":"[passage of 23 words]","relation":"asserts","source":"the article"},{"text":"Routinely allowing AI to perform the reading, summarizing or reasoning could give students fewer opportunities to develop those skills.","span":"[passage of 24 words]","relation":"asserts","source":"the article"},{"text":"Important skills attributed to critical thinking are declining.","span":"[passage of 13 words]","relation":"reports","source":"the findings"},{"text":"The decline in skills that matter most in the AI age is most troubling.","span":"[passage of 33 words]","relation":"reports","source":"the report"},{"text":"The share of ‘hasty readers’ almost doubled between 2018 and 2025.","span":"[passage of 22 words]","relation":"reports","source":"the report"},{"text":"In a world increasingly flooded with information, students are less likely to think deeply and separate signal from noise.","span":"[passage of 20 words]","relation":"reports","source":"the report"}]},{"article":"A4","propositions":[{"text":"Artificial intelligence is spreading in classrooms.","span":"[passage of 22 words]","relation":"asserts","source":"the article"},{"text":"The impact of AI on learning depends less on the technology than on how students use it.","span":"[passage of 22 words]","relation":"asserts","source":"the article"},{"text":"Hundreds of millions of primary and secondary students are starting their schools for the new academic year this month.","span":"[passage of 19 words]","relation":"asserts","source":"the article"},{"text":"The advent of Artificial Intelligence is changing the students’ learning process.","span":"[passage of 12 words]","relation":"asserts","source":"the article"},{"text":"Students and teachers are grappling with the question of what homework is for when an AI chatbot can finish it in seconds.","span":"[passage of 21 words]","relation":"asserts","source":"the article"},{"text":"China requires at least eight hours of AI instruction a year.","span":"[passage of 41 words]","relation":"asserts","source":"the article"},{"text":"The United Arab Emirates, Saudi Arabia, and Qatar have begun integrating AI into their curricula.","span":"[passage of 41 words]","relation":"asserts","source":"the article"},{"text":"AI chatbots can make learning faster and easier.","span":"[passage of 8 words]","relation":"asserts","source":"the article"},{"text":"David Stromberg of Stockholm University, with Victor Lei and Yanhui Wu of the University of Hong Kong, ran one of the largest studies of its kind, tracking about 27,000 students aged 12 to 18 in China for 30 months.","span":"[passage of 42 words]","relation":"asserts","source":"the article"},{"text":"The study combined data on homework, monthly closed-book exams, and high-stakes entrance exams across nine subjects.","span":"[passage of 17 words]","relation":"asserts","source":"the article"},{"text":"After adopting generative AI, students’ homework scores rose by 18 percent.","span":"[passage of 31 words]","relation":"asserts","source":"the article"},{"text":"The time spent on each assignment fell by about 30 percent, from 64 minutes to 45 minutes on average, after adopting generative AI.","span":"[passage of 31 words]","relation":"asserts","source":"the article"},{"text":"When the same students sat monthly exams without AI, their scores fell by 20 percent within six months.","span":"[passage of 19 words]","relation":"asserts","source":"the article"},{"text":"Students' performance in high-stakes entrance exams declined, with the full effect emerging over a longer period.","span":"[passage of 17 words]","relation":"asserts","source":"the article"},{"text":"The Organisation for Economic Co-operation and Development (OECD) came to a similar conclusion in its Digital Education Outlook 2026.","span":"[passage of 29 words]","relation":"asserts","source":"the article"},{"text":"Generative AI is neither built to teach nor used under any structure, and outsourcing tasks to the model improves performance with no real learning gains.","span":"[passage of 27 words]","relation":"reports","source":"the Organisation for Economic Co-operation and Development (OECD)"},{"text":"Research co-authored by Dragan Gasevic describes the potential erosion of productive cognitive effort as “metacognitive laziness”.","span":"[passage of 16 words]","relation":"asserts","source":"the article"},{"text":"How students use AI tools turns out to matter more than whether they use them.","span":"[passage of 15 words]","relation":"asserts","source":"the article"},{"text":"A survey by Ipsos for the Vodafone Foundation asked 7,000 students aged 12 to 17 across seven European countries how they use AI when studying outside school and without teacher instruction.","span":"[passage of 31 words]","relation":"asserts","source":"the article"},{"text":"The most common use of AI was getting information, reported by 56 percent of students.","span":"[passage of 13 words]","relation":"asserts","source":"the article"},{"text":"45 percent of students used AI to have terms and concepts explained to them.","span":"[passage of 13 words]","relation":"asserts","source":"the article"},{"text":"31 percent of students said they used AI to provide complete solutions to tasks.","span":"[passage of 13 words]","relation":"asserts","source":"the article"},{"text":"29 percent of students used interactive or adaptive content to guide their learning.","span":"[passage of 28 words]","relation":"asserts","source":"the article"},{"text":"20 percent of students used AI to create personalised learning plans and track their progress.","span":"[passage of 28 words]","relation":"asserts","source":"the article"},{"text":"AI is becoming more than a tool for completing schoolwork for students.","span":"[passage of 12 words]","relation":"asserts","source":"the article"},{"text":"AI is increasingly part of the wider student experience, from getting instant help to finding someone to talk to.","span":"[passage of 19 words]","relation":"asserts","source":"the article"},{"text":"The HEPI/Kortext Student Generative AI Survey 2026 is based on 1,054 full-time undergraduates in the United Kingdom.","span":"[passage of 27 words]","relation":"asserts","source":"the article"},{"text":"49 percent of full-time undergraduates in the United Kingdom believe AI has improved their student experience.","span":"[passage of 27 words]","relation":"asserts","source":"the article"},{"text":"Students pointed to saving time, better understanding, and instant, personalised support as improvements from AI.","span":"[passage of 11 words]","relation":"asserts","source":"the article"},{"text":"59 percent of students said AI made no difference to their loneliness.","span":"[passage of 9 words]","relation":"asserts","source":"the article"},{"text":"21 percent of students felt less lonely due to AI.","span":"[passage of 17 words]","relation":"asserts","source":"the article"},{"text":"20 percent of students felt more lonely due to AI.","span":"[passage of 17 words]","relation":"asserts","source":"the article"}]},{"article":"A5","propositions":[{"text":"Middlebury College political science professor Allison Stanger uses AI to help her write.","span":"[passage of 17 words]","relation":"asserts","source":"the article"},{"text":"Allison Stanger wrote in The Wall Street Journal that AI used well can strengthen thinking.","span":"[passage of 17 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is often viewed as a creativity killer when it comes to writing.","span":"[passage of 14 words]","relation":"asserts","source":"the article"},{"text":"AI is a wonderful collaborator, according to Allison Stanger.","span":"[passage of 19 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is like having the scientist John von Neumann on speed dial 24/7, according to Allison Stanger.","span":"[passage of 21 words]","relation":"reports","source":"Allison Stanger"},{"text":"Allison Stanger uses AI to think through things and check the mechanics of her writing.","span":"[passage of 16 words]","relation":"reports","source":"Allison Stanger"},{"text":"All the ideas, openings, and conclusions in Allison Stanger's writing are her own.","span":"[passage of 12 words]","relation":"reports","source":"Allison Stanger"},{"text":"Allison Stanger talks to AI about anything she wants to explore further.","span":"[passage of 14 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is something that is absolutely miraculous, according to Allison Stanger.","span":"[passage of 17 words]","relation":"reports","source":"Allison Stanger"},{"text":"Anyone who criticizes AI without a simultaneous sense of wonder is missing something important, according to Allison Stanger.","span":"[passage of 10 words]","relation":"reports","source":"Allison Stanger"},{"text":"Allison Stanger always writes her own first drafts.","span":"[passage of 8 words]","relation":"reports","source":"Allison Stanger"},{"text":"Allison Stanger always outlines her argument.","span":"[passage of 5 words]","relation":"reports","source":"Allison Stanger"},{"text":"Allison Stanger goes back and forth with AI to make sure her argument is sound.","span":"[passage of 26 words]","relation":"reports","source":"Allison Stanger"},{"text":"Humans are best at judging what good writing is, according to Allison Stanger.","span":"[passage of 22 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is not going to get you to good writing, according to Allison Stanger.","span":"[passage of 12 words]","relation":"reports","source":"Allison Stanger"},{"text":"Sometimes, we finish something in the middle of the night and don't have another human to show it to yet, according to Allison Stanger.","span":"[passage of 24 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI can be quite useful when we don't have another human to show our work to yet, according to Allison Stanger.","span":"[passage of 7 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is a middle-of-the-night editor, according to Allison Stanger.","span":"[passage of 14 words]","relation":"reports","source":"Allison Stanger"},{"text":"There is a fear that AI kills creativity and is mentally enfeebling.","span":"[passage of 20 words]","relation":"asserts","source":"the article"},{"text":"Allison Stanger worries about AI killing creativity.","span":"[passage of 8 words]","relation":"reports","source":"Allison Stanger"},{"text":"Part of the problem with AI is not with the technology but with the concentration of power, according to Allison Stanger.","span":"[passage of 23 words]","relation":"reports","source":"Allison Stanger"},{"text":"Allison Stanger has written a larger book about the concentration of power in AI.","span":"[passage of 11 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is extraordinarily useful, according to Allison Stanger.","span":"[passage of 9 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is potentially very, very dangerous, according to Allison Stanger.","span":"[passage of 8 words]","relation":"reports","source":"Allison Stanger"},{"text":"We still have to think for ourselves and teach our students to do that, according to Allison Stanger.","span":"[passage of 19 words]","relation":"reports","source":"Allison Stanger"},{"text":"There has to be a power balance, and the human has to keep pushing back, according to Allison Stanger.","span":"[passage of 21 words]","relation":"reports","source":"Allison Stanger"},{"text":"We have to find ways to enable a power balance, according to Allison Stanger.","span":"[passage of 12 words]","relation":"reports","source":"Allison Stanger"},{"text":"Otherwise, we're in big danger, according to Allison Stanger.","span":"[passage of 5 words]","relation":"reports","source":"Allison Stanger"},{"text":"Writing and editing are just two of many uses of AI.","span":"[passage of 21 words]","relation":"asserts","source":"the article"},{"text":"There might be other uses of AI that might not require as much hesitation, according to Allison Stanger.","span":"[passage of 29 words]","relation":"reports","source":"Allison Stanger"},{"text":"For writing, there's a pause needed, according to Allison Stanger.","span":"[passage of 7 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is a pattern-recognizer, according to Allison Stanger.","span":"[passage of 8 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI can help you recognize something that's important to explore further, according to Allison Stanger.","span":"[passage of 24 words]","relation":"reports","source":"Allison Stanger"}]},{"article":"A6","propositions":[{"text":"The effects of artificial intelligence on learning are still largely unclear.","span":"[passage of 11 words]","relation":"asserts","source":"the article"},{"text":"A new poll of K-12 teachers found that nearly 3-in-4 believe AI has bigger implications for education than past innovations like the internet or computers.","span":"[passage of 28 words]","relation":"asserts","source":"the article"},{"text":"The poll surveyed 545 respondents and paints a complex picture of teachers' views on AI.","span":"[passage of 49 words]","relation":"asserts","source":"the article"},{"text":"Many teachers are using AI to save time and improve their teaching materials.","span":"[passage of 49 words]","relation":"asserts","source":"the article"},{"text":"A majority of teachers are worried AI is making it harder for students to learn to think for themselves.","span":"[passage of 49 words]","relation":"asserts","source":"the article"},{"text":"Teachers feel like AI is going to fundamentally reshape the future of education moving forward.","span":"[passage of 29 words]","relation":"reports","source":"Mallory Newall"},{"text":"Teachers have serious concerns about AI's impact on how they relate to their students and how students relate to each other.","span":"[passage of 21 words]","relation":"reports","source":"Mallory Newall"},{"text":"A resounding majority of polled teachers think schools should teach responsible use of AI.","span":"[passage of 25 words]","relation":"asserts","source":"the article"},{"text":"Teachers are acknowledging that AI is having humongous implications on education as we know it.","span":"[passage of 26 words]","relation":"reports","source":"Mallory Newall"},{"text":"AI is not going away.","span":"[passage of 4 words]","relation":"reports","source":"Mallory Newall"},{"text":"Now is the time to act regarding AI in education.","span":"[passage of 8 words]","relation":"reports","source":"Mallory Newall"},{"text":"Students aren't widely using AI in the classroom yet.","span":"[passage of 16 words]","relation":"asserts","source":"the article"},{"text":"A little more than half of teachers say the technology isn't being used in class by students at all.","span":"[passage of 35 words]","relation":"asserts","source":"the article"},{"text":"About 2-in-5 teachers say students are using AI in class at least once a week.","span":"[passage of 35 words]","relation":"asserts","source":"the article"},{"text":"A majority of teachers polled say they've used AI themselves to help with work tasks.","span":"[passage of 19 words]","relation":"asserts","source":"the article"},{"text":"Michele Naber allows her students to use AI during certain lessons to teach them how to properly prompt chatbots and verify their accuracy.","span":"[passage of 38 words]","relation":"asserts","source":"the article"},{"text":"Michele Naber tells her students to ask ChatGPT to describe a particular animal's physical characteristics and habitat, then verify what the chatbot generated with reliable sources.","span":"[passage of 29 words]","relation":"asserts","source":"the article"},{"text":"The lesson shows students that AI still gets it wrong sometimes.","span":"[passage of 13 words]","relation":"asserts","source":"the article"},{"text":"Michele Naber has had success using AI to generate multiple choice questions for assessments.","span":"[passage of 15 words]","relation":"asserts","source":"the article"},{"text":"Generating multiple choice questions with AI minimizes the task to five minutes.","span":"[passage of 28 words]","relation":"reports","source":"Michele Naber"},{"text":"A majority of surveyed teachers who report using AI on work-related tasks say it saves them time.","span":"[passage of 34 words]","relation":"asserts","source":"the article"},{"text":"Most teachers say the time savings from using AI equates to two hours or less per week.","span":"[passage of 34 words]","relation":"asserts","source":"the article"},{"text":"Joann Purcell has found AI useful for coming up with professional development activities for her fellow educators.","span":"[passage of 34 words]","relation":"asserts","source":"the article"},{"text":"Joann Purcell doesn't use AI with her students.","span":"[passage of 8 words]","relation":"asserts","source":"the article"},{"text":"Joann Purcell says AI isn't reliable enough to generate math questions.","span":"[passage of 11 words]","relation":"asserts","source":"the article"},{"text":"It's a pain to go through and see where the mistakes are in AI-generated math questions, according to Joann Purcell.","span":"[passage of 36 words]","relation":"reports","source":"Joann Purcell"},{"text":"More than half of polled teachers say AI makes it harder for students to learn critical thinking skills.","span":"[passage of 19 words]","relation":"asserts","source":"the article"},{"text":"Christa Corricelli says AI could be a valuable technology for learning, but too often students are using it as an answer machine.","span":"[passage of 40 words]","relation":"asserts","source":"the article"},{"text":"Students who aren't already intrinsically self-motivated to be critical thinkers will see their critical thinking skills atrophy over time, according to Christa Corricelli.","span":"[passage of 43 words]","relation":"reports","source":"Christa Corricelli"},{"text":"Michele Naber feels a deep responsibility to teach her students that humans must always interrogate and verify what AI generates.","span":"[passage of 21 words]","relation":"asserts","source":"the article"},{"text":"Michele Naber wants her students to be able to look at the world and figure out things for themselves, not rely on a piece of software.","span":"[passage of 31 words]","relation":"reports","source":"Michele Naber"},{"text":"If we stop questioning what AI says, we can be led to believe anything, according to Michele Naber.","span":"[passage of 20 words]","relation":"reports","source":"Michele Naber"},{"text":"More than half of teachers polled think AI is mostly just a shortcut for students to avoid doing more work.","span":"[passage of 23 words]","relation":"asserts","source":"the article"},{"text":"Ellie Rodriguez says AI can be especially helpful for students with disabilities.","span":"[passage of 28 words]","relation":"asserts","source":"the article"},{"text":"One of Ellie Rodriguez's students, who is on the autism spectrum, recently used AI to get help with an assignment.","span":"[passage of 22 words]","relation":"asserts","source":"the article"},{"text":"Ellie Rodriguez praised her student for using AI to complete an assignment.","span":"[passage of 20 words]","relation":"reports","source":"Ellie Rodriguez"},{"text":"AI got Ellie Rodriguez's student to do the work and helped him apply using resources.","span":"[passage of 38 words]","relation":"reports","source":"Ellie Rodriguez"},{"text":"Ellie Rodriguez worries AI could hamper learning for students who don't have disabilities or who are capable of doing assignments without the assistance of AI.","span":"[passage of 27 words]","relation":"asserts","source":"the article"},{"text":"Ellie Rodriguez and her colleagues, including some English teachers, are deeply concerned about the impact AI is having on students' ability to think for themselves.","span":"[passage of 27 words]","relation":"asserts","source":"the article"},{"text":"Nearly 6-in-10 surveyed educators say AI is eroding the level of trust between students and teachers.","span":"[passage of 16 words]","relation":"asserts","source":"the article"},{"text":"About 4-in-10 educators say they've required more assignments to be done by hand as a result of AI.","span":"[passage of 30 words]","relation":"asserts","source":"the article"},{"text":"About 4-in-10 educators say they've required more assignments to be done in class as a result of AI.","span":"[passage of 30 words]","relation":"asserts","source":"the article"},{"text":"The erosion of trust caused by AI is one of the biggest red flags in the data, according to Mallory Newall.","span":"[passage of 21 words]","relation":"reports","source":"Mallory Newall"},{"text":"The erosion of trust issue is compounded by another survey finding: 70% of teachers believe the public's perception of them has gotten worse.","span":"[passage of 22 words]","relation":"asserts","source":"the article"},{"text":"Teachers are trying to navigate complex challenges in an environment that is already rife with mistrust, according to Mallory Newall.","span":"[passage of 26 words]","relation":"reports","source":"Mallory Newall"},{"text":"Michele Naber has had to adapt to how easy it is now for students to fake assignments.","span":"[passage of 18 words]","relation":"asserts","source":"the article"},{"text":"Michele Naber offered extra credit to students who participated in beach cleanups and habitat restorations outside of school.","span":"[passage of 21 words]","relation":"asserts","source":"the article"},{"text":"Students had to show Michele Naber a picture to prove they were at the event for extra credit.","span":"[passage of 17 words]","relation":"asserts","source":"the article"},{"text":"Michele Naber's son showed her how easy it is to use AI to create a fake image of a registration table for an event.","span":"[passage of 26 words]","relation":"asserts","source":"the article"},{"text":"Michele Naber had to stop offering extra credit for participation in events because she can't verify it.","span":"[passage of 16 words]","relation":"reports","source":"Michele Naber"},{"text":"Michele Naber has modified her curriculum so that all lab work is done in class in front of her.","span":"[passage of 28 words]","relation":"asserts","source":"the article"},{"text":"Homework matters far less for students' grades in Michele Naber's curriculum.","span":"[passage of 28 words]","relation":"asserts","source":"the article"},{"text":"Teachers are much more suspect of things that students do outside the classroom, according to Christa Corricelli.","span":"[passage of 39 words]","relation":"reports","source":"Christa Corricelli"},{"text":"Josh Kauffman teaches seventh-grade English at Alabama Destinations Career Academy, a virtual public school that serves students across the state.","span":"[passage of 20 words]","relation":"asserts","source":"the article"},{"text":"Josh Kauffman has noticed a substantial uptick in the number of AI-generated assignments his students submit.","span":"[passage of 32 words]","relation":"asserts","source":"the article"},{"text":"Josh Kauffman tries to persuade his students that there's value in their own writing.","span":"[passage of 16 words]","relation":"asserts","source":"the article"},{"text":"Josh Kauffman tells his students he would rather deal with all of their typos and know that they're theirs than to wonder how much they're standing on other people's shoulders to do their work for them.","span":"[passage of 36 words]","relation":"reports","source":"Josh Kauffman"},{"text":"Joann Purcell doesn't necessarily think AI has eroded trust.","span":"[passage of 10 words]","relation":"asserts","source":"the article"},{"text":"Students found ways to cheat on assignments long before AI came along, according to Joann Purcell.","span":"[passage of 14 words]","relation":"reports","source":"Joann Purcell"},{"text":"Teachers need to be creative in how they use AI and force kids to think with it just like they would with any other tool, according to Joann Purcell.","span":"[passage of 29 words]","relation":"reports","source":"Joann Purcell"},{"text":"Many educators are having to adapt to AI with little guidance from their school or district, according to the survey results.","span":"[passage of 21 words]","relation":"asserts","source":"the article"},{"text":"Among teachers whose school provides AI software, only 35% say they have a formal policy on teacher use of AI.","span":"[passage of 36 words]","relation":"asserts","source":"the article"},{"text":"About half of all polled teachers say their school hasn't offered any guidance on AI, or they're not sure what the guidance is.","span":"[passage of 23 words]","relation":"asserts","source":"the article"},{"text":"Teachers are looking for additional guidance from their district and from their students on what AI is going to mean for the future of education, according to Mallory Newall.","span":"[passage of 30 words]","relation":"reports","source":"Mallory Newall"},{"text":"Only about 4-in-10 teachers say their school offers professional development or training related to AI, according to the poll.","span":"[passage of 19 words]","relation":"asserts","source":"the article"},{"text":"Ellie Rodriguez hasn't received any training on AI and wishes she could.","span":"[passage of 17 words]","relation":"asserts","source":"the article"},{"text":"Schools need to teach teachers how to apply AI information to what they do and most importantly to how they teach to be able to utilize AI in a positive way, according to Ellie Rodriguez.","span":"[passage of 33 words]","relation":"reports","source":"Ellie Rodriguez"},{"text":"Josh Kauffman agrees that there isn't enough attention being paid to how to teach what we are teaching differently to account for the flexibility and the resources that AI can make available.","span":"[passage of 32 words]","relation":"reports","source":"Josh Kauffman"},{"text":"Schools are often slow to adapt to change, and that's been a challenge for educators, according to Christa Corricelli.","span":"[passage of 26 words]","relation":"reports","source":"Christa Corricelli"},{"text":"Educators are trying not to drown with the whole AI thing, according to Christa Corricelli.","span":"[passage of 17 words]","relation":"reports","source":"Christa Corricelli"}]}]}
```

</details>

<details><summary>Haiku 4.5, temperature 0 · Round 1 · 16 October 2026, 13:01</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (4846 words)

```text
The following 6 news articles are labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A3: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A6: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]




Task: for each article, list the propositions about the world that it contains.

A proposition is a single claim about the world that an article states or reports: what happened or is the case, what a number is, what a rule or status is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each proposition contains exactly one claim. Test every proposition before you list it: if it can be divided into two statements, each of which could be true while the other is false, divide it and list both. Two numbers, two findings, a finding and a second finding about its size or timing, or a fact and a comment on it are two claims. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal claim (A causes B) is one proposition only when the causal link is the claim.
2. Each proposition must stand on its own: a reader who has not seen the article must be able to understand it. Resolve pronouns, give full names, and include the time, place and population when the claim's truth depends on them. Add nothing else.
3. State the proposition as a claim about the world, not about the article. When an article reports a claim made by a person or a study, state the claim itself and record the source in "relation" and "source"; do not write "the article says".
4. Keep the article's meaning. Do not strengthen, weaken, generalise or soften the claim.
5. Leave out rhetorical flourishes, questions, and claims whose meaning cannot be resolved from the article.
6. Each proposition must come from the article it is listed under. Copy, character for character, the shortest passage of that article that states it ("span").
7. List every proposition the article contains. Do not list the same proposition twice in different words.

For each proposition, give "relation": "asserts" (the article states it in its own voice), "reports" (the article reports a person, group or study saying it), or "hedges" (the article states it with doubt or qualification), and "source": who makes the claim (a person, group or study as named in the article, or "the article" when it is the article's own voice).

Return JSON of the form {"articles": [{"article": "<label>", "propositions": [{"text": "<proposition>", "span": "<exact passage>", "relation": "asserts|reports|hedges", "source": "<who>"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (8551 words)

````text
```json
{
  "articles": [
    {
      "article": "A1",
      "propositions": [
        {
          "text": "Georgia Tech is welcoming its incoming freshman class to campus in the week of August 20, 2026.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Georgia Tech is known for its computer science, engineering and other STEM programs.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing industries including computer science, engineering and other STEM fields.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing how professors plan their lessons.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Nearly 15,000 students at Georgia Tech are majoring in or minoring in AI-related fields, including computer science.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Georgia Tech recognizes that AI is changing STEM industries.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Some Georgia Tech professors are building their own AI agents that serve as tutors for classes.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Some Georgia Tech professors are reacting to AI by changing assignments from requiring a 10-page essay to having class discussions instead.",
          "span": "[passage of 24 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "AI can help students complete some tasks more quickly.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "The model of going to college for four years and then having a 40-year career has been dead for a while.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "AI provides a tool to help people go through processes faster.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "With AI, people will formulate an idea, have AI help write software, and then encounter the next big challenge, rather than spending three weeks building software before encountering the next challenge.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "David Joyner"
        }
      ]
    },
    {
      "article": "A2",
      "propositions": [
        {
          "text": "High-school students across Asia are pulling ahead of their Western peers in a global assessment.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is spurring a worldwide race for talent and reshaping how young people learn.",
          "span": "[passage of 14 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Reading, science and math performance among 15-year-olds has continued a decline globally across the board according to the 2025 Programme for International Student Assessment.",
          "span": "[passage of 24 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students in Beijing and Shanghai were among the top performers in the 2025 PISA assessment.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students in Jiangsu and Zhejiang provinces were among the top performers in the 2025 PISA assessment.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students in Singapore were among the top performers in the 2025 PISA assessment.",
          "span": "[passage of 4 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Japan and South Korea were in the top 10 performers in the 2025 PISA assessment across all three subjects.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Macao was in the top 10 performers in the 2025 PISA assessment across all three subjects.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Taiwan was in the top 10 performers in the 2025 PISA assessment across all three subjects.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Secondary students in the US saw their reading scores fall close to 25-year lows.",
          "span": "[passage of 14 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "US secondary students' reading scores lag more starkly behind their counterparts in China.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "China has long held a lead in PISA exams, at least in the four major Chinese jurisdictions that submitted test scores.",
          "span": "[passage of 27 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The US and China are engaged in an intensifying rivalry to outpace the other in technological advancement.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The US and China are competing to direct more funding toward innovation.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "China has surpassed the US in published scientific reports.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "China has surpassed the US in research spending.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Both the US and China exceeded $1 trillion in research spending in 2024.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The growing adoption of AI could significantly impact secondary education.",
          "span": "[passage of 10 words]",
          "relation": "hedges",
          "source": "the article"
        },
        {
          "text": "The decline in skills for evaluating information, making connections across multiple sources, and thinking critically about what is read is most troubling in the AI age.",
          "span": "[passage of 30 words]",
          "relation": "reports",
          "source": "Andreas Schleicher"
        },
        {
          "text": "In a world increasingly flooded with information, students are less likely to think deeply and separate signal from noise.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Andreas Schleicher"
        },
        {
          "text": "China's PISA data is not without critics in part because the test only includes students from Shanghai, Beijing, Jiangsu and Zhejiang, some of the country's wealthiest eastern coastal areas.",
          "span": "[passage of 36 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The US has experienced a continued drop in PISA scores over the last decade.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The continued drop in US PISA scores over the last decade has alarmed many educationalists.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "As technology has progressed, student performance has become less linked with national or family wealth.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Higher digital distraction in the classroom is a challenge identified in the 2025 PISA report.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Fewer than 10% of students from China, Japan and South Korea reported that their peers were distracted by digital devices during science lessons.",
          "span": "[passage of 23 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The global average of students reporting that their peers were distracted by digital devices during science lessons is 28%.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Singapore used technology in its classrooms but also emphasized reading comprehension early on as an example of how educators might balance digital tools.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The proportion of hasty readers nearly doubled between 2018 and 2025.",
          "span": "[passage of 22 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The average performance among OECD countries in science, reading and math has reached record lows.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Record lows in average performance among OECD countries in science, reading and math could have broader economic implications among the world's biggest nations.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Performance meeting a basic level aptitude in PISA among all 15-year-old Americans could add over $40 trillion to the US economy over their working lives according to a Stanford University study.",
          "span": "[passage of 34 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The percentage of OECD students below the baseline performance level increased to 20% in 2025 from 16% in 2022.",
          "span": "[passage of 18 words]",
          "relation": "asserts",
          "source": "the article"
        }
      ]
    },
    {
      "article": "A3",
      "propositions": [
        {
          "text": "The OECD's latest Program for International Student Assessment found that AI has led to a decline in multiple student skills.",
          "span": "[passage of 21 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The OECD's latest Program for International Student Assessment found that AI has led to a drop in test scores.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Moderate AI use is associated with stronger performance in certain subjects compared to limited or daily use according to the OECD's latest PISA.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who used AI moderately, from about once a month to once or twice a week, recorded higher average science scores than students who rarely used AI.",
          "span": "[passage of 26 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who used AI moderately, from about once a month to once or twice a week, recorded higher average science scores than students who used it almost every day.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The advantage of moderate AI use over limited or daily use was especially clear when students used AI to summarize assigned reading.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The advantage of moderate AI use over limited or daily use was especially clear when students used AI to conduct preliminary research on a new topic.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who reported using AI weekly to summarize assigned reading or conduct preliminary research tended to perform at about the same level as AI nonusers after accounting for socioeconomic status.",
          "span": "[passage of 25 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who used AI almost every day tended to have lower science scores than AI nonusers.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who rarely used AI tended to have lower science scores than AI nonusers.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The relationships between AI use frequency and science performance do not necessarily imply a negative impact of AI use on science performance according to the OECD.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The relationships between AI use frequency and science performance may reflect a complex mix of who adopts AI and how they use it according to the OECD.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Moderate and intentional use of AI for schoolwork and learning may be positively related to student performance according to the OECD.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Digital tools can support learning when used purposefully and in moderation according to the OECD.",
          "span": "[passage of 22 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Excessive or unguided use of digital tools can contribute to distraction and shallower engagement according to the OECD.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Learning does not occur through the consumption of content but as a productive cognitive struggle of the mind with new material according to the OECD.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Reading, mathematics and science scores have dropped since 2003.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "86% of students across OECD countries had used AI chatbots for at least one of the schoolwork purposes examined in the PISA assessment.",
          "span": "[passage of 22 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "14% of students across OECD countries had never or almost never used AI for any of the schoolwork purposes examined in the PISA assessment.",
          "span": "[passage of 18 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who do not use AI chatbots for schoolwork generally score higher than students who do according to PISA.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "About one in five students reported using AI almost every day.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who use AI almost every day tended to score lower in science than students who did not, accounting for socioeconomic status.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "A feedback loop exists for students who rely too heavily on AI.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The weaker a student's ability to read critically, the harder it may be to recognize when an AI-generated answer is incomplete or incorrect.",
          "span": "[passage of 23 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Routinely allowing AI to perform the reading, summarizing or reasoning could give students fewer opportunities to develop those skills.",
          "span": "[passage of 24 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Important skills attributed to critical thinking are declining.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The decline in skills for evaluating information, making connections across multiple sources, and thinking critically about what is read is most troubling in the AI age.",
          "span": "[passage of 30 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The share of hasty readers almost doubled between 2018 and 2025.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "In a world increasingly flooded with information, students are less likely to think deeply and separate signal from noise.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "the article"
        }
      ]
    },
    {
      "article": "A4",
      "propositions": [
        {
          "text": "Artificial intelligence is spreading in classrooms.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The impact of AI on learning depends less on the technology than on how students use it.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Hundreds of millions of primary and secondary students are starting their schools for the new academic year in September 2026.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing the students' learning process.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students and teachers are grappling with the question of what homework is for when an AI chatbot can finish it in seconds.",
          "span": "[passage of 21 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "China requires at least eight hours of AI instruction a year.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The United Arab Emirates has begun integrating AI into its curricula.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Saudi Arabia has begun integrating AI into its curricula.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Qatar has begun integrating AI into its curricula.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "AI chatbots can make learning faster and easier.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "David Stromberg of Stockholm University, Victor Lei and Yanhui Wu of the University of Hong Kong ran one of the largest studies of its kind tracking about 27,000 students aged 12 to 18 in China for 30 months.",
          "span": "[passage of 39 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The study combined data on homework, monthly closed-book exams and high-stakes entrance exams across nine subjects.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "After adopting generative AI, students' homework scores rose by 18 percent.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "After adopting generative AI, the time spent on each assignment fell by about 30 percent, from 64 minutes to 45 minutes on average.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "When the same students sat monthly exams without AI, their scores fell by 20 percent within six months.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students' performance in high-stakes entrance exams declined after adopting generative AI, with the full effect emerging over a longer period.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The OECD came to a similar conclusion in its Digital Education Outlook 2026 published in January.",
          "span": "[passage of 29 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Where generative AI is neither built to teach nor used under any structure, outsourcing tasks to the model improves performance with no real learning gains according to the OECD.",
          "span": "[passage of 27 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Research co-authored by Dragan Gasevic describes the potential erosion of productive cognitive effort as metacognitive laziness.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "How students use AI tools matters more than whether they use them.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "A survey by Ipsos for the Vodafone Foundation asked 7,000 students aged 12 to 17 across seven European countries how they use AI when studying outside school and without teacher instruction.",
          "span": "[passage of 31 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "56% of students surveyed by Ipsos for the Vodafone Foundation reported getting information as their most common use of AI.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "45% of students surveyed by Ipsos for the Vodafone Foundation used AI to have terms and concepts explained to them.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "31% of students surveyed by Ipsos for the Vodafone Foundation said they used AI to provide complete solutions to tasks.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "29% of students surveyed by Ipsos for the Vodafone Foundation used interactive or adaptive content to guide their learning.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "20% of students surveyed by Ipsos for the Vodafone Foundation used AI to create personalised learning plans and track their progress.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "For students, AI is becoming more than a tool for completing schoolwork.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "AI is increasingly part of the wider student experience, from getting instant help to finding someone to talk to.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The HEPI/Kortext Student Generative AI Survey 2026 was based on 1,054 full-time undergraduates in the United Kingdom.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "49% of undergraduates surveyed in the HEPI/Kortext Student Generative AI Survey 2026 believe AI has improved their student experience.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Undergraduates surveyed in the HEPI/Kortext Student Generative AI Survey 2026 pointed to saving time as a reason AI has improved their student experience.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Undergraduates surveyed in the HEPI/Kortext Student Generative AI Survey 2026 pointed to better understanding as a reason AI has improved their student experience.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Undergraduates surveyed in the HEPI/Kortext Student Generative AI Survey 2026 pointed to instant, personalised support as a reason AI has improved their student experience.",
          "span": "[passage of 3 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "59% of undergraduates surveyed in the HEPI/Kortext Student Generative AI Survey 2026 said AI made no difference to their loneliness.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "21% of undergraduates surveyed in the HEPI/Kortext Student Generative AI Survey 2026 felt less lonely due to AI.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "20% of undergraduates surveyed in the HEPI/Kortext Student Generative AI Survey 2026 felt more lonely due to AI.",
          "span": "[passage of 4 words]",
          "relation": "asserts",
          "source": "the article"
        }
      ]
    },
    {
      "article": "A5",
      "propositions": [
        {
          "text": "Allison Stanger is a political science professor at Middlebury College.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Allison Stanger openly admits she uses AI to help her write.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Allison Stanger wrote in The Wall Street Journal that AI used well can strengthen thinking.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "AI is a wonderful collaborator according to Allison Stanger.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger uses AI to think through things.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger uses AI to check the mechanics of her writing.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "All of Allison Stanger's ideas, openings and conclusions are her own.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger uses AI to explore things further.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Humans are best at judging what good writing is according to Allison Stanger.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "People write for humans according to Allison Stanger.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "AI is not going to get you to good writing according to Allison Stanger.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "You have to show your writing to another human to get to good writing according to Allison Stanger.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger always writes her own first drafts.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger always outlines her argument.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger goes back and forth with AI to make sure her argument is sound.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger has AI play devil's advocate.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "AI can be useful when finishing something in the middle of the night when you don't have another human to show it to yet according to Allison Stanger.",
          "span": "[passage of 30 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger worries that AI does kill creativity.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Part of the problem with AI is not with the technology but with the concentration of power according to Allison Stanger.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger has written a larger book about the concentration of power in AI.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "AI is extraordinarily useful according to Allison Stanger.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "AI is potentially very, very dangerous according to Allison Stanger.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "People still have to think for themselves according to Allison Stanger.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Teachers have to teach their students to think for themselves according to Allison Stanger.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "There has to be a power balance with AI according to Allison Stanger.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "The human has to keep pushing back against AI according to Allison Stanger.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "We have to find ways to enable power balance with AI according to Allison Stanger.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "AI is a pattern-recognizer according to Allison Stanger.",
          "span": "[passage of 4 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Anything you want to try to think about involves patterns according to Allison Stanger.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "AI can help you recognize something that's important to explore further according to Allison Stanger.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        }
      ]
    },
    {
      "article": "A6",
      "propositions": [
        {
          "text": "The effects of artificial intelligence on learning are still largely unclear.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Nearly 3-in-4 K-12 teachers surveyed believe AI has bigger implications for education than past innovations like the internet or computers.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The poll surveyed 545 K-12 teachers.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Many K-12 teachers are using AI to save time.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Many K-12 teachers are using AI to improve their teaching materials.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "A majority of K-12 teachers surveyed are worried AI is making it harder for students to learn to think for themselves.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Nearly 8-in-10 K-12 teachers surveyed think schools should teach responsible use of AI.",
          "span": "[passage of 18 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "A little more than half of K-12 teachers surveyed say the technology isn't being used in class by students at all.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "About 2-in-5 K-12 teachers surveyed say students are using AI in class at least once a week.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "6-in-10 K-12 teachers surveyed have used AI themselves to help with work tasks.",
          "span": "[passage of 18 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Michele Naber is a veteran biology teacher at El Toro High School in Orange County, California.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Michele Naber allows her students to use AI during certain lessons to teach them how to properly prompt chatbots and verify their accuracy.",
          "span": "[passage of 23 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber tells her students to ask ChatGPT to describe a particular animal's physical characteristics and habitat, then verify what the chatbot generated with reliable sources.",
          "span": "[passage of 25 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber's lesson shows students that AI still gets it wrong sometimes.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber has had success using AI to generate multiple choice questions for assessments.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Generating multiple choice questions normally would have taken Michele Naber probably upwards of an hour.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Using AI minimized the task of generating multiple choice questions to five minutes for Michele Naber.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "A majority of surveyed K-12 teachers who report using AI on work-related tasks say it saves them time.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "63% of surveyed K-12 teachers who report using AI on work-related tasks say that time savings equates to two hours or less per week.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Joann Purcell is a math teacher and instructional coach at Downers Grove North High School in the Chicago suburbs.",
          "span": "[passage of 18 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Joann Purcell has found AI useful for coming up with professional development activities for her fellow educators.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Joann Purcell doesn't use AI with her students.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Joann Purcell says AI isn't reliable enough to generate math questions.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "54% of surveyed K-12 teachers say AI makes it harder for students to learn critical thinking skills.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Christa Corricelli is a special education teacher at Saugus Middle/High School outside Boston.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Christa Corricelli says AI could be a valuable technology for learning.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Too often students are using AI as an answer machine rather than a tool to bolster their thinking according to Christa Corricelli.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Christa Corricelli thinks students who aren't already intrinsically self-motivated to be critical thinkers will see their critical thinking skills atrophy over time.",
          "span": "[passage of 41 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber feels a deep responsibility to teach her students that humans must always interrogate and verify what AI generates.",
          "span": "[passage of 21 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "55% of surveyed K-12 teachers think AI is mostly just a shortcut for students to avoid doing more work.",
          "span": "[passage of 23 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez is a special education teacher at Royal Palm Beach Community High School near Palm Beach, Florida.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez says AI can be especially helpful for students with disabilities.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "One of Ellie Rodriguez's students, who is on the autism spectrum, recently used AI to get help with an assignment.",
          "span": "[passage of 22 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez praised her student for using AI to get help with an assignment.",
          "span": "[passage of 3 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The student would not have been able to complete the assignment without the help AI provided according to Ellie Rodriguez.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez worries the technology could hamper learning for students who don't have disabilities or who are capable of doing assignments without the assistance of AI.",
          "span": "[passage of 27 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez and her colleagues, including some English teachers, are deeply concerned about the impact AI is having on students' ability to think for themselves.",
          "span": "[passage of 27 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Nearly 6-in-10 surveyed K-12 educators say AI is eroding the level of trust between students and teachers.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "About 4-in-10 surveyed K-12 teachers have required more assignments to be done by hand as a result of AI.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "About 4-in-10 surveyed K-12 teachers have required more assignments to be done in class as a result of AI.",
          "span": "[passage of 18 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "70% of surveyed K-12 teachers believe the public's perception of them has gotten worse.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Michele Naber offered extra credit to students who participated in beach cleanups and habitat restorations outside of school for years.",
          "span": "[passage of 39 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber's students only had to show her a picture to prove they were at beach cleanups and habitat restorations.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber's son showed her how easy it is to use AI to create a fake image of a registration table for a beach cleanup or habitat restoration event.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber had to stop offering extra credit for beach cleanups and habitat restorations because she can't verify the pictures.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber has modified her curriculum so that all lab work is done in class in front of her.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "For Michele Naber's students, homework matters far less for their grades.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Teachers are much more suspect of things that students do outside the classroom according to Christa Corricelli.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Josh Kauffman teaches seventh-grade English at Alabama Destinations Career Academy, a virtual public school that serves students across the state.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Josh Kauffman has noticed a substantial uptick in the number of AI-generated assignments his students submit.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Josh Kauffman can't require more in-class work because it's a virtual school.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Josh Kauffman tries to persuade his students that there's value in their own writing.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Joann Purcell doesn't necessarily think AI has eroded trust.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Students found ways to cheat on assignments long before AI came along according to Joann Purcell.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Teachers need to be creative in how they use AI according to Joann Purcell.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Teachers need to force kids to think with AI just like they would with any other tool according to Joann Purcell.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Many K-12 educators are having to adapt to AI with little guidance from their school or district.",
          "span": "[passage of 21 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Among K-12 teachers whose school provides AI software, only 35% say they have a formal policy on teacher use of AI.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "About half of all surveyed K-12 teachers say their school hasn't offered any guidance on AI, or they're not sure what the guidance is.",
          "span": "[passage of 23 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Only about 4-in-10 surveyed K-12 teachers say their school offers professional development or training related to AI.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez hasn't received any training on AI technology.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez wishes she could receive training on AI technology.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Schools need to teach educators how to apply AI information to what they do according to Ellie Rodriguez.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Schools need to teach educators how to teach differently to account for the flexibility and resources that AI can make available according to Ellie Rodriguez.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Josh Kauffman agrees that there isn't enough attention being paid to how to teach what we are teaching differently to account for the flexibility and resources that AI can make available.",
          "span": "[passage of 32 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Christa Corricelli isn't totally surprised by the lack of training.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Schools are often slow to adapt to change according to Christa Corricelli.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The slow adaptation of schools to change has been a challenge for educators according to Christa Corricelli.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "the article"
        }
      ]
    }
  ]
}
```
````

</details>

<details><summary>Haiku 4.5, temperature 1 · Round 1 · 16 October 2026, 13:10</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (4846 words)

```text
The following 6 news articles are labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A3: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A6: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]




Task: for each article, list the propositions about the world that it contains.

A proposition is a single claim about the world that an article states or reports: what happened or is the case, what a number is, what a rule or status is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each proposition contains exactly one claim. Test every proposition before you list it: if it can be divided into two statements, each of which could be true while the other is false, divide it and list both. Two numbers, two findings, a finding and a second finding about its size or timing, or a fact and a comment on it are two claims. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal claim (A causes B) is one proposition only when the causal link is the claim.
2. Each proposition must stand on its own: a reader who has not seen the article must be able to understand it. Resolve pronouns, give full names, and include the time, place and population when the claim's truth depends on them. Add nothing else.
3. State the proposition as a claim about the world, not about the article. When an article reports a claim made by a person or a study, state the claim itself and record the source in "relation" and "source"; do not write "the article says".
4. Keep the article's meaning. Do not strengthen, weaken, generalise or soften the claim.
5. Leave out rhetorical flourishes, questions, and claims whose meaning cannot be resolved from the article.
6. Each proposition must come from the article it is listed under. Copy, character for character, the shortest passage of that article that states it ("span").
7. List every proposition the article contains. Do not list the same proposition twice in different words.

For each proposition, give "relation": "asserts" (the article states it in its own voice), "reports" (the article reports a person, group or study saying it), or "hedges" (the article states it with doubt or qualification), and "source": who makes the claim (a person, group or study as named in the article, or "the article" when it is the article's own voice).

Return JSON of the form {"articles": [{"article": "<label>", "propositions": [{"text": "<proposition>", "span": "<exact passage>", "relation": "asserts|reports|hedges", "source": "<who>"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (9853 words)

````text
```json
{
  "articles": [
    {
      "article": "A1",
      "propositions": [
        {
          "text": "Georgia Tech is welcoming its incoming freshman class to campus in the week of August 20, 2026.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Georgia Tech is known for its computer science, engineering and other STEM programs.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing the industries of computer science, engineering and other STEM fields.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing how professors plan their lessons.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Nearly 15,000 students are majoring in or minoring in AI-related fields, including computer science, at Georgia Tech.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Georgia Tech recognizes that artificial intelligence is changing STEM industries.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Some Georgia Tech professors are building their own AI agents that serve as tutors for classes.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Some Georgia Tech professors are rethinking assignments so that instead of requiring essays, they require in-class discussion.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Artificial intelligence can help students complete some tasks more quickly.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "The traditional model of attending college for four years followed by a 40-year career has been obsolete for a while.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Artificial intelligence can help people formulate an idea and write software faster than without it.",
          "span": "[passage of 35 words]",
          "relation": "reports",
          "source": "David Joyner"
        }
      ]
    },
    {
      "article": "A2",
      "propositions": [
        {
          "text": "High-school students across Asia are pulling ahead of their Western peers in an annual global assessment.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence spurs a worldwide race for talent and reshapes how young people learn.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Reading, science and math performance among 15-year-olds has continued a decline globally across the board between 2022 and 2025.",
          "span": "[passage of 28 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The 2025 Programme for International Student Assessment was released by the Organisation for Economic Co-operation and Development.",
          "span": "[passage of 18 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students in the Chinese cities of Beijing and Shanghai were among last year's top performers in the 2025 PISA assessment.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students in the Chinese provinces Jiangsu and Zhejiang were among last year's top performers in the 2025 PISA assessment.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students in the city-state of Singapore were among last year's top performers in the 2025 PISA assessment.",
          "span": "[passage of 4 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Japan and South Korea were in the Asia-dominated top 10 in the 2025 PISA assessment across all three subjects.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The semi-autonomous Chinese city of Macao was in the top 10 in the 2025 PISA assessment across all three subjects.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The self-governing democracy of Taiwan was in the top 10 in the 2025 PISA assessment across all three subjects.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Secondary students in the United States saw their reading scores fall close to 25-year lows in the 2025 PISA assessment.",
          "span": "[passage of 14 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Secondary students in the United States lag more starkly behind their counterparts in China in the 2025 PISA assessment.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The four major Chinese jurisdictions that submitted 2025 PISA test scores are Beijing, Shanghai, Jiangsu, and Zhejiang.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Exam results in the 2025 PISA assessment come amid an intensifying rivalry between the United States and China to outpace the other in technological advancement.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Exam results in the 2025 PISA assessment come amid a rivalry between the United States and China to direct more funding toward innovation.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "China has surpassed the United States in published scientific reports.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "China has surpassed the United States in research spending.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Both the United States and China exceeded $1 trillion in research spending in 2024.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The growing adoption of artificial intelligence could significantly impact secondary education.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Evaluating information is one of the skills that matters most in the AI age.",
          "span": "[passage of 30 words]",
          "relation": "reports",
          "source": "Andreas Schleicher"
        },
        {
          "text": "Making connections across multiple sources is one of the skills that matters most in the AI age.",
          "span": "[passage of 30 words]",
          "relation": "reports",
          "source": "Andreas Schleicher"
        },
        {
          "text": "Thinking critically about what is read is one of the skills that matters most in the AI age.",
          "span": "[passage of 30 words]",
          "relation": "reports",
          "source": "Andreas Schleicher"
        },
        {
          "text": "The skills of evaluating information, making connections across multiple sources, and thinking critically are in decline.",
          "span": "[passage of 30 words]",
          "relation": "reports",
          "source": "Andreas Schleicher"
        },
        {
          "text": "In a world increasingly flooded with information, students are less likely to think deeply.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Andreas Schleicher"
        },
        {
          "text": "In a world increasingly flooded with information, students are less likely to separate signal from noise.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Andreas Schleicher"
        },
        {
          "text": "The 2025 PISA test data for China includes only students from the provinces of Shanghai, Beijing, Jiangsu and Zhejiang, some of the country's wealthiest eastern coastal areas.",
          "span": "[passage of 36 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The 2025 PISA testing has shown a continued drop in United States scores over the last decade.",
          "span": "[passage of 14 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Continued drops in United States scores over the last decade have alarmed many educationalists.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "As technology has progressed, student performance has become less linked with national or family wealth.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Higher digital distraction in the classroom is one challenge identified in the 2025 PISA report.",
          "span": "[passage of 29 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Among students from China, Japan and South Korea, fewer than 10% reported that their peers were distracted by digital devices during science lessons.",
          "span": "[passage of 23 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The global average percentage of students who reported that their peers were distracted by digital devices during science lessons is 28%.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Singapore used technology in its classrooms but also emphasized reading comprehension early on.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The proportion of students who are 'hasty readers' nearly doubled between 2018 and 2025.",
          "span": "[passage of 22 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Hasty readers are students who rush through their texts and give incorrect answers.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "As the average performance among OECD countries in science, reading and math has reached record lows, this could have broader economic implications among the world's biggest nations.",
          "span": "[passage of 27 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Performance meeting a basic level of aptitude in PISA among all 15-year-old Americans could add over $40 trillion to the United States economy over their working lives.",
          "span": "[passage of 34 words]",
          "relation": "reports",
          "source": "Stanford University"
        },
        {
          "text": "The percentage of OECD students below the baseline performance level was 16% in 2022.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The percentage of OECD students below the baseline performance level was 20% in 2025.",
          "span": "[passage of 14 words]",
          "relation": "asserts",
          "source": "the article"
        }
      ]
    },
    {
      "article": "A3",
      "propositions": [
        {
          "text": "The OECD's latest Program for International Student Assessment found that artificial intelligence has led to a decline in multiple student skills.",
          "span": "[passage of 21 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The OECD's latest Program for International Student Assessment found that artificial intelligence has led to a drop in test scores.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Moderate use of artificial intelligence is associated with stronger performance in certain subjects compared to limited or daily use.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who used artificial intelligence from about once a month to once or twice a week recorded higher average science scores than both students who rarely used AI and those who used it almost every day.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The advantage in science scores for moderate artificial intelligence use was especially clear when students used AI to summarize assigned reading.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The advantage in science scores for moderate artificial intelligence use was especially clear when students used AI to conduct preliminary research on a new topic.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who reported using artificial intelligence for summarizing assigned reading or conducting preliminary research on a new topic weekly tended to perform at about the same level as AI nonusers after accounting for socioeconomic status.",
          "span": "[passage of 25 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who used artificial intelligence almost every day tended to have lower science scores than weekly or non-users.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who rarely used artificial intelligence tended to have lower science scores than moderate users.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The observed relationships between artificial intelligence use frequency and science performance may reflect a complex mix of who adopts AI and how they use it.",
          "span": "[passage of 30 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Moderate and intentional use of artificial intelligence for schoolwork and learning may be positively related to student performance.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Digital tools can support learning when used purposefully and in moderation.",
          "span": "[passage of 22 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Excessive or unguided use of digital tools can contribute to distraction and shallower engagement.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Learning does not occur through the consumption of content.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Learning occurs as a productive cognitive struggle of the mind with new material.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Reading, mathematics and science scores have dropped since 2003.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "86% of students across OECD countries had used AI chatbots for at least one of the schoolwork purposes examined in the 2025 PISA assessment.",
          "span": "[passage of 27 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "14% of students across OECD countries said they had never or almost never used AI for any of the schoolwork purposes examined in the 2025 PISA assessment.",
          "span": "[passage of 18 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who do not use artificial intelligence chatbots for schoolwork generally score higher than students who do.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "About one in five students across OECD countries reported using artificial intelligence chatbots almost every day.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students who use artificial intelligence chatbots almost every day tended to score lower in science than students who did not, accounting for socioeconomic status.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "A student's ability to read critically is related to their ability to recognize when an AI-generated answer is incomplete or incorrect.",
          "span": "[passage of 23 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Routinely allowing artificial intelligence to perform reading, summarizing or reasoning could give students fewer opportunities to develop those skills.",
          "span": "[passage of 24 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Skills attributed to critical thinking are declining.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The share of 'hasty readers'—students who rush through texts and give quick but incorrect answers—almost doubled between 2018 and 2025.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "In a world increasingly flooded with information, students are less likely to think deeply and separate signal from noise.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "the article"
        }
      ]
    },
    {
      "article": "A4",
      "propositions": [
        {
          "text": "Artificial intelligence's impact on learning depends less on the technology than on how students use it.",
          "span": "[passage of 22 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Hundreds of millions of primary and secondary students are starting school for the new academic year in the month the article was written.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing the learning process for students and teachers.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Students and teachers are grappling with the question of what homework is for when an AI chatbot can finish it in seconds.",
          "span": "[passage of 21 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "China requires at least eight hours of artificial intelligence instruction per year.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The United Arab Emirates has begun integrating artificial intelligence into its curricula.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Saudi Arabia has begun integrating artificial intelligence into its curricula.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Qatar has begun integrating artificial intelligence into its curricula.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence chatbots can make learning faster.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence chatbots can make learning easier.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "David Stromberg of Stockholm University, Victor Lei and Yanhui Wu of the University of Hong Kong conducted one of the largest studies tracking artificial intelligence use by students.",
          "span": "[passage of 29 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The study by Stromberg, Lei and Wu tracked about 27,000 students aged 12 to 18 in China for 30 months.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The study combined data on homework, monthly closed-book exams and high-stakes entrance exams across nine subjects.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "After adopting generative artificial intelligence, students' homework scores rose by 18 percent.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The time spent on each assignment fell by about 30 percent after adopting generative artificial intelligence.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Before adopting generative artificial intelligence, students spent an average of 64 minutes on each assignment.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "After adopting generative artificial intelligence, students spent an average of 45 minutes on each assignment.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "When the same students who adopted generative artificial intelligence sat monthly exams without artificial intelligence, their scores fell by 20 percent within six months.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The performance of students in high-stakes entrance exams declined after adopting generative artificial intelligence, with the full effect emerging over a longer period.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The Organisation for Economic Co-operation and Development published a Digital Education Outlook 2026.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The Digital Education Outlook 2026 was published in January 2026.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "According to the OECD Digital Education Outlook 2026, when generative artificial intelligence is neither built to teach nor used under any structure, outsourcing tasks to the model improves performance with no real learning gains.",
          "span": "[passage of 27 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Research has described the potential erosion of productive cognitive effort as 'metacognitive laziness'.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "How students use artificial intelligence tools matters more than whether they use them.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "A survey by Ipsos for the Vodafone Foundation asked 7,000 students aged 12 to 17 across seven European countries how they use artificial intelligence when studying outside school.",
          "span": "[passage of 31 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The most common use of artificial intelligence among the surveyed students was getting information, reported by 56 percent of students.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "45 percent of the surveyed students used artificial intelligence to have terms and concepts explained to them.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "31 percent of the surveyed students said they used artificial intelligence to provide complete solutions to tasks.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "29 percent of the surveyed students used interactive or adaptive content to guide their learning.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Only 20 percent of the surveyed students used artificial intelligence to create personalised learning plans and track their progress.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is becoming more than a tool for completing schoolwork for students.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is increasingly part of the wider student experience, from getting instant help to finding someone to talk to.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The HEPI/Kortext Student Generative AI Survey 2026 was based on 1,054 full-time undergraduates in the United Kingdom.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "49 percent of surveyed undergraduates in the United Kingdom believe artificial intelligence has improved their student experience.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Surveyed undergraduates who believed artificial intelligence improved their student experience pointed to saving time.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Surveyed undergraduates who believed artificial intelligence improved their student experience pointed to better understanding.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Surveyed undergraduates who believed artificial intelligence improved their student experience pointed to instant, personalised support.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Most surveyed undergraduates, 59 percent, said artificial intelligence made no difference to their loneliness.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "21 percent of surveyed undergraduates felt less lonely because of artificial intelligence.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "20 percent of surveyed undergraduates felt more lonely because of artificial intelligence.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "the article"
        }
      ]
    },
    {
      "article": "A5",
      "propositions": [
        {
          "text": "Middlebury College political science professor Allison Stanger uses artificial intelligence to help her write.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Allison Stanger wrote in The Wall Street Journal that artificial intelligence used well can strengthen thinking.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is a wonderful collaborator according to Allison Stanger.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger uses artificial intelligence to think through things.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger uses artificial intelligence to check the mechanics of her writing.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger's ideas, openings and conclusions are her own.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger uses artificial intelligence to explore things further.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Artificial intelligence is miraculous according to Allison Stanger.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Anyone who criticizes artificial intelligence without a simultaneous sense of wonder at what has been accomplished is missing something important according to Allison Stanger.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger always writes her own first drafts.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger always outlines her argument.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger goes back and forth with artificial intelligence to make sure her argument is sound.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger has artificial intelligence play devil's advocate.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Humans are best at judging what good writing is according to Allison Stanger.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Humans are writing for humans according to Allison Stanger.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Artificial intelligence is not going to get you to the final product according to Allison Stanger.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger needs to show her work to another human according to Allison Stanger.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Artificial intelligence can be useful when finishing something in the middle of the night according to Allison Stanger.",
          "span": "[passage of 31 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger worries that artificial intelligence kills creativity.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Part of the problem with artificial intelligence is not with the technology but with the concentration of power according to Allison Stanger.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Allison Stanger has written a larger book about the concentration of power in artificial intelligence.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Artificial intelligence is extraordinarily useful according to Allison Stanger.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Artificial intelligence is potentially very dangerous according to Allison Stanger.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Humans still have to think for themselves according to Allison Stanger.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Students have to be taught to think for themselves according to Allison Stanger.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "There must be a power balance with artificial intelligence according to Allison Stanger.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Exactly there has to be a power balance with artificial intelligence according to Allison Stanger.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "There are dangers if there is not a power balance with artificial intelligence according to Allison Stanger.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Artificial intelligence is a pattern-recognizer according to Allison Stanger.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        },
        {
          "text": "Artificial intelligence can help recognize things that are important to explore further according to Allison Stanger.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "Allison Stanger"
        }
      ]
    },
    {
      "article": "A6",
      "propositions": [
        {
          "text": "The effects of artificial intelligence on learning are still largely unclear.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Nearly 3-in-4 K-12 teachers surveyed believe artificial intelligence has bigger implications for education than past innovations like the internet or computers.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The poll surveyed 545 K-12 teachers who were nationally representative.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Many surveyed teachers are using artificial intelligence to save time.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Many surveyed teachers are using artificial intelligence to improve their teaching materials.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "A majority of surveyed teachers are worried artificial intelligence is making it harder for students to learn to think for themselves.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Teachers feel that artificial intelligence is going to fundamentally reshape the future of education moving forward.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Mallory Newall"
        },
        {
          "text": "Teachers have serious concerns about artificial intelligence's impact on how they relate to their students.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Teachers have serious concerns about artificial intelligence's impact on how students relate to each other.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Nearly 8-in-10 surveyed teachers think schools should teach responsible use of artificial intelligence.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The teacher poll shows students aren't widely using artificial intelligence in the classroom at least as of June 2026.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "A little more than half of surveyed teachers say artificial intelligence isn't being used in class by students at all.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "About 2-in-5 of surveyed teachers say students are using artificial intelligence in class at least once a week.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "A majority of surveyed teachers, 6-in-10, have used artificial intelligence themselves to help with work tasks.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber is a biology teacher at El Toro High School in Orange County, California.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Michele Naber allows her students to use artificial intelligence during certain lessons to teach them how to properly prompt chatbots.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber allows her students to use artificial intelligence to teach them to verify its accuracy.",
          "span": "[passage of 4 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber tells her students to ask ChatGPT to describe a particular animal's physical characteristics and habitat, then verify what the chatbot generated with reliable sources.",
          "span": "[passage of 27 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber says the lesson shows students that artificial intelligence still gets it wrong sometimes.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber has had success using artificial intelligence to generate multiple choice questions for assessments.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Generating multiple choice questions for assessments normally takes a teacher upwards of an hour.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "Michele Naber"
        },
        {
          "text": "Artificial intelligence minimized the task of generating multiple choice questions to five minutes.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "Michele Naber"
        },
        {
          "text": "A majority of surveyed teachers who report using artificial intelligence on work-related tasks say it saves them time.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Most surveyed teachers who report using artificial intelligence say the time savings equates to two hours or less per week.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Joann Purcell is a math teacher at Downers Grove North High School in the Chicago suburbs.",
          "span": "[passage of 18 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Joann Purcell is an instructional coach at Downers Grove North High School in the Chicago suburbs.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Joann Purcell has found artificial intelligence useful for coming up with professional development activities for educators.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Joann Purcell doesn't use artificial intelligence with her students.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Joann Purcell says artificial intelligence isn't reliable enough to generate math questions.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Joann Purcell says it is a pain to go through artificial intelligence generated math questions to see where the mistakes are.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "Joann Purcell"
        },
        {
          "text": "Joann Purcell says if she has to go through and check artificial intelligence generated math questions for mistakes, she might as well write the question herself.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "Joann Purcell"
        },
        {
          "text": "More than half, 54%, of surveyed teachers say artificial intelligence makes it harder for students to learn critical thinking skills.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Christa Corricelli is a special education teacher at Saugus Middle/High School outside Boston.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence could be a valuable technology for learning according to Christa Corricelli.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Too often students are using artificial intelligence as an answer machine rather than a tool to bolster their thinking according to Christa Corricelli.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Critical thinking skills will atrophy over time for students who aren't already intrinsically self-motivated to be critical thinkers according to Christa Corricelli.",
          "span": "[passage of 41 words]",
          "relation": "reports",
          "source": "Christa Corricelli"
        },
        {
          "text": "Michele Naber feels a deep responsibility to teach her students that humans must always interrogate and verify what artificial intelligence generates.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber wants her students to be able to look at the world and figure out things for themselves rather than rely on a piece of software.",
          "span": "[passage of 29 words]",
          "relation": "reports",
          "source": "Michele Naber"
        },
        {
          "text": "If people stop questioning what artificial intelligence says, they can be led to believe anything according to Michele Naber.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "Michele Naber"
        },
        {
          "text": "The possibility of being led to believe anything by artificial intelligence is what really scares Michele Naber.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "Michele Naber"
        },
        {
          "text": "More than half of surveyed teachers, 55%, think artificial intelligence is mostly just a shortcut for students to avoid doing more work.",
          "span": "[passage of 23 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez is a special education teacher at Royal Palm Beach Community High School near Palm Beach, Florida.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence can be especially helpful for students with disabilities according to Ellie Rodriguez.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "One of Ellie Rodriguez's students, who is on the autism spectrum, recently used artificial intelligence to get help with an assignment.",
          "span": "[passage of 22 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez praised her student for using artificial intelligence to get help with an assignment.",
          "span": "[passage of 3 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The student would not have been able to complete the assignment without the help artificial intelligence provided according to Ellie Rodriguez.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence got the student to do the work according to Ellie Rodriguez.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "Ellie Rodriguez"
        },
        {
          "text": "Artificial intelligence helped the student apply using resources like encyclopedias and library books according to Ellie Rodriguez.",
          "span": "[passage of 29 words]",
          "relation": "reports",
          "source": "Ellie Rodriguez"
        },
        {
          "text": "Ellie Rodriguez worries the technology of artificial intelligence could hamper learning for students who don't have disabilities.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez worries artificial intelligence could hamper learning for students capable of doing assignments without the assistance of artificial intelligence.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez and her colleagues are deeply concerned about the impact artificial intelligence is having on students' ability to think for themselves.",
          "span": "[passage of 27 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Nearly 6-in-10 surveyed educators say artificial intelligence is eroding the level of trust between students and teachers.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "About 4-in-10 surveyed educators say they've required more assignments to be done by hand as a result of artificial intelligence.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "About 4-in-10 surveyed educators say they've required more assignments to be done in class as a result of artificial intelligence.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The erosion of trust caused by artificial intelligence is one of the biggest red flags in survey data according to Mallory Newall.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "Mallory Newall"
        },
        {
          "text": "70% of surveyed teachers believe the public's perception of them has gotten worse.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "The erosion of trust caused by artificial intelligence is compounded by the finding that teachers believe the public's perception of them has gotten worse according to Mallory Newall.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "Mallory Newall"
        },
        {
          "text": "Teachers are trying to navigate complex challenges in an environment that is already rife with mistrust according to Mallory Newall.",
          "span": "[passage of 24 words]",
          "relation": "reports",
          "source": "Mallory Newall"
        },
        {
          "text": "Michele Naber has had to adapt to how easy it is to use artificial intelligence to create fake images.",
          "span": "[passage of 82 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber had to stop offering extra credit for beach cleanups and habitat restorations because she can't verify the pictures.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "Michele Naber"
        },
        {
          "text": "Michele Naber says it was sad that she had to stop offering extra credit for beach cleanups and habitat restorations because she can't verify the pictures.",
          "span": "[passage of 3 words]",
          "relation": "reports",
          "source": "Michele Naber"
        },
        {
          "text": "Michele Naber has modified her curriculum so that all lab work is done in class in front of her.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Michele Naber has modified her grading so that homework matters far less for students' grades.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Teachers are much more suspect of things that students do outside the classroom as a result of artificial intelligence.",
          "span": "[passage of 35 words]",
          "relation": "reports",
          "source": "Christa Corricelli"
        },
        {
          "text": "Josh Kauffman teaches seventh-grade English at Alabama Destinations Career Academy, a virtual public school that serves students across the state.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Josh Kauffman has noticed a substantial uptick in the number of artificial intelligence-generated assignments his students submit.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Josh Kauffman cannot require more in-class work because he teaches at a virtual school.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Josh Kauffman tries to persuade his students that there's value in their own writing.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Josh Kauffman would rather deal with his students' typos and know they are theirs than wonder how much they are standing on other people's shoulders.",
          "span": "[passage of 34 words]",
          "relation": "reports",
          "source": "Josh Kauffman"
        },
        {
          "text": "Joann Purcell doesn't think artificial intelligence has eroded trust between teachers and students.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Students found ways to cheat on assignments long before artificial intelligence came along according to Joann Purcell.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Teachers need to be creative in how they use artificial intelligence according to Joann Purcell.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Joann Purcell"
        },
        {
          "text": "Teachers need to force kids to think with artificial intelligence just like they would with any other tool according to Joann Purcell.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "Joann Purcell"
        },
        {
          "text": "Many educators are having to adapt to artificial intelligence with little guidance from their school or district.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Among teachers whose school provides artificial intelligence software, only 35% say they have a formal policy on teacher use of artificial intelligence.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Schools are more often providing artificial intelligence tools without a formal policy for their use.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "About half of all surveyed teachers say their school hasn't offered any guidance on artificial intelligence.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "About half of all surveyed teachers say they're not sure what their school's guidance on artificial intelligence is.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Teachers are looking for additional guidance from their district and from their students on what artificial intelligence is going to mean for the future of education according to Mallory Newall.",
          "span": "[passage of 28 words]",
          "relation": "reports",
          "source": "Mallory Newall"
        },
        {
          "text": "Only about 4-in-10 surveyed teachers say their school offers professional development or training related to artificial intelligence.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez hasn't received any training on artificial intelligence.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Ellie Rodriguez wishes she could receive training on artificial intelligence.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Teachers need to be taught how to apply artificial intelligence information to what they do according to Ellie Rodriguez.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "Ellie Rodriguez"
        },
        {
          "text": "Teachers need to be taught how to apply artificial intelligence to how they teach according to Ellie Rodriguez.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "Ellie Rodriguez"
        },
        {
          "text": "Josh Kauffman says there isn't enough attention being paid to how to teach what educators are teaching differently to account for the flexibility and resources that artificial intelligence can make available.",
          "span": "[passage of 30 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Christa Corricelli isn't totally surprised by the lack of training on artificial intelligence.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Schools are often slow to adapt to change according to Christa Corricelli.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "Being slow to adapt to change has been a challenge for educators according to Christa Corricelli.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "the article"
        },
        {
          "text": "All educators are just trying not to drown with artificial intelligence according to Christa Corricelli.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "Christa Corricelli"
        }
      ]
    }
  ]
}
```
````

</details>

<details><summary>Sonnet 5.5 · Round 1 · 16 October 2026, 12:47</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (4846 words)

```text
The following 6 news articles are labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A3: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A6: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]




Task: for each article, list the propositions about the world that it contains.

A proposition is a single claim about the world that an article states or reports: what happened or is the case, what a number is, what a rule or status is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each proposition contains exactly one claim. Test every proposition before you list it: if it can be divided into two statements, each of which could be true while the other is false, divide it and list both. Two numbers, two findings, a finding and a second finding about its size or timing, or a fact and a comment on it are two claims. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal claim (A causes B) is one proposition only when the causal link is the claim.
2. Each proposition must stand on its own: a reader who has not seen the article must be able to understand it. Resolve pronouns, give full names, and include the time, place and population when the claim's truth depends on them. Add nothing else.
3. State the proposition as a claim about the world, not about the article. When an article reports a claim made by a person or a study, state the claim itself and record the source in "relation" and "source"; do not write "the article says".
4. Keep the article's meaning. Do not strengthen, weaken, generalise or soften the claim.
5. Leave out rhetorical flourishes, questions, and claims whose meaning cannot be resolved from the article.
6. Each proposition must come from the article it is listed under. Copy, character for character, the shortest passage of that article that states it ("span").
7. List every proposition the article contains. Do not list the same proposition twice in different words.

For each proposition, give "relation": "asserts" (the article states it in its own voice), "reports" (the article reports a person, group or study saying it), or "hedges" (the article states it with doubt or qualification), and "source": who makes the claim (a person, group or study as named in the article, or "the article" when it is the article's own voice).

Return JSON of the form {"articles": [{"article": "<label>", "propositions": [{"text": "<proposition>", "span": "<exact passage>", "relation": "asserts|reports|hedges", "source": "<who>"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (3135 words)

```text
{"articles":[{"article":"A1","propositions":[{"text":"Georgia Tech is welcoming its incoming freshman class to campus this week.","span":"[passage of 12 words]","relation":"asserts","source":"the article"},{"text":"Georgia Tech is known for its computer science, engineering and other STEM programs.","span":"[passage of 13 words]","relation":"asserts","source":"the article"},{"text":"Artificial intelligence is changing STEM industries and how Georgia Tech approaches its curriculum.","span":"[passage of 15 words]","relation":"asserts","source":"the article"},{"text":"Nearly 15,000 Georgia Tech students are majoring or minoring in AI-related fields, including computer science.","span":"[passage of 14 words]","relation":"reports","source":"David Joyner"},{"text":"Some Georgia Tech professors are building their own AI agents that serve as tutors for classes.","span":"[passage of 17 words]","relation":"reports","source":"David Joyner"},{"text":"Many Georgia Tech faculty are replacing take-home essay assignments with in-class discussion because assigning a 10-page essay is no longer sufficient.","span":"[passage of 24 words]","relation":"reports","source":"David Joyner"},{"text":"The old model of going to college for four years and then having a 40-year career has been dead for a while.","span":"[passage of 23 words]","relation":"reports","source":"David Joyner"},{"text":"AI gives students a new tool to complete tasks such as building software faster.","span":"[passage of 19 words]","relation":"reports","source":"David Joyner"}]},{"article":"A2","propositions":[{"text":"High-school students across Asia are pulling ahead of their Western peers in an annual global assessment.","span":"[passage of 16 words]","relation":"asserts","source":"the article"},{"text":"Reading, science and math performance among 15-year-olds declined globally across the board in the 2025 PISA.","span":"[passage of 15 words]","relation":"reports","source":"OECD PISA 2025"},{"text":"Students in Beijing, Shanghai, Jiangsu, Zhejiang and Singapore were among the top performers in the 2025 PISA.","span":"[passage of 25 words]","relation":"asserts","source":"the article"},{"text":"Japan, South Korea, Macao and Taiwan were also in the Asia-dominated top 10 across all three subjects.","span":"[passage of 29 words]","relation":"asserts","source":"the article"},{"text":"US secondary students' reading scores fell close to 25-year lows.","span":"[passage of 14 words]","relation":"asserts","source":"the article"},{"text":"China has surpassed the US in published scientific reports and research spending.","span":"[passage of 14 words]","relation":"asserts","source":"the article"},{"text":"Both China and the US spent over $1 trillion on research in 2024.","span":"[passage of 9 words]","relation":"asserts","source":"the article"},{"text":"The growing adoption of AI could significantly impact secondary education.","span":"[passage of 14 words]","relation":"hedges","source":"PISA report"},{"text":"The decline in skills such as evaluating information, connecting multiple sources and critical thinking is the most troubling trend in the AI age.","span":"[passage of 30 words]","relation":"reports","source":"Andreas Schleicher"},{"text":"The Chinese PISA data is criticised because only four wealthy eastern coastal provinces took part.","span":"[passage of 36 words]","relation":"reports","source":"critics"},{"text":"US PISA scores have continued to drop over the last decade, alarming many educationalists.","span":"[passage of 18 words]","relation":"asserts","source":"the article"},{"text":"As technology has progressed, student performance has become less linked with national or family wealth.","span":"[passage of 19 words]","relation":"reports","source":"PISA report"},{"text":"The study identified higher digital distraction in the classroom as one challenge.","span":"[passage of 12 words]","relation":"reports","source":"PISA report"},{"text":"Fewer than 10% of students in China, Japan and South Korea reported peers being distracted by digital devices in science lessons, versus a global average of 28%.","span":"[passage of 30 words]","relation":"reports","source":"PISA report"},{"text":"Singapore uses technology in classrooms but emphasizes reading comprehension early on.","span":"[passage of 16 words]","relation":"reports","source":"PISA report"},{"text":"The proportion of hasty readers nearly doubled between 2018 and 2025.","span":"[passage of 22 words]","relation":"reports","source":"PISA report"},{"text":"Average OECD performance in science, reading and math reached record lows.","span":"[passage of 15 words]","relation":"asserts","source":"the article"},{"text":"Basic-level PISA aptitude among all 15-year-old Americans could add over $40 trillion to the US economy over their working lives.","span":"[passage of 25 words]","relation":"reports","source":"Stanford University study"},{"text":"The percentage of OECD students below baseline performance rose to 20% in 2025 from 16% in 2022.","span":"[passage of 18 words]","relation":"reports","source":"PISA report"}]},{"article":"A3","propositions":[{"text":"PISA found that AI has led to a decline in multiple student skills and a drop in test scores.","span":"[passage of 20 words]","relation":"reports","source":"OECD PISA"},{"text":"Moderate AI use is associated with stronger performance in certain subjects than limited or daily use.","span":"[passage of 16 words]","relation":"reports","source":"OECD PISA"},{"text":"Students who used AI about once a month to once or twice a week had higher average science scores than both rare and near-daily users.","span":"[passage of 34 words]","relation":"reports","source":"OECD PISA"},{"text":"The advantage of moderate use was especially clear when students used AI to summarize reading or conduct preliminary research.","span":"[passage of 21 words]","relation":"reports","source":"OECD PISA"},{"text":"Students who used AI weekly to summarize reading performed about the same as non-users after accounting for socioeconomic status.","span":"[passage of 25 words]","relation":"reports","source":"OECD PISA"},{"text":"The relationships between AI use and science performance may reflect who adopts AI and how, rather than a negative impact of AI.","span":"[passage of 30 words]","relation":"hedges","source":"OECD PISA study"},{"text":"Digital tools can support learning when used purposefully and in moderation, but excessive or unguided use can contribute to distraction and shallower engagement.","span":"[passage of 23 words]","relation":"reports","source":"OECD"},{"text":"Learning occurs through productive cognitive struggle with new material, not through consuming content.","span":"[passage of 24 words]","relation":"reports","source":"OECD PISA findings"},{"text":"Reading, mathematics and science scores have dropped since 2003, so lower scores are not all due to AI.","span":"[passage of 13 words]","relation":"reports","source":"PISA"},{"text":"86% of students across OECD countries had used AI chatbots for at least one schoolwork purpose examined.","span":"[passage of 22 words]","relation":"reports","source":"PISA"},{"text":"14% of OECD students said they never or almost never used AI for any of the schoolwork purposes.","span":"[passage of 17 words]","relation":"reports","source":"PISA"},{"text":"Students who do not use AI chatbots for schoolwork generally score higher than students who do.","span":"[passage of 19 words]","relation":"reports","source":"PISA"},{"text":"About one in five students reported using AI almost every day.","span":"[passage of 10 words]","relation":"reports","source":"PISA"},{"text":"Near-daily AI users tended to score lower in science than non-users, accounting for socioeconomic status.","span":"[passage of 17 words]","relation":"reports","source":"PISA"},{"text":"Students who rely heavily on AI may fall into a feedback loop where weaker critical reading makes it harder to spot flawed AI answers and AI doing the reading reduces chances to develop those skills.","span":"[passage of 23 words]","relation":"hedges","source":"the article"},{"text":"Skills attributed to critical thinking are declining, and the share of hasty readers almost doubled between 2018 and 2025.","span":"[passage of 20 words]","relation":"reports","source":"PISA report"}]},{"article":"A4","propositions":[{"text":"The impact of AI in classrooms depends less on the technology than on how students use it.","span":"[passage of 15 words]","relation":"asserts","source":"the article"},{"text":"China requires at least eight hours of AI instruction a year.","span":"[passage of 11 words]","relation":"asserts","source":"the article"},{"text":"The UAE, Saudi Arabia and Qatar have begun integrating AI into their curricula.","span":"[passage of 16 words]","relation":"asserts","source":"the article"},{"text":"After adopting generative AI, Chinese students' homework scores rose by 18 percent.","span":"[passage of 7 words]","relation":"reports","source":"Stromberg, Lei and Wu study"},{"text":"After adopting generative AI, time spent per assignment fell about 30 percent, from 64 to 45 minutes.","span":"[passage of 19 words]","relation":"reports","source":"Stromberg, Lei and Wu study"},{"text":"Students' scores on monthly closed-book exams without AI fell 20 percent within six months.","span":"[passage of 18 words]","relation":"reports","source":"Stromberg, Lei and Wu study"},{"text":"Students' performance in high-stakes entrance exams also declined, with the full effect emerging over a longer period.","span":"[passage of 17 words]","relation":"reports","source":"Stromberg, Lei and Wu study"},{"text":"The study tracked about 27,000 students aged 12 to 18 in China for 30 months.","span":"[passage of 13 words]","relation":"asserts","source":"the article"},{"text":"Where generative AI is neither built to teach nor used under structure, outsourcing tasks to it improves performance without real learning gains.","span":"[passage of 27 words]","relation":"reports","source":"OECD Digital Education Outlook 2026"},{"text":"Erosion of productive cognitive effort from AI can be described as metacognitive laziness.","span":"[passage of 11 words]","relation":"reports","source":"Dragan Gasevic"},{"text":"56 percent of surveyed European students aged 12 to 17 use AI to get information when studying outside school.","span":"[passage of 13 words]","relation":"reports","source":"Ipsos/Vodafone Foundation survey"},{"text":"45 percent of those students use AI to have terms and concepts explained.","span":"[passage of 13 words]","relation":"reports","source":"Ipsos/Vodafone Foundation survey"},{"text":"31 percent of those students use AI to provide complete solutions to tasks.","span":"[passage of 12 words]","relation":"reports","source":"Ipsos/Vodafone Foundation survey"},{"text":"29 percent of those students use AI for interactive or adaptive content to guide their learning.","span":"[passage of 13 words]","relation":"reports","source":"Ipsos/Vodafone Foundation survey"},{"text":"20 percent of those students use AI to create personalised learning plans and track progress.","span":"[passage of 14 words]","relation":"reports","source":"Ipsos/Vodafone Foundation survey"},{"text":"49 percent of UK full-time undergraduates believe AI has improved their student experience.","span":"[passage of 9 words]","relation":"reports","source":"HEPI/Kortext Student Generative AI Survey 2026"},{"text":"59 percent of UK undergraduates said AI made no difference to loneliness.","span":"[passage of 9 words]","relation":"reports","source":"HEPI/Kortext Student Generative AI Survey 2026"},{"text":"21 percent of UK undergraduates felt less lonely because of AI.","span":"[passage of 5 words]","relation":"reports","source":"HEPI/Kortext Student Generative AI Survey 2026"},{"text":"20 percent of UK undergraduates felt more lonely because of AI.","span":"[passage of 3 words]","relation":"reports","source":"HEPI/Kortext Student Generative AI Survey 2026"}]},{"article":"A5","propositions":[{"text":"AI is often viewed as a creativity killer when it comes to writing.","span":"[passage of 14 words]","relation":"asserts","source":"the article"},{"text":"AI used well can strengthen thinking.","span":"[passage of 6 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is a wonderful collaborator.","span":"[passage of 5 words]","relation":"reports","source":"Allison Stanger"},{"text":"Stanger writes her own first drafts and outlines her arguments, with the ideas, openings and conclusions being her own.","span":"[passage of 12 words]","relation":"reports","source":"Allison Stanger"},{"text":"Stanger uses AI to check the mechanics of her writing and to play devil's advocate on her arguments.","span":"[passage of 15 words]","relation":"reports","source":"Allison Stanger"},{"text":"Humans are best at judging what good writing is, so AI alone will not get writing to a finished standard.","span":"[passage of 26 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is useful as an editor late at night when no human is available.","span":"[passage of 30 words]","relation":"reports","source":"Allison Stanger"},{"text":"The problem with AI lies in the concentration of power, not in the technology itself.","span":"[passage of 18 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is extraordinarily useful but also potentially very dangerous.","span":"[passage of 14 words]","relation":"reports","source":"Allison Stanger"},{"text":"People must still think for themselves and teach students to do so.","span":"[passage of 15 words]","relation":"reports","source":"Allison Stanger"},{"text":"AI is a pattern-recognizer that can help identify important things to explore further.","span":"[passage of 15 words]","relation":"reports","source":"Allison Stanger"}]},{"article":"A6","propositions":[{"text":"Nearly 3 in 4 K-12 teachers believe AI has bigger implications for education than the internet or computers.","span":"[passage of 17 words]","relation":"reports","source":"NPR/Ipsos poll of K-12 teachers"},{"text":"The poll surveyed 545 respondents and was nationally representative.","span":"[passage of 7 words]","relation":"asserts","source":"the article"},{"text":"A majority of teachers are worried AI is making it harder for students to learn to think for themselves.","span":"[passage of 19 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"Nearly 8 in 10 teachers think schools should teach responsible use of AI.","span":"[passage of 11 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"A little more than half of teachers say students are not using AI in class at all.","span":"[passage of 19 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"About 2 in 5 teachers say students use AI in class at least once a week.","span":"[passage of 15 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"6 in 10 teachers have used AI themselves to help with work tasks.","span":"[passage of 18 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"63% of teachers who use AI for work say the time savings amount to two hours or less per week.","span":"[passage of 16 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"54% of teachers say AI makes it harder for students to learn critical thinking skills.","span":"[passage of 16 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"55% of teachers think AI is mostly just a shortcut for students to avoid doing more work.","span":"[passage of 16 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"Nearly 6 in 10 teachers say AI is eroding trust between students and teachers.","span":"[passage of 16 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"About 4 in 10 teachers have required more assignments to be done by hand because of AI.","span":"[passage of 12 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"About 4 in 10 teachers have required more assignments to be done in class because of AI.","span":"[passage of 17 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"70% of teachers believe the public's perception of them has gotten worse.","span":"[passage of 12 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"Erosion of trust caused by AI is one of the biggest red flags in the data.","span":"[passage of 9 words]","relation":"reports","source":"Mallory Newall"},{"text":"Among teachers whose school provides AI software, only 35% say there is a formal policy on teacher use of AI.","span":"[passage of 13 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"About half of teachers say their school hasn't offered any guidance on AI or they're unsure what it is.","span":"[passage of 23 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"Only about 4 in 10 teachers say their school offers AI professional development or training.","span":"[passage of 15 words]","relation":"reports","source":"NPR/Ipsos poll"},{"text":"Biology teacher Michele Naber lets students use AI in certain lessons to learn prompting and verify accuracy, showing that AI still sometimes gets things wrong.","span":"[passage of 22 words]","relation":"reports","source":"Michele Naber"},{"text":"AI cut the time to create multiple choice assessment questions from upwards of an hour to five minutes.","span":"[passage of 10 words]","relation":"reports","source":"Michele Naber"},{"text":"AI isn't reliable enough to generate math questions, and checking its mistakes isn't worth the effort.","span":"[passage of 8 words]","relation":"reports","source":"Joann Purcell"},{"text":"Students who are not already intrinsically motivated critical thinkers will see their critical thinking skills atrophy over time due to AI.","span":"[passage of 11 words]","relation":"reports","source":"Christa Corricelli"},{"text":"AI can be especially helpful for students with disabilities.","span":"[passage of 9 words]","relation":"reports","source":"Ellie Rodriguez"},{"text":"Naber can no longer verify extra-credit photos because AI can easily create fake images, so she stopped offering the extra credit.","span":"[passage of 11 words]","relation":"reports","source":"Michele Naber"},{"text":"Josh Kauffman has noticed a substantial uptick in AI-generated assignments from his students at a virtual school.","span":"[passage of 14 words]","relation":"reports","source":"Josh Kauffman"},{"text":"Purcell doesn't think AI has eroded trust, because students found ways to cheat before AI.","span":"[passage of 14 words]","relation":"reports","source":"Joann Purcell"}]}]}
```

</details>

<details><summary>GPT-4o, temperature 0 · Round 4, ICE articles · 16 October 2026, 14:29</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (5013 words)

```text
The following 6 news articles are labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News, 2026-07-29, “Colombian father detained by ICE while pumping gas in Doral describes conditions inside detention centers”, 522 words. Text not included.]
[Article A2: Breitbart, 2026-06-18, “EXCLUSIVE: 735 Criminal Illegal Aliens Arrested by ICE-Houston Officers in May — Nearly 1,200 with Violent Convictions, Including Murderers, Child Predators”, 557 words. Text not included.]
[Article A3: NBC News, 2026-09-22, “ICE officer who shot man in Austin was issued a body camera but wasn’t wearing it”, 1373 words. Text not included.]
[Article A4: NPR, 2026-07-17, “Ex-wife says ICE agent who killed man in Maine had racist beliefs, violent tendencies”, 933 words. Text not included.]
[Article A5: Fox News, 2026-05-20, “Feds say Arizona suspect vandalized ICE facility and attempted to ignite lobby area”, 491 words. Text not included.]
[Article A6: Breitbart, 2026-06-15, “Exclusive: ICE Agents Arrest Illegal Aliens Convicted of Pedophilia, Child Abuse, Domestic Violence”, 490 words. Text not included.]




Task: for each article, list the propositions about the world that it contains.

A proposition is a single claim about the world that an article states or reports: what happened or is the case, what a number is, what a rule or status is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each proposition contains exactly one claim. Test every proposition before you list it: if it can be divided into two statements, each of which could be true while the other is false, divide it and list both. Two numbers, two findings, a finding and a second finding about its size or timing, or a fact and a comment on it are two claims. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal claim (A causes B) is one proposition only when the causal link is the claim.
2. Each proposition must stand on its own: a reader who has not seen the article must be able to understand it. Resolve pronouns, give full names, and include the time, place and population when the claim's truth depends on them. Add nothing else.
3. State the proposition as a claim about the world, not about the article. When an article reports a claim made by a person or a study, state the claim itself and record the source in "relation" and "source"; do not write "the article says".
4. Keep the article's meaning. Do not strengthen, weaken, generalise or soften the claim.
5. Leave out rhetorical flourishes, questions, and claims whose meaning cannot be resolved from the article.
6. Each proposition must come from the article it is listed under. Copy, character for character, the shortest passage of that article that states it ("span"). The passage must be one continuous stretch of the article, with every word, letter and punctuation mark exactly as in the article: do not change a word, do not shorten it with "...", and do not join passages from different places. Copy the passage as it stands even where the proposition itself resolves a pronoun or gives a full name.
7. List every proposition the article contains. Do not list the same proposition twice in different words.

For each proposition, give "relation": "asserts" (the article states it in its own voice), "reports" (the article reports a person, group or study saying it), or "hedges" (the article states it with doubt or qualification), and "source": who makes the claim (a person, group or study as named in the article, or "the article" when it is the article's own voice).

Return JSON of the form {"articles": [{"article": "<label>", "propositions": [{"text": "<proposition>", "span": "<exact passage>", "relation": "asserts|reports|hedges", "source": "<who>"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (7739 words)

```text
{"articles": [{"article": "A1", "propositions": [{"text": "Carlos Betancur was detained by U.S. Immigration and Customs Enforcement while pumping gas in Doral.", "span": "[passage of 30 words]", "relation": "asserts", "source": "the article"}, {"text": "Carlos Betancur spent 16 days in federal custody before being released with an ankle monitor.", "span": "[passage of 40 words]", "relation": "reports", "source": "Carlos Betancur"}, {"text": "Carlos Betancur was detained on July 8.", "span": "[passage of 30 words]", "relation": "asserts", "source": "the article"}, {"text": "Carlos Betancur was released and reunited with his family.", "span": "[passage of 32 words]", "relation": "asserts", "source": "the article"}, {"text": "Carlos Betancur was approached by an immigration officer from behind while he was at the gas pump.", "span": "[passage of 19 words]", "relation": "reports", "source": "Carlos Betancur"}, {"text": "Carlos Betancur handed over his Florida driver's license to the officer.", "span": "[passage of 28 words]", "relation": "reports", "source": "Carlos Betancur"}, {"text": "Carlos Betancur's daughter, Maria Alejandra Betancur, argued that his detention was unjustified.", "span": "[passage of 7 words]", "relation": "reports", "source": "Maria Alejandra Betancur"}, {"text": "ICE stated that Carlos Betancur had overstayed his visa.", "span": "[passage of 26 words]", "relation": "reports", "source": "ICE"}, {"text": "Carlos Betancur is now required to wear an ankle monitor while his immigration case proceeds.", "span": "[passage of 14 words]", "relation": "asserts", "source": "the article"}, {"text": "Carlos Betancur initially spent eight days at the Miramar Processing Center.", "span": "[passage of 24 words]", "relation": "reports", "source": "Carlos Betancur"}, {"text": "Carlos Betancur described overcrowded conditions at the Miramar Processing Center.", "span": "[passage of 23 words]", "relation": "reports", "source": "Carlos Betancur"}, {"text": "Carlos Betancur was transferred to the Krome Detention Center after eight days.", "span": "[passage of 17 words]", "relation": "reports", "source": "Carlos Betancur"}, {"text": "Maria Alejandra Betancur believes the public attention surrounding the case may have played a role in the timeline of Carlos Betancur's transfer.", "span": "[passage of 20 words]", "relation": "reports", "source": "Maria Alejandra Betancur"}, {"text": "Immigration advocates gathered outside the Miramar Processing Center to protest prolonged detentions.", "span": "[passage of 25 words]", "relation": "asserts", "source": "the article"}, {"text": "Yarelys Mendez Zamora said the Miramar Processing Center is acting as a detention center when it should not.", "span": "[passage of 41 words]", "relation": "reports", "source": "Yarelys Mendez Zamora"}, {"text": "Carlos Betancur is represented by an immigration attorney.", "span": "[passage of 23 words]", "relation": "asserts", "source": "the article"}, {"text": "Carlos Betancur is scheduled to appear before an immigration judge next month.", "span": "[passage of 23 words]", "relation": "asserts", "source": "the article"}, {"text": "The outlet reached out to ICE for comment regarding Carlos Betancur's release and the allegations about conditions at the Miramar Processing Center.", "span": "[passage of 21 words]", "relation": "asserts", "source": "the article"}, {"text": "As of Wednesday evening, ICE had not responded to the outlet's inquiry.", "span": "[passage of 9 words]", "relation": "asserts", "source": "the article"}]}, {"article": "A2", "propositions": [{"text": "735 criminal illegal aliens were arrested in the Houston area in May.", "span": "[passage of 38 words]", "relation": "asserts", "source": "the article"}, {"text": "The 735 criminal illegal aliens arrested in May accounted for more than 1,700 criminal convictions.", "span": "[passage of 38 words]", "relation": "asserts", "source": "the article"}, {"text": "Nearly 1,200 of the criminal convictions involved violent crimes or threats to public safety.", "span": "[passage of 38 words]", "relation": "asserts", "source": "the article"}, {"text": "The arrests included murderers, rapists, child predators, arsonists, drug traffickers, and members of MS‑13, Surenos 13, 18th Street, Tango Blast, and other brutal gangs.", "span": "[passage of 24 words]", "relation": "asserts", "source": "the article"}, {"text": "Gabriel Martinez said the numbers reflect who ICE is arresting every single month.", "span": "[passage of 25 words]", "relation": "reports", "source": "Gabriel Martinez"}, {"text": "Gabriel Martinez said the data is a snapshot of who ICE is arresting every single month.", "span": "[passage of 60 words]", "relation": "reports", "source": "Gabriel Martinez"}, {"text": "Gabriel Martinez said the public needs to know that the aliens ICE is targeting are not harmless economic migrants.", "span": "[passage of 25 words]", "relation": "reports", "source": "Gabriel Martinez"}, {"text": "Gabriel Martinez said the aliens ICE is targeting are violent criminals who repeatedly violate laws.", "span": "[passage of 38 words]", "relation": "reports", "source": "Gabriel Martinez"}, {"text": "25 of the criminal aliens arrested were members of violent gangs.", "span": "[passage of 16 words]", "relation": "reports", "source": "Officials"}, {"text": "The gangs included MS-13, Surenos 13, 18th Street, Tango Blast, Paisas, Chucos Tangos, Southwest Cholos, Brown and Proud, and La Primera.", "span": "[passage of 21 words]", "relation": "asserts", "source": "the article"}, {"text": "Gabriel Martinez said everyone should want dangerous criminal illegal aliens removed from the community.", "span": "[passage of 29 words]", "relation": "reports", "source": "Gabriel Martinez"}, {"text": "Gabriel Martinez said there are individuals and groups opposed to any form of immigration enforcement.", "span": "[passage of 41 words]", "relation": "reports", "source": "Gabriel Martinez"}, {"text": "Gabriel Martinez said ICE officers remain undeterred and will continue to execute their mission.", "span": "[passage of 34 words]", "relation": "reports", "source": "Gabriel Martinez"}, {"text": "The 735 criminal aliens arrested in May had accumulated more than 1,711 criminal convictions.", "span": "[passage of 16 words]", "relation": "reports", "source": "officials"}, {"text": "Seventy percent of the criminal convictions were for violent crimes.", "span": "[passage of 17 words]", "relation": "asserts", "source": "the article"}, {"text": "Carlos Galeano Lara is a 37-year-old criminal illegal alien and foreign fugitive wanted in Honduras for homicide.", "span": "[passage of 23 words]", "relation": "reports", "source": "officials"}, {"text": "Carlos Galeano Lara was arrested by ICE on May 25.", "span": "[passage of 19 words]", "relation": "asserts", "source": "the article"}, {"text": "Carlos Galeano Lara remains in ICE custody pending the disposition of his immigration proceedings.", "span": "[passage of 19 words]", "relation": "asserts", "source": "the article"}, {"text": "ICE officials warn that the arrests are not outliers but a monthly snapshot of those who came into the country illegally.", "span": "[passage of 27 words]", "relation": "reports", "source": "ICE officials"}, {"text": "Houston's May numbers underscore a simple reality: without sustained enforcement and deportation, more Americans will pay the price.", "span": "[passage of 22 words]", "relation": "reports", "source": "officials"}]}, {"article": "A3", "propositions": [{"text": "An ICE officer shot a Venezuelan man in Austin on Sunday.", "span": "[passage of 46 words]", "relation": "reports", "source": "two officials with the Department of Homeland Security"}, {"text": "The ICE officer who shot the Venezuelan man was issued a body camera but was not wearing it during the shooting.", "span": "[passage of 46 words]", "relation": "reports", "source": "two officials with the Department of Homeland Security"}, {"text": "Another ICE officer in the same vehicle was wearing a body camera.", "span": "[passage of 17 words]", "relation": "reports", "source": "two officials with the Department of Homeland Security"}, {"text": "The body camera footage does not include the moment of the shooting.", "span": "[passage of 22 words]", "relation": "reports", "source": "two officials with the Department of Homeland Security"}, {"text": "Wilber Rafael Garcés Pérez was shot early Sunday afternoon by an ICE officer while making deliveries as a DoorDash driver.", "span": "[passage of 22 words]", "relation": "asserts", "source": "the article"}, {"text": "Wilber Rafael Garcés Pérez was taken to a hospital and then into immigration custody at the South Texas ICE Processing Center in Pearsall, Texas.", "span": "[passage of 31 words]", "relation": "reports", "source": "his attorney"}, {"text": "A federal judge granted an emergency order temporarily blocking deportation proceedings against Wilber Rafael Garcés Pérez.", "span": "[passage of 22 words]", "relation": "reports", "source": "Kate Lincoln-Goldfinch"}, {"text": "The Travis County District Attorney’s Office requested that Wilber Rafael Garcés Pérez be allowed to remain in the country.", "span": "[passage of 39 words]", "relation": "asserts", "source": "the article"}, {"text": "Austin Police Chief Lisa Davis shared some of the first video footage obtained by the department as part of their probe into the shooting.", "span": "[passage of 27 words]", "relation": "asserts", "source": "the article"}, {"text": "The videos came from an off-duty officer who captured part of the encounter between ICE and Wilber Rafael Garcés Pérez.", "span": "[passage of 33 words]", "relation": "asserts", "source": "the article"}, {"text": "Austin police are seeking the public’s help in obtaining any video evidence that can help them piece together the pursuit that preceded the shooting.", "span": "[passage of 25 words]", "relation": "asserts", "source": "the article"}, {"text": "Wilber Rafael Garcés Pérez began experiencing an inability to move his arm the day after he was shot.", "span": "[passage of 22 words]", "relation": "reports", "source": "attorney Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez was taken to the hospital Monday afternoon for several hours and then sent back to the detention center.", "span": "[passage of 21 words]", "relation": "reports", "source": "attorney Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez told a news conference via phone from detention that he was in a lot of pain and wasn’t getting the medical care he needed.", "span": "[passage of 28 words]", "relation": "asserts", "source": "the article"}, {"text": "Wilber Rafael Garcés Pérez's communication privileges were revoked after he spoke out at the news conference.", "span": "[passage of 56 words]", "relation": "reports", "source": "attorney Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez was handcuffed, shackled at the ankles, placed in a waist chain, and handled roughly during his transfer to the hospital.", "span": "[passage of 26 words]", "relation": "reports", "source": "attorney Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez was given morphine for his pain.", "span": "[passage of 24 words]", "relation": "reports", "source": "attorney Lincoln-Goldfinch"}, {"text": "The gunshot fractured Wilber Rafael Garcés Pérez's clavicle.", "span": "[passage of 22 words]", "relation": "reports", "source": "attorney Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez was discharged from the hospital around midnight and taken back to the detention center.", "span": "[passage of 30 words]", "relation": "reports", "source": "attorney Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez is receiving Tylenol and ibuprofen for his ongoing pain.", "span": "[passage of 30 words]", "relation": "reports", "source": "attorney Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez remains in isolation, on a flat bed, and without the tablet he previously used to communicate.", "span": "[passage of 19 words]", "relation": "reports", "source": "attorney Lincoln-Goldfinch"}, {"text": "Rep. Joaquin Castro said ICE has forced Wilber Rafael Garcés Pérez out of the hospital and back to the South Texas ICE Processing Center in Pearsall, Texas.", "span": "[passage of 46 words]", "relation": "reports", "source": "Rep. Joaquin Castro"}, {"text": "Rep. Joaquin Castro and Rep. Greg Casar would visit Wilber Rafael Garcés Pérez on Wednesday.", "span": "[passage of 23 words]", "relation": "asserts", "source": "the article"}, {"text": "A DHS spokesperson said Wilber Rafael Garcés Pérez was in stable condition and was in federal custody pending removal from the U.S.", "span": "[passage of 26 words]", "relation": "reports", "source": "A DHS spokesperson"}, {"text": "A senior administration official said Wilber Rafael Garcés Pérez did not have a criminal history beyond being in the country illegally.", "span": "[passage of 24 words]", "relation": "reports", "source": "A senior administration official"}, {"text": "Wilber Rafael Garcés Pérez entered the country legally and was seeking asylum.", "span": "[passage of 13 words]", "relation": "reports", "source": "Kate Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez had filed a change of address in immigration court.", "span": "[passage of 29 words]", "relation": "reports", "source": "Kate Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez was ordered deported in absentia because he missed his immigration hearing.", "span": "[passage of 17 words]", "relation": "reports", "source": "Kate Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez was making a delivery when an unmarked black truck sideswiped him.", "span": "[passage of 21 words]", "relation": "reports", "source": "Kate Lincoln-Goldfinch"}, {"text": "Wilber Rafael Garcés Pérez did not know it was ICE as the truck chased him.", "span": "[passage of 28 words]", "relation": "reports", "source": "Kate Lincoln-Goldfinch"}, {"text": "DHS has accused immigrants involved in shootings with ICE of using their cars as weapons while fleeing agents.", "span": "[passage of 25 words]", "relation": "asserts", "source": "the article"}, {"text": "DHS did not make the accusation in the case of Wilber Rafael Garcés Pérez.", "span": "[passage of 35 words]", "relation": "asserts", "source": "the article"}, {"text": "ICE Director David Venturella previously told the outlet that every ICE officer and agent would be equipped with body cameras by the end of August.", "span": "[passage of 38 words]", "relation": "reports", "source": "ICE Director David Venturella"}, {"text": "A person who witnessed the aftermath of the shooting said he saw immigration agents surrounding a car.", "span": "[passage of 52 words]", "relation": "reports", "source": "A person who witnessed the aftermath of the shooting"}, {"text": "The witness said he saw a man who looked sad and with his eyes full of tears.", "span": "[passage of 18 words]", "relation": "reports", "source": "A person who witnessed the aftermath of the shooting"}, {"text": "The witness said the man told him he was shot in the back.", "span": "[passage of 35 words]", "relation": "reports", "source": "A person who witnessed the aftermath of the shooting"}, {"text": "A social media video captures the sound of tires screeching followed by a person exiting a dark-colored SUV.", "span": "[passage of 36 words]", "relation": "asserts", "source": "the article"}, {"text": "The sedan appears to be damaged on the passenger side.", "span": "[passage of 10 words]", "relation": "asserts", "source": "the article"}, {"text": "At least three gunshots are heard as the person approaches the sedan.", "span": "[passage of 22 words]", "relation": "asserts", "source": "the article"}, {"text": "The video shows the person standing next to the sedan’s driver’s side as it stops in front of an intersection.", "span": "[passage of 20 words]", "relation": "asserts", "source": "the article"}, {"text": "Another video shows the blue sedan with its driver’s side door open and Wilber Rafael Garcés Pérez hunched over in the driver’s seat.", "span": "[passage of 36 words]", "relation": "asserts", "source": "the article"}, {"text": "The woman taking the video says, “Why did he do that to him?”", "span": "[passage of 13 words]", "relation": "asserts", "source": "the article"}, {"text": "The officers tell the woman taking the video that an ambulance is coming.", "span": "[passage of 9 words]", "relation": "asserts", "source": "the article"}, {"text": "The video shows Wilber Rafael Garcés Pérez being taken out of the car and handcuffed behind his back.", "span": "[passage of 16 words]", "relation": "asserts", "source": "the article"}, {"text": "The agents make Wilber Rafael Garcés Pérez sit on the ground.", "span": "[passage of 8 words]", "relation": "asserts", "source": "the article"}, {"text": "There appears to be a large bloodstain down Wilber Rafael Garcés Pérez's back.", "span": "[passage of 10 words]", "relation": "asserts", "source": "the article"}, {"text": "The officers cut open the back of Wilber Rafael Garcés Pérez's shirt, revealing a bullet hole.", "span": "[passage of 13 words]", "relation": "asserts", "source": "the article"}, {"text": "The woman taking the video says in Spanish that “they just shot him because he didn’t want to stop” his vehicle.", "span": "[passage of 97 words]", "relation": "asserts", "source": "the article"}, {"text": "The woman taking the video says, “This is unjust,” as she’s recording the video.", "span": "[passage of 10 words]", "relation": "asserts", "source": "the article"}]}, {"article": "A4", "propositions": [{"text": "An ICE officer allegedly fatally shot a Colombian man in Maine.", "span": "[passage of 37 words]", "relation": "asserts", "source": "the article"}, {"text": "Ashley Brouillette said her ex-husband, David Brouillette, was the officer who fatally shot Joan Durán Guerrero.", "span": "[passage of 30 words]", "relation": "reports", "source": "Ashley Brouillette"}, {"text": "David Brouillette called Ashley Brouillette on Wednesday, asking her to vouch for his character.", "span": "[passage of 23 words]", "relation": "reports", "source": "Ashley Brouillette"}, {"text": "David Brouillette asked Ashley Brouillette not to talk about the abuse in their marriage.", "span": "[passage of 76 words]", "relation": "reports", "source": "Ashley Brouillette"}, {"text": "David Brouillette did not respond to messages from the outlet seeking comment.", "span": "[passage of 12 words]", "relation": "asserts", "source": "the article"}, {"text": "An ICE spokesperson said the agency will not confirm or deny whether David Brouillette was the ICE officer responsible for Durán Guerrero's death.", "span": "[passage of 22 words]", "relation": "reports", "source": "An ICE spokesperson"}, {"text": "The ICE officer in question has nearly a decade of federal law enforcement experience with required training.", "span": "[passage of 27 words]", "relation": "reports", "source": "ICE spokesperson Lauren Bis"}, {"text": "Scott Collins testified on behalf of Ashley Brouillette in the divorce proceedings.", "span": "[passage of 29 words]", "relation": "asserts", "source": "the article"}, {"text": "David Brouillette had a bad tendency of going out and looking for fights.", "span": "[passage of 14 words]", "relation": "reports", "source": "Scott Collins"}, {"text": "David Brouillette used anti-Black racial slurs in high school.", "span": "[passage of 13 words]", "relation": "reports", "source": "Scott Collins"}, {"text": "Ashley Brouillette worries racism may have played a part in Durán Guerrero's death.", "span": "[passage of 15 words]", "relation": "reports", "source": "Ashley Brouillette"}, {"text": "David Brouillette's nickname in high school was 'White Boy David.'", "span": "[passage of 20 words]", "relation": "reports", "source": "Ashley Brouillette"}, {"text": "Ashley Brouillette has known David Brouillette since they were preteens.", "span": "[passage of 12 words]", "relation": "asserts", "source": "the article"}, {"text": "There were many moments of violence in Ashley Brouillette and David Brouillette's marriage.", "span": "[passage of 17 words]", "relation": "reports", "source": "Ashley Brouillette"}, {"text": "Ashley Brouillette recanted her story after complaining to authorities about her ex-husband's behavior.", "span": "[passage of 23 words]", "relation": "reports", "source": "Ashley Brouillette"}, {"text": "Ashley Brouillette kept a profanity-laced voicemail message from November.", "span": "[passage of 20 words]", "relation": "asserts", "source": "the article"}, {"text": "In the voicemail, David Brouillette slurs his speech and ends by saying that Ashley Brouillette and the women in her family should have their throats cut.", "span": "[passage of 28 words]", "relation": "asserts", "source": "the article"}, {"text": "Ashley Brouillette reached out to Brouillette's platoon leader in the Maine Army National Guard during their divorce in 2009.", "span": "[passage of 32 words]", "relation": "reports", "source": "Ashley Brouillette"}, {"text": "Ashley Brouillette offered to fax over paperwork showing that David Brouillette had been diagnosed as having bipolar disorder and borderline schizophrenia.", "span": "[passage of 31 words]", "relation": "reports", "source": "Ashley Brouillette"}, {"text": "Ashley Brouillette is unsure if there was a background check when David Brouillette was hired by ICE.", "span": "[passage of 10 words]", "relation": "asserts", "source": "the article"}, {"text": "Child protective services and the police were called to David Brouillette's home after he threw his then-13 year-old daughter through a glass coffee table.", "span": "[passage of 32 words]", "relation": "reports", "source": "Ashley Brouillette"}, {"text": "In a 2021 court filing, David Brouillette was stripped of his firearms temporarily.", "span": "[passage of 13 words]", "relation": "asserts", "source": "the article"}, {"text": "Lucinda Brouillette accused David Brouillette of becoming more aggressive with their then 13-year-old daughter.", "span": "[passage of 19 words]", "relation": "asserts", "source": "the article"}, {"text": "Ashley Brouillette is distraught over this week's events.", "span": "[passage of 17 words]", "relation": "asserts", "source": "the article"}, {"text": "Ashley Brouillette feels she needs to push and be heard now to prevent something like this from happening again.", "span": "[passage of 41 words]", "relation": "reports", "source": "Ashley Brouillette"}]}, {"article": "A5", "propositions": [{"text": "An Arizona man is facing federal charges after prosecutors said he vandalized and attempted to set fire to an ICE facility.", "span": "[passage of 38 words]", "relation": "asserts", "source": "the article"}, {"text": "Gerardo Mendoza-Acoltzi of Avondale was indicted by a federal grand jury on charges of malicious damage to federal property and willful depredation against property of the United States.", "span": "[passage of 38 words]", "relation": "reports", "source": "The U.S. Attorney’s Office for the District of Arizona"}, {"text": "Mendoza-Acoltzi broke a window at the ICE property before attempting to ignite the building.", "span": "[passage of 25 words]", "relation": "asserts", "source": "the article"}, {"text": "Surveillance video showed Mendoza-Acoltzi arriving at the facility shortly before midnight.", "span": "[passage of 23 words]", "relation": "reports", "source": "Federal authorities"}, {"text": "Mendoza-Acoltzi unloaded a propane tank near the front entrance of the facility.", "span": "[passage of 23 words]", "relation": "reports", "source": "Federal authorities"}, {"text": "Mendoza-Acoltzi smashed a lobby window with the propane tank and used a torch connected to the tank to ignite window shades inside the building.", "span": "[passage of 28 words]", "relation": "reports", "source": "Prosecutors"}, {"text": "Mendoza-Acoltzi arranged rocks outside the facility to spell an anti-ICE message before leaving the area.", "span": "[passage of 18 words]", "relation": "asserts", "source": "the article"}, {"text": "Mendoza-Acoltzi was arrested May 7 and made his initial appearance in federal court shortly afterward.", "span": "[passage of 18 words]", "relation": "reports", "source": "Federal prosecutors"}, {"text": "The FBI was investigating \"significant criminal damage\" at the federal ICE warehouse facility after vandals targeted the property with anti-law enforcement graffiti and damaged windows.", "span": "[passage of 30 words]", "relation": "asserts", "source": "the article"}, {"text": "If convicted, Mendoza-Acoltzi could face years in federal prison.", "span": "[passage of 9 words]", "relation": "asserts", "source": "the article"}, {"text": "Attempted arson of federal property carries a potential sentence of up to 20 years behind bars.", "span": "[passage of 25 words]", "relation": "asserts", "source": "the article"}, {"text": "Federal officials have increasingly warned about threats and attacks targeting immigration enforcement facilities and personnel.", "span": "[passage of 24 words]", "relation": "asserts", "source": "the article"}, {"text": "The Arizona case comes amid heightened concerns over threats targeting immigration enforcement and DHS facilities nationwide.", "span": "[passage of 20 words]", "relation": "asserts", "source": "the article"}, {"text": "State and federal authorities launched an investigation into an attempted arson attack at a DHS office building in Meridian, Idaho.", "span": "[passage of 25 words]", "relation": "asserts", "source": "the article"}, {"text": "The suspect allegedly stole an ambulance from a bay at St. Luke’s West hospital.", "span": "[passage of 38 words]", "relation": "reports", "source": "Meridian Police Chief Tracy Basterrechea"}, {"text": "The suspect drove the ambulance into the North Portico building, which houses DHS offices.", "span": "[passage of 20 words]", "relation": "reports", "source": "Meridian Police Chief Tracy Basterrechea"}, {"text": "Investigators believe the suspect poured an accelerant inside and around the outside of the ambulance but was unable to ignite it before being interrupted by responding officers.", "span": "[passage of 27 words]", "relation": "asserts", "source": "the article"}, {"text": "Tracy Basterrechea said there has been a lot of rhetoric surrounding the Department of Homeland Security leasing office space at the location.", "span": "[passage of 21 words]", "relation": "reports", "source": "Tracy Basterrechea"}, {"text": "Tracy Basterrechea said comments on social media, such as ‘property damage isn't violence,’ is absolutely false.", "span": "[passage of 13 words]", "relation": "reports", "source": "Tracy Basterrechea"}, {"text": "Tracy Basterrechea said the attempted arson was absolutely an act of violence.", "span": "[passage of 35 words]", "relation": "reports", "source": "Tracy Basterrechea"}, {"text": "The charges against Mendoza-Acoltzi are allegations, and he is presumed innocent unless proven guilty in court.", "span": "[passage of 16 words]", "relation": "asserts", "source": "the article"}]}, {"article": "A6", "propositions": [{"text": "ICE is continuing to arrest illegal aliens across the United States.", "span": "[passage of 38 words]", "relation": "asserts", "source": "the article"}, {"text": "ICE recently arrested illegal aliens convicted of child sexual abuse, child abuse, domestic violence, and drug trafficking.", "span": "[passage of 38 words]", "relation": "asserts", "source": "the article"}, {"text": "Lauren Bis said ICE law enforcement was hard at work arresting pedophiles, drug traffickers, and other violent criminals over the weekend.", "span": "[passage of 41 words]", "relation": "reports", "source": "Lauren Bis"}, {"text": "Miguel Gorasieta Jaimes of Mexico was convicted of aggravated sexual assault of a child in Harris County, Texas.", "span": "[passage of 26 words]", "relation": "asserts", "source": "the article"}, {"text": "Teodolo Resendiz-Figueroa of Mexico was convicted of continuous sexual abuse of a child and three counts of lewd act upon a child in Los Angeles, California.", "span": "[passage of 26 words]", "relation": "asserts", "source": "the article"}, {"text": "Cesar Martin Sanchez-Martinez of Mexico was previously convicted of felony vehicular assault and child abuse with serious bodily injury in Arapahoe County, Colorado.", "span": "[passage of 28 words]", "relation": "asserts", "source": "the article"}, {"text": "Urbano Estrada-Santizo of Guatemala was convicted of drunk driving and felony incest in Nashville, Tennessee.", "span": "[passage of 17 words]", "relation": "asserts", "source": "the article"}, {"text": "Edinson Amador of the Dominican Republic was arrested after being convicted of drug trafficking cocaine in Boston, Massachusetts.", "span": "[passage of 20 words]", "relation": "asserts", "source": "the article"}, {"text": "Noe Moreno-Salazar, a criminal illegal alien from Mexico, was convicted for criminal sexual abuse, possession of a controlled substance, and aggravated unlawful use of a loaded weapon in St. Charles, Illinois.", "span": "[passage of 30 words]", "relation": "asserts", "source": "the article"}, {"text": "Santos Ruben Gutierrez, a criminal illegal alien from El Salvador, was convicted for indecency with a child in Lewisville, Texas.", "span": "[passage of 19 words]", "relation": "asserts", "source": "the article"}, {"text": "Ramon R. Castillo, a criminal illegal alien from Mexico, was convicted for lewd or lascivious acts with a child under 14 years old in Santa Clarita, California.", "span": "[passage of 26 words]", "relation": "asserts", "source": "the article"}, {"text": "Alex Jimenez-Cochancela, a criminal illegal alien from Ecuador, was convicted for promoting a sexual performance by a child in Carmel, New York.", "span": "[passage of 21 words]", "relation": "asserts", "source": "the article"}, {"text": "Salomon Santos-Cach, a criminal illegal alien from Mexico, was convicted for assault of a minor with intent to commit rape in Sonoma, California.", "span": "[passage of 22 words]", "relation": "asserts", "source": "the article"}, {"text": "Santa Mongar, a criminal illegal alien from Bhutan, was convicted for assault and battery and first-degree sexual abuse in Lancaster, Pennsylvania.", "span": "[passage of 20 words]", "relation": "asserts", "source": "the article"}, {"text": "Jose Victor Gonzalez-Rosales, a criminal illegal alien from El Salvador, was convicted of battery of spouse, obstructing/resisting a police officer, and burglary in Los Angeles, California.", "span": "[passage of 25 words]", "relation": "asserts", "source": "the article"}, {"text": "Luis Ramos-Sacramento, a criminal illegal alien from Mexico, was convicted for endangering the welfare of a child – abuse/neglect and aggravated assault – domestic violence in Freehold, New Jersey.", "span": "[passage of 28 words]", "relation": "asserts", "source": "the article"}, {"text": "Nicandro Garcia-Perez, a criminal illegal alien from Mexico, was convicted for possession with the intent to distribute five kilograms or more of cocaine in the U.S. District Court for the District of Nebraska.", "span": "[passage of 32 words]", "relation": "asserts", "source": "the article"}, {"text": "James Ayur Garang, a criminal illegal alien from Sudan, was convicted for conspiracy to distribute a controlled substance in Sioux Falls, South Dakota.", "span": "[passage of 22 words]", "relation": "asserts", "source": "the article"}, {"text": "Lauren Bis said ICE law enforcement works around the clock to deliver on President Trump’s promise to make America safe again.", "span": "[passage of 21 words]", "relation": "reports", "source": "Lauren Bis"}, {"text": "Lauren Bis said ICE will continue to target the worst of the worst and protect American communities.", "span": "[passage of 20 words]", "relation": "reports", "source": "Lauren Bis"}]}]}
```

</details>

<details><summary>Haiku 4.5, temperature 0 · Round 4, ICE articles · 16 October 2026, 14:27</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (5013 words)

```text
The following 6 news articles are labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News, 2026-07-29, “Colombian father detained by ICE while pumping gas in Doral describes conditions inside detention centers”, 522 words. Text not included.]
[Article A2: Breitbart, 2026-06-18, “EXCLUSIVE: 735 Criminal Illegal Aliens Arrested by ICE-Houston Officers in May — Nearly 1,200 with Violent Convictions, Including Murderers, Child Predators”, 557 words. Text not included.]
[Article A3: NBC News, 2026-09-22, “ICE officer who shot man in Austin was issued a body camera but wasn’t wearing it”, 1373 words. Text not included.]
[Article A4: NPR, 2026-07-17, “Ex-wife says ICE agent who killed man in Maine had racist beliefs, violent tendencies”, 933 words. Text not included.]
[Article A5: Fox News, 2026-05-20, “Feds say Arizona suspect vandalized ICE facility and attempted to ignite lobby area”, 491 words. Text not included.]
[Article A6: Breitbart, 2026-06-15, “Exclusive: ICE Agents Arrest Illegal Aliens Convicted of Pedophilia, Child Abuse, Domestic Violence”, 490 words. Text not included.]




Task: for each article, list the propositions about the world that it contains.

A proposition is a single claim about the world that an article states or reports: what happened or is the case, what a number is, what a rule or status is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each proposition contains exactly one claim. Test every proposition before you list it: if it can be divided into two statements, each of which could be true while the other is false, divide it and list both. Two numbers, two findings, a finding and a second finding about its size or timing, or a fact and a comment on it are two claims. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal claim (A causes B) is one proposition only when the causal link is the claim.
2. Each proposition must stand on its own: a reader who has not seen the article must be able to understand it. Resolve pronouns, give full names, and include the time, place and population when the claim's truth depends on them. Add nothing else.
3. State the proposition as a claim about the world, not about the article. When an article reports a claim made by a person or a study, state the claim itself and record the source in "relation" and "source"; do not write "the article says".
4. Keep the article's meaning. Do not strengthen, weaken, generalise or soften the claim.
5. Leave out rhetorical flourishes, questions, and claims whose meaning cannot be resolved from the article.
6. Each proposition must come from the article it is listed under. Copy, character for character, the shortest passage of that article that states it ("span"). The passage must be one continuous stretch of the article, with every word, letter and punctuation mark exactly as in the article: do not change a word, do not shorten it with "...", and do not join passages from different places. Copy the passage as it stands even where the proposition itself resolves a pronoun or gives a full name.
7. List every proposition the article contains. Do not list the same proposition twice in different words.

For each proposition, give "relation": "asserts" (the article states it in its own voice), "reports" (the article reports a person, group or study saying it), or "hedges" (the article states it with doubt or qualification), and "source": who makes the claim (a person, group or study as named in the article, or "the article" when it is the article's own voice).

Return JSON of the form {"articles": [{"article": "<label>", "propositions": [{"text": "<proposition>", "span": "<exact passage>", "relation": "asserts|reports|hedges", "source": "<who>"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (10075 words)

````text
```json
{
  "articles": [
    {
      "article": "A1",
      "propositions": [
        {
          "text": "Carlos Betancur, a South Florida father from Colombia, was detained by U.S. Immigration and Customs Enforcement while pumping gas in Doral on the morning of July 8.",
          "span": "[passage of 24 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Carlos Betancur spent 16 days in federal custody before being released with an ankle monitor.",
          "span": "[passage of 28 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Carlos Betancur was detained at a Marathon gas station on Northwest 58th Street in Doral.",
          "span": "[passage of 27 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "An immigration officer approached Carlos Betancur from behind while he was at the gas pump.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "Carlos Betancur"
        },
        {
          "text": "Carlos Betancur handed over his Florida driver's license to the officer.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "Carlos Betancur"
        },
        {
          "text": "ICE stated that Carlos Betancur had overstayed his visa.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "ICE"
        },
        {
          "text": "Carlos Betancur is now required to wear an ankle monitor while his immigration case proceeds.",
          "span": "[passage of 14 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Carlos Betancur initially spent eight days at the Miramar Processing Center.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Carlos Betancur"
        },
        {
          "text": "On one day at the Miramar Processing Center, there were 93 people in the room.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "Carlos Betancur"
        },
        {
          "text": "On another day at the Miramar Processing Center, there were 104 people in the room.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "Carlos Betancur"
        },
        {
          "text": "Detainees at the Miramar Processing Center took turns sitting down, sleeping and using the restroom because there was not enough space for everyone.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "Carlos Betancur"
        },
        {
          "text": "Carlos Betancur was transferred to the Krome Detention Center after eight days at the Miramar Processing Center.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "Carlos Betancur"
        },
        {
          "text": "Maria Alejandra Betancur believes the public attention surrounding the case may have played a role in the timeline of her father's transfer.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Maria Alejandra Betancur"
        },
        {
          "text": "Carlos Betancur was moved the morning after the outlet story aired.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "Maria Alejandra Betancur"
        },
        {
          "text": "On Wednesday, immigration advocates gathered outside the Miramar Processing Center to protest what they describe as prolonged detentions at a facility intended for short-term processing.",
          "span": "[passage of 25 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Yarelys Mendez Zamora is an activist with the American Friends Service Committee.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The Miramar Processing Center is acting as a detention center when in fact it should not, according to Yarelys Mendez Zamora.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "Yarelys Mendez Zamora"
        },
        {
          "text": "People are being held at the Miramar Processing Center for three or more days and told they must self-deport, according to Yarelys Mendez Zamora.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "Yarelys Mendez Zamora"
        },
        {
          "text": "Carlos Betancur is represented by an immigration attorney.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Carlos Betancur is scheduled to appear before an immigration judge next month.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Carlos Betancur has political asylum documents.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Carlos Betancur has a work permit.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        }
      ]
    },
    {
      "article": "A2",
      "propositions": [
        {
          "text": "735 criminal illegal aliens were arrested by ICE-Houston officers in May.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "The 735 criminal illegal aliens arrested by ICE-Houston officers in May accounted for more than 1,700 criminal convictions.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "Nearly 1,200 of the convictions of the 735 criminal illegal aliens arrested by ICE-Houston officers in May involved violent crimes or threats to public safety.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "The arrests by ICE-Houston officers in May included murderers, rapists, child predators, arsonists, drug traffickers, and members of MS‑13, Surenos 13, 18th Street, Tango Blast, and other brutal gangs.",
          "span": "[passage of 24 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "Gabriel Martinez is ICE Enforcement and Removal Operations Houston acting Field Office Director.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The numbers of arrests reflect who ICE is arresting every single month, not an anomaly, according to Gabriel Martinez.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Gabriel Martinez"
        },
        {
          "text": "25 of the criminal aliens arrested by ICE-Houston officers in May were members of violent gangs.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "The violent gangs whose members were arrested by ICE-Houston officers in May included MS-13, Surenos 13, 18th Street, Tango Blast, Paisas, Chucos Tangos, Southwest Cholos, Brown and Proud, and La Primera.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "The 735 criminal aliens arrested by ICE-Houston officers in May had accumulated more than 1,711 criminal convictions.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "Seventy percent of the convictions of the 735 criminal aliens arrested by ICE-Houston officers in May were for violent crimes which pose threats to the safety of the community.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "ICE arrested more than 200 criminal illegal aliens who have pending criminal charges in the U.S. or abroad in May.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "Carlos Galeano Lara is a 37-year-old criminal illegal alien and foreign fugitive wanted in Honduras for homicide.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "ICE arrested Carlos Galeano Lara on May 25.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        },
        {
          "text": "Carlos Galeano Lara remains in ICE custody pending the disposition of his immigration proceedings.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "U.S. Immigration and Customs Enforcement officials"
        }
      ]
    },
    {
      "article": "A3",
      "propositions": [
        {
          "text": "An ICE officer shot a Venezuelan man in Austin on Sunday.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The shooting left a bullet lodged in the Venezuelan man's back.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The ICE officer who shot the Venezuelan man in Austin was issued a body camera but was not wearing it during the shooting.",
          "span": "[passage of 32 words]",
          "relation": "reports",
          "source": "two officials with the Department of Homeland Security"
        },
        {
          "text": "It was not clear why the ICE officer was not wearing his body camera.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "two officials with the Department of Homeland Security"
        },
        {
          "text": "Another ICE officer who was in the same vehicle was wearing a body camera.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "two officials with the Department of Homeland Security"
        },
        {
          "text": "The body camera of the other ICE officer captured partial footage of the incident.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "two officials with the Department of Homeland Security"
        },
        {
          "text": "The footage from the other ICE officer's body camera does not include the moment of the shooting.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "two officials with the Department of Homeland Security"
        },
        {
          "text": "Wilber Rafael Garcés Pérez is 28 years old.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Wilber Rafael Garcés Pérez is Venezuelan.",
          "span": "[passage of 3 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Wilber Rafael Garcés Pérez was shot early Sunday afternoon by an ICE officer.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Wilber Rafael Garcés Pérez was making deliveries as a DoorDash driver when he was shot.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Wilber Rafael Garcés Pérez was taken to a hospital after being shot.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Four hours after Wilber Rafael Garcés Pérez was shot, he was taken into immigration custody at the South Texas ICE Processing Center in Pearsall, Texas.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "his attorney"
        },
        {
          "text": "The bullet remains in Wilber Rafael Garcés Pérez's back.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "On Tuesday, a federal judge granted an emergency order temporarily blocking deportation proceedings against Wilber Rafael Garcés Pérez.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "his attorney"
        },
        {
          "text": "The Travis County District Attorney's Office sent a letter to DHS and ICE leadership requesting that Wilber Rafael Garcés Pérez be allowed to remain in the country since he is a material witness in their criminal investigation into the shooting.",
          "span": "[passage of 39 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Austin Police Chief Lisa Davis shared video footage obtained by the department as part of their probe into the shooting on Tuesday evening.",
          "span": "[passage of 27 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The videos came from an off-duty officer who captured part of the encounter between ICE and Wilber Rafael Garcés Pérez using his personal dash cam and cellphone.",
          "span": "[passage of 33 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The videos captured the sound of three gunshots.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The off-duty officer alerted his colleagues to the shooting, allowing Austin police to quickly respond to the scene.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Austin Police Chief Lisa Davis said they are seeking the public's help in obtaining any video evidence that can help them piece together the pursuit that preceded the shooting.",
          "span": "[passage of 25 words]",
          "relation": "reports",
          "source": "Austin Police Chief Lisa Davis"
        },
        {
          "text": "The day after he was shot, Wilber Rafael Garcés Pérez began experiencing an inability to move his arm.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez was taken to the hospital Monday afternoon for several hours.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez was sent back to the detention center after being taken to the hospital Monday afternoon.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez told a news conference via phone from detention that he was in a lot of pain and wasn't getting the medical care he needed.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "Wilber Rafael Garcés Pérez"
        },
        {
          "text": "After Wilber Rafael Garcés Pérez spoke out at a news conference, guards at the detention center forcibly took the tablet from his hands.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "After Wilber Rafael Garcés Pérez spoke out at a news conference, guards at the detention center revoked his communication privileges.",
          "span": "[passage of 4 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "After Wilber Rafael Garcés Pérez spoke out at a news conference, guards at the detention center moved him out of the infirmary into an isolated room with a flat bed that cannot be adjusted like a medical bed.",
          "span": "[passage of 23 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez was taken to the hospital around 5 p.m. after losing his ability to move his arm.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez was handcuffed, shackled at the ankles, placed in a waist chain, and handled roughly during his transfer to the hospital.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Doctors spoke to Wilber Rafael Garcés Pérez about his care and gave him morphine for his pain on Tuesday morning.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "The gunshot fractured Wilber Rafael Garcés Pérez's clavicle.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez has significant swelling and is wearing a sling.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez was discharged from the hospital around midnight and taken back to the detention center.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez is receiving Tylenol and ibuprofen for his ongoing pain at the detention center.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez remains in isolation at the detention center.",
          "span": "[passage of 4 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez is on a flat bed at the detention center.",
          "span": "[passage of 4 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez is without the tablet he previously used to communicate at the detention center.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Attorney Lincoln-Goldfinch is asking for Wilber Rafael Garcés Pérez's communication privileges to be immediately restored.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Attorney Lincoln-Goldfinch is asking for Wilber Rafael Garcés Pérez to be provided an appropriate medical bed and adequate medical care.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Attorney Lincoln-Goldfinch is asking for Wilber Rafael Garcés Pérez's immediate release.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Rep. Joaquin Castro said that despite losing movement on his left side and having a bullet lodged next to his spine, ICE has forced Wilber Rafael Garcés Pérez out of the hospital and back to the South Texas ICE Processing Center in Pearsall, Texas.",
          "span": "[passage of 37 words]",
          "relation": "reports",
          "source": "Rep. Joaquin Castro"
        },
        {
          "text": "Rep. Joaquin Castro and Rep. Greg Casar would visit Wilber Rafael Garcés Pérez on Wednesday.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Rep. Joaquin Castro"
        },
        {
          "text": "A DHS spokesperson said on late Sunday that Wilber Rafael Garcés Pérez was in stable condition.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "DHS spokesperson"
        },
        {
          "text": "A DHS spokesperson said on late Sunday that Wilber Rafael Garcés Pérez was in federal custody pending removal from the U.S.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "DHS spokesperson"
        },
        {
          "text": "A senior administration official said on Monday that Wilber Rafael Garcés Pérez did not have a criminal history beyond being in the country illegally.",
          "span": "[passage of 24 words]",
          "relation": "reports",
          "source": "senior administration official"
        },
        {
          "text": "Wilber Rafael Garcés Pérez entered the country legally.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez was seeking asylum.",
          "span": "[passage of 4 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez filed a change of address in immigration court.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez received a notice to appear in court at the old address and never got it.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Because Wilber Rafael Garcés Pérez missed his immigration hearing, he was ordered deported in absentia.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "An unmarked black truck sideswiped Wilber Rafael Garcés Pérez's vehicle.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "Wilber Rafael Garcés Pérez did not know it was ICE as the truck chased him as he tried to make a U-turn.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "ICE pulled Wilber Rafael Garcés Pérez out of the car.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "attorney Lincoln-Goldfinch"
        },
        {
          "text": "ICE Director David Venturella previously told the outlet that every ICE officer and agent would be equipped with body cameras by the end of August.",
          "span": "[passage of 25 words]",
          "relation": "reports",
          "source": "ICE Director David Venturella"
        },
        {
          "text": "ICE would allow the expedited release of bodycam footage when appropriate, according to ICE Director David Venturella.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "ICE Director David Venturella"
        },
        {
          "text": "The possibility of DHS Secretary Markwayne Mullin potentially switching or adding new vendors for body cameras is further delaying the timeline for equipping all ICE officers with body cameras.",
          "span": "[passage of 21 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "A person who witnessed the aftermath of the shooting was waiting on customers at an ice cream shop when he heard gunshots and ran outside.",
          "span": "[passage of 44 words]",
          "relation": "reports",
          "source": "witness"
        },
        {
          "text": "The witness saw immigration agents surrounding a car after the shooting.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "witness"
        },
        {
          "text": "The witness approached the car and saw a man who looked sad and with his eyes full of tears.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "witness"
        },
        {
          "text": "The man told the witness that he was shot in the back.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "witness"
        },
        {
          "text": "A social media video verified by the outlet captures the sound of tires screeching followed by a person exiting a dark-colored SUV as a blue sedan is stopped next to it.",
          "span": "[passage of 31 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Both vehicles in the video are facing each other.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The blue sedan appears to be damaged on the passenger side.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "At least three gunshots are heard in the video as the person approaches the sedan and runs up to it as it slowly lurches forward.",
          "span": "[passage of 22 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The video shows the person standing next to the sedan's driver's side as it stops in front of an intersection.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Another video shows the blue sedan with its driver's side door open and Wilber Rafael Garcés Pérez hunched over in the driver's seat, holding his left upper chest, near his shoulder.",
          "span": "[passage of 29 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Multiple law enforcement officers gather around the blue sedan in the video.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The woman taking the video says \"Why did he do that to him?\"",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The officers tell the woman taking the video that an ambulance is coming.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The video shows Wilber Rafael Garcés Pérez being taken out of the car and handcuffed behind his back.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The agents make Wilber Rafael Garcés Pérez sit on the ground.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "There appears to be a large bloodstain down Wilber Rafael Garcés Pérez's back in the video.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The officers cut open the back of Wilber Rafael Garcés Pérez's shirt in the video.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "A bullet hole is revealed in the back of Wilber Rafael Garcés Pérez's shirt in the video.",
          "span": "[passage of 4 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "An officer asks the woman taking the video if she saw what happened.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The woman taking the video replies in Spanish that they just shot him because he didn't want to stop his vehicle.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The woman taking the video says \"This is unjust\" as she's recording the video.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        }
      ]
    },
    {
      "article": "A4",
      "propositions": [
        {
          "text": "An ICE officer allegedly fatally shot a Colombian man in Maine on Monday.",
          "span": "[passage of 18 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The ICE officer was prone to violence and held racist beliefs, according to some of the people who were close to him.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "people close to the officer"
        },
        {
          "text": "Ashley Brouillette is the ex-wife of the ICE officer who allegedly fatally shot a Colombian man in Maine.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "David Brouillette is the ICE officer who allegedly fatally shot a Colombian man in Maine.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Joan Durán Guerrero is the Colombian man who was allegedly fatally shot by an ICE officer in Maine on Monday.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Joan Durán Guerrero was fatally shot four times during an attempted traffic stop in Biddeford, Maine, on Monday.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette found out that David Brouillette was the officer responsible for the shooting when he called her on Wednesday.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "David Brouillette asked Ashley Brouillette to vouch for his character.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "David Brouillette asked Ashley Brouillette not to talk bad about him.",
          "span": "[passage of 16 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "David Brouillette asked Ashley Brouillette not to talk to anybody if she couldn't not talk bad about him.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "David Brouillette asked Ashley Brouillette not to talk about the abuse in their marriage.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette told David Brouillette that she was not going to lie for him.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "David Brouillette did not respond to messages from the outlet seeking comment.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "An ICE spokesperson said the agency will not confirm or deny whether David Brouillette was the ICE officer responsible for Joan Durán Guerrero's death.",
          "span": "[passage of 22 words]",
          "relation": "reports",
          "source": "ICE spokesperson"
        },
        {
          "text": "ICE spokesperson Lauren Bis said the ICE officer in question has nearly a decade of federal law enforcement experience with required training.",
          "span": "[passage of 27 words]",
          "relation": "reports",
          "source": "ICE spokesperson Lauren Bis"
        },
        {
          "text": "Scott Collins was best friends with David Brouillette in high school in Maine.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "Scott Collins"
        },
        {
          "text": "Scott Collins testified on behalf of Ashley Brouillette in the divorce proceedings.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "David Brouillette's attorneys said that Scott Collins and David Brouillette were once friends, but their relationship ended because Scott Collins was jealous of David Brouillette's successful career.",
          "span": "[passage of 24 words]",
          "relation": "reports",
          "source": "David Brouillette's attorneys"
        },
        {
          "text": "Scott Collins said David Brouillette had a bad tendency of going out and looking for fights.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Scott Collins"
        },
        {
          "text": "Scott Collins said if David Brouillette saw something online that he didn't like, that somebody said that he knew, he would go out and start that fight.",
          "span": "[passage of 23 words]",
          "relation": "reports",
          "source": "Scott Collins"
        },
        {
          "text": "Scott Collins said David Brouillette used anti-Black racial slurs in high school.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "Scott Collins"
        },
        {
          "text": "Ashley Brouillette says she worries racism may have played a part in Joan Durán Guerrero's death.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "David Brouillette has displayed racism.",
          "span": "[passage of 4 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "David Brouillette's nickname in high school was 'White Boy David.'",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette has known David Brouillette since they were preteens.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "There were many moments of violence in Ashley Brouillette and David Brouillette's marriage.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette and David Brouillette's marriage lasted from 2007 to 2009.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "David Brouillette came into the bathroom with a gun and pointed it at Ashley Brouillette and told her that he was going to blow her brains all over the bathtub.",
          "span": "[passage of 44 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "There are no police reports to corroborate Ashley Brouillette's story about David Brouillette coming into the bathroom with a gun.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Ashley Brouillette recanted her story about David Brouillette coming into the bathroom with a gun.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette recanted her story on other occasions after complaining to authorities about David Brouillette's behavior.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette said that even though David Brouillette did horrible things to her, in a way, he was still like her security blanket because he's all she ever known.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette would recant her story and say David Brouillette didn't do anything so then the police wouldn't arrest him for it.",
          "span": "[passage of 23 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "David Brouillette always intimidated Ashley Brouillette.",
          "span": "[passage of 4 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette said intimidation is part of the reason why she stayed silent all these years about things that she has gone through.",
          "span": "[passage of 18 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette kept a profanity-laced voicemail message from November from David Brouillette.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Ashley Brouillette had filed a restraining order against David Brouillette when she received the voicemail message.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "In the voicemail, David Brouillette slurs his speech.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "In the voicemail, David Brouillette says that Ashley Brouillette and the women in her family should have their throats cut.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "David Brouillette says in the voicemail \"Am I threatening that I'm gonna do that? No, no. But do I think that you should have your f****** throat cuts? Or should have had them cut. Yep.\"",
          "span": "[passage of 29 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "When Ashley Brouillette and David Brouillette's marriage had collapsed and they were in the middle of a contentious divorce in 2009, Ashley Brouillette reached out to David Brouillette's platoon leader in the Maine Army National Guard.",
          "span": "[passage of 32 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette offered to fax over paperwork showing that David Brouillette had been diagnosed as having bipolar disorder and borderline schizophrenia.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "The Maine Army National Guard dismissed Ashley Brouillette's concerns as ravings of a petty ex-wife.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "A phone call and message to the Maine National Guard were not immediately returned.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "At the end of last year, David Brouillette first told Ashley Brouillette that he had been hired by ICE.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette honestly thought that David Brouillette was being delusional and she didn't believe it when he told her he had been hired by ICE.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette is unsure if there was a background check for David Brouillette.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "If there had been a background check, they might have seen a trail of violence in David Brouillette's history.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "In 2022, David Brouillette threw his then-13 year-old daughter through a glass coffee table.",
          "span": "[passage of 32 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Child protective services and the police were both called to David Brouillette's home in 2022 after he threw his then-13 year-old daughter through a glass coffee table.",
          "span": "[passage of 24 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "In a 2021 court filing, David Brouillette was stripped of his firearms temporarily.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "In the 2021 court filing, David Brouillette's second ex-wife, Lucinda Brouillette, accused him of becoming more aggressive with their then 13-year-old daughter.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Lucinda Brouillette wrote in the 2021 court filing that David Brouillette asked his then 13-year-old daughter if she thought he was verbally abusive and she told him yes and he grabbed her feet and dragged her out of bed, laughed and asked if she thought he was physically abusive now.",
          "span": "[passage of 37 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Ashley Brouillette said she is distraught over the week's events.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette said that someone has lost their life.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        },
        {
          "text": "Ashley Brouillette said she feels like even though she tried to bring awareness to David Brouillette's mental health conditions before and she got ignored, that she really needs to push and be heard now and hopefully prevent something like this from happening again.",
          "span": "[passage of 39 words]",
          "relation": "reports",
          "source": "Ashley Brouillette"
        }
      ]
    },
    {
      "article": "A5",
      "propositions": [
        {
          "text": "An Arizona man is facing federal charges after prosecutors said he vandalized and attempted to set fire to an Immigration and Customs Enforcement facility.",
          "span": "[passage of 25 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The Arizona man used a propane tank and torch to ignite materials inside the ICE building.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi is from Avondale.",
          "span": "[passage of 4 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi was indicted by a federal grand jury on charges of malicious damage to federal property.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "U.S. Attorney's Office for the District of Arizona"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi was indicted by a federal grand jury on charges of willful depredation against property of the United States.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "U.S. Attorney's Office for the District of Arizona"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi broke a window at the ICE property.",
          "span": "[passage of 8 words]",
          "relation": "reports",
          "source": "prosecutors"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi attempted to ignite the ICE building just after 1 a.m. on Feb. 21, 2026.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "prosecutors"
        },
        {
          "text": "Surveillance video showed Gerardo Mendoza-Acoltzi arriving at the ICE facility shortly before midnight.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "federal authorities"
        },
        {
          "text": "Surveillance video showed Gerardo Mendoza-Acoltzi unloading a propane tank near the front entrance of the ICE facility.",
          "span": "[passage of 9 words]",
          "relation": "reports",
          "source": "federal authorities"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi later returned to the ICE facility and smashed a lobby window with the propane tank.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "prosecutors"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi used a torch connected to the propane tank to ignite window shades inside the ICE building.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "prosecutors"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi arranged rocks outside the ICE facility to spell an anti-ICE message.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "federal authorities"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi left the area after arranging rocks outside the ICE facility.",
          "span": "[passage of 4 words]",
          "relation": "reports",
          "source": "federal authorities"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi was arrested May 7.",
          "span": "[passage of 5 words]",
          "relation": "reports",
          "source": "federal authorities"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi made his initial appearance in federal court shortly after his arrest.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "federal authorities"
        },
        {
          "text": "If convicted, Gerardo Mendoza-Acoltzi could face years in federal prison.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Attempted arson of federal property carries a potential sentence of up to 20 years behind bars.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Depredation against U.S. property carries additional penalties.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Federal officials have increasingly warned about threats and attacks targeting immigration enforcement facilities and personnel.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Threats and attacks targeting immigration enforcement facilities and personnel are occurring amid heightened tensions surrounding border security and deportation operations.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Days before the Arizona incident, state and federal authorities launched an investigation into an attempted arson attack at a DHS office building in Meridian, Idaho.",
          "span": "[passage of 25 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "A suspect allegedly stole an ambulance from a bay at St. Luke's West hospital in Meridian, Idaho.",
          "span": "[passage of 14 words]",
          "relation": "reports",
          "source": "Meridian Police Chief Tracy Basterrechea"
        },
        {
          "text": "The suspect drove the ambulance through a parking lot in Meridian, Idaho.",
          "span": "[passage of 6 words]",
          "relation": "reports",
          "source": "Meridian Police Chief Tracy Basterrechea"
        },
        {
          "text": "The suspect retrieved gas cans that had been staged in nearby vegetation in Meridian, Idaho.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "Meridian Police Chief Tracy Basterrechea"
        },
        {
          "text": "The suspect drove the ambulance into the North Portico building in Meridian, Idaho.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "Meridian Police Chief Tracy Basterrechea"
        },
        {
          "text": "The North Portico building houses DHS offices.",
          "span": "[passage of 4 words]",
          "relation": "reports",
          "source": "Meridian Police Chief Tracy Basterrechea"
        },
        {
          "text": "Investigators believe the suspect poured an accelerant inside and around the outside of the ambulance.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "The suspect was unable to ignite the accelerant before being interrupted by responding officers.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "There has been a lot of rhetoric surrounding the Department of Homeland Security leasing office space at the North Portico building in Meridian, Idaho, according to Meridian Police Chief Tracy Basterrechea.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "Meridian Police Chief Tracy Basterrechea"
        },
        {
          "text": "Comments on social media, such as 'property damage isn't violence,' are false, according to Meridian Police Chief Tracy Basterrechea.",
          "span": "[passage of 13 words]",
          "relation": "reports",
          "source": "Meridian Police Chief Tracy Basterrechea"
        },
        {
          "text": "The attempted arson at the North Portico building in Meridian, Idaho was an act of violence, according to Meridian Police Chief Tracy Basterrechea.",
          "span": "[passage of 7 words]",
          "relation": "reports",
          "source": "Meridian Police Chief Tracy Basterrechea"
        },
        {
          "text": "If the suspect had not been interrupted, there is no doubt the North Portico building in Meridian, Idaho would have been burned, according to Meridian Police Chief Tracy Basterrechea.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "Meridian Police Chief Tracy Basterrechea"
        },
        {
          "text": "If the North Portico building in Meridian, Idaho had been burned, it would have put the lives of first responders and others at risk, according to Meridian Police Chief Tracy Basterrechea.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "Meridian Police Chief Tracy Basterrechea"
        },
        {
          "text": "The charges against Gerardo Mendoza-Acoltzi are allegations.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Gerardo Mendoza-Acoltzi is presumed innocent unless proven guilty in court.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        }
      ]
    },
    {
      "article": "A6",
      "propositions": [
        {
          "text": "Immigration and Customs Enforcement is continuing to arrest illegal aliens across the United States.",
          "span": "[passage of 15 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "ICE has recently arrested illegal aliens convicted of child sexual abuse, child abuse, domestic violence, and drug trafficking, among other crimes.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Over the weekend, while Americans enjoyed UFC Freedom 250 in the nation's capital, the men and women of ICE law enforcement were hard at work arresting pedophiles, drug traffickers, and other violent criminals, according to the Department of Homeland Security's Lauren Bis.",
          "span": "[passage of 33 words]",
          "relation": "reports",
          "source": "Department of Homeland Security's Lauren Bis"
        },
        {
          "text": "Miguel Gorasieta Jaimes is from Mexico.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Miguel Gorasieta Jaimes was convicted of aggravated sexual assault of a child in Harris County, Texas.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Teodolo Resendiz-Figueroa is from Mexico.",
          "span": "[passage of 4 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Teodolo Resendiz-Figueroa was convicted of continuous sexual abuse of a child in Los Angeles, California.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Teodolo Resendiz-Figueroa was convicted of three counts of lewd act upon a child in Los Angeles, California.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Cesar Martin Sanchez-Martinez is from Mexico.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Cesar Martin Sanchez-Martinez was previously convicted of felony vehicular assault in Arapahoe County, Colorado.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Cesar Martin Sanchez-Martinez was previously convicted of child abuse with serious bodily injury in Arapahoe County, Colorado.",
          "span": "[passage of 11 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Urbano Estrada-Santizo is from Guatemala.",
          "span": "[passage of 4 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Urbano Estrada-Santizo was convicted of drunk driving in Nashville, Tennessee.",
          "span": "[passage of 4 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Urbano Estrada-Santizo was convicted of felony incest in Nashville, Tennessee.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Edinson Amador is from the Dominican Republic.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Edinson Amador was convicted of drug trafficking cocaine in Boston, Massachusetts.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Noe Moreno-Salazar is a criminal illegal alien from Mexico.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Noe Moreno-Salazar was convicted for criminal sexual abuse in St. Charles, Illinois.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Noe Moreno-Salazar was convicted for possession of a controlled substance in St. Charles, Illinois.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Noe Moreno-Salazar was convicted for aggravated unlawful use of a loaded weapon in St. Charles, Illinois.",
          "span": "[passage of 12 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Santos Ruben Gutierrez is a criminal illegal alien from El Salvador.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Santos Ruben Gutierrez was convicted for indecency with a child in Lewisville, Texas.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Ramon R. Castillo is a criminal illegal alien from Mexico.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Ramon R. Castillo was convicted for lewd or lascivious acts with a child under 14 years old in Santa Clarita, California.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Alex Jimenez-Cochancela is a criminal illegal alien from Ecuador.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Alex Jimenez-Cochancela was convicted for promoting a sexual performance by a child in Carmel, New York.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Salomon Santos-Cach is a criminal illegal alien from Mexico.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Salomon Santos-Cach was convicted for assault of a minor with intent to commit rape in Sonoma, California.",
          "span": "[passage of 14 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Santa Mongar is a criminal illegal alien from Bhutan.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Santa Mongar was convicted for assault and battery in Lancaster, Pennsylvania.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Santa Mongar was convicted for first-degree sexual abuse in Lancaster, Pennsylvania.",
          "span": "[passage of 7 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Jose Victor Gonzalez-Rosales is a criminal illegal alien from El Salvador.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Jose Victor Gonzalez-Rosales was convicted of battery of spouse in Los Angeles, California.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Jose Victor Gonzalez-Rosales was convicted of obstructing/resisting a police officer in Los Angeles, California.",
          "span": "[passage of 4 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Jose Victor Gonzalez-Rosales was convicted of burglary in Los Angeles, California.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Luis Ramos-Sacramento is a criminal illegal alien from Mexico.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Luis Ramos-Sacramento was convicted for endangering the welfare of a child – abuse/neglect in Freehold, New Jersey.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Luis Ramos-Sacramento was convicted for aggravated assault – domestic violence in Freehold, New Jersey.",
          "span": "[passage of 10 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Nicandro Garcia-Perez is a criminal illegal alien from Mexico.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Nicandro Garcia-Perez was convicted for possession with the intent to distribute five kilograms or more of cocaine in the U.S. District Court for the District of Nebraska.",
          "span": "[passage of 24 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "James Ayur Garang is a criminal illegal alien from Sudan.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "James Ayur Garang was convicted for conspiracy to distribute a controlled substance in Sioux Falls, South Dakota.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "ICE law enforcement works around the clock to deliver on President Trump's promise to make America safe again, according to the Department of Homeland Security's Lauren Bis.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "Department of Homeland Security's Lauren Bis"
        },
        {
          "text": "Under President Trump and Secretary Mullin, ICE will continue to target the worst of the worst and protect American communities, according to the Department of Homeland Security's Lauren Bis.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Department of Homeland Security's Lauren Bis"
        }
      ]
    }
  ]
}
```
````

</details>
