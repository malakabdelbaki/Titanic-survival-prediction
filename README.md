# Titanic survival prediction : using Logistic Regression
Notebook on kaggle can be found [here](https://www.kaggle.com/code/malakabdelbaki/titanic-survival-predictions)
## Data Collection

Dataset can be found [here](https://www.kaggle.com/competitions/titanic)

## Data Preprocessing

- Null values found in columns
    - Cabin : 687 null values out of 891, so column is dropped
    - Age : 177 null values out of 891, so null values are replaced by the mean age
    - Embarked : 2 null values out of 891, so null values are replaced by the mode
- Do encoding on categorical features
    - Gender
    - Embarked: S, C, or Q

### Data Analysis

- Distribution plots to explore continuous values:
    - Age
- Count plots to explore discrete values
    - Gender
    - survived
    - Gender, survived
    - Pclass
    - Pclass, survived

### Splitting features and Target

- Split the dataset to 2 arrays
    - `X` : features
    - `Y` : target
    

### Split data into training data and testing data

- `X_train, Y_train` : 80% of data to train model
- `X_test, Y_test` : 20% of data to test accuracy

### Train the model

- Train a Logistic regression model on `X_train, Y_train`

### Model Evaluation

- using accuracy_score compare the `Y_train`, with the predictions generated by the model
- Use the model to predict the cost for `X_test,` and using accuracy_score value compare the `Y_test` with the predictions generated by the model
- Accuracy Score of testing data : 0.7709

Submitting the predictions generated by the model in the Kaggle competition, it got a **Score: 0.75837**
