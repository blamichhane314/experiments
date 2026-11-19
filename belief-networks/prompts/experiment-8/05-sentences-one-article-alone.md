# Experiment 8, prompt test, step 5 of 7: Sentences: one article alone

Sentences of an article, with type and tone. Requests sent: 13. Models: Haiku 4.5, GPT-4o, Sonnet 5.5, Sonnet 4.6. First and last request: 16 October 2026, 12:44 to 14:27 (Pacific time).

The request asks: “Extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.”

## The template

`label_A.txt`. The parts in braces are filled in for each request.

```text
The following news article is labelled {labels}. The name of the outlet has been removed.

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

## Requests as sent (11)

One request for each combination of model, round, with its reply. Each request opens to show the system prompt, the request and the reply.

<details><summary>GPT-4o, temperature 0 · Round 1 · 16 October 2026, 12:48</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (580 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




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

**The reply** (245 words)

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
     "text": "[sentence of 40 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 13,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 14,
     "text": "[sentence of 25 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 15,
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

<details><summary>Haiku 4.5, temperature 0 · Round 1 · 16 October 2026, 12:53</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (580 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




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

**The reply** (417 words)

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
     "tone": "neutral"
    }
   ]
  }
 ]
}
```

</details>

<details><summary>Haiku 4.5, temperature 1 · Round 1 · 16 October 2026, 13:03</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (580 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




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

**The reply** (408 words)

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
     "tone": "neutral"
    },
    {
     "n": 10,
     "text": "[sentence of 40 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "positive"
    },
    {
     "n": 12,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 13,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 14,
     "text": "[sentence of 25 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 15,
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

<details><summary>Sonnet 4.6, temperature 0 · Round 1 · 16 October 2026, 12:48</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (580 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




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

**The reply** (408 words)

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
     "text": "[sentence of 40 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "positive"
    },
    {
     "n": 12,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 13,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 14,
     "text": "[sentence of 25 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 15,
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

<details><summary>Sonnet 5.5 · Round 1 · 16 October 2026, 12:44</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (580 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: CBS News Atlanta, 2026-08-20, “Georgia Tech professors turn to AI tutors and rethink traditional assignments”, 259 words. Text not included.]




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

**The reply** (246 words)

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
     "text": "[sentence of 57 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 10,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "positive"
    },
    {
     "n": 11,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 13,
     "text": "[sentence of 25 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 14,
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

<details><summary>GPT-4o, temperature 0 · Round 2 · 16 October 2026, 13:17</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1127 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]




Task: extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.

Copy each sentence exactly as it appears in its article, character for character. Do not include the headline. Do not skip any sentence, and do not merge or split sentences. A sentence ends at a full stop, a question mark or an exclamation mark, or at a closing quotation mark that follows one of these, unless the mark is part of an abbreviation or a number.

If the article is a transcript, in which passages begin with a speaker's name followed by a colon (for example "SMITH:"), leave the speaker's name and the colon out of the sentence, and treat each sentence as said by that speaker.

Decide the type in this order, and use the first that applies:
1. "quote": the sentence's main content is words of a person or source given in quotation marks, or, in a transcript, words said by anyone other than the outlet's own host or reporter. Each sentence of a quotation that runs over several sentences is a quote. A sentence that reports what someone said without quotation marks, outside a transcript, is not a quote; classify it by the rules below.
2. "opinion": the sentence expresses the writer's own view, judgement or evaluation.
3. "borderline": the sentence has the form of a factual statement but also contains the writer's own judging or interpreting words.
4. "fact": the sentence has the form of a factual statement. It need not be true; do not judge whether it is true.
5. "other": none of the above, for example a question or a line addressed to the reader.
In a transcript, the writer is the outlet's own host or reporter.

Tone is how the sentence presents its main subject (the person, group, institution, event or policy the sentence is chiefly about), judged from the sentence itself and not from your own view of that subject:
- "positive": it presents the subject favourably;
- "negative": it presents the subject unfavourably;
- "neutral": it presents the subject neither favourably nor unfavourably.
For a quote, judge how the quoted words present their subject.

Return JSON of the form {"articles": [{"article": "<label>", "sentences": [{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (1276 words)

```text
{
 "articles": [
  {
   "article": "A1",
   "sentences": [
    {
     "n": 1,
     "text": "[sentence of 21 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 2,
     "text": "[sentence of 14 words]",
     "type": "fact",
     "tone": "negative"
    },
    {
     "n": 3,
     "text": "[sentence of 17 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 4,
     "text": "[sentence of 17 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 5,
     "text": "[sentence of 8 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 6,
     "text": "[sentence of 5 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 7,
     "text": "[sentence of 4 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 8,
     "text": "[sentence of 2 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 9,
     "text": "[sentence of 4 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 10,
     "text": "[sentence of 5 words]",
     "type": "other",
     "tone": "positive"
    },
    {
     "n": 11,
     "text": "[sentence of 12 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 14 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 13,
     "text": "[sentence of 10 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 14,
     "text": "[sentence of 15 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 15,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 16,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 17,
     "text": "[sentence of 21 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 18,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 19,
     "text": "[sentence of 8 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 20,
     "text": "[sentence of 3 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 21,
     "text": "[sentence of 15 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 22,
     "text": "[sentence of 12 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 23,
     "text": "[sentence of 14 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 24,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 25,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 26,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 27,
     "text": "[sentence of 18 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 28,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 29,
     "text": "[sentence of 5 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 30,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 31,
     "text": "[sentence of 22 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 32,
     "text": "[sentence of 12 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 33,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 34,
     "text": "[sentence of 24 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 35,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 36,
     "text": "[sentence of 4 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 37,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 38,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 39,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 40,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 41,
     "text": "[sentence of 19 words]",
     "type": "other",
     "tone": "negative"
    },
    {
     "n": 42,
     "text": "[sentence of 5 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 43,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 44,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 45,
     "text": "[sentence of 16 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 46,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 47,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 48,
     "text": "[sentence of 9 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 49,
     "text": "[sentence of 8 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 50,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 51,
     "text": "[sentence of 20 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 52,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 53,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 54,
     "text": "[sentence of 9 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 55,
     "text": "[sentence of 5 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 56,
     "text": "[sentence of 20 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 57,
     "text": "[sentence of 29 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 58,
     "text": "[sentence of 7 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 59,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 60,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 61,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 62,
     "text": "[sentence of 13 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 63,
     "text": "[sentence of 4 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 64,
     "text": "[sentence of 8 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 65,
     "text": "[sentence of 2 words]",
     "type": "other",
     "tone": "positive"
    }
   ]
  }
 ]
}
```

</details>

<details><summary>GPT-4o, temperature 0 · Round 3 · 16 October 2026, 13:20</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1175 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]




Task: extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.

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

Return JSON of the form {"articles": [{"article": "<label>", "sentences": [{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (615 words)

```text
{
 "articles": [
  {
   "article": "A1",
   "sentences": [
    {
     "n": 1,
     "text": "[sentence of 21 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 2,
     "text": "[sentence of 14 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 3,
     "text": "[sentence of 17 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 4,
     "text": "[sentence of 17 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 5,
     "text": "[sentence of 8 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 6,
     "text": "[sentence of 5 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 7,
     "text": "[sentence of 4 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 8,
     "text": "[sentence of 2 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 9,
     "text": "[sentence of 4 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 10,
     "text": "[sentence of 5 words]",
     "type": "other",
     "tone": "positive"
    },
    {
     "n": 11,
     "text": "[sentence of 12 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 14 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 13,
     "text": "[sentence of 10 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 14,
     "text": "[sentence of 15 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 15,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 16,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 17,
     "text": "[sentence of 21 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 18,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 19,
     "text": "[sentence of 8 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 20,
     "text": "[sentence of 3 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 21,
     "text": "[sentence of 15 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 22,
     "text": "[sentence of 12 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 23,
     "text": "[sentence of 14 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 24,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 25,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 26,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 27,
     "text": "[sentence of 18 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 28,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 29,
     "text": "[sentence of 5 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 30,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 31,
     "text": "[sentence of 22 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 32,
     "text": "[sentence of 12 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 33,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 34,
     "text": "[sentence of 24 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 35,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 36,
     "text": "[sentence of 4 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 37,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 38,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 39,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 40,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 41,
     "text": "[sentence of 19 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 42,
     "text": "[sentence of 5 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 43,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 44,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 45,
     "text": "[sentence of 16 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 46,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 47,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 48,
     "text": "[sentence of 9 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 49,
     "text": "[sentence of 8 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 50,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 51,
     "text": "[sentence of 20 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 52,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 53,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 54,
     "text": "[sentence of 9 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 55,
     "text": "[sentence of 5 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 56,
     "text": "[sentence of 20 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 57,
     "text": "[sentence of 29 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 58,
     "text": "[sentence of 7 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 59,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 60,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 61,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 62,
     "text": "[sentence of 13 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 63,
     "text": "[sentence of 4 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 64,
     "text": "[sentence of 8 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 65,
     "text": "[sentence of 2 words]",
     "type": "other",
     "tone": "positive"
    }
   ]
  }
 ]
}
```

</details>

<details><summary>GPT-4o, temperature 0 · Round 4, ICE articles · 16 October 2026, 14:27</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (969 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: Breitbart, 2026-06-15, “Exclusive: ICE Agents Arrest Illegal Aliens Convicted of Pedophilia, Child Abuse, Domestic Violence”, 490 words. Text not included.]




Task: extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.

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

Return JSON of the form {"articles": [{"article": "<label>", "sentences": [{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (473 words)

```text
{
 "articles": [
  {
   "article": "A1",
   "sentences": [
    {
     "n": 1,
     "text": "[sentence of 38 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 2,
     "text": "[sentence of 41 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 3,
     "text": "[sentence of 52 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 4,
     "text": "[sentence of 45 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 5,
     "text": "[sentence of 20 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 6,
     "text": "[sentence of 8 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 7,
     "text": "[sentence of 30 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 8,
     "text": "[sentence of 19 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 9,
     "text": "[sentence of 26 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 10,
     "text": "[sentence of 21 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 22 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 20 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 13,
     "text": "[sentence of 25 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 14,
     "text": "[sentence of 28 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 15,
     "text": "[sentence of 32 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 16,
     "text": "[sentence of 22 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 17,
     "text": "[sentence of 21 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 18,
     "text": "[sentence of 20 words]",
     "type": "quote",
     "tone": "positive"
    }
   ]
  }
 ]
}
```

</details>

<details><summary>Haiku 4.5, temperature 0 · Round 2 · 16 October 2026, 13:14</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1127 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]




Task: extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.

Copy each sentence exactly as it appears in its article, character for character. Do not include the headline. Do not skip any sentence, and do not merge or split sentences. A sentence ends at a full stop, a question mark or an exclamation mark, or at a closing quotation mark that follows one of these, unless the mark is part of an abbreviation or a number.

If the article is a transcript, in which passages begin with a speaker's name followed by a colon (for example "SMITH:"), leave the speaker's name and the colon out of the sentence, and treat each sentence as said by that speaker.

Decide the type in this order, and use the first that applies:
1. "quote": the sentence's main content is words of a person or source given in quotation marks, or, in a transcript, words said by anyone other than the outlet's own host or reporter. Each sentence of a quotation that runs over several sentences is a quote. A sentence that reports what someone said without quotation marks, outside a transcript, is not a quote; classify it by the rules below.
2. "opinion": the sentence expresses the writer's own view, judgement or evaluation.
3. "borderline": the sentence has the form of a factual statement but also contains the writer's own judging or interpreting words.
4. "fact": the sentence has the form of a factual statement. It need not be true; do not judge whether it is true.
5. "other": none of the above, for example a question or a line addressed to the reader.
In a transcript, the writer is the outlet's own host or reporter.

Tone is how the sentence presents its main subject (the person, group, institution, event or policy the sentence is chiefly about), judged from the sentence itself and not from your own view of that subject:
- "positive": it presents the subject favourably;
- "negative": it presents the subject unfavourably;
- "neutral": it presents the subject neither favourably nor unfavourably.
For a quote, judge how the quoted words present their subject.

Return JSON of the form {"articles": [{"article": "<label>", "sentences": [{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (1248 words)

```text
{
 "articles": [
  {
   "article": "A1",
   "sentences": [
    {
     "n": 1,
     "text": "[sentence of 14 words]",
     "type": "fact",
     "tone": "negative"
    },
    {
     "n": 2,
     "text": "[sentence of 17 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 3,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 4,
     "text": "[sentence of 8 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 5,
     "text": "[sentence of 5 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 6,
     "text": "[sentence of 4 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 7,
     "text": "[sentence of 2 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 8,
     "text": "[sentence of 4 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 9,
     "text": "[sentence of 5 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 10,
     "text": "[sentence of 12 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 14 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 12,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 13,
     "text": "[sentence of 15 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 14,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 15,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 16,
     "text": "[sentence of 21 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 17,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 18,
     "text": "[sentence of 8 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 19,
     "text": "[sentence of 3 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 20,
     "text": "[sentence of 15 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 21,
     "text": "[sentence of 12 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 22,
     "text": "[sentence of 14 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 23,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 24,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 25,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 26,
     "text": "[sentence of 18 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 27,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 28,
     "text": "[sentence of 5 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 29,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 30,
     "text": "[sentence of 22 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 31,
     "text": "[sentence of 12 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 32,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 33,
     "text": "[sentence of 24 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 34,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 35,
     "text": "[sentence of 4 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 36,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 37,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 38,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 39,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 40,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 41,
     "text": "[sentence of 5 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 42,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 43,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 44,
     "text": "[sentence of 16 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 45,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 46,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 47,
     "text": "[sentence of 9 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 48,
     "text": "[sentence of 8 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 49,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 50,
     "text": "[sentence of 20 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 51,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 52,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 53,
     "text": "[sentence of 9 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 54,
     "text": "[sentence of 5 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 55,
     "text": "[sentence of 20 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 56,
     "text": "[sentence of 29 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 57,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 58,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 59,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 60,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 61,
     "text": "[sentence of 13 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 62,
     "text": "[sentence of 4 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 63,
     "text": "[sentence of 8 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 64,
     "text": "[sentence of 2 words]",
     "type": "quote",
     "tone": "neutral"
    }
   ]
  }
 ]
}
```

</details>

<details><summary>Haiku 4.5, temperature 0 · Round 3 · 16 October 2026, 13:20</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (1175 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: NPR, 2026-08-19, “College professor shares why she believes AI can help 'strengthen thinking'”, 698 words. Text not included.]




Task: extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.

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

Return JSON of the form {"articles": [{"article": "<label>", "sentences": [{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (1265 words)

```text
{
 "articles": [
  {
   "article": "A1",
   "sentences": [
    {
     "n": 1,
     "text": "[sentence of 21 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 2,
     "text": "[sentence of 14 words]",
     "type": "fact",
     "tone": "negative"
    },
    {
     "n": 3,
     "text": "[sentence of 17 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 4,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 5,
     "text": "[sentence of 8 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 6,
     "text": "[sentence of 5 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 7,
     "text": "[sentence of 2 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 8,
     "text": "[sentence of 4 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 9,
     "text": "[sentence of 5 words]",
     "type": "other",
     "tone": "positive"
    },
    {
     "n": 10,
     "text": "[sentence of 12 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 14 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 10 words]",
     "type": "fact",
     "tone": "positive"
    },
    {
     "n": 13,
     "text": "[sentence of 15 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 14,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 15,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 16,
     "text": "[sentence of 21 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 17,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 18,
     "text": "[sentence of 8 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 19,
     "text": "[sentence of 3 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 20,
     "text": "[sentence of 15 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 21,
     "text": "[sentence of 12 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 22,
     "text": "[sentence of 14 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 23,
     "text": "[sentence of 17 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 24,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 25,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 26,
     "text": "[sentence of 18 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 27,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 28,
     "text": "[sentence of 5 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 29,
     "text": "[sentence of 26 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 30,
     "text": "[sentence of 22 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 31,
     "text": "[sentence of 12 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 32,
     "text": "[sentence of 10 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 33,
     "text": "[sentence of 24 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 34,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 35,
     "text": "[sentence of 4 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 36,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 37,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 38,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 39,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 40,
     "text": "[sentence of 19 words]",
     "type": "other",
     "tone": "negative"
    },
    {
     "n": 41,
     "text": "[sentence of 5 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 42,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 43,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 44,
     "text": "[sentence of 16 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 45,
     "text": "[sentence of 7 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 46,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 47,
     "text": "[sentence of 9 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 48,
     "text": "[sentence of 8 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 49,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 50,
     "text": "[sentence of 20 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 51,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 52,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 53,
     "text": "[sentence of 9 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 54,
     "text": "[sentence of 5 words]",
     "type": "quote",
     "tone": "negative"
    },
    {
     "n": 55,
     "text": "[sentence of 20 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 56,
     "text": "[sentence of 29 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 57,
     "text": "[sentence of 7 words]",
     "type": "other",
     "tone": "neutral"
    },
    {
     "n": 58,
     "text": "[sentence of 1 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 59,
     "text": "[sentence of 6 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 60,
     "text": "[sentence of 11 words]",
     "type": "quote",
     "tone": "neutral"
    },
    {
     "n": 61,
     "text": "[sentence of 13 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 62,
     "text": "[sentence of 4 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 63,
     "text": "[sentence of 8 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 64,
     "text": "[sentence of 2 words]",
     "type": "other",
     "tone": "neutral"
    }
   ]
  }
 ]
}
```

</details>

<details><summary>Haiku 4.5, temperature 0 · Round 4, ICE articles · 16 October 2026, 14:22</summary>

**System prompt**

```text
Reply with a single JSON object and nothing else.
```

**The request** (969 words)

```text
The following news article is labelled A1. The name of the outlet has been removed.

[Article A1: Breitbart, 2026-06-15, “Exclusive: ICE Agents Arrest Illegal Aliens Convicted of Pedophilia, Child Abuse, Domestic Violence”, 490 words. Text not included.]




Task: extract every sentence of the text of the article labelled A1, in order, and classify each sentence by type and by tone.

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

Return JSON of the form {"articles": [{"article": "<label>", "sentences": [{"n": 1, "text": "<sentence>", "type": "quote|opinion|borderline|fact|other", "tone": "positive|neutral|negative"}, ...]}, ...]}, with one entry in "articles" for each article you were asked about.
```

**The reply** (656 words)

```text
{
 "articles": [
  {
   "article": "A1",
   "sentences": [
    {
     "n": 1,
     "text": "[sentence of 38 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 2,
     "text": "[sentence of 33 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 3,
     "text": "[sentence of 52 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 4,
     "text": "[sentence of 45 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 5,
     "text": "[sentence of 20 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 6,
     "text": "[sentence of 8 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 7,
     "text": "[sentence of 30 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 8,
     "text": "[sentence of 19 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 9,
     "text": "[sentence of 26 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 10,
     "text": "[sentence of 21 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 11,
     "text": "[sentence of 22 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 12,
     "text": "[sentence of 20 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 13,
     "text": "[sentence of 25 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 14,
     "text": "[sentence of 28 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 15,
     "text": "[sentence of 32 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 16,
     "text": "[sentence of 22 words]",
     "type": "fact",
     "tone": "neutral"
    },
    {
     "n": 17,
     "text": "[sentence of 19 words]",
     "type": "quote",
     "tone": "positive"
    },
    {
     "n": 18,
     "text": "[sentence of 20 words]",
     "type": "quote",
     "tone": "positive"
    }
   ]
  }
 ]
}
```

</details>
