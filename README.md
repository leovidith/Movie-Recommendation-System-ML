# Movie Recommendation System

## Overview
This project implements a movie recommendation system that predicts user ratings for movies based on various features, such as genre, runtime, and vote count. The system utilizes regression-based models to make predictions. Users can input their preferred genres and receive movie recommendations based on predicted ratings. The model is trained on a dataset that includes features like movie title, genre, runtime, release year, and vote count. The primary objective is to predict the **user score** (ratings), helping users find movies that match their preferences.

## Results

### Dataset Visualization

#### Bar Plot of `Genre` Column
The bar plot visualizes the frequency of different genres in the dataset, providing insight into the distribution of genres across the movie collection.

<img src="https://github.com/leovidith/Movie-Recommendation-System-ML/blob/main/images/barplot.png" width="1000px">

### Model Performance

The table below summarizes the performance of several regression models evaluated using **Mean Absolute Error (MAE)** and **Mean Squared Error (MSE)** on the test set.

| Model                    | MAE  | MSE  |
|--------------------------|------|------|
| Linear Regression         | 0.50 | 0.42 |
| Decision Tree Regressor   | 0.67 | 0.76 |
| Random Forest Regressor   | 0.50 | 0.41 |
| XGBoost Regressor         | 0.50 | 0.41 |
| Gradient Boosting Regressor | 0.48 | 0.39 |

## Features
- **Genre**: The genre of the movie, which can influence the predicted rating.
- **Runtime**: The total duration of the movie in minutes.
- **Vote Count**: The number of votes the movie has received.
- **Release Year**: The year the movie was released.
- **User Score**: The predicted rating for the movie, used as the target for training.

## Sprints
1. **Data Preprocessing**:
   - Cleaned and transformed the raw dataset.
   - Handled missing data and standardized numerical features.
  
2. **Model Training**:
   - Evaluated various regression models like Linear Regression, Decision Tree, Random Forest, XGBoost, and Gradient Boosting.
   - Fine-tuned model parameters to optimize performance.
  
3. **Model Evaluation**:
   - Performance evaluation based on MAE and MSE.
   - Gradient Boosting Regressor outperformed other models in predicting user ratings.

4. **Final Model**:
   - Implemented the Gradient Boosting Regressor for movie recommendations.
   - Ensured proper use of `user_score` as the target label in the training phase.

## Conclusion
The movie recommendation system predicts user ratings using regression models. After evaluating multiple models, the **Gradient Boosting Regressor** proved to be the most accurate, providing the best user score predictions. This model is used to generate movie recommendations based on the user's genre preferences. The system helps users discover movies they are likely to enjoy, enhancing their movie selection experience.
