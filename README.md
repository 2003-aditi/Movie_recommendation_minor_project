# Movie_recommendation_minor_project

## Overview
This project implements a **content-based movie recommendation system** using textual features such as genres, keywords, tagline, cast, and director. By applying **TF-IDF vectorization** and **cosine similarity**, the system suggests movies similar to a user’s favorite choice.

##  Objectives
- Clean and preprocess movie data  
- Engineer combined textual features for recommendation  
- Build a similarity matrix using TF-IDF and cosine similarity  
- Provide interactive movie recommendations based on user input  

##  Dataset
- **Source**: `movies.csv` (4803 rows, 24 columns)  
- **Features Used**: Genres, Keywords, Tagline, Cast, Director  
- **Sample Entries**: Avatar, Pirates of the Caribbean sequels, Star Trek films  

##  Data Cleaning
- Removed duplicates  
- Handled missing values by filling with empty strings  
- Selected key features for recommendation  

##  Feature Engineering
- Concatenated selected features into a single `combined_features` column  
- Applied **TF-IDF Vectorizer** to convert text into numerical vectors  
- Generated a sparse matrix of shape (4803 × 17318)  

##  Model Building
- Used **Cosine Similarity** on TF-IDF vectors  
- Constructed a similarity matrix (4803 × 4803)  
- Enabled efficient retrieval of top similar movies  

##  Recommendation Logic
- User inputs a movie title (e.g., *Guardians of the Galaxy*)  
- System finds the closest match in dataset  
- Retrieves similarity scores and outputs top recommendations  

##  Example Output
For *Guardians of the Galaxy*, recommendations include:  
- Avatar  
- The Chronicles of Riddick  
- Star Trek Beyond  
- Star Trek Into Darkness  
- Moonraker  

## Tools & Technologies
- Python  
- Pandas, NumPy  
- Scikit-learn (TF-IDF, Cosine Similarity)  

