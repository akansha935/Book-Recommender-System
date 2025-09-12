# Book-Recommender-System

Project Overview

This project implements a Book Recommender System using the Book-Crossing Dataset
, which contains information about books, users, and ratings.

The goal is to recommend books to users based on:

Popularity (most-read or highly-rated books)

Collaborative Filtering (user-user & item-item similarity)

Content-Based Filtering (author, title, publisher similarity)

Hybrid Approach (combination of collaborative & content-based methods)

📂 Dataset

The dataset consists of three files:

Books.csv → ISBN, Title, Author, Publisher, Year of Publication, Book Images

Ratings.csv → User-ID, ISBN, Book-Rating (0 = implicit, 1–10 = explicit)

Users.csv → User-ID, Location, Age

🔍 Exploratory Data Analysis (EDA)

Key findings from the dataset:

Ratings are sparse; most users rated very few books.

A small number of books (e.g., Harry Potter, Wild Animus) dominate the ratings.

Publication years include invalid values (e.g., 0, 2050).

User ages range widely, with some invalid values (>100).

Most users are from the USA, Canada, Germany.

📊 EDA includes:

Rating distribution

Most rated books

Most active users

Publication year trends

User age distribution

Top authors and publishers

⚙️ Methodology
1. Popularity-Based Recommender

Recommends the most rated or highest-rated books overall.

2. Collaborative Filtering

User-Based CF: Finds users with similar taste and recommends their books.

Item-Based CF: Finds books similar to the ones the user has rated.

Implemented using surprise library (KNN, SVD).

📈 Results

Popularity-based recommendations work well for new users.

Collaborative filtering improves personalization but suffers from sparsity.

Content-based recommendations work for new items (no cold-start for books).

Hybrid system balances both approaches for better accuracy.

📌 Future Work

Improve data cleaning (better handling of missing/invalid values).

Use deep learning models (e.g., Neural Collaborative Filtering).

Deploy on Heroku/Streamlit Cloud for public demo.

Add demographic-based filtering (using age, location).
