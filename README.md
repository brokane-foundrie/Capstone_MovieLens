MovieLens Capstone Project – Personalized Content Recommendation System
==========================================================================

Overview
--------
This capstone project demonstrates how to build a personalized content recommendation system
using the MovieLens dataset. The project involves data loading, diagnostics, merging,
aggregation, feature engineering, and modeling using Logistic Regression. The final model
predicts whether a movie is "popular" based on its average rating and the number of ratings.

Data Sources
------------
- **MovieLens 100K Dataset:**  
  - **Movies File:** A pipe-separated file (movies.csv) containing movie details. For this project,
    only the first two columns (movieId and title) are used.
  - **Ratings File:** A tab-separated file (ratings.csv) containing user ratings. The file includes
    the columns: userId, movieId, rating, and timestamp.

Methodology
-----------
1. **Data Loading & Diagnostics:**  
   - The movies file is read using a pipe (`|`) as the separator and only the necessary columns
     (movieId and title) are loaded.
   - The ratings file is read using a tab (`\t`) separator.
   - Basic diagnostics are performed (checking DataFrame shapes, data types, and unique values).

2. **Data Merging & Aggregation:**  
   - The ratings and movies DataFrames are merged on the common column `movieId`.
   - The merged DataFrame is aggregated to compute movie-level statistics:
     - **rating_mean:** The mean rating for each movie.
     - **rating_count:** The total number of ratings for each movie.

3. **Feature Engineering:**  
   - A binary target variable, `popular`, is created. A movie is marked as popular (1) if its
     average rating is equal to or greater than a threshold (set at 3.5 in this project), otherwise 0.

4. **Modeling:**  
   - A Logistic Regression model is built using the aggregated features (rating_mean and rating_count).
   - The data is split into training and testing sets (with stratification to maintain class distribution).
   - The model is evaluated using accuracy, a classification report, and a confusion matrix.

How to Run the Project
----------------------
1. **File Setup:**  
   Ensure that your project folder contains the following files:
   - `movies.csv` – The movies file from the MovieLens dataset.
   - `ratings.csv` – The ratings file from the MovieLens dataset.
   - `Capstone_EDA_MovieLens.ipynb` – The Jupyter Notebook containing the full analysis.
   - `README.txt` – This file.

2. **Running the Notebook:**  
   - Open `Capstone_EDA_MovieLens.ipynb` in Google Colab or Codio.
   - Run the cells sequentially. The notebook will:
     - Mount your Google Drive (if using Colab).
     - Load and diagnose the movies and ratings data.
     - Merge and aggregate the data.
     - Create features and a target variable.
     - Train and evaluate the Logistic Regression model.
   - Review the outputs and diagnostic plots to understand the data and model performance.

Project Structure
-----------------
MovieLensCapstone/
  |-- Capstone_EDA_MovieLens.ipynb   # Jupyter Notebook with the full analysis
  |-- movies.csv                     # Movies file from the MovieLens dataset
  |-- ratings.csv                    # Ratings file from the MovieLens dataset
  |-- README.txt                     # This file

Future Work / Next Steps
------------------------
- Experiment with additional feature engineering, such as incorporating movie genres.
- Explore alternative machine learning models (e.g., Random Forest, XGBoost) for improved performance.
- Enhance visualizations and reporting for clearer insights and presentation.
# Capstone_MovieLens
Module 20 - Capstone
