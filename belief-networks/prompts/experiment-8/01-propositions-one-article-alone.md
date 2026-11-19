# Experiment 8, prompt test, step 1 of 7: Propositions: one article alone

Propositions of an article. Requests sent: 9. Models: Haiku 4.5, GPT-4o, Sonnet 5.5. First and last request: 16 October 2026, 12:46 to 14:28 (Pacific time).

The request asks: “List the propositions about the world that the article labelled A1 contains.”

## The template

`props_A.txt`. The parts in braces are filled in for each request.

```text
The following news article is labelled {labels}. The name of the outlet has been removed.

{articles}

Task: list the propositions about the world that the article labelled {target} contains.

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

## Requests as sent (9)

One request for each combination of model, round, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>GPT-4o, temperature 0 · Round 1 · 16 October 2026, 12:50</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (729 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




Task: list the propositions about the world that the article labelled A1 contains.

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

**The reply** (601 words)

```text
{
  "articles": [
    {
      "article": "A1",
      "propositions": [
        {
          "text": "Georgia Tech is welcoming its incoming freshman class to campus this week.",
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
          "text": "Artificial intelligence is changing STEM industries.",
          "span": "[passage of 5 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing how Georgia Tech approaches its curriculum.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing the job market.",
          "span": "[passage of 8 words]",
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
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Georgia Tech recognizes that AI is changing STEM industries.",
          "span": "[passage of 11 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Some professors at Georgia Tech are building their own AI agents that are serving as tutors for classes.",
          "span": "[passage of 17 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Plenty of faculty at Georgia Tech are reacting to AI by changing their assignments from essays to class discussions.",
          "span": "[passage of 40 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "AI can help students complete some tasks more quickly.",
          "span": "[passage of 12 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "The old model of going to college for four years and then having a 40-year career has been dead for a while.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "AI provides a new tool to help go through a process faster.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "AI means that students are not going to spend time formulating an idea, spend three weeks building software, and then encounter the next big challenge.",
          "span": "[passage of 25 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Students are going to formulate the idea and have AI help them write the software.",
          "span": "[passage of 15 words]",
          "relation": "reports",
          "source": "David Joyner"
        }
      ]
    }
  ]
}
```

</details>

<details><summary>Haiku 4.5, temperature 0 · Round 1 · 16 October 2026, 12:58</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (729 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




Task: list the propositions about the world that the article labelled A1 contains.

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

**The reply** (564 words)

````text
```json
{
  "articles": [
    {
      "article": "A1",
      "propositions": [
        {
          "text": "Georgia Tech is welcoming its incoming freshman class to campus this week in 2026.",
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
          "text": "Artificial intelligence is changing industries in computer science, engineering and other STEM fields.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing how Georgia Tech approaches its curriculum.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing the job market.",
          "span": "[passage of 8 words]",
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
          "text": "Georgia Tech recognizes that artificial intelligence is changing STEM industries.",
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
          "text": "Some Georgia Tech professors are reacting to artificial intelligence by changing assignment types from essays to class discussions.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Artificial intelligence can help students complete some tasks more quickly.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "The model of attending college for four years followed by a 40-year career has been dead for a while.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Artificial intelligence provides a tool to help people complete processes faster.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "With artificial intelligence assistance, people will formulate ideas and have AI help write software rather than spending weeks building software before encountering the next challenge.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "David Joyner"
        }
      ]
    }
  ]
}
```
````

</details>

<details><summary>Haiku 4.5, temperature 1 · Round 1 · 16 October 2026, 13:08</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (729 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




Task: list the propositions about the world that the article labelled A1 contains.

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

**The reply** (569 words)

````text
```json
{
  "articles": [
    {
      "article": "A1",
      "propositions": [
        {
          "text": "Georgia Tech is welcoming its incoming freshman class to campus this week in 2026.",
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
          "text": "Artificial intelligence is changing industries in computer science, engineering and other STEM fields.",
          "span": "[passage of 6 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing how Georgia Tech approaches its curriculum.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing the job market.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing how Georgia Tech professors plan their lessons.",
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
          "text": "Some Georgia Tech faculty members are responding to artificial intelligence by changing their assignments from traditional essays to in-class discussions.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Artificial intelligence can help students complete some tasks more quickly.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "The traditional model of attending college for four years and then having a 40-year career is no longer current.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Artificial intelligence provides a tool to help complete processes faster than previously possible.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Using artificial intelligence, people can formulate ideas, have AI help write software, and encounter the next challenge without spending three weeks building software themselves.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "David Joyner"
        }
      ]
    }
  ]
}
```
````

</details>

<details><summary>Sonnet 5.5 · Round 1 · 16 October 2026, 12:46</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (729 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




Task: list the propositions about the world that the article labelled A1 contains.

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

**The reply** (388 words)

```text
{"articles":[{"article":"A1","propositions":[{"text":"Georgia Tech is welcoming its incoming freshman class to campus during the week of 20 August 2026.","span":"[passage of 12 words]","relation":"asserts","source":"the article"},{"text":"Georgia Tech is known for its computer science, engineering and other STEM programs.","span":"[passage of 13 words]","relation":"asserts","source":"the article"},{"text":"Artificial intelligence is changing STEM industries.","span":"[passage of 7 words]","relation":"asserts","source":"the article"},{"text":"Artificial intelligence is changing how Georgia Tech approaches its curriculum.","span":"[passage of 7 words]","relation":"asserts","source":"the article"},{"text":"Artificial intelligence is changing the job market.","span":"[passage of 8 words]","relation":"asserts","source":"the article"},{"text":"Artificial intelligence is changing how professors plan their lessons.","span":"[passage of 9 words]","relation":"asserts","source":"the article"},{"text":"Nearly 15,000 Georgia Tech students are majoring or minoring in AI-related fields, including computer science.","span":"[passage of 15 words]","relation":"reports","source":"David Joyner"},{"text":"Georgia Tech recognizes that AI is changing STEM industries.","span":"[passage of 11 words]","relation":"reports","source":"David Joyner"},{"text":"Some Georgia Tech professors are building their own AI agents that serve as tutors for their classes.","span":"[passage of 17 words]","relation":"reports","source":"David Joyner"},{"text":"Plenty of Georgia Tech faculty are replacing assignments such as 10-page essays with in-class discussion in reaction to AI.","span":"[passage of 38 words]","relation":"reports","source":"David Joyner"},{"text":"AI can help students complete some tasks more quickly.","span":"[passage of 12 words]","relation":"reports","source":"David Joyner"},{"text":"The old model of going to college for four years and then having a 40-year career has been dead for a while, and students are aware of this.","span":"[passage of 26 words]","relation":"reports","source":"David Joyner"},{"text":"AI gives people a new tool to go through a process faster.","span":"[passage of 19 words]","relation":"reports","source":"David Joyner"},{"text":"With AI, people can formulate an idea and have AI help write the software, rather than spending three weeks building the software themselves.","span":"[passage of 13 words]","relation":"reports","source":"David Joyner"}]}]}
```

</details>

<details><summary>GPT-4o, temperature 0 · Round 2 · 16 October 2026, 13:18</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (770 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




Task: list the propositions about the world that the article labelled A1 contains.

A proposition is a single claim about the world that an article states or reports: what happened or is the case, what a number is, what a rule or status is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each proposition contains exactly one claim. Test every proposition before you list it: if it can be divided into two statements, each of which could be true while the other is false, divide it and list both. Two numbers, two findings, a finding and a second finding about its size or timing, or a fact and a comment on it are two claims. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal claim (A causes B) is one proposition only when the causal link is the claim.
2. Each proposition must stand on its own: a reader who has not seen the article must be able to understand it. Resolve pronouns, give full names, and include the time, place and population when the claim's truth depends on them. Add nothing else.
3. State the proposition as a claim about the world, not about the article. When an article reports a claim made by a person or a study, state the claim itself and record the source in "relation" and "source"; do not write "the article says".
4. Keep the article's meaning. Do not strengthen, weaken, generalise or soften the claim.
5. Leave out rhetorical flourishes, questions, and claims whose meaning cannot be resolved from the article.
6. Each proposition must come from the article it is listed under. Copy, character for character, the shortest passage of that article that states it ("span"). The passage must be one continuous stretch of the article, with every word, letter and punctuation mark exactly as in the article: do not change a word, do not shorten it with "...", and do not join passages from different places.
7. List every proposition the article contains. Do not list the same proposition twice in different words.

For each proposition, give "relation": "asserts" (the article states it in its own voice), "reports" (the article reports a person, group or study saying it), or "hedges" (the article states it with doubt or qualification), and "source": who makes the claim (a person, group or study as named in the article, or "the article" when it is the article's own voice).

Return JSON of the form {"articles": [{"article": "<label>", "propositions": [{"text": "<proposition>", "span": "<exact passage>", "relation": "asserts|reports|hedges", "source": "<who>"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (581 words)

```text
{"articles": [{"article": "A1", "propositions": [{"text": "Georgia Tech is welcoming its incoming freshman class to campus this week.", "span": "[passage of 12 words]", "relation": "asserts", "source": "the article"}, {"text": "Georgia Tech is known for its computer science, engineering and other STEM programs.", "span": "[passage of 13 words]", "relation": "asserts", "source": "the article"}, {"text": "Artificial intelligence is changing the industries of computer science, engineering and other STEM fields.", "span": "[passage of 15 words]", "relation": "asserts", "source": "the article"}, {"text": "Artificial intelligence is changing how Georgia Tech approaches its curriculum.", "span": "[passage of 15 words]", "relation": "asserts", "source": "the article"}, {"text": "AI is changing the job market.", "span": "[passage of 8 words]", "relation": "asserts", "source": "the article"}, {"text": "AI is changing how professors plan their lessons.", "span": "[passage of 9 words]", "relation": "asserts", "source": "the article"}, {"text": "Nearly 15,000 students at Georgia Tech are majoring in or minoring in AI-related fields, including computer science.", "span": "[passage of 26 words]", "relation": "reports", "source": "David Joyner"}, {"text": "Georgia Tech recognizes that AI is changing STEM industries.", "span": "[passage of 11 words]", "relation": "reports", "source": "David Joyner"}, {"text": "Some professors at Georgia Tech are building their own AI agents that are serving as tutors for classes.", "span": "[passage of 17 words]", "relation": "reports", "source": "David Joyner"}, {"text": "Plenty of faculty at Georgia Tech are reacting to AI by changing their assignments from essays to class discussions.", "span": "[passage of 40 words]", "relation": "reports", "source": "David Joyner"}, {"text": "AI can help students complete some tasks more quickly.", "span": "[passage of 12 words]", "relation": "reports", "source": "David Joyner"}, {"text": "The old model of going to college for four years and then having a 40-year career has been dead for a while.", "span": "[passage of 26 words]", "relation": "reports", "source": "David Joyner"}, {"text": "AI provides a new tool to help go through a process faster.", "span": "[passage of 19 words]", "relation": "reports", "source": "David Joyner"}, {"text": "AI means that students are not going to spend time formulating an idea, spend three weeks building software, and then encounter the next big challenge.", "span": "[passage of 25 words]", "relation": "reports", "source": "David Joyner"}, {"text": "Students are going to formulate the idea and have AI help them write the software.", "span": "[passage of 15 words]", "relation": "reports", "source": "David Joyner"}]}]}
```

</details>

<details><summary>GPT-4o, temperature 0 · Round 4, ICE articles · 16 October 2026, 14:28</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1022 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: Breitbart, 2026-06-15, “Exclusive: ICE Agents Arrest Illegal Aliens Convicted of Pedophilia, Child Abuse, Domestic Violence”, 490 words. Text not included.]




Task: list the propositions about the world that the article labelled A1 contains.

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

**The reply** (1311 words)

```text
{
  "articles": [
    {
      "article": "A1",
      "propositions": [
        {
          "text": "Immigration and Customs Enforcement (ICE) is continuing to arrest illegal aliens across the United States.",
          "span": "[passage of 38 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "ICE is arresting illegal aliens convicted of child sexual abuse, child abuse, domestic violence, and drug trafficking.",
          "span": "[passage of 38 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Americans enjoyed UFC Freedom 250 in the nation’s capital over the weekend.",
          "span": "[passage of 41 words]",
          "relation": "reports",
          "source": "Lauren Bis"
        },
        {
          "text": "ICE law enforcement was hard at work arresting pedophiles, drug traffickers, and other violent criminals over the weekend.",
          "span": "[passage of 41 words]",
          "relation": "reports",
          "source": "Lauren Bis"
        },
        {
          "text": "Miguel Gorasieta Jaimes of Mexico was convicted of aggravated sexual assault of a child in Harris County, Texas.",
          "span": "[passage of 52 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Teodolo Resendiz-Figueroa of Mexico was convicted of continuous sexual abuse of a child and three counts of lewd act upon a child in Los Angeles, California.",
          "span": "[passage of 52 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Cesar Martin Sanchez-Martinez of Mexico was previously convicted of felony vehicular assault and child abuse with serious bodily injury in Arapahoe County, Colorado.",
          "span": "[passage of 45 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Urbano Estrada-Santizo of Guatemala was convicted of drunk driving and felony incest in Nashville, Tennessee.",
          "span": "[passage of 45 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Edinson Amador of the Dominican Republic was convicted of drug trafficking cocaine in Boston, Massachusetts.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Noe Moreno-Salazar, a criminal illegal alien from Mexico, was convicted for criminal sexual abuse, possession of a controlled substance, and aggravated unlawful use of a loaded weapon in St. Charles, Illinois.",
          "span": "[passage of 30 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Santos Ruben Gutierrez, a criminal illegal alien from El Salvador, was convicted for indecency with a child in Lewisville, Texas.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Ramon R. Castillo, a criminal illegal alien from Mexico, was convicted for lewd or lascivious acts with a child under 14 years old in Santa Clarita, California.",
          "span": "[passage of 26 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Alex Jimenez-Cochancela, a criminal illegal alien from Ecuador, was convicted for promoting a sexual performance by a child in Carmel, New York.",
          "span": "[passage of 21 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Salomon Santos-Cach, a criminal illegal alien from Mexico, was convicted for assault of a minor with intent to commit rape in Sonoma, California.",
          "span": "[passage of 22 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Santa Mongar, a criminal illegal alien from Bhutan, was convicted for assault and battery and first-degree sexual abuse in Lancaster, Pennsylvania.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Jose Victor Gonzalez-Rosales, a criminal illegal alien from El Salvador, was convicted of battery of spouse, obstructing/resisting a police officer, and burglary in Los Angeles, California.",
          "span": "[passage of 25 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Luis Ramos-Sacramento, a criminal illegal alien from Mexico, was convicted for endangering the welfare of a child – abuse/neglect and aggravated assault – domestic violence in Freehold, New Jersey.",
          "span": "[passage of 28 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Nicandro Garcia-Perez, a criminal illegal alien from Mexico, was convicted for possession with the intent to distribute five kilograms or more of cocaine in the U.S. District Court for the District of Nebraska.",
          "span": "[passage of 32 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "James Ayur Garang, a criminal illegal alien from Sudan, was convicted for conspiracy to distribute a controlled substance in Sioux Falls, South Dakota.",
          "span": "[passage of 22 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "ICE law enforcement works around the clock to deliver on President Trump’s promise to make America safe again.",
          "span": "[passage of 21 words]",
          "relation": "reports",
          "source": "Lauren Bis"
        },
        {
          "text": "Under President Trump and Secretary Mullin, ICE will continue to target the worst of the worst and protect American communities.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Lauren Bis"
        }
      ]
    }
  ]
}
```

</details>

<details><summary>Haiku 4.5, temperature 0 · Round 2 · 16 October 2026, 13:16</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (770 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




Task: list the propositions about the world that the article labelled A1 contains.

A proposition is a single claim about the world that an article states or reports: what happened or is the case, what a number is, what a rule or status is, what causes what, what will happen, or what is good, bad or should be done. Follow these rules.
1. Each proposition contains exactly one claim. Test every proposition before you list it: if it can be divided into two statements, each of which could be true while the other is false, divide it and list both. Two numbers, two findings, a finding and a second finding about its size or timing, or a fact and a comment on it are two claims. Do not join two claims with "and", "while", "with", "as well as", "but", "which", a comma or a semicolon. "And" may appear only inside a name, or in a list that is itself the single thing the claim is about. A causal claim (A causes B) is one proposition only when the causal link is the claim.
2. Each proposition must stand on its own: a reader who has not seen the article must be able to understand it. Resolve pronouns, give full names, and include the time, place and population when the claim's truth depends on them. Add nothing else.
3. State the proposition as a claim about the world, not about the article. When an article reports a claim made by a person or a study, state the claim itself and record the source in "relation" and "source"; do not write "the article says".
4. Keep the article's meaning. Do not strengthen, weaken, generalise or soften the claim.
5. Leave out rhetorical flourishes, questions, and claims whose meaning cannot be resolved from the article.
6. Each proposition must come from the article it is listed under. Copy, character for character, the shortest passage of that article that states it ("span"). The passage must be one continuous stretch of the article, with every word, letter and punctuation mark exactly as in the article: do not change a word, do not shorten it with "...", and do not join passages from different places.
7. List every proposition the article contains. Do not list the same proposition twice in different words.

For each proposition, give "relation": "asserts" (the article states it in its own voice), "reports" (the article reports a person, group or study saying it), or "hedges" (the article states it with doubt or qualification), and "source": who makes the claim (a person, group or study as named in the article, or "the article" when it is the article's own voice).

Return JSON of the form {"articles": [{"article": "<label>", "propositions": [{"text": "<proposition>", "span": "<exact passage>", "relation": "asserts|reports|hedges", "source": "<who>"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (512 words)

````text
```json
{
  "articles": [
    {
      "article": "A1",
      "propositions": [
        {
          "text": "Georgia Tech is known for its computer science, engineering and other STEM programs.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing industries in computer science, engineering and other STEM fields.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing how Georgia Tech approaches its curriculum.",
          "span": "[passage of 14 words]",
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
          "text": "Georgia Tech recognizes that artificial intelligence is changing STEM industries.",
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
          "text": "Some Georgia Tech professors are reacting to artificial intelligence by changing their assignment formats away from traditional essays.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Artificial intelligence can help students complete some tasks more quickly.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "The model of attending college for four years followed by a 40-year career has been dead for a while.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Artificial intelligence provides a tool to help complete processes faster.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "With artificial intelligence assistance, the process of formulating an idea and building software will be faster than the previous model of spending three weeks building software after formulating an idea.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "David Joyner"
        }
      ]
    }
  ]
}
```
````

</details>

<details><summary>Haiku 4.5, temperature 0 · Round 3 · 16 October 2026, 13:22</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (789 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




Task: list the propositions about the world that the article labelled A1 contains.

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

**The reply** (506 words)

````text
```json
{
  "articles": [
    {
      "article": "A1",
      "propositions": [
        {
          "text": "Georgia Tech is known for its computer science, engineering and other STEM programs.",
          "span": "[passage of 13 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing industries in computer science, engineering and other STEM fields.",
          "span": "[passage of 8 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Artificial intelligence is changing how Georgia Tech approaches its curriculum.",
          "span": "[passage of 14 words]",
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
          "text": "Georgia Tech recognizes that artificial intelligence is changing STEM industries.",
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
          "text": "Some Georgia Tech professors are reacting to artificial intelligence by changing their assignment formats away from traditional essays.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Artificial intelligence can help students complete some tasks more quickly.",
          "span": "[passage of 10 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "The model of attending college for four years followed by a 40-year career has been dead for a while.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Artificial intelligence provides a tool to help complete processes faster.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "With artificial intelligence assistance, the process of formulating an idea, building software, and encountering the next challenge will be faster than the traditional approach.",
          "span": "[passage of 38 words]",
          "relation": "reports",
          "source": "David Joyner"
        }
      ]
    }
  ]
}
```
````

</details>

<details><summary>Haiku 4.5, temperature 0 · Round 4, ICE articles · 16 October 2026, 14:24</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1022 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: Breitbart, 2026-06-15, “Exclusive: ICE Agents Arrest Illegal Aliens Convicted of Pedophilia, Child Abuse, Domestic Violence”, 490 words. Text not included.]




Task: list the propositions about the world that the article labelled A1 contains.

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

**The reply** (1833 words)

````text
```json
{
  "articles": [
    {
      "article": "A1",
      "propositions": [
        {
          "text": "Immigration and Customs Enforcement (ICE) is continuing to arrest illegal aliens across the United States.",
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
          "text": "Over the weekend, ICE law enforcement arrested pedophiles, drug traffickers, and other violent criminals.",
          "span": "[passage of 33 words]",
          "relation": "reports",
          "source": "Lauren Bis"
        },
        {
          "text": "Miguel Gorasieta Jaimes of Mexico was convicted of aggravated sexual assault of a child in Harris County, Texas.",
          "span": "[passage of 17 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Miguel Gorasieta Jaimes of Mexico was arrested by ICE.",
          "span": "[passage of 14 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Teodolo Resendiz-Figueroa of Mexico was convicted of continuous sexual abuse of a child in Los Angeles, California.",
          "span": "[passage of 25 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Teodolo Resendiz-Figueroa of Mexico was convicted of three counts of lewd act upon a child in Los Angeles, California.",
          "span": "[passage of 25 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Teodolo Resendiz-Figueroa of Mexico was arrested by ICE.",
          "span": "[passage of 19 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Cesar Martin Sanchez-Martinez of Mexico was convicted of felony vehicular assault in Arapahoe County, Colorado.",
          "span": "[passage of 24 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Cesar Martin Sanchez-Martinez of Mexico was convicted of child abuse with serious bodily injury in Arapahoe County, Colorado.",
          "span": "[passage of 24 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Cesar Martin Sanchez-Martinez of Mexico was arrested by ICE.",
          "span": "[passage of 9 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Urbano Estrada-Santizo of Guatemala was convicted of drunk driving in Nashville, Tennessee.",
          "span": "[passage of 14 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Urbano Estrada-Santizo of Guatemala was convicted of felony incest in Nashville, Tennessee.",
          "span": "[passage of 14 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Urbano Estrada-Santizo of Guatemala was arrested by ICE.",
          "span": "[passage of 16 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Edinson Amador of the Dominican Republic was convicted of drug trafficking cocaine in Boston, Massachusetts.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Edinson Amador of the Dominican Republic was arrested by ICE.",
          "span": "[passage of 9 words]",
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
          "text": "Noe Moreno-Salazar was convicted of criminal sexual abuse in St. Charles, Illinois.",
          "span": "[passage of 30 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Noe Moreno-Salazar was convicted of possession of a controlled substance in St. Charles, Illinois.",
          "span": "[passage of 30 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Noe Moreno-Salazar was convicted of aggravated unlawful use of a loaded weapon in St. Charles, Illinois.",
          "span": "[passage of 30 words]",
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
          "text": "Santos Ruben Gutierrez was convicted of indecency with a child in Lewisville, Texas.",
          "span": "[passage of 19 words]",
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
          "text": "Ramon R. Castillo was convicted of lewd or lascivious acts with a child under 14 years old in Santa Clarita, California.",
          "span": "[passage of 26 words]",
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
          "text": "Alex Jimenez-Cochancela was convicted of promoting a sexual performance by a child in Carmel, New York.",
          "span": "[passage of 21 words]",
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
          "text": "Salomon Santos-Cach was convicted of assault of a minor with intent to commit rape in Sonoma, California.",
          "span": "[passage of 22 words]",
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
          "text": "Santa Mongar was convicted of assault and battery in Lancaster, Pennsylvania.",
          "span": "[passage of 20 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Santa Mongar was convicted of first-degree sexual abuse in Lancaster, Pennsylvania.",
          "span": "[passage of 20 words]",
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
          "span": "[passage of 25 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Jose Victor Gonzalez-Rosales was convicted of obstructing/resisting a police officer in Los Angeles, California.",
          "span": "[passage of 25 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Jose Victor Gonzalez-Rosales was convicted of burglary in Los Angeles, California.",
          "span": "[passage of 25 words]",
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
          "text": "Luis Ramos-Sacramento was convicted of endangering the welfare of a child – abuse/neglect in Freehold, New Jersey.",
          "span": "[passage of 28 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "Luis Ramos-Sacramento was convicted of aggravated assault – domestic violence in Freehold, New Jersey.",
          "span": "[passage of 28 words]",
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
          "text": "Nicandro Garcia-Perez was convicted of possession with the intent to distribute five kilograms or more of cocaine in the U.S. District Court for the District of Nebraska.",
          "span": "[passage of 32 words]",
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
          "text": "James Ayur Garang was convicted of conspiracy to distribute a controlled substance in Sioux Falls, South Dakota.",
          "span": "[passage of 22 words]",
          "relation": "asserts",
          "source": "the article"
        },
        {
          "text": "ICE law enforcement works around the clock to deliver on President Trump's promise to make America safe again.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "Lauren Bis"
        },
        {
          "text": "Under President Trump and Secretary Mullin, ICE will continue to target the worst of the worst and protect American communities.",
          "span": "[passage of 20 words]",
          "relation": "reports",
          "source": "Lauren Bis"
        }
      ]
    }
  ]
}
```
````

</details>
