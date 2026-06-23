# Theory and Reflection Questions

## 1. The Vector Conflict
When I ran the dot product, I noticed that Sentence 1 and Sentence 2 got a non-zero similarity score even though "light" means completely different things in each. This is because CountVectorizer just counts how many times a word appears — it has no idea what the word actually means in that sentence. So whether "light" refers to calories or to actual light coming through a box, the model treats it as the exact same thing. That's the core problem with static vectors.

## 2. The Context Blindspot
The biggest issue with Bag-of-Words is that it completely throws away the meaning behind words. Imagine searching "light snack" on a website — a BoW-based search engine could easily return results about light bulbs just because the word "light" appears. The same problem hits chatbots, which could misunderstand what a user is actually asking. Once you convert text into word counts, all the context and real meaning is just gone.

## 3. The GenAI Architectural Fix
This is exactly the problem that modern LLMs like GPT solve using Self-Attention. Instead of giving "light" one fixed vector forever, the model looks at all the surrounding words and builds a meaning based on context. So "light" next to "stomach" gets a totally different vector than "light" next to "box." That's how Context-Aware Embeddings work — the same word gets a different mathematical identity depending on where it appears.
