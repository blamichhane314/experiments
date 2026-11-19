# Experiment 1, step 4 of 18: Splitting compound statements

Writing and preparing the statements. Requests sent: 47. Models: Sonnet 5.5. First and last request: 10 October 2026, 23:33 to 23:57 (Pacific time).

The request asks: “Split every statement that makes more than one claim into statements that each make exactly one claim.”

## The template

`split.txt`. The parts in braces are filled in for each request.

```text
Here are {n} statements.

{statements}

Task: split every statement that makes more than one claim into statements that each make exactly one claim.

A statement makes more than one claim when it can be divided into two statements, each of which could be true while the other is false. Two numbers, two findings, a finding and a second finding about its size or timing, a claim and the reason or explanation given for it, a fact and a comment on it, and two prescriptions are each two claims. A causal statement (A causes B) is one claim when the causal link is the claim. "And" inside a name, or in a list that is itself the single thing the claim is about, does not make two claims.

Rules for the parts.
1. Each part makes exactly one claim.
2. Taken together, the parts say what the original said: nothing added, nothing dropped, nothing strengthened or weakened.
3. Each part stands on its own: repeat the subject, time, place and population in every part where the claim's truth depends on them, and resolve pronouns.
4. Use the original's words as far as possible.
5. A statement that already makes one claim is returned unchanged, as a list with that one statement, copied exactly.

Return JSON of the form {{"split": {{"b0": ["<part>", "<part>"], "b1": ["<statement unchanged>"], ...}}}} with every statement id.
```

## Requests as sent (1)

With the reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Sonnet 5.5 · Both sets · 10 October 2026, 23:33</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (228 words)

```text
Here are 0 statements.



Task: split every statement that makes more than one claim into statements that each make exactly one claim.

A statement makes more than one claim when it can be divided into two statements, each of which could be true while the other is false. Two numbers, two findings, a finding and a second finding about its size or timing, a claim and the reason or explanation given for it, a fact and a comment on it, and two prescriptions are each two claims. A causal statement (A causes B) is one claim when the causal link is the claim. "And" inside a name, or in a list that is itself the single thing the claim is about, does not make two claims.

Rules for the parts.
1. Each part makes exactly one claim.
2. Taken together, the parts say what the original said: nothing added, nothing dropped, nothing strengthened or weakened.
3. Each part stands on its own: repeat the subject, time, place and population in every part where the claim's truth depends on them, and resolve pronouns.
4. Use the original's words as far as possible.
5. A statement that already makes one claim is returned unchanged, as a list with that one statement, copied exactly.

Return JSON of the form {"split": {"b0": ["<part>", "<part>"], "b1": ["<statement unchanged>"], ...}} with every statement id.
```

**The reply** (2 words)

```text
{"split": {}}
```

</details>
