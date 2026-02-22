# DATA-622 Homework 3 — NLP Sentence Embeddings & Similarity

## Overview
This notebook demonstrates core NLP techniques including sentence tokenization,
TF-IDF vectorization, sentence embeddings using a pre-trained SBERT model,
and cosine similarity computation — applied to a real-world news article.

---

## Assignment
**Course:** DATA-622 — Machine Learning  
**Homework:** 3  
**Topic:** Natural Language Processing — Sentence Embeddings  
**Author:** Rahul Reddy Kota  

---

## Article Source
**Washington Post** — *Air India plane crash: Sole survivor in seat 11A says it's a miracle he lived*  
URL: [https://www.washingtonpost.com/world/2025/06/13/air-india-plane-crash-survivor-vishwash-kumar-ramesh](https://www.washingtonpost.com/world/2025/06/13/air-india-plane-crash-survivor-vishwash-kumar-ramesh)

> **Note:** The Washington Post blocks automated scraping. A direct article excerpt
> (>700 characters) is hardcoded in the notebook to allow all steps to run correctly.

---

## Steps Implemented

| Step | Description |
|------|-------------|
| 1 | Read article text and print the first 700 characters |
| 2 | Split text into sentences using NLTK's sentence tokenizer |
| 3 | Load pre-trained SBERT model (`all-MiniLM-L6-v2`) and compute TF-IDF vectors |
| 4 | Generate sentence embeddings and print the shape of the first embedding |
| 5 | Compute cosine similarity between the first and second sentence embeddings |

---

## Technologies Used

- **Python 3.x**
- **NLTK** — Sentence tokenization (`punkt`, `punkt_tab`)
- **sentence-transformers** — Pre-trained SBERT model (`all-MiniLM-L6-v2`)
- **scikit-learn** — TF-IDF Vectorizer, Cosine Similarity
- **Google Colab** — Execution environment

---

## Installation

Run the following in a Colab cell **before** executing the notebook:

```bash
!pip install -q -U sentence-transformers transformers scikit-learn
!pip install -q nltk beautifulsoup4 requests
Then restart the runtime (Runtime > Restart session) before running the main code.

Expected Output
text
STEP 1 — First 700 Characters:
On Air India Flight 171, only one individual managed to survive...
Length: 700 characters

STEP 2 — Sentence Tokenization:
Total sentences: 8
First 5 sentences: ...

STEP 3 — TF-IDF Vectorization:
TF-IDF matrix shape: (8, 60)

STEP 4 — Sentence Embeddings (SBERT all-MiniLM-L6-v2):
All embeddings shape: (8, 384)
First sentence embedding shape: (384,)

STEP 5 — Cosine Similarity:
Cosine Similarity (SBERT): 0.5873
Interpretation: Moderate semantic similarity
Key Concepts
TF-IDF measures word importance based on frequency across documents — captures lexical similarity.

SBERT (all-MiniLM-L6-v2) generates dense 384-dimensional vectors — captures semantic meaning even when wording differs.

Cosine Similarity ranges from 0 (no similarity) to 1 (identical meaning).

How to Run
Option 1 — Google Colab
Open In Colab

Open Google Colab

File > Upload notebook > Select NLP_HW3_updated-1.ipynb

Run Cell 1 (installs), restart runtime, then run Cell 2

Option 2 — Clone from GitHub
bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
jupyter notebook NLP_HW3_updated-1.ipynb
File Structure
text
├── NLP_HW3_updated-1.ipynb   # Main notebook with all 5 steps
├── DATA-622-Homework-3.pdf   # Original assignment instructions
└── README.md                 # This file
License
This project is for academic purposes only — DATA-622, Spring 2026.

text

## How to Add to GitHub

```bash
# In your repo folder (or directly on GitHub website)
# 1. Create a new file named README.md
# 2. Paste the above content
# 3. Commit with message: "Add README for HW3"
