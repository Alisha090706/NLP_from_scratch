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
