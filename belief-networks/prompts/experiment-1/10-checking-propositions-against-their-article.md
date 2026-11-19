# Experiment 1, step 10 of 18: Checking propositions against their article

Writing and preparing the statements. Requests sent: 36. Models: Opus 5.5. First and last request: 10 October 2026, 23:42 to 11 October 2026, 00:06 (Pacific time).

The request asks: “For each proposition, answer three questions about this article only. 1. "supported": does the article, read as a whole, state or report the proposition with the same meaning?”

## The template

`faithfulness.txt`. The parts in braces are filled in for each request.

```text
Here is a news article, labelled {label}.

{article}

Here are {n} propositions, each with a passage said to come from this article and a description of how the article states it.

{items}

For each proposition, answer three questions about this article only.
1. "supported": does the article, read as a whole, state or report the proposition with the same meaning? "yes", "partly" (the article states something close but the proposition adds, drops or changes part of the meaning), or "no".
2. "relation_correct": is the description of how the article states it ("asserts" in its own voice, "reports" a source saying it, "hedges") correct? "yes" or "no".
3. "standalone": can the proposition be understood correctly without the article? "yes" or "no".
Judge against the article, not against your own knowledge of the world.

Return JSON of the form {{"checks": {{"q0": {{"supported": "...", "relation_correct": "...", "standalone": "..."}}, ...}}}} with every id.
```

## Requests as sent (1)

With the reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Opus 5.5 · Both sets · 10 October 2026, 23:42</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (493 words)

```text
Here is a news article, labelled A6.

[Article A6: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]



Here are 2 propositions, each with a passage said to come from this article and a description of how the article states it.

q0: Georgia Tech professors are building AI tutor agents in response to AI.
   passage: "Some of them are they're building their own AI agents that are serving as tutors for classes."
   how the article states it: reports

q1: Georgia Tech professors are replacing long essays with in-class discussion in response to AI.
   passage: "Some of them are they're building their own AI agents that are serving as tutors for classes."
   how the article states it: reports

For each proposition, answer three questions about this article only.
1. "supported": does the article, read as a whole, state or report the proposition with the same meaning? "yes", "partly" (the article states something close but the proposition adds, drops or changes part of the meaning), or "no".
2. "relation_correct": is the description of how the article states it ("asserts" in its own voice, "reports" a source saying it, "hedges") correct? "yes" or "no".
3. "standalone": can the proposition be understood correctly without the article? "yes" or "no".
Judge against the article, not against your own knowledge of the world.

Return JSON of the form {"checks": {"q0": {"supported": "...", "relation_correct": "...", "standalone": "..."}, ...}} with every id.
```

**The reply** (15 words)

```text
{"checks": {"q0": {"supported": "yes", "relation_correct": "yes", "standalone": "yes"}, "q1": {"supported": "yes", "relation_correct": "yes", "standalone": "yes"}}}
```

</details>
