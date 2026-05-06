# student_score_prediction
ML project predicting student exam scores
# Student Score Prediction

A machine learning project that predicts student exam scores based on study-related and demographic features.

## Overview

This project uses Python, pandas, and scikit-learn to analyze student performance data and build a regression model that predicts academic scores.  
The dataset includes information such as gender, race/ethnicity, parental education level, lunch type, test preparation course, and the student's reading and writing scores.

The goal of this project is to explore how different factors relate to student performance and to use machine learning to predict math scores from the available features.

## Features

- Loads and explores the student performance dataset.
- Displays basic data inspection such as `head()` and column names.
- Prepares input features and target values for machine learning.
- Splits the dataset into training and testing sets.
- Trains a regression model using scikit-learn.
- Evaluates the model performance on test data.

## Dataset

The project uses `exam.csv`, which contains student performance data with the following columns:

- gender
- race/ethnicity
- parental level of education
- lunch
- test preparation course
- math score
- reading score
- writing score

The target variable in this project is `math score`.

## Technologies Used

- Python
- pandas
- NumPy
- scikit-learn
- Jupyter Notebook

## Project Structure

```text
student_score_prediction/
├── student_score_prediction_ML.ipynb
├── exam.csv
└── README.md
```

## How It Works

1. The dataset is loaded into a pandas DataFrame.
2. The data is inspected to understand its structure.
3. The target variable is selected as `math score`.
4. The input features are selected from the remaining useful columns.
5. The data is split into training and testing sets.
6. A regression model is trained on the training set.
7. The model is used to make predictions on the test set.
8. The predicted values are compared with the actual values to evaluate performance.

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/Chamas-cyber/student_score_prediction.git
cd student_score_prediction
```

### 2. Install the required packages

If you do not already have the required libraries installed, run:

```bash
pip install pandas scikit-learn notebook
```

### 3. Open the notebook

Open `student_score_prediction_ML.ipynb` in:

- Jupyter Notebook
- JupyterLab
- VS Code

### 4. Run the cells

Run the notebook cells from top to bottom.

## Example Workflow in the Notebook

```python
import pandas as pd

df = pd.read_csv("exam.csv")
df.head()
```

```python
y = df["math score"]
X = df[["reading score", "writing score"]]
```

```python
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
model = LinearRegression()
model.fit(X_train, y_train)
```

## Results

The model learns patterns from the dataset and attempts to predict a student's math score using the selected input features.  
The notebook can be extended with additional feature engineering, categorical encoding, and model comparison to improve prediction quality.

## Future Improvements

- Include categorical feature encoding for all non-numeric columns.
- Test additional regression models.
- Add performance metrics such as MAE, MSE, and R².
- Create visualizations for score relationships.
- Build a simple web app using Streamlit or Flask.

## Contributing

If you want to improve this project:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Open a pull request.


## Author

**Chamas-cyber**