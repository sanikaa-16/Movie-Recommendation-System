# 🎬 Movie Recommendation System

This machine learning model uses **TF-IDF** and **Cosine Similarity** to recommend movies based on your input (favorite movie). It implements both **Content-Based** and **Popularity-Based** recommendation systems to suggest relevant and interesting titles.

---

## 📚 Types of Recommendation Systems

1. **Content-Based Recommendation System**  
   Recommends movies that are similar to those the user has already enjoyed. Similarity is determined based on features like keywords, cast, director, genre, and storyline (tagline).

2. **Popularity-Based Recommendation System**  
   Suggests movies that are currently trending or most-watched in a region. Platforms like Netflix’s *Top 10 Today* or Prime Video’s *Most Popular* use this approach.

3. **Collaborative Filtering Recommendation System**  
   Groups users based on similar watching patterns. Recommendations are made by identifying what other users in the same group have liked. If a new user watches 2–3 movies from a group, they get more suggestions from that same group.

---

## 🚀 Project Overview

In this project, I’ve built both **Content-Based** and **Popularity-Based** movie recommendation systems.

---

## ✅ Project Outcomes

The model provides **highly relevant recommendations**. Based on a given movie title, the system suggests similar movies that align well with the input in terms of theme, genre, cast, and more.

---

## 🔁 Workflow

1. **Data Collection**  
   I used a `movies.csv` file from a public dataset available on Google Datasets.

2. **Data Analysis and Preprocessing**  
   - Explored the dataset and cleaned it.
   - Chose relevant features for content-based filtering: `keywords`, `tagline`, `cast`, `director`, and `genre`.
   - Handled missing values by replacing them with `'NULL'` strings.

3. **Feature Extraction**  
   - Used `difflib` to match the user's input with the closest movie title.
   - Retrieved the index of the selected movie and calculated similarity scores using **Cosine Similarity**.
   - Returned the top 10 movies based on descending similarity scores.

4. **Popularity-Based System**  
   - Used the `popularity` column in the dataset to rank movies.
   - Displayed the top 10 most popular movies directly.

---

## 🧠 How TF-IDF Works

TF-IDF stands for **Term Frequency-Inverse Document Frequency**. It doesn’t analyze context but measures the importance of words across documents.

- **TF (Term Frequency)** = (Number of times a word appears in a document) / (Total words in the document)  
- **IDF (Inverse Document Frequency)** = log(N / n), where:
  - *N* = Total number of documents
  - *n* = Number of documents containing the term  

So,  
**TF-IDF = TF × IDF**

TF-IDF is widely used in recommendation systems and spam filters. However, since it doesn't understand language context, it's limited compared to NLP-based models.

---

## 🔮 Future Work

- Use a live **movie database API** (like TMDB or OMDb) to fetch the latest movie data dynamically.
- Implement **NLP models** (e.g., BERT, Word2Vec) to understand the semantic context of movies better.
- Add a **Collaborative Filtering** module using user ratings and viewing behavior.
- Build a **web application** using Flask or Streamlit for a more interactive user experience.
- Integrate user **ratings and reviews** for more personalized recommendations.
- Use **deep learning models** such as Neural Collaborative Filtering (NCF) or Autoencoders for improved accuracy.

---
