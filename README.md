# Using Machine Learning to predict the risk of customer churn at BETA BANK

## PROJECT OVERVIEW

The banking company Beta Bank is experiencing customer churn, with customers closing their accounts with the bank every month. Financial analysts have found that it is cheaper to retain existing customers than to attract new ones.

We have access to data on the past behaviour of customers and on those who have cancelled their contracts with the bank.

We will develop a model that allows us to predict whether a customer will leave the bank soon. The model must obtain an `F1 metric` value of at least 0.59. In addition, we will measure the `AUC-ROC` metric.


For the development of the model we will use the `Churn` dataset and apply the following machine learning algorithms:

- Logistic Regression
- Decision Tree
- Random Forest

The overall data will be split into training, validation, and test sets. Models will be trained and fine-tuned using the training and validation sets, with the goal of optimizing hyperparameters to achieve maximum accuracy. Once the optimal hyperparameters are established, the models will be evaluated using the test set, and the one with the highest accuracy will be selected as the final model.


## STEPS:

### STEP 1: IMPORTING LIBRARIES

### STEP 2: IMPORTING DATABASES

### STEP 3: DATA EXPLORATION

### STEP 4: MODELING

### STEP 5: TEST THE MODEL

## CONCLUSION 

The initial step to fulfill Beta Bank’s request was to preprocess the data and features. Features were transformed from numerical form by using One-Hot Encoding into categorical features. Finally, all features were standardized to ensure equal importance.

Once the data was preprocessed, we observed an imbalance in the target classes: the negative class accounts for around 80% and the positive class accounts for only 20% of the data. To evaluate the performance, the Logistic Regression model was tested with the original class imbalance and the other models were trained with adjustments made to balance the class imbalance.

The best performing model was determined by training Logistic Regression, Decision Tree, and Random Forest models. Each model was trained three times, and each model type used a different method to adjust for class imbalance in the target data. The first model of each type used the parameter `class_weight='balanced'`, the second model was trained on oversampled data, and the third model was trained on undersampled data.

`The best performing model was the Random Forest` trained on `oversampled data` using a `max_depth of 14` and `n_estimators of 20`. The model was tested on the test dataset and achieved an `F1 score of 0.5931`, which meets the minimum score requirement set by Beta Bank. Therefore, this model is considered a suitable solution for Beta Bank to predict customer churn.

PROJECT BY: GIORGIO RAMIREZ QUIROZ
