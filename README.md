# AI/Machine Learning Intern Challenge: Simple Content-Based Recommendation

# Content-Based Movie Recommendation System

This project implements a content-based recommendation system for movies using a Jupyter Notebook. The system leverages movie data (including plot summaries, genres, and other metadata) to recommend similar movies based on user input. The core method uses TF-IDF vectorization of movie content and cosine similarity to measure similarity between movies.

## Overview

The project is divided into three main parts:

1. **Loading the Dataset:**  
   The dataset is loaded from a CSV file (e.g., `sampled_movies.csv`), which is generated from the CMU Movie Summary Corpus. The CSV file contains the following fields:
   - `wikipedia_movie_id`
   - `movie_name`
   - `release_date`
   - `all_genres`
   - `overview` (plot summary)

2. **Vectorising the Text:**  
   The content (plot summaries, optionally combined with genres) is transformed into TF-IDF vectors using Scikit-learn's `TfidfVectorizer`. A custom preprocessor is used to remove generic terms (like "movie", "movies", or "film") that might disrupt the search.

3. **Recommendation with Cosine Similarity:**  
   A user query is vectorized in the same space, and cosine similarity is computed between the query vector and each movie vector. The top N movies with the highest similarity scores are returned as recommendations.

## Setup & Installation

### Prerequisites

- Python 3.7 or higher
- [Jupyter Notebook](https://jupyter.org/) installed

### Installing Dependencies

The project uses the following Python libraries:
- `pandas`
- `numpy`
- `scikit-learn`

