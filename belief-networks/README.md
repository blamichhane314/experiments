# Belief networks elicited from large language models

Six experiments elicited propositions, agreement ratings and belief networks from large language models prompted with news articles or with fixed lists of statements. In the first group, a model extracted propositions from a set of news articles. In the second, a model assigned an agreement rating to each statement on a fixed list and identified the related pairs among them. In the third, a model was given articles in sequence and, after each article, returned an updated network of propositions, attitudes toward them, and links between them.

The site: https://blamichhane314.github.io/experiments/belief-networks/

## Contents

| Folder | Contents |
|---|---|
| [articles](articles/) | `articles.csv`: every news article used in the six experiments, with its date, outlet, headline, the number of words given to the model, and its address. The article texts are not included. |
| [prompts](prompts/) | One folder per experiment. Each step has a Markdown file with the prompt template, where one exists, and example requests exactly as sent, each with the model's reply. `requests.json` holds the same requests for the site. |
| [results](results/) | One folder per kind of result. Each holds the files the site reads (`.json`) and the same data as tables (`.csv`). |
| [assets](assets/) | The site's index files, fonts and image. |

## Experiments

| Experiment | Sent (Pacific time) | Requests | Prompts | Results |
|---|---|---|---|---|
| Experiment 1: belief networks on the effects of AI on learners' thinking and learning | 10 October 2026, 23:32 to 11 October 2026, 00:20 | 6,868 | [prompts/experiment-1](prompts/experiment-1/) | [results/propositions-from-articles](results/propositions-from-articles/) |
| Beliefs generated for five more topics | 29 September 2026, 12:35 to 12:40 | 314 | [prompts/five-topics](prompts/five-topics/) | [results/propositions-from-articles](results/propositions-from-articles/) |
| Experiment 8, prompt test: how far what a model reports an article to contain depends on how it is asked | 16 October 2026, 12:44 to 14:29 | 67 | [prompts/experiment-8](prompts/experiment-8/) | [results/propositions-from-articles](results/propositions-from-articles/) |
| Calibration: wording, paraphrase and negation, structure, article effects, size | 29 September 2026, 12:25 to 14:37 | 10,185 | [prompts/calibration](prompts/calibration/) | [results/networks-over-a-fixed-list](results/networks-over-a-fixed-list/) |
| Experiment 3: new information and pressure over rounds, and eight agents on a social network (ICE enforcement) | 11 October 2026, 16:56 to 17:24 | 2,013 | [prompts/experiment-3](prompts/experiment-3/) | [results/ratings-over-rounds](results/ratings-over-rounds/) |
| Experiment 9: does the answer come from the model's own record? | 28 October 2026, 21:05 to 23:42 | 2,472 | [prompts/experiment-9](prompts/experiment-9/) | [results/networks-across-articles](results/networks-across-articles/) |

## Notes

- In every prompt, each article's text is replaced by its label, outlet, date, headline and length.
- Counts include retried requests.
- The fonts (Newsreader, Geist and Geist Mono) are under the SIL Open Font License; see `assets/fonts`.
