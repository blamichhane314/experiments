# Experiment 8, prompt test, step 7 of 7: Sentences: six articles, one asked for

Sentences of an article, with type and tone. Requests sent: 8. Models: Haiku 4.5, Sonnet 5.5, GPT-4o. First and last request: 16 October 2026, 12:46 to 13:07 (Pacific time).

The request asks: “Extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.”

## The template

`label_Bone.txt`. The parts in braces are filled in for each request.

```text
The following {n_articles} news articles are labelled {labels}. The names of the outlets have been removed.

{articles}

Task: extract every sentence of the text of the article labelled {target}, in order, and classify each sentence by type and by tone.

Copy each sentence exactly as it appears in its article, character for character. Do not include the headline: in each article, the line after the label and date is the headline, and it is not a sentence of the text. Do not skip any sentence, and do not merge or split sentences. A sentence ends at a full stop, a question mark or an exclamation mark, or at a closing quotation mark that follows one of these, unless the mark is part of an abbreviation or a number.

If the article is a transcript, in which passages begin with a speaker's name followed by a colon (for example "SMITH:"), leave the speaker's name and the colon out of the sentence, and treat each sentence as said by that speaker.

Decide the type in this order, and use the first that applies:
1. "quote": the sentence's main content is words of a person or source given in quotation marks, or, in a transcript, words said by anyone other than the outlet's own host or reporter. Each sentence of a quotation that runs over several sentences is a quote. A sentence that reports what someone said without quotation marks, outside a transcript, is not a quote; classify it by the rules below.
2. "opinion": the sentence expresses the writer's own view, judgement or evaluation.
3. "borderline": the sentence has the form of a factual statement but also contains the writer's own judging or interpreting words.
4. "fact": the sentence has the form of a factual statement. It need not be true; do not judge whether it is true.
5. "other": none of the above, for example a question or a line addressed to the reader.
In a transcript, sentences said by the outlet's own host or reporter are the writer's own sentences: classify them by rules 2 to 5, and a greeting, a thanks or a question put to a guest is "other".

Tone is how the sentence presents its main subject (the person, group, institution, event or policy the sentence is chiefly about), judged from the sentence itself and not from your own view of that subject:
- "positive": it presents the subject favourably;
- "negative": it presents the subject unfavourably;
- "neutral": it presents the subject neither favourably nor unfavourably.
For a quote, judge how the quoted words present their subject.

Return JSON of the form {{"articles": [{{"article": "<label>", "sentences": [{{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}}, ...]}}, ...]}}, with one entry in "articles" for each article you were asked about.
```

## Requests as sent (4)

One request for each combination of model, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>GPT-4o, temperature 0 · Round 1 · 16 October 2026, 12:50</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (4697 words)

