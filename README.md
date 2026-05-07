# Titanic Survival Prediction using Machine Learning

A beginner-friendly Machine Learning project based on the famous Titanic Survival Prediction competition. This project uses Python, Pandas, NumPy, and Scikit-Learn to clean data, preprocess features, train a Random Forest model, and generate predictions for passenger survival.

---

## Features

- Data preprocessing using Pandas
- Missing value handling
- Label encoding for categorical data
- Random Forest Classification
- Train-test split validation
- Prediction generation for Kaggle submission
- Beginner-friendly implementation

---

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-Learn

---

## Dataset

Dataset files used:
- `train.csv`
- `test.csv`
- `gender_submission.csv`

Dataset source:
[Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic)

---

## Project Workflow

### 1. Data Loading
The training and testing datasets are loaded using Pandas.

### 2. Data Exploration
Basic dataset inspection using:
- `head()`
- `info()`
- `describe()`
- `isnull().sum()`

### 3. Data Cleaning

Handled missing values:
- Filled missing `Age` values with `28`
- Filled missing `Embarked` values with `"S"`
- Dropped the `Cabin` column because of excessive missing data

### 4. Encoding

Converted categorical values into numeric form:

#### Sex Encoding
- Male → `1`
- Female → `0`

#### Embarked Encoding
- `S` → `0`
- `C` → `1`
- `Q` → `2`

---

## Feature Selection

Selected important features:

```python
features = ["Pclass", "Sex", "Age", "SibSp", "Parch", "Fare", "Embarked"]
```

---

## Model Training

Used the Random Forest Classifier:

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(
    n_estimators=100,
    random_state=42
)
```

---

## Model Evaluation

Achieved an accuracy of approximately:

```python
82.12%
```

---

## Submission File Generation

Predictions on the Kaggle test dataset are saved into:

```python
submission.csv
```

---

## Installation

Clone the repository:

```bash
git clone <your-repository-link>
```

Install required dependencies:

```bash
pip install numpy pandas scikit-learn
```

---

## Running the Project

Run using Python:

```bash
python main.py
```

Or open with Jupyter Notebook:

```bash
jupyter notebook
```

---

## Sample Imports

```python
import numpy as np
import pandas as pd

from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score
```

---

## Model Used

### Random Forest Classifier

Why Random Forest?
- Performs well on structured datasets
- Handles nonlinear relationships
- Reduces overfitting
- Easy to use for beginners
- Gives strong baseline accuracy

---

## Output

The model generates:
- Survival predictions
- Accuracy score
- Kaggle-compatible `submission.csv`

---

## Future Improvements

- Hyperparameter tuning
- Feature engineering
- Cross-validation
- Trying advanced models like:
  - XGBoost
  - LightGBM
  - CatBoost

---

## Learning Outcomes

This project helps beginners understand:
- Data preprocessing
- Machine Learning workflow
- Classification problems
- Feature engineering basics
- Model evaluation
- Kaggle competition pipelines

---

## Author

**Debjyoti Ganguly**  
CSE Undergraduate | Machine Learning Enthusiast | Developer

---

## License

This project is open-source and available under the MIT License.
