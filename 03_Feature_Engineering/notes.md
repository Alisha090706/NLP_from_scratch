# 🧠 One-Hot Encoding (NLP)

## 📌 Definition
- A basic text representation technique in NLP
- Converts each word into a binary vector
- Vector length equals the vocabulary size
- Exactly one index is `1`, all others are `0`

---

## 📝 Example

Sentence:
I love NLP

Vocabulary:
["I", "love", "NLP"]


One-Hot Vectors:
- I → [1, 0, 0]
- love → [0, 1, 0]
- NLP → [0, 0, 1]

---
# Bag of Words (BoW) – NLP Notes

## What is Bag of Words?
Bag of Words (BoW) is a text representation technique that converts text into numerical vectors based on word frequency, ignoring grammar and word order.

---

## Core Idea
- Treat text as a **bag of words**
- Order of words is ignored
- Only **frequency/count** of words matters

---

## Steps Involved
1. Collect text documents
2. Tokenize text
3. (Optional) Remove stopwords & punctuation
4. Create a vocabulary of unique words
5. Count word occurrences
6. Represent each document as a vector

---

## Example
Documents:
- D1: "I love NLP"
- D2: "I love AI"

Vocabulary:
["I", "love", "NLP", "AI"]


Vectors:
D1 → [1, 1, 1, 0]
D2 → [1, 1, 0, 1]


---

## Document-Term Matrix (DTM)
- Rows → Documents  
- Columns → Words  
- Values → Frequency  

---

## Types of BoW
- **Binary BoW** → 0 or 1 (presence)
- **Count BoW** → word frequency
- **Term Frequency (TF)** → normalized counts

---

## Advantages
- Simple and easy to implement
- Fast computation
- Works well as a baseline model

---

## Disadvantages
- Ignores word order
- No semantic meaning
- Produces sparse vectors
- Large vocabulary size

---

## Use Cases
- Text classification
- Spam detection
- Basic sentiment analysis
- Baseline NLP models

---

## Key Limitation
BoW cannot capture context, meaning, or relationships between words.

---
# N-grams 

## What is an N-gram?
An N-gram is a sequence of **N consecutive words or characters** extracted from a text.  
It helps capture **local word order**, which Bag of Words ignores.

---

## Types of N-grams
- **Unigram (1-gram)** → single word  
- **Bigram (2-gram)** → two consecutive words  
- **Trigram (3-gram)** → three consecutive words  

Example sentence:
"I love NLP"

- Unigrams → `["I", "love", "NLP"]`
- Bigrams → `["I love", "love NLP"]`
- Trigrams → `["I love NLP"]`

---

## Why Use N-grams?
- Capture word order
- Preserve local context
- Differentiate phrases like `"not good"` vs `"good"`

---

## N-grams with Bag of Words
- N-grams extend Bag of Words by using word sequences instead of single words
- Commonly used with **CountVectorizer** and **TF-IDF**

---

## ngram_range (sklearn)
- `(1,1)` → Unigrams
- `(2,2)` → Bigrams
- `(1,2)` → Unigrams + Bigrams
- `(1,3)` → Uni + Bi + Trigrams

---

## Advantages
- Better context than BoW
- Simple to implement
- Improves text classification performance

---

## Disadvantages
- Large vocabulary size
- Sparse feature vectors
- Still no semantic understanding

---

## Use Cases
- Sentiment analysis
- Text classification
- Basic language modeling
- Phrase detection

---

## Key Takeaway
N-grams capture **local context and word order**, making them more powerful than simple Bag of Words.

---
# TF-IDF

## What is TF-IDF?
TF-IDF stands for **Term Frequency – Inverse Document Frequency**.  
It is a text representation technique that measures **how important a word is to a document relative to a collection of documents**.

---

## Why TF-IDF?
- Common words like *“is”, “the”, “and”* appear frequently but carry little meaning
- TF-IDF **reduces the weight of common words**
- Highlights **important and rare words**

---

## Components

### 1. Term Frequency (TF)
Measures how often a word appears in a document.
TF(word) = (Number of times word appears in document) / (Total words in document)


---

### 2. Inverse Document Frequency (IDF)
Measures how rare a word is across all documents.


IDF(word) = log(Total documents / Documents containing the word)


---

### 3. TF-IDF Formula


TF-IDF = TF × IDF


---

## Intuition
- Word appears **many times in one document** → important
- Word appears **in many documents** → less important
- TF-IDF balances both

---

## Example
Documents:
- D1: "I love NLP"
- D2: "I love AI"

- Word **"love"** appears in both → low IDF
- Word **"NLP"** appears only in D1 → high IDF

✔ TF-IDF gives **higher weight to "NLP"**

---

## TF-IDF vs Bag of Words
| Feature | BoW | TF-IDF |
|------|-----|--------|
| Uses frequency | ✅ | ✅ |
| Penalizes common words | ❌ | ✅ |
| Importance-based | ❌ | ✅ |
| Sparse vectors | ✅ | ✅ |

---

## Advantages
- Reduces impact of stopwords
- Better feature importance than BoW
- Simple and effective
- Widely used baseline

---

## Disadvantages
- Ignores word order
- No semantic meaning
- Still produces sparse vectors

---

## Use Cases
- Text classification
- Search engines
- Information retrieval
- Sentiment analysis

---

## Key Takeaway
TF-IDF highlights **important words** by down-weighting common ones, making it more powerful than simple Bag of Words.

---