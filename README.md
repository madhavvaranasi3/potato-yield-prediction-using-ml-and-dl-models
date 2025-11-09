## Potato Yield Prediction Using Machine Learning and Deep Learning Models – TIH Internship Project

## Overview
Accurate crop yield forecasting enables better agricultural decision-making and supports improved water resource management. In this project, potato yield is predicted by analyzing reservoir and field-related parameters through a structured machine learning workflow that progresses from data cleaning to model evaluation, including advanced neural network models.

---

## Project Structure
```
potato-yield-prediction-using-ML-and-DL-Models/
├── datasets/
│   ├── merged_potato_reservoir.csv                 # Raw dataset
│   └── potato_reservoir_cleaned_dataset.csv        # Cleaned dataset
├── potato_yield_prediction.ipynb                   # Full ML + DL workflow (main notebook)
├── BiLSTM Model.ipynb                              # Extended deep learning notebook (BiLSTM)
├── requirements.txt                                # Required dependencies
└── .gitignore
```

---

## Dataset Description
- The target variable used for prediction is **yield**.
- Raw dataset contains original agricultural and reservoir features.
- The cleaned dataset includes processed features after:
  - Missing value handling
  - Data cleaning and formatting
  - Feature selection and preprocessing

---

## Preprocessing Summary
- Missing values handled
- Numerical feature scaling using StandardScaler or MinMaxScaler
- Categorical handling where required
- Train-test split for model validation

---

## Models Implemented

Implemented in **potato_yield_prediction.ipynb**

### Classical Machine Learning Models
- RandomForestRegressor (baseline)
- XGBRegressor
- Ensemble Model (RandomForestRegressor + XGBRegressor)
- RandomForestRegressor with GridSearchCV for hyperparameter optimization

### Deep Learning Models
- LSTM
- Bidirectional LSTM (BiLSTM)

---

### Extended Deep Learning Notebook (BiLSTM)

A dedicated **`BiLSTM Model.ipynb`** notebook is included as part of this repository to demonstrate an **enhanced deep learning approach** for crop yield forecasting.  
This notebook specifically focuses on the **Bidirectional LSTM (BiLSTM)** architecture, incorporating **past yield values as temporal features** to strengthen sequential learning.

It serves as an **extension of the primary notebook** (`potato_yield_prediction.ipynb`), enabling deeper experimentation with time-series modeling and improved prediction accuracy.  
Key highlights include:
- Achieved **R² ≈ 0.95** on the cleaned potato reservoir dataset.  
- Implements **past-yield-integrated sequence generation (V2 approach)**.  
- Designed for **reuse on other agricultural or environmental datasets** requiring sequence-based forecasting.

---

## Evaluation
Models are evaluated using the following regression metrics:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Coefficient of Determination (R² Score)

Additional evaluation includes:
- Actual vs Predicted comparisons
- Residual/error-based visual assessment (where applicable)

---

## Workflow Summary
1. Data exploration and preprocessing  
2. Classical machine learning baselines  
3. Hyperparameter tuning for improved performance  
4. Deep learning models for sequence-driven learning  
5. Performance evaluation using metrics and visual analysis

---

## Results
Metric scores and visual outputs for each model are recorded within the notebook.  
Comparative conclusions will be refined as further improvements are made.

---

## Setup and Execution

Install dependencies:
```
pip install -r requirements.txt
```

Run the notebook:
```
jupyter notebook potato_yield_prediction.ipynb
```
Ensure dataset file paths remain consistent with repository structure.

---

**Future Enhancements**

- Improve deep learning architecture performance (regularization, tuning)
- Integrate additional climate and soil features
- Deploy best model as an interactive application with input UI
- Add model explainability using SHAP/feature importance

---

**Author**

Varanasi Sai Madhav,
B.Tech – Computer Science and Engineering (AI & ML)

