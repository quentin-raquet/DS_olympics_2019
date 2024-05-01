# Data Science Olympics

This repository contains the code for the Data Science Olympics competition.

## Information about the test

In this test, the `requests` dataset contains information about the requests made by group of individuals (or family) to the french emergency housing public service. A sample of the `requests` dataset corresponds to a unique request.

The goal is to predict the categorical variable `granted_number_of_nights` which represents the number of nights of emergency housing granted to a group. You can train your model on the `train_requests`, the predictions should be made for requests listed in the `test_requests` dataset.

The evaluation metric is given by the `competition_scorer` defined above. It corresponds to a weighted log-loss with weights 1, 10, 100, or 1000 if the `granted_number_of_nights` takes the value 0, 1, 2, or 3 respectively. Thus beware that you will be penalized harder for classification mistakes made on the higher labels.

Good luck!

## Dependencies

This project uses several Python libraries, including:

- pandas
- pandas-profiling
- sklearn
- nltk
- category-encoders
- lightgbm
- matplotlib
- requests
- tqdm

You can install these dependencies using Poetry, a tool for dependency management in Python.
The dependencies are listed in the [`pyproject.toml`](pyproject.toml) file.

## Usage

To get the best results, run the Jupyter notebook `best_submission.ipynb`.
This notebook includes the following steps:

1. Importing necessary libraries.
2. Setting pandas display options.
3. Loading and preprocessing the data.
4. Training the CatBoostClassifier model.
5. Making predictions and evaluating the model.

The predictions are saved in the `submissions` directory with the format `CV_catboost_{score}.csv`.
