# 🎬 Movie Recommendation System (MovieLens 100K)

This project implements a movie recommendation system using the [MovieLens 100K Dataset](https://grouplens.org/datasets/movielens/100k/).  
It demonstrates three collaborative filtering approaches to recommend movies to users based on historical rating data.

---

## 📁 Dataset

- Source: [MovieLens 100K Dataset](https://www.kaggle.com/datasets/heeraldedhia/movielens-dataset)
- Contains:
  - u.data: User ratings (user_id, movie_id, rating, timestamp)
  - u.item: Movie information (movie_id, movie_title, ...)
  - u.user: (optional) User demographic info

---

## 🚀 Features

✅ User-Based Collaborative Filtering  
✅ Item-Based Collaborative Filtering  
✅ Matrix Factorization using SVD (Singular Value Decomposition)  
✅ Ratings clipped to a realistic range (1 to 5)

---

## 🧠 Recommendation Methods

### 👤 1. User-Based Collaborative Filtering

- Measures similarity between users using cosine similarity
- Recommends movies liked by similar users that the target user hasn't rated

### 🎬 2. Item-Based Collaborative Filtering

- Measures similarity between movies
- Recommends movies that are similar to the ones the user liked

### 🧮 3. Matrix Factorization (SVD)

- Uses TruncatedSVD from scikit-learn
- Compresses the user-movie matrix into latent features
- Predicts ratings for all user-movie pairs
- Predictions are clipped to a 1–5 scale

---

## 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Seaborn
- Matplotlib

---

## 📊 Example Usage

```python
# Recommend movies using user-based CF
recommend_movies(10)

# Recommend using item-based CF
recommend_items(10)

# Recommend using SVD predictions
recommend_svd(10)
