# Week 3: Tech Stack Recommender
 
## Overview
A content based recommendation engine that matches a user's skills to job roles. It uses TF IDF vectorization and cosine similarity to score and rank the best fitting career paths.
 
## How it works
- Loads a dataset of job roles and their associated skills from a CSV file.
- Converts the skills text into TF IDF vectors using `TfidfVectorizer`.
- Takes at least three skills as input from the user.
- Transforms the user input into the same TF IDF vector space.
- Computes cosine similarity between the user vector and every role vector.
- Sorts roles by match score and returns the Top 3 recommendations.
## Tech Stack
- Python
- pandas
- scikit-learn
## Pipeline Steps
1. Ingestion: Load and vectorize the job roles dataset.
2. User Input: Collect at least three skills from the user.
3. Scoring: Calculate cosine similarity between user and role vectors.
4. Sorting and Filtering: Rank roles and keep the Top 3 matches.
5. Display: Print the recommended career paths with match scores.
## Cold Start Handling
If a user enters skills that do not exist in the dataset vocabulary, all similarity scores will be zero. Suggested fixes include an onboarding survey to guide skill entry or expanding the vocabulary over time.

