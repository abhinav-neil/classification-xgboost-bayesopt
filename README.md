# Classification with XGBoost and Bayesian Optimization

## Data
The dataset contains various (numeric) indicators of breast cancer, along with the diagnosis (benign or malignant). <a href="https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset"> (Source) </a> The task is to train a binary classification model to make predictions of cancer based on indicators.

## Model
We use XGBoost, augmented with hyperparameter optimization using Bayesian sampling.
Stages:
- Load breast cancer dataset
    - Cleaning & EDA
    - Visualization
- Feature engineering
    - Prepare feature and targets and drop non-informative features
    - Split into train and test sets
- Bayesian optimization
    - Define XGBoost classifier model, search space, evaluation metric & cross-validaion strategy (stratified k-fold)
    - Run optimization for n iterations to find best parameters
- Model training and analysis
    - Configure XGBoost model with best parameters and fit to train set
    - Draw tree graphs
    - Plot feature importance
- Evaluation
    - Use fitted model to make predictions on test set
    - Compute mean accuracy
    - Draw confusion matrix
