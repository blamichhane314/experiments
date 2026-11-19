# Experiment 1, step 9 of 18: Writing negations and paraphrases

Writing and preparing the statements. Requests sent: 8. Models: Sonnet 5.5. First and last request: 10 October 2026, 23:39 to 11 October 2026, 00:04 (Pacific time).

The request asks: “For each statement, write five related statements. 1. "negation": the statement's contradiction.”

## The template

`derive.txt`. The parts in braces are filled in for each request.

```text
Here are {n} statements.

{statements}

For each statement, write five related statements.
1. "negation": the statement's contradiction. It must be true exactly when the original is false. Negate the main claim and nothing else; prefer a natural wording ("does not lower", "is not the main cause") to an opposite ("raises", "is a minor cause"), because an opposite is a contrary, not a contradiction. Do not use a double negation.
2. "weaker": a slightly weaker version: one that the original implies but that does not imply the original (for example narrower in scope, less extreme, or less certain in degree), otherwise as close to the original as possible.
3. "stronger": a slightly stronger version: one that implies the original but is not implied by it, otherwise as close to the original as possible.
4. "paraphrase_1" and "paraphrase_2": two rewordings with exactly the same meaning as the original, worded differently from it and from each other.
5. "negation_paraphrase_1" and "negation_paraphrase_2": two rewordings with exactly the same meaning as your negation.

Every statement you write must stand on its own and keep the time, place and population of the original.

Return JSON of the form {{"derived": {{"b0": {{"negation": "...", "weaker": "...", "stronger": "...", "paraphrase_1": "...", "paraphrase_2": "...", "negation_paraphrase_1": "...", "negation_paraphrase_2": "..."}}, ...}}}} with every statement id.
```

## Requests as sent (1)

With the reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>Sonnet 5.5 · Both sets · 10 October 2026, 23:39</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (401 words)

```text
Here are 13 statements.

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


For each statement, write five related statements.
1. "negation": the statement's contradiction. It must be true exactly when the original is false. Negate the main claim and nothing else; prefer a natural wording ("does not lower", "is not the main cause") to an opposite ("raises", "is a minor cause"), because an opposite is a contrary, not a contradiction. Do not use a double negation.
2. "weaker": a slightly weaker version: one that the original implies but that does not imply the original (for example narrower in scope, less extreme, or less certain in degree), otherwise as close to the original as possible.
3. "stronger": a slightly stronger version: one that implies the original but is not implied by it, otherwise as close to the original as possible.
4. "paraphrase_1" and "paraphrase_2": two rewordings with exactly the same meaning as the original, worded differently from it and from each other.
5. "negation_paraphrase_1" and "negation_paraphrase_2": two rewordings with exactly the same meaning as your negation.

Every statement you write must stand on its own and keep the time, place and population of the original.

Return JSON of the form {"derived": {"b0": {"negation": "...", "weaker": "...", "stronger": "...", "paraphrase_1": "...", "paraphrase_2": "...", "negation_paraphrase_1": "...", "negation_paraphrase_2": "..."}, ...}} with every statement id.
```

**The reply** (1288 words)

