# Movie Recommendation System

## Overview

This project is a **content-based Movie Recommendation System** built using Machine Learning.
It recommends movies similar to a selected movie based on features like **genres, keywords, cast, crew, and overview**.

The system uses **Natural Language Processing (NLP)** and **cosine similarity** to find and suggest relevant movies.

---

##  Features

*  Personalized movie recommendations
*  Content-based filtering using **TF-IDF**
*  Weighted feature engineering (genres, overview, cast, etc.)
*  Movie posters using **TMDB API**
*  Interactive web application using **Streamlit**
*  Fast similarity computation

---

##  How It Works

### 1. Data Collection

* TMDB 5000 Movies Dataset

### 2. Data Preprocessing

* Merge movie and credit datasets
* Extract:

  * Genres
  * Keywords
  * Cast (top 3 actors)
  * Director
* Remove missing values and duplicates

### 3. Feature Engineering

* Combine features into a single **tags** column
* Apply weights:

  * Genres → 3
  * Overview → 2
  * Keywords → 2
  * Cast → 2
  * Crew → 1

### 4. Text Processing

* Convert text to lowercase
* Apply stemming using **PorterStemmer**

### 5. Vectorization

* Use **TF-IDF Vectorizer**

### 6. Similarity Calculation

* Compute **cosine similarity** between movies

### 7. Recommendation

* Return top 5 most similar movies

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* NLTK
* Streamlit
* TMDB API

---

##  Project Structure

```
project/
│
├── data/
│   ├── tmdb_5000_movies.csv
│   ├── tmdb_5000_credits.csv
│
├── notebooks/
│   └── model.ipynb / Note.py
│
├── report/
│   └── Movie_Recommend_System_Report.pdf
├── app.py
├── movies.pkl
├── similarity.pkl
├── requirements.txt
└── README.md
```

---

## ▶ How to Run

### 1. Clone the Repository

```
git clone https://github.com/sarthak25bai10443-ui/Movie-Recommendation-System-Using-ML
cd Movie-Recommendation-System-Using-ML
```

### 2. Install Dependencies

```
pip install -r requirements.txt
```

### Generate similarity file locally

```
python model.py #Will take time 
```

### 3. Run the App

```
streamlit run app.py
```

---

## Screenshots

<img width="989" height="801" alt="{E924F007-ADBB-43D7-9C45-3DE07E8CE972}" src="https://github.com/user-attachments/assets/f0c6548a-469f-4552-ac6e-d2176e4c2be6" />

---

## 📊 Example Output

**Input:**

```
Movie: Avatar
```

**Output:**

```
Recommended Movies:
- Battle: Los Angeles
- Falcon Rising
- Aliens vs Predator : Requiem
- Aliens
- Lifeforce
```

---

## Future Improvements

*  Add search functionality
*  Hybrid recommendation system
*  Deep learning (BERT embeddings)
*  Deploy on cloud

---

##  Learning Outcomes

* Understanding recommendation systems
* Feature engineering and NLP
* Working with real-world datasets
* Building interactive ML applications

---

##  Author

**Sarthak Jajodia**
B.Tech AI & ML
VIT Bhopal

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!
