# Experiment 1: belief networks on the effects of AI on learners' thinking and learning

- Two sets of six news articles on the effects of AI on learners: a balanced set and a set of negatively charged articles, chosen by a written rule from nineteen labelled articles.
- For each set, Claude Sonnet 5.5 generated statements ten times in each of two ways (the beliefs a reader could form from the articles, and the propositions the articles contain) and three times as statements about the articles as texts. Claude Opus 5.5 generated one reference list per set.
- Sonnet split compound statements, and Opus checked the splits. Sonnet proposed matching statements across runs, and Opus accepted or rejected each proposed pair; the forty statements that recurred most formed the list.
- Claude Haiku 4.5 was then prompted for ratings of the forty statements and their negations, and for the related pairs among them. These later steps are folded below.

Requests were sent from 10 October 2026, 23:32 to 11 October 2026, 00:20 (Pacific time).

| Step | Group | Requests sent | Models | First and last request |
|---|---|---|---|---|
| [1. Reader beliefs from six articles](01-reader-beliefs-from-six-articles.md) | Writing and preparing the statements | 27 | Sonnet 5.5, Opus 5.5 | 10 October 2026, 23:32 to 11 October 2026, 00:00 |
| [2. Propositions from six articles](02-propositions-from-six-articles.md) | Writing and preparing the statements | 20 | Sonnet 5.5 | 10 October 2026, 23:33 to 23:57 |
| [3. Statements about the articles as texts](03-statements-about-the-articles-as-texts.md) | Writing and preparing the statements | 6 | Sonnet 5.5 | 10 October 2026, 23:33 to 23:56 |
| [4. Splitting compound statements](04-splitting-compound-statements.md) | Writing and preparing the statements | 47 | Sonnet 5.5 | 10 October 2026, 23:33 to 23:57 |
| [5. Checking the splits](05-checking-the-splits.md) | Writing and preparing the statements | 2 | Opus 5.5 | 10 October 2026, 23:34 to 23:57 |
| [6. Matching statements across runs](06-matching-statements-across-runs.md) | Writing and preparing the statements | 105 | Sonnet 5.5 | 10 October 2026, 23:35 to 11 October 2026, 00:02 |
| [7. Judging the proposed matches](07-judging-the-proposed-matches.md) | Writing and preparing the statements | 119 | Opus 5.5 | 10 October 2026, 23:35 to 11 October 2026, 00:05 |
| [8. Typing each statement](08-typing-each-statement.md) | Writing and preparing the statements | 6 | Sonnet 5.5, Opus 5.5 | 10 October 2026, 23:36 to 11 October 2026, 00:06 |
| [9. Writing negations and paraphrases](09-writing-negations-and-paraphrases.md) | Writing and preparing the statements | 8 | Sonnet 5.5 | 10 October 2026, 23:39 to 11 October 2026, 00:04 |
| [10. Checking propositions against their article](10-checking-propositions-against-their-article.md) | Writing and preparing the statements | 36 | Opus 5.5 | 10 October 2026, 23:42 to 11 October 2026, 00:06 |
| [11. Checking reader beliefs against the articles](11-checking-reader-beliefs-against-the-articles.md) | Writing and preparing the statements | 12 | Opus 5.5 | 10 October 2026, 23:43 to 11 October 2026, 00:06 |
| [12. Rating one statement, without articles](12-rating-one-statement-without-articles.md) | Ratings and a network over the forty statements | 6,240 | Haiku 4.5 | 10 October 2026, 23:43 to 11 October 2026, 00:13 |
| [13. Rating what one article conveys about each statement](13-rating-what-one-article-conveys-about-each-statement.md) | Ratings and a network over the forty statements | 120 | Haiku 4.5 | 10 October 2026, 23:49 to 11 October 2026, 00:14 |
| [14. Ratings with the articles in the prompt](14-ratings-with-the-articles-in-the-prompt.md) | Ratings and a network over the forty statements | 60 | Haiku 4.5 | 10 October 2026, 23:50 to 11 October 2026, 00:15 |
| [15. Stances on the eighty statements](15-stances-on-the-eighty-statements.md) | Ratings and a network over the forty statements | 20 | Haiku 4.5 | 10 October 2026, 23:51 to 11 October 2026, 00:19 |
| [16. Related pairs among the eighty statements](16-related-pairs-among-the-eighty-statements.md) | Ratings and a network over the forty statements | 20 | Haiku 4.5 | 10 October 2026, 23:51 to 11 October 2026, 00:20 |
| [17. Stances, asked again after the network](17-stances-asked-again-after-the-network.md) | Ratings and a network over the forty statements | 10 | Haiku 4.5 | 10 October 2026, 23:51 to 11 October 2026, 00:17 |
| [18. Related pairs, asked again](18-related-pairs-asked-again.md) | Ratings and a network over the forty statements | 10 | Haiku 4.5 | 10 October 2026, 23:51 to 11 October 2026, 00:17 |
