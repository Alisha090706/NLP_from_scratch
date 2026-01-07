## Part-of-Speech (POS) Tagging

POS tagging assigns grammatical labels (noun, verb, adjective, etc.)
to each word in a sentence.

### Why POS tagging?
- Helps in syntactic analysis
- Required for lemmatization
- Improves downstream NLP tasks

### Example
"She is reading a book"
→ She/PRP is/VBZ reading/VBG a/DT book/NN
---
## Named Entity Recognition (NER)

Named Entity Recognition (NER) is an NLP task that identifies and classifies
important entities in text into predefined categories such as people,
organizations, locations, dates, etc.

NER is **not basic text preprocessing**.
It is a **higher-level information extraction task** performed after
tokenization and POS tagging.

---

### Why NER is important

- Extracts structured information from unstructured text
- Used in search engines, chatbots, recommendation systems
- Helps in information retrieval and knowledge graphs
- Crucial for real-world NLP applications

---

### Example

Sentence:
"Alisha studies at IGDTUW in Delhi."

NER Output:
- Alisha → PERSON
- IGDTUW → ORG
- Delhi → GPE

---

### Common Named Entity Types

- **PERSON** — Names of people  
  *Example:* Alisha, Abraham Lincoln

- **ORG** — Organizations, institutions  
  *Example:* Google, IGDTUW

- **GPE** — Geo-political entities (countries, cities, states)  
  *Example:* India, Delhi

- **LOC** — Locations (non-political)  
  *Example:* Himalayas

- **DATE** — Dates  
  *Example:* 2024, July 4

- **TIME** — Time expressions  
  *Example:* morning, 5 PM

- **MONEY** — Monetary values  
  *Example:* $10, ₹500

- **PERCENT** — Percentages  
  *Example:* 50%

---
