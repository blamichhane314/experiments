# Experiment 9: does the answer come from the model's own record?

A model is given four news articles on immigration enforcement, one per prompt. After each article it returns an updated record of propositions and attitudes, and after the last it is asked to answer a user’s question. The experiment asks whether the answer depends on that record.

- The same four articles, in the same order, in every run.
- Nine set-ups: the record is a network or a written summary; the prompt asks for the model’s own beliefs, or (reader-neutral) for the propositions readers of any background might come to believe and then an attitude toward each; each prompt contains the record and the current article, or all articles so far; links are reasons, or state what fits or clashes; and in D no record is kept.
- Main run: Claude Haiku 4.5, nine set-ups, four user questions, five runs each. Prompt tests with Claude Sonnet 5.5 and Gemini 3.8 Flash.
- The edit test: before the answer, the record is changed (a proposition’s attitude flipped, a proposition removed or rewritten as its denial, or the whole record rewritten to point the other way), to see whether the answer follows.

Requests were sent from 28 October 2026, 21:05 to 23:42 (Pacific time).

| Step | Group | Requests sent | Models | First and last request |
|---|---|---|---|---|
| [1. After article 1](01-after-article-1.md) | Reading the four articles | 185 | Haiku 4.5, Sonnet 5.5, Gemini 3.8 Flash | 28 October 2026, 21:05 to 22:19 |
| [2. After article 2](02-after-article-2.md) | Reading the four articles | 182 | Haiku 4.5, Sonnet 5.5, Gemini 3.8 Flash | 28 October 2026, 21:05 to 22:21 |
| [3. After article 3](03-after-article-3.md) | Reading the four articles | 183 | Haiku 4.5, Sonnet 5.5, Gemini 3.8 Flash | 28 October 2026, 21:05 to 22:04 |
| [4. After article 4](04-after-article-4.md) | Reading the four articles | 182 | Haiku 4.5, Sonnet 5.5, Gemini 3.8 Flash | 28 October 2026, 21:06 to 22:04 |
| [5. The answer to the user](05-the-answer-to-the-user.md) (in 4 files) | The answer | 1,510 | Haiku 4.5, Sonnet 5.5, Gemini 3.8 Flash | 28 October 2026, 21:06 to 23:24 |
| [6. Generating the denial of a proposition](06-generating-the-denial-of-a-proposition.md) | Edits to the record, by a second model | 66 | Sonnet 5.5 | 28 October 2026, 22:41 to 22:52 |
| [7. Rewriting the record to the opposite position](07-rewriting-the-record-to-the-opposite-position.md) | Edits to the record, by a second model | 32 | Sonnet 5.5 | 28 October 2026, 23:13 to 23:23 |
| [8. Checking the rewritten record](08-checking-the-rewritten-record.md) | Edits to the record, by a second model | 55 | Sonnet 5.5 | 28 October 2026, 23:20 to 23:24 |
| [9. Correcting what still points the old way](09-correcting-what-still-points-the-old-way.md) | Edits to the record, by a second model | 37 | Sonnet 5.5 | 28 October 2026, 23:20 to 23:24 |
| [10. The question alone, without articles or record](10-the-question-alone-without-articles-or-record.md) | The question alone | 40 | Haiku 4.5, Sonnet 5.5 | 28 October 2026, 23:41 to 23:42 |
