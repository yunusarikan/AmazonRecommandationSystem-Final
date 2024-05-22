# Amazon Recommendation System

## Overview

This project aims to develop a recommendation system for Amazon products using collaborative filtering techniques. The goal is to provide personalized product recommendations based on user ratings. The recommendation system leverages the power of the Surprise library to implement a Singular Value Decomposition (SVD) model to predict user ratings and suggest products accordingly.

## Dataset
We used from kaggle, you can go to the link by [clicking](https://www.kaggle.com/datasets/saurav9786/amazon-product-reviews) here.
The dataset used in this project is the Amazon product ratings dataset, which includes the following columns:
- userId: Unique identifier for each user.
- productId: Unique identifier for each product.
- rating: Rating given by the user to the product (typically on a scale from 1 to 5).
- timestamp: Time when the rating was given.

### Data Preprocessing

Data preprocessing involves the following steps:
1. *Loading the dataset*: The dataset is loaded into a Pandas DataFrame for analysis.
2. *Data cleaning*: Duplicate ratings are identified and removed to ensure data integrity.
3. *User-item matrix creation*: The data is transformed into a user-item matrix format, where rows represent users and columns represent products, with the cell values indicating the ratings.

## Model Development

### Collaborative Filtering

Collaborative filtering is implemented using the Surprise library. The following steps outline the model development process:

1. *Algorithm selection*: The SVD (Singular Value Decomposition) algorithm is selected for its effectiveness in handling large sparse matrices typical of recommendation systems.
2. *Data splitting*: The dataset is split into training and testing sets to evaluate model performance.
3. *Model training*: The SVD model is trained on the training set to learn user and item latent factors.
4. *Prediction*: The trained model predicts ratings for the test set, and these predictions are used to generate recommendations.

### Model Evaluation

The model's performance is evaluated using the RMSE (Root Mean Squared Error) metric, which measures the average deviation of the predicted ratings from the actual ratings. A lower RMSE indicates better model performance. Additionally, the F1 Score is calculated to balance precision and recall for a comprehensive evaluation.

## Results

The recommendation system's performance is as follows:
- *RMSE*: The model achieves an RMSE score of X.XX, indicating the accuracy of the rating predictions.
- *F1 Score*: The F1 score is calculated to provide a balanced measure of precision and recall, indicating the model's ability to correctly predict relevant products.

## Usage

To use this project, follow these steps:

1. *Clone the repository*:
    bash
    git clone https://github.com/yunusarikan/AmazonRecommandationSystem-Final.git
    cd AmazonRecommandationSystem-Final


## Conclusion

The Amazon recommendation system effectively predicts user ratings for products, providing personalized recommendations based on collaborative filtering. The use of the SVD algorithm in the Surprise library demonstrates the potential of matrix factorization techniques in recommendation systems. Future work could explore incorporating more advanced models, additional features such as user demographics or product metadata, and hybrid approaches combining collaborative and content-based filtering.

## References
- [Guide to Recommendation System](https://stratoflow.com/guide-to-recommendation-system/)
- [Movie Recommend system](https://github.com/topspinj/tmls-2020-recommender-workshop/blob/master/tutorial_walkthrough.ipynb)
- [Surprise Library Documentation](https://surprise.readthedocs.io/en/stable/)
- [Pandas Documentation](https://pandas.pydata.org/)

