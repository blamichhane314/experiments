# Experiment 8, prompt test, step 4 of 7: Propositions: one article beside an unrelated article

Propositions of an article. Requests sent: 4. Models: Haiku 4.5, Sonnet 5.5, GPT-4o. First and last request: 16 October 2026, 12:48 to 13:13 (Pacific time).

The request asks: “List the propositions about the world that the article labelled A1 contains.”

## Requests as sent (4)

One request for each combination of model, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>GPT-4o, temperature 0 · Round 1 · 16 October 2026, 12:52</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1325 words)

```text
The following 2 news articles are labelled A1, A2. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: Science News, 2026-06-02, “Microsoft’s quantum chip got an upgrade. Critics are still skeptical”, 578 words. Text not included.]




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

**The reply** (585 words)

```text
{"articles": [{"article": "A1", "propositions": [{"text": "Georgia Tech is welcoming its incoming freshman class to campus this week.", "span": "[passage of 12 words]", "relation": "asserts", "source": "the article"}, {"text": "Georgia Tech is known for its computer science, engineering and other STEM programs.", "span": "[passage of 13 words]", "relation": "asserts", "source": "the article"}, {"text": "Artificial intelligence is changing the industries of computer science, engineering, and other STEM fields.", "span": "[passage of 15 words]", "relation": "asserts", "source": "the article"}, {"text": "Artificial intelligence is changing how Georgia Tech approaches its curriculum.", "span": "[passage of 15 words]", "relation": "asserts", "source": "the article"}, {"text": "AI is changing the job market.", "span": "[passage of 8 words]", "relation": "asserts", "source": "the article"}, {"text": "AI is changing how professors plan their lessons.", "span": "[passage of 9 words]", "relation": "asserts", "source": "the article"}, {"text": "Nearly 15,000 students at Georgia Tech are majoring in or minoring in AI-related fields, including computer science.", "span": "[passage of 26 words]", "relation": "reports", "source": "David Joyner"}, {"text": "Georgia Tech recognizes that AI is changing STEM industries.", "span": "[passage of 11 words]", "relation": "reports", "source": "David Joyner"}, {"text": "Some professors at Georgia Tech are building their own AI agents that are serving as tutors for classes.", "span": "[passage of 17 words]", "relation": "reports", "source": "David Joyner"}, {"text": "Plenty of faculty at Georgia Tech are reacting to AI by changing their assignments from essays to class discussions.", "span": "[passage of 40 words]", "relation": "reports", "source": "David Joyner"}, {"text": "AI can help students complete some tasks more quickly.", "span": "[passage of 12 words]", "relation": "reports", "source": "David Joyner"}, {"text": "The old model of going to college for four years and then having a 40-year career has been dead for a while.", "span": "[passage of 26 words]", "relation": "reports", "source": "David Joyner"}, {"text": "AI plays a role in giving a new tool to help go through a process faster.", "span": "[passage of 19 words]", "relation": "reports", "source": "David Joyner"}, {"text": "AI means that students are not going to spend time formulating an idea, spend three weeks building software, and then encounter the next big challenge.", "span": "[passage of 25 words]", "relation": "reports", "source": "David Joyner"}, {"text": "Students are going to formulate the idea and have AI help them write the software.", "span": "[passage of 15 words]", "relation": "reports", "source": "David Joyner"}]}]}
```

</details>

<details><summary>Haiku 4.5, temperature 0 · Round 1 · 16 October 2026, 13:03</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1325 words)

```text
The following 2 news articles are labelled A1, A2. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: Science News, 2026-06-02, “Microsoft’s quantum chip got an upgrade. Critics are still skeptical”, 578 words. Text not included.]




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

**The reply** (514 words)