```text
The following 6 news articles are labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A3: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A6: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]




Task: extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.

Copy each sentence exactly as it appears in its article, character for character. Do not include the headline. Do not skip any sentence, and do not merge or split sentences.

Decide the type in this order, and use the first that applies:
1. "quote": the sentence's main content is words of a person or source given in quotation marks. Each sentence of a quotation that runs over several sentences is a quote. A sentence that reports what someone said without quotation marks is not a quote; classify it by the rules below.
2. "opinion": the sentence expresses the writer's own view, judgement or evaluation.
3. "borderline": the sentence has the form of a factual statement but also contains the writer's own judging or interpreting words.
4. "fact": the sentence has the form of a factual statement. It need not be true; do not judge whether it is true.
5. "other": none of the above, for example a question or a line addressed to the reader.

Tone is how the sentence presents its main subject (the person, group, institution, event or policy the sentence is chiefly about), judged from the sentence itself and not from your own view of that subject:
- "positive": it presents the subject favourably;
- "negative": it presents the subject unfavourably;
- "neutral": it presents the subject neither favourably nor unfavourably.
For a quote, judge how the quoted words present their subject.

Return JSON of the form {"articles": [{"article": "<label>", "sentences": [{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (375 words)

```text
{
 "articles": [
  {
   "article": "A1",
   "sentences": [
    {
     "n": 1,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 2,
     "text": "[sentence of 13 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 3,
     "text": "[sentence of 15 words]",
     "type": "borderline",
     "tone": "neutral"
    },
    {
     "n": 4,
     "text": "[sentence of 8 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 5,
     "text": "[sentence of 9 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 6,
     "text": "[sentence of 26 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 7,
     "text": "[sentence of 11 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 8,
     "text": "[sentence of 11 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 9,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 10,
     "text": "[sentence of 29 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 13,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 14,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 15,
     "text": "[sentence of 25 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 16,
     "text": "[sentence of 15 words]",
     "type": "quote",
     "tone": "positive"
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

**The request** (4697 words)

```text
The following 6 news articles are labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A3: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A6: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]




Task: extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.

Copy each sentence exactly as it appears in its article, character for character. Do not include the headline. Do not skip any sentence, and do not merge or split sentences.

Decide the type in this order, and use the first that applies:
1. "quote": the sentence's main content is words of a person or source given in quotation marks. Each sentence of a quotation that runs over several sentences is a quote. A sentence that reports what someone said without quotation marks is not a quote; classify it by the rules below.
2. "opinion": the sentence expresses the writer's own view, judgement or evaluation.
3. "borderline": the sentence has the form of a factual statement but also contains the writer's own judging or interpreting words.
4. "fact": the sentence has the form of a factual statement. It need not be true; do not judge whether it is true.
5. "other": none of the above, for example a question or a line addressed to the reader.

Tone is how the sentence presents its main subject (the person, group, institution, event or policy the sentence is chiefly about), judged from the sentence itself and not from your own view of that subject:
- "positive": it presents the subject favourably;
- "negative": it presents the subject unfavourably;
- "neutral": it presents the subject neither favourably nor unfavourably.
For a quote, judge how the quoted words present their subject.

Return JSON of the form {"articles": [{"article": "<label>", "sentences": [{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (415 words)

```text
{
 "articles": [
  {
   "article": "A1",
   "sentences": [
    {
     "n": 1,
     "text": "[sentence of 10 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 2,
     "text": "[sentence of 13 words]",
     "type": "fact",
     "tone": "positive"
    },
    {
     "n": 3,
     "text": "[sentence of 15 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 4,
     "text": "[sentence of 8 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 5,
     "text": "[sentence of 9 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 6,
     "text": "[sentence of 26 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 7,
     "text": "[sentence of 11 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 8,
     "text": "[sentence of 11 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 9,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 10,
     "text": "[sentence of 29 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "positive"
    },
    {
     "n": 13,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 14,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 15,
     "text": "[sentence of 25 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 16,
     "text": "[sentence of 15 words]",
     "type": "quote",
     "tone": "positive"
    }
   ]
  }
 ]
}
```

</details>

<details><summary>Haiku 4.5, temperature 1 · Round 1 · 16 October 2026, 13:07</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (4697 words)

```text
The following 6 news articles are labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A3: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A6: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]




Task: extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.

Copy each sentence exactly as it appears in its article, character for character. Do not include the headline. Do not skip any sentence, and do not merge or split sentences.

Decide the type in this order, and use the first that applies:
1. "quote": the sentence's main content is words of a person or source given in quotation marks. Each sentence of a quotation that runs over several sentences is a quote. A sentence that reports what someone said without quotation marks is not a quote; classify it by the rules below.
2. "opinion": the sentence expresses the writer's own view, judgement or evaluation.
3. "borderline": the sentence has the form of a factual statement but also contains the writer's own judging or interpreting words.
4. "fact": the sentence has the form of a factual statement. It need not be true; do not judge whether it is true.
5. "other": none of the above, for example a question or a line addressed to the reader.

Tone is how the sentence presents its main subject (the person, group, institution, event or policy the sentence is chiefly about), judged from the sentence itself and not from your own view of that subject:
- "positive": it presents the subject favourably;
- "negative": it presents the subject unfavourably;
- "neutral": it presents the subject neither favourably nor unfavourably.
For a quote, judge how the quoted words present their subject.

Return JSON of the form {"articles": [{"article": "<label>", "sentences": [{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (415 words)

```text
{
 "articles": [
  {
   "article": "A1",
   "sentences": [
    {
     "n": 1,
     "text": "[sentence of 10 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 2,
     "text": "[sentence of 13 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 3,
     "text": "[sentence of 15 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 4,
     "text": "[sentence of 8 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 5,
     "text": "[sentence of 9 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 6,
     "text": "[sentence of 26 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 7,
     "text": "[sentence of 11 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 8,
     "text": "[sentence of 11 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 9,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 10,
     "text": "[sentence of 29 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "positive"
    },
    {
     "n": 13,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 14,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 15,
     "text": "[sentence of 25 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 16,
     "text": "[sentence of 15 words]",
     "type": "quote",
     "tone": "positive"
    }
   ]
  }
 ]
}
```

</details>

<details><summary>Sonnet 5.5 · Round 1 · 16 October 2026, 12:46</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (4697 words)

```text
The following 6 news articles are labelled A1, A2, A3, A4, A5, A6. The names of the outlets have been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]
[Article A2: CNN, 2026-09-10, “Asian teens race ahead of US peers for reading, science and math in global rankings”, 566 words. Text not included.]
[Article A3: Fortune, 2026-09-11, “Students are using AI in school and test scores are down, but the OECD finds that those who use it once or twice a week perform similarly to nonusers”, 561 words. Text not included.]
[Article A4: Al Jazeera, 2026-09-02, “Faster homework, poor exam results: What AI is doing to students’ learning”, 591 words. Text not included.]
[Article A5: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]
[Article A6: NPR, 2026-06-05, “Most K-12 teachers say AI's impact on education will eclipse the internet or computers”, 1584 words. Text not included.]




Task: extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.

Copy each sentence exactly as it appears in its article, character for character. Do not include the headline. Do not skip any sentence, and do not merge or split sentences.

Decide the type in this order, and use the first that applies:
1. "quote": the sentence's main content is words of a person or source given in quotation marks. Each sentence of a quotation that runs over several sentences is a quote. A sentence that reports what someone said without quotation marks is not a quote; classify it by the rules below.
2. "opinion": the sentence expresses the writer's own view, judgement or evaluation.
3. "borderline": the sentence has the form of a factual statement but also contains the writer's own judging or interpreting words.
4. "fact": the sentence has the form of a factual statement. It need not be true; do not judge whether it is true.
5. "other": none of the above, for example a question or a line addressed to the reader.

Tone is how the sentence presents its main subject (the person, group, institution, event or policy the sentence is chiefly about), judged from the sentence itself and not from your own view of that subject:
- "positive": it presents the subject favourably;
- "negative": it presents the subject unfavourably;
- "neutral": it presents the subject neither favourably nor unfavourably.
For a quote, judge how the quoted words present their subject.

Return JSON of the form {"articles": [{"article": "<label>", "sentences": [{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (244 words)

```text
{
 "articles": [
  {
   "article": "A1",
   "sentences": [
    {
     "n": 1,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 2,
     "text": "[sentence of 13 words]",
     "type": "fact",
     "tone": "positive"
    },
    {
     "n": 3,
     "text": "[sentence of 15 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 4,
     "text": "[sentence of 8 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 5,
     "text": "[sentence of 9 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 6,
     "text": "[sentence of 26 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 7,
     "text": "[sentence of 11 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 8,
     "text": "[sentence of 11 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 9,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 10,
     "text": "[sentence of 29 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "positive"
    },
    {
     "n": 13,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 14,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 15,
     "text": "[sentence of 25 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 16,
     "text": "[sentence of 15 words]",
     "type": "quote",
     "tone": "positive"
    }
   ]
  }
 ]
}
```

</details>
