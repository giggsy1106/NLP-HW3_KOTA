# Article NLP Pipeline (TF-IDF + SBERT + Similarity)

This project extracts text from an article (or a local file), splits it into sentences, and computes:
- TF-IDF vectors (sparse representation)
- Sentence embeddings using SentenceTransformers (SBERT)
- Cosine similarity between sentences
- Top-K sentences most similar to a query (title or first sentence)
- A simple extractive summary

## Why this exists
Some websites (especially paywalled ones like Washington Post) often return paywall or partial HTML in automated environments (like GitHub Actions).  
So this repo supports **offline mode** using a saved HTML or plain text file for reproducible results.

---

## Project Structure
.
├── main.py
├── requirements.txt
└── README.md


---

## Setup (Local)

### 1) Create a virtual environment
```bash
python -m venv .venv
source .venv/bin/activate   # Mac/Linux
# .venv\Scripts\activate    # Windows
2) Install dependencies
pip install -r requirements.txt
3) Download NLTK tokenizer data (IMPORTANT)

This project intentionally does NOT download NLTK resources during runtime (GitHub-safe).

python -c "import nltk; nltk.download('punkt')"
