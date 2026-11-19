# Experiment 8, prompt test: how far what a model reports an article to contain depends on how it is asked

A language model is given news articles and asked to return what they contain, either every sentence with its type and tone, or every proposition with the passage it comes from. The experiment asks how much of that output belongs to the article and how much to the way of asking.

- A prompt test in three rounds, with the prompts revised between rounds, and a fourth round on articles about immigration enforcement.
- Four contexts: one article alone; the six articles of a set, with every article’s output asked for; the six articles, with one article’s output asked for; one article beside an unrelated article.
- Claude Haiku 4.5 at temperature 0 and 1.0, GPT-4o at temperature 0, Claude Sonnet 5.5 as a reference, and one request to Claude Sonnet 4.6.
- The articles are experiment 1’s balanced set and the balanced set on immigration enforcement from the second domain study.

Requests were sent from 16 October 2026, 12:44 to 14:29 (Pacific time).

| Step | Group | Requests sent | Models | First and last request |
|---|---|---|---|---|
| [1. Propositions: one article alone](01-propositions-one-article-alone.md) | Propositions of an article | 9 | Haiku 4.5, GPT-4o, Sonnet 5.5 | 16 October 2026, 12:46 to 14:28 |
| [2. Propositions: six articles, each asked for](02-propositions-six-articles-each-asked-for.md) | Propositions of an article | 10 | Haiku 4.5, GPT-4o, Sonnet 5.5 | 16 October 2026, 12:47 to 14:29 |
| [3. Propositions: six articles, one asked for](03-propositions-six-articles-one-asked-for.md) | Propositions of an article | 10 | Haiku 4.5, GPT-4o, Sonnet 5.5 | 16 October 2026, 12:48 to 13:18 |
| [4. Propositions: one article beside an unrelated article](04-propositions-one-article-beside-an-unrelated-article.md) | Propositions of an article | 4 | Haiku 4.5, Sonnet 5.5, GPT-4o | 16 October 2026, 12:48 to 13:13 |
| [5. Sentences: one article alone](05-sentences-one-article-alone.md) | Sentences of an article, with type and tone | 13 | Haiku 4.5, GPT-4o, Sonnet 5.5, Sonnet 4.6 | 16 October 2026, 12:44 to 14:27 |
| [6. Sentences: six articles, each asked for](06-sentences-six-articles-each-asked-for.md) | Sentences of an article, with type and tone | 13 | Haiku 4.5, GPT-4o, Sonnet 5.5 | 16 October 2026, 12:45 to 14:28 |
| [7. Sentences: six articles, one asked for](07-sentences-six-articles-one-asked-for.md) | Sentences of an article, with type and tone | 8 | Haiku 4.5, Sonnet 5.5, GPT-4o | 16 October 2026, 12:46 to 13:07 |
