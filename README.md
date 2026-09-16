# Language Model Lab

I'm learning how language models work by trying small experiments as I go.

## What I'm learning

- How text can be represented as embeddings
- How cosine similarity compares sentences
- Why similar topics don't always mean similar intent

## Experiments

### 01 — Sentence Embeddings & Semantic Similarity

I started with a small customer support example to see if similar problems would have similar embeddings. One result surprised me: two tickets I considered the same type of problem only had a similarity of 0.41. So I tried KMeans and, in this small example, it grouped the tickets the way I expected.

Then I tried another example with passwords. The recovery and stealing sentences had the highest similarity even though the intent was very different.

That made me realize that semantic similarity alone isn't enough to understand what someone actually wants.

### 02 — Scam Message Detection

I wanted to test if embeddings could warn someone about a scam message by comparing it to known scam examples.

It worked at first, but then I removed one legitimate example from my reference list and the same message flipped from "legitimate" to "scam" — even though the scam scores never changed.

So the system wasn't really detecting scams. It was checking whether I happened to have something similar in my list.

## Learning from

Hugging Face LLM Course
