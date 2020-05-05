# machine-learning-challenge
# Machine Learning Homework - Exoplanet Exploration

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, you will create machine learning models capable of classifying candidate exoplanets from the raw dataset.

In this homework assignment, we are to:

1. [Preprocess the raw data](#Preprocessing)
2. [Tune the models](#Tune-Model-Parameters)
3. [Compare two or more models](#Evaluate-Model-Performance)

- - -

## Instructions

### Preprocess the Data

* Preprocess the dataset prior to fitting the model.
* Perform feature selection and remove unnecessary features.
* Use `MinMaxScaler` to scale the numerical data.
* Separate the data into training and testing data.

### Tune Model Parameters

* Use `GridSearch` to tune model parameters.
* Tune and compare at least two different classifiers.

- - -

## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)

- - -

# Tools / Technologies
* Python 
* SVM (Machine Learning Model)
* Random forest (Machine Learning Model)

# Summary
Random Forest is better than SVM, even without GridSearchCV.
***

## **SVM**

|                | Before CV   | After CV  |
| -------------- |:-----------:| :--------:|
| Training Score | 0.85026     | 0.88777   |
| Testing Score  | 0.83898     | 0.88106   |

---

|                | precision| recall   | f1-score  | support |
| -------------- |---------:| --------:| ---------:| -------:|
| CANDIDATE      | 0.85     | 0.65     | 0.73      | 523     |
| CONFIRMED      | 0.75     | 0.87     | 0.81      | 594     |
| FALSE POS      | 0.98     | 1.00     | 0.99      | 1069    |
| micro avg      | 0.88     | 0.88     | 0.88      | 2186    |
| macro avg      | 0.86     | 0.84     | 0.84      | 2186    |
| weighted avg   | 0.88     | 0.88     | 0.88      | 2186    |

***

## **Random Forest**

|                | Before CV   | After CV  |
| -------------- |------------:| ---------:|
| Training Score | 0.99497     | 1.0       |
| Testing Score  | 0.87740     | 0.89616   |

---

|                | precision| recall   | f1-score  | support |
| -------------- |---------:| --------:| ---------:| -------:|
| CANDIDATE      | 0.84     | 0.73     | 0.78      | 523     |
| CONFIRMED      | 0.81     | 0.86     | 0.83      | 594     |
| FALSE POS      | 0.97     | 1.00     | 0.98      | 1069    |
| micro avg      | 0.90     | 0.90     | 0.90      | 2186    |
| macro avg      | 0.87     | 0.86     | 0.87      | 2186    |
| weighted avg   | 0.89     | 0.90     | 0.89      | 2186    |
