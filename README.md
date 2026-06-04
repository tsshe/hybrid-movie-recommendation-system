# Hybrid Movie Recommendation System
### Semester V Project | NMIMS BSc Applied Mathematical Computing, November 2024

**Authors:** Juhi Kariya · Tanushri Shetty  
**Supervisor:** Dr. Debasmita Mukherjee, NSOMASA, NMIMS Mumbai

---

## Objective
Build a personalised movie recommendation system using three complementary 
techniques, combined into a mixed hybrid approach.

---

## Methods

| Method | Technique | Output |
|--------|-----------|--------|
| Content-Based Filtering | TF-IDF + Cosine Similarity on genres | 5 genre-similar movies |
| Collaborative Filtering (Correlation) | Pearson correlation across users | 5 user-behaviour-based picks |
| Collaborative Filtering (SVD) | Matrix factorisation via Surprise library | 5 latent-factor-based picks |
| **Hybrid** | Top 2 from each method by avg rating | **6 final recommendations** |

---

## Dataset
[MovieLens 20M](https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset) — 
20M ratings across 27,278 movies from 138,493 users.  
We use 50% of users to manage computation time.

> See `data/README.md` for download instructions. Do not upload the raw CSV files.

---

## Results
- SVD RMSE: **~0.79** (on 20% held-out test set)
- System validated on real ratings from both authors

---

## Tech Stack
- **Python** — pandas, numpy, scikit-learn, matplotlib
- **Recommendation** — `scikit-learn` (TF-IDF, cosine similarity), `Surprise` (SVD)

---

## How to Run

```bash
git clone https://github.com/YOUR_USERNAME/hybrid-movie-recommendation-system.git
pip install pandas numpy scikit-learn scikit-surprise
# Download dataset to data/ folder (see data/README.md)
jupyter notebook Hybrid_Movie_Recommendation_System.ipynb
```

---

## References
- Lekakos & Caravelas (2006) — *A hybrid approach for movie recommendation*
- Harper & Konstan (2015) — *The MovieLens Datasets*
- Hug, N. (2020) — *Matrix factorization for recommendation systems*
