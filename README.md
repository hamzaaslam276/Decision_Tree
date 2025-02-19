# Decision Tree Classification

## Overview
This repository contains a Decision Tree Classification implementation using scikit-learn in Python. The project involves training a model to predict whether a person's salary exceeds $100,000 based on features such as company, job role, and degree level.

## Dataset
The dataset (`salaries.csv`) consists of the following columns:
- `company`: Name of the company (e.g., Google, Facebook, ABC Pharma)
- `job`: Job role (e.g., Sales Executive, Business Manager, Computer Programmer)
- `degree`: Education level (Bachelors or Masters)
- `salary_more_then_100k`: Target variable (1 if salary is more than $100,000, otherwise 0)

## Data Preprocessing
The dataset undergoes preprocessing steps, including:
1. Encoding categorical variables (`company`, `job`, and `degree`) using `LabelEncoder`.
2. Dropping original categorical columns and using the numerical encoded values.
3. Splitting the dataset into input features (`inputs_n`) and target variable (`target`).

## Model Training
- The `DecisionTreeClassifier` from `sklearn.tree` is used to train the model.
- The model is trained using all available data.
- The model achieves a perfect score (1.0) on the training set.

## Predictions
Example predictions:
- **Google, Computer Engineer, Bachelors degree** → Salary ≤ $100K (`0`)
- **Google, Computer Engineer, Masters degree** → Salary > $100K (`1`)

## Titanic Survival Prediction (Exercise)
An additional exercise is included to predict survival on the Titanic using a decision tree model.

### Dataset:
The dataset (`titanic.csv`) consists of the following columns:
- `Pclass`: Passenger class (1st, 2nd, 3rd)
- `Sex`: Gender of the passenger
- `Age`: Age of the passenger
- `Fare`: Ticket fare
- `Survived`: Target variable (1 if survived, 0 otherwise)

### Steps:
1. Unnecessary columns are dropped.
2. Missing values in the `Age` column are filled with the median.
3. `Sex` is encoded using `LabelEncoder`.
4. The dataset is split into features (`Pclass`, `Age`, `Fare`, `sex`) and target (`Survived`).
5. The `DecisionTreeClassifier` is trained on the dataset.

## Requirements
Ensure you have the following Python libraries installed:
```bash
pip install pandas scikit-learn seaborn matplotlib
```

## Usage
Run the script to train the models and make predictions:
```bash
python decision_tree_classifier.py
```

## Contributing
Feel free to fork the repository and submit pull requests for improvements or additional exercises.

## License
This project is open-source under the MIT License.

