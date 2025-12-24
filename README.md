# Movie Recommender System (Content-Based)

A **content-based movie recommendation system** built using **Python, Machine Learning, and Streamlit**. The system recommends movies similar to a selected movie based on textual features such as genres, keywords, cast, and crew, and displays movie posters using the **TMDB API**.

---

## Project Overview

This project demonstrates the complete pipeline of a **machine learning-based recommender system**, starting from data preprocessing and feature engineering to similarity computation and deployment using **Streamlit**.

The user selects a movie from a dropdown, and the system recommends **5 similar movies** along with their posters.

---

## What I Did in This Project

### 1. Data Collection

* Used the **TMDB 5000 Movies Dataset** containing movie metadata such as:

  * Movie title
  * Genres
  * Keywords
  * Cast
  * Crew
  * Movie ID

### 2. Data Preprocessing

* Merged movies and credits datasets
* Selected important features for recommendation
* Converted JSON-like columns into readable lists
* Cleaned and normalized text data
* Created a combined **"tags"** column for each movie

### 3. Feature Engineering

* Applied **CountVectorizer** to convert text data into numerical vectors
* Limited features to the most relevant tokens
* Removed stopwords to improve quality

### 4. Similarity Computation

* Used **Cosine Similarity** to measure similarity between movies
* Generated a similarity matrix
* Stored the matrix using `pickle` for fast reuse

### 5. Recommendation Logic

* For a selected movie:

  * Found its index
  * Sorted movies based on similarity score
  * Returned the top 5 most similar movies

### 6. Poster Fetching

* Integrated **TMDB API** to fetch movie posters dynamically
* Displayed posters using Streamlit UI

### 7. Deployment

* Built an interactive web app using **Streamlit**
* Loaded preprocessed data and similarity matrix
* Displayed movie names and posters in a clean layout

---

## Tech Stack Used

* **Python**
* **Pandas & NumPy** – Data handling
* **Scikit-learn** – Vectorization & similarity
* **Streamlit** – Web application
* **Pickle** – Model persistence
* **TMDB API** – Movie posters

---

## Project Structure

```
Movie-Recommender-System/
│
├── app.py                  # Streamlit application
├── Movie-Recommender-System.ipynb  # Notebook (EDA + Model)
├── movie_dict.pkl          # Movie data
├── similarity.pkl          # Cosine similarity matrix
├── requirements.txt        # Dependencies
├── README.md               # Project documentation
```

---


## Application Screenshot

> *Add a screenshot of your Streamlit app here*

```
<img width="1418" height="939" alt="image" src="https://github.com/user-attachments/assets/685657a5-ad59-49c6-987f-f111609b629e" />

```

---

## Dataset Used

**TMDB 5000 Movies Dataset**
[https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

---

## API Used

* **The Movie Database (TMDB) API**
  Used to fetch movie posters dynamically.

🔗 [https://www.themoviedb.org/documentation/api](https://www.themoviedb.org/documentation/api)

---

## Key Features

* Content-based recommendation
* Fast similarity lookup using pickled matrix
* Interactive UI with posters
* Scalable and easy to extend

---

## Future Improvements

* Add collaborative filtering
* Improve UI/UX
* Add movie overview & ratings
* Deploy on Streamlit Cloud / Render

---

