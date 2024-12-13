# Movie Recommendation System

## Abstract

This program implements a movie recommendation system that predicts user ratings for movies based on their features, such as genre, runtime, and vote count. The system uses regression-based models to make predictions, and users can input their preferred genres to receive movie recommendations based on predicted ratings. The model is trained on a dataset that includes features such as movie title, genre, runtime, release year, and vote count.

The primary objective of the system is to predict the **user score** (ratings) for movies, helping users find movies that are likely to match their preferences based on their selected genres.


## Why Did We Use Regression?

Regression models are used in this project because the task is to predict a **continuous** value—the **user score** (rating) of a movie. Unlike classification, where the outcome is discrete (like assigning a label), regression allows us to predict values on a continuous scale. 

In this case, we aim to predict ratings, which can take any value within a range, making regression an appropriate choice. We evaluated different regression models to find the one with the best performance.

## BarPlot of `Genre` column
<img src="https://github.com/leovidith/Movie-Recommendation-System-ML/blob/main/images/barplot.png" width=1000px>

## Model Performance

The table below summarizes the performance of various regression models on the test set, evaluated using **Mean Absolute Error (MAE)** and **Mean Squared Error (MSE)**.

| Model                    | MAE  | MSE  |
|--------------------------|------|------|
| Linear Regression         | 0.50 | 0.42 |
| Decision Tree Regressor   | 0.67 | 0.76 |
| Random Forest Regressor   | 0.50 | 0.41 |
| XGBoost Regressor         | 0.50 | 0.41 |
| Gradient Boosting Regressor | 0.48 | 0.39 |



## Highlighting Gradient Boosting Regressor

Among all the models tested, the **Gradient Boosting Regressor** yielded the **lowest MAE (0.48)** and **MSE (0.39)**, outperforming the other models. These metrics suggest that the Gradient Boosting Regressor provides the most accurate predictions of the user scores, making it the best choice for this movie recommendation system.


## Use of `user_score` in Both Features and Labels

We initially attempted to exclude the **`user_score`** column from the feature dataframe, but this approach led to failures in the execution of the `recommend_movie` function. Specifically, whenever we removed `user_score` from the feature set, the function would not work properly and throw errors. As a result, we decided to keep `user_score` as part of the training process, but it is **only used as the target label** during training. It is not used as a feature during prediction or recommendation.


## Conclusion

The movie recommendation system leverages various regression models to predict user ratings and recommend movies based on the user's preferred genres. After testing multiple models, we found that the **Gradient Boosting Regressor** provided the best performance in terms of accuracy. This model is now used to generate recommendations based on the user's input.

By accurately predicting the user score for movies, the system helps users discover movies they may enjoy, improving their overall experience with movie selection.

