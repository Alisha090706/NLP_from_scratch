## NLTK

### What is punkt?
`punkt` is a pretrained sentence tokenizer model required by `sent_tokenize()`.

### Why punkt_tab?
Newer Python/NLTK versions require an additional resource (`punkt_tab`) for sentence tokenization.

These resources are downloaded once and reused.

---
## Tokenization

### What is Tokenization?
Tokenization is the process of breaking raw text into smaller units called tokens.
Tokens can be words, characters, or subwords.

### Why is Tokenization important?
- Machine learning models cannot process raw text
- Helps create vocabulary
- Directly affects model performance

### Types of Tokenization

1. Word Tokenization  
Splits text into words.

2. Character Tokenization  
Splits text into individual characters.

3. Subword Tokenization  
Breaks words into meaningful sub-parts (used in modern models like BERT).

### Example
Input:
"I love NLP!"

Word Tokens:
["I", "love", "NLP"]

Character Tokens:
["I", " ", "l", "o", "v", "e", " ", "N", "L", "P", "!"]

### Libraries Used
- NLTK
- spaCy
- Hugging Face Tokenizers

### Common Issues
- Handling punctuation
- Language dependency
- Unknown words (OOV problem)
---

## Stemming

### What is Stemming?
Stemming reduces words to their root form using rule-based heuristics.

### Why use Stemming?
- Reduces vocabulary size
- Improves efficiency in traditional ML models

### Example
playing, played → play

### Drawback
Stemmed words may not be valid English words.

### Common Algorithms
- Porter Stemmer
- Snowball Stemmer
- Regexp Stemmer

---
## Lemmatization

Lemmatization reduces words to their base or dictionary form (lemma)
using vocabulary and grammatical analysis.

Unlike stemming, lemmatization produces meaningful words.

### Example
- running → run
- better → good
- studies → study

Lemmatization works best when Part-of-Speech (POS) is provided.
