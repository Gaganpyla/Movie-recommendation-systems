# 🎬 Movie Recommendation System

[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Library-Pandas-red.svg)](https://pandas.pydata.org/)

## 📌 Project Overview
This project is a **Content-Based Movie Recommendation System** that suggests movies similar to a user's favorite film. It leverages Natural Language Processing (NLP) techniques and similarity metrics to analyze movie metadata and provide personalized recommendations.

## 📊 Dataset
The system utilizes a `movies.csv` dataset containing information on over 4,800 films. Key features used for building the recommendation engine include:
* **Genres**: The category of the movie (e.g., Action, Sci-Fi).
* **Keywords**: Significant words associated with the film's plot.
* **Tagline**: The catchphrase of the movie.
* **Cast**: The lead actors in the film.
* **Director**: The person who directed the movie.

## 🛠️ Technical Workflow
The recommendation logic follows these core steps as implemented in the notebook:

1.  **Data Preprocessing**: Handles missing values in the metadata by replacing null strings with empty spaces.
2.  **Feature Fusion**: Combines the selected features (genres, keywords, tagline, cast, and director) into a single unified string for each movie.
3.  **Vectorization**: Uses **TF-IDF (Term Frequency-Inverse Document Frequency) Vectorizer** to convert text data into numerical feature vectors.
4.  **Similarity Calculation**: Computes the **Cosine Similarity** score between all movie vectors to determine how closely related each film is to the others.
5.  **User Interaction**: 
    * Accepts a movie title from the user.
    * Uses the `difflib` library to find the closest match in the dataset, accounting for typos or partial names.
6.  **Ranking**: Identifies movies with the highest similarity scores and displays the top recommendations.

## 🚀 Getting Started

### Prerequisites
Ensure you have the following Python libraries installed:
```bash
pip install numpy pandas scikit-learn