```text
{"derived":{"b0":{"negation":"Schools should not teach students the responsible use of AI.","weaker":"Schools should consider teaching students the responsible use of AI.","stronger":"Schools must teach all students the responsible use of AI as a core part of the curriculum.","paraphrase_1":"Students ought to be taught by their schools how to use AI responsibly.","paraphrase_2":"Instruction in responsible AI use belongs in schools' teaching for students.","negation_paraphrase_1":"It is not the case that schools should teach students the responsible use of AI.","negation_paraphrase_2":"Teaching students responsible AI use is not something schools should do."},"b1":{"negation":"The share of hasty readers among 15-year-olds did not almost double between 2018 and 2025.","weaker":"The share of hasty readers among 15-year-olds rose substantially between 2018 and 2025.","stronger":"The share of hasty readers among 15-year-olds more than doubled between 2018 and 2025.","paraphrase_1":"Between 2018 and 2025, the proportion of 15-year-olds who read hastily nearly doubled.","paraphrase_2":"The fraction of 15-year-olds classed as hasty readers came close to doubling from 2018 to 2025.","negation_paraphrase_1":"Between 2018 and 2025, the proportion of 15-year-olds who read hastily did not nearly double.","negation_paraphrase_2":"The fraction of 15-year-olds classed as hasty readers did not come close to doubling from 2018 to 2025."},"b2":{"negation":"AI use is not eroding trust between students and teachers.","weaker":"AI use is sometimes straining trust between students and teachers.","stronger":"AI use is seriously eroding trust between students and teachers across schools.","paraphrase_1":"The use of AI is wearing away trust between students and their teachers.","paraphrase_2":"Trust between teachers and students is being undermined by AI use.","negation_paraphrase_1":"The use of AI is not wearing away trust between students and their teachers.","negation_paraphrase_2":"Trust between teachers and students is not being undermined by AI use."},"b3":{"negation":"AI is the only cause of declines in student test scores.","weaker":"AI is probably not the only cause of declines in student test scores.","stronger":"AI plays at most a minor role in declines in student test scores, which have other causes.","paraphrase_1":"Declines in student test scores have causes besides AI.","paraphrase_2":"AI alone does not account for falling student test scores.","negation_paraphrase_1":"AI is solely responsible for declines in student test scores.","negation_paraphrase_2":"Declines in student test scores have no cause other than AI."},"b4":{"negation":"How students use AI does not matter more for learning than whether they use it.","weaker":"How students use AI matters at least as much for learning as whether they use it.","stronger":"How students use AI matters far more for learning than whether they use it.","paraphrase_1":"For learning, the manner in which students use AI is more important than whether they use it at all.","paraphrase_2":"Whether students learn depends more on how they use AI than on whether they use it.","negation_paraphrase_1":"For learning, the manner in which students use AI is not more important than whether they use it at all.","negation_paraphrase_2":"Whether students use AI matters at least as much for learning as how they use it."},"b5":{"negation":"Chinese PISA results are representative of the whole country.","weaker":"Chinese PISA results may not be fully representative of the whole country.","stronger":"Chinese PISA results are unrepresentative of the whole country and reflect only a few wealthy regions.","paraphrase_1":"The PISA results from China do not reflect the whole country.","paraphrase_2":"China's PISA results fail to be representative of the country as a whole.","negation_paraphrase_1":"The PISA results from China reflect the whole country.","negation_paraphrase_2":"China's PISA results are representative of the country as a whole."},"b6":{"negation":"US 15-year-olds' reading scores on PISA have not fallen to close to 25-year lows.","weaker":"US 15-year-olds' reading scores on PISA have fallen to near their lowest levels in over a decade.","stronger":"US 15-year-olds' reading scores on PISA have fallen to their lowest level in 25 years.","paraphrase_1":"On PISA, reading scores of 15-year-olds in the US are now near their lowest in a quarter century.","paraphrase_2":"American 15-year-olds' PISA reading results have dropped to levels close to 25-year lows.","negation_paraphrase_1":"On PISA, reading scores of 15-year-olds in the US are not near their lowest in a quarter century.","negation_paraphrase_2":"American 15-year-olds' PISA reading results have not dropped to levels close to 25-year lows."},"b7":{"negation":"AI cannot help students with disabilities complete assignments they otherwise could not.","weaker":"AI can help some students with disabilities complete assignments more easily.","stronger":"AI enables students with disabilities to complete assignments they otherwise could never do.","paraphrase_1":"Students with disabilities can use AI to finish assignments that would otherwise be beyond them.","paraphrase_2":"With AI's help, students with disabilities can complete work they could not complete otherwise.","negation_paraphrase_1":"Students with disabilities cannot use AI to finish assignments that would otherwise be beyond them.","negation_paraphrase_2":"AI does not make it possible for students with disabilities to complete work they could not complete otherwise."},"b8":{"negation":"Chinese students who adopted generative AI did not see their closed-book monthly exam scores fall by about 20% within six months.","weaker":"Chinese students who adopted generative AI saw their closed-book monthly exam scores fall within six months.","stronger":"Chinese students who adopted generative AI saw their closed-book monthly exam scores fall by more than 20% within six months.","paraphrase_1":"Within six months, closed-book monthly exam scores of Chinese students who took up generative AI dropped by roughly 20%.","paraphrase_2":"Chinese students adopting generative AI experienced a roughly 20% decline in closed-book monthly exam scores over six months.","negation_paraphrase_1":"Within six months, closed-book monthly exam scores of Chinese students who took up generative AI did not drop by roughly 20%.","negation_paraphrase_2":"Chinese students adopting generative AI did not experience a roughly 20% decline in closed-book monthly exam scores over six months."},"b9":{"negation":"A majority of US K-12 teachers do not worry that AI makes it harder for students to learn to think critically.","weaker":"A large share of US K-12 teachers worry that AI makes it harder for students to learn to think critically.","stronger":"Nearly all US K-12 teachers worry that AI makes it harder for students to learn to think critically.","paraphrase_1":"Most US K-12 teachers are concerned that AI makes critical thinking harder for students to learn.","paraphrase_2":"More than half of US K-12 teachers fear AI makes it more difficult for students to learn to think critically.","negation_paraphrase_1":"Most US K-12 teachers are not concerned that AI makes critical thinking harder for students to learn.","negation_paraphrase_2":"Half or fewer of US K-12 teachers fear AI makes it more difficult for students to learn to think critically."},"b10":{"negation":"Students who do not use AI chatbots for schoolwork do not generally score higher than students who do.","weaker":"Students who do not use AI chatbots for schoolwork sometimes score higher than students who do.","stronger":"Students who do not use AI chatbots for schoolwork always score higher than students who do.","paraphrase_1":"In general, students who avoid AI chatbots for schoolwork get higher scores than those who use them.","paraphrase_2":"Students not using AI chatbots for schoolwork typically outscore students who do.","negation_paraphrase_1":"In general, students who avoid AI chatbots for schoolwork do not get higher scores than those who use them.","negation_paraphrase_2":"Students not using AI chatbots for schoolwork typically do not outscore students who do."},"b11":{"negation":"Student performance has not become less linked to national or family wealth as technology has progressed.","weaker":"Student performance has become somewhat less linked to national or family wealth as technology has progressed.","stronger":"Student performance has become unrelated to national and family wealth as technology has progressed.","paraphrase_1":"As technology has advanced, the connection between student performance and national or family wealth has weakened.","paraphrase_2":"Wealth, national or familial, predicts student performance less than it used to as technology has progressed.","negation_paraphrase_1":"As technology has advanced, the connection between student performance and national or family wealth has not weakened.","negation_paraphrase_2":"Wealth, national or familial, predicts student performance no less than it used to as technology has progressed."},"b12":{"negation":"Most US K-12 teachers do not believe AI will affect education more than the internet or computers did.","weaker":"Many US K-12 teachers believe AI will affect education more than the internet or computers did.","stronger":"Nearly all US K-12 teachers believe AI will affect education far more than the internet or computers did.","paraphrase_1":"A majority of US K-12 teachers think AI will have a bigger impact on education than the internet or computers did.","paraphrase_2":"Most US K-12 teachers expect AI to change education more than the internet or computers did.","negation_paraphrase_1":"Half or fewer of US K-12 teachers think AI will have a bigger impact on education than the internet or computers did.","negation_paraphrase_2":"Most US K-12 teachers do not expect AI to change education more than the internet or computers did."}}}
```

</details>
