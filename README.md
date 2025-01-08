# Movie Recommender System

This repository contains the code for a **Content-Based Movie Recommender System** built using Python. The system recommends movies based on their metadata (e.g., genres, keywords, cast, crew, and overview). The implementation leverages the `pandas` library for data processing and `scikit-learn` for machine learning tasks like vectorization and calculating cosine similarity.

## Overview

The system processes two datasets:
- **Movies Dataset**: Contains information about various movies (e.g., title, overview, genres).
- **Credits Dataset**: Contains cast and crew information for each movie.

It then uses this data to recommend movies based on their content similarity.

## How It Works

1. **Data Preprocessing**:
   - The data is loaded and merged.
   - Important columns (such as genres, keywords, cast, crew, and overview) are extracted.
   - Missing or duplicate data is handled.
   
2. **Feature Engineering**:
   - Genres, keywords, cast, crew, and the overview are processed and combined into a single "tags" column for each movie.
   - Text data is cleaned by removing spaces, converting text to lowercase, and applying stemming to reduce words to their root forms.

3. **Vectorization**:
   - The `CountVectorizer` from `scikit-learn` is used to convert the tags into a numerical format that can be used for machine learning.
   
4. **Recommendation**:
   - The system computes the cosine similarity between movies based on their tags.
   - Given a movie, it recommends other movies that are most similar based on their metadata.

5. **Model Outputs**:
   - The preprocessed data and similarity matrix are saved in pickle files (`movie_list.pkl` and `similarity.pkl`) for later use, so you don’t need to recalculate them each time.

## Files

- **CSV Files**: 
  - `tmdb_5000_movies.csv`: Movies dataset.
  - `tmdb_5000_credits.csv`: Movie credits dataset.

- **Artifacts**:
  - `movie_list.pkl`: The preprocessed movie list.
  - `similarity.pkl`: The similarity matrix for the movies.

## Prerequisites

To run this code, you need Python 3.x and the following libraries:

- `pandas`
- `numpy`
- `nltk`
- `scikit-learn`

You can install the required libraries using the following command:


`pip install -r requirements.txt`


### Downloading Data Files

The datasets (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) can be accessed and downloaded from the following links:

- [Movies dataset (https://www.kaggle.com/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv)

Place the downloaded files in the `csv/` directory.

## In the Project

* Robert Steve Onyango
* Victor Sabare Oketch
* Nelie Nyaboke