````text
```json
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
          "text": "Artificial intelligence is changing industries in computer science, engineering and other STEM fields.",
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
          "text": "Nearly 15,000 students are majoring in or minoring in AI-related fields, including computer science, at Georgia Tech.",
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
          "text": "Some Georgia Tech professors are reacting to AI by changing their assignments from requiring 10-page essays to having in-class discussions instead.",
          "span": "[passage of 38 words]",
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
          "text": "The model of attending college for four years and then having a 40-year career has been dead for a while.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "AI provides a tool to help complete processes faster.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "With AI assistance, people will formulate an idea, have AI help write software, and then encounter the next big challenge, rather than spending three weeks building software after formulating an idea.",
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

<details><summary>Haiku 4.5, temperature 1 · Round 1 · 16 October 2026, 13:13</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1325 words)

```text
The following 2 news articles are labelled A1, A2. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: Science News, 2026-06-02, “Microsoft’s quantum chip got an upgrade. Critics are still skeptical”, 578 words. Text not included.]




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

**The reply** (555 words)

````text
```json
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
          "text": "Artificial intelligence is changing the industries of computer science, engineering and other STEM fields.",
          "span": "[passage of 7 words]",
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
          "span": "[passage of 17 words]",
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
          "text": "Some Georgia Tech professors are reacting to AI by changing their assignments so that students come to class for discussion instead of delivering essays.",
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
          "text": "The traditional model of attending college for four years and then having a 40-year career has ended.",
          "span": "[passage of 26 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "AI provides a new tool to help people complete a process faster.",
          "span": "[passage of 19 words]",
          "relation": "reports",
          "source": "David Joyner"
        },
        {
          "text": "Using AI can reduce the time spent on certain tasks like writing software, allowing people to move on to the next big challenge more quickly.",
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

<details><summary>Sonnet 5.5 · Round 1 · 16 October 2026, 12:48</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1325 words)

```text
The following 2 news articles are labelled A1, A2. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: Science News, 2026-06-02, “Microsoft’s quantum chip got an upgrade. Critics are still skeptical”, 578 words. Text not included.]




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

**The reply** (355 words)

```text
{"articles":[{"article":"A1","propositions":[{"text":"Georgia Tech is welcoming its incoming freshman class to campus during the week of this article (August 2026).","span":"[passage of 12 words]","relation":"asserts","source":"the article"},{"text":"Georgia Tech is known for its computer science, engineering and other STEM programs.","span":"[passage of 13 words]","relation":"asserts","source":"the article"},{"text":"Artificial intelligence is changing STEM industries.","span":"[passage of 7 words]","relation":"asserts","source":"the article"},{"text":"Artificial intelligence is changing how Georgia Tech approaches its curriculum.","span":"[passage of 7 words]","relation":"asserts","source":"the article"},{"text":"Artificial intelligence is changing the job market.","span":"[passage of 8 words]","relation":"asserts","source":"the article"},{"text":"Artificial intelligence is changing how professors plan their lessons.","span":"[passage of 9 words]","relation":"asserts","source":"the article"},{"text":"Nearly 15,000 Georgia Tech students are majoring or minoring in AI-related fields, including computer science.","span":"[passage of 15 words]","relation":"reports","source":"David Joyner"},{"text":"Some Georgia Tech professors are building their own AI agents that serve as tutors for their classes.","span":"[passage of 17 words]","relation":"reports","source":"David Joyner"},{"text":"Many Georgia Tech faculty are responding to AI by moving away from assigning long essays, such as a 10-page essay, and instead having students come to class for discussion.","span":"[passage of 38 words]","relation":"reports","source":"David Joyner"},{"text":"AI can help students complete some tasks more quickly.","span":"[passage of 12 words]","relation":"reports","source":"David Joyner"},{"text":"The old model of going to college for four years and then having a 40-year career has been dead for a while.","span":"[passage of 23 words]","relation":"reports","source":"David Joyner"},{"text":"AI gives people a new tool to go through a process faster, such as formulating an idea and having AI help write the software rather than spending three weeks building it.","span":"[passage of 19 words]","relation":"reports","source":"David Joyner"}]}]}
```

</details>
