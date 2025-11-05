Potato Yield Prediction – TIH Internship Project

Overview

Accurate crop yield forecasting enables better agricultural decision-making and supports improved water resource management. In this project, potato yield is predicted by analyzing reservoir and field-related parameters through a structured machine learning workflow that progresses from data cleaning to model evaluation, including advanced neural network models.

**Project Structure**
```
tih_internship_project/
├── datasets/
│   ├── merged_potato_reservoir.csv                 # Raw dataset
│   └── potato_reservior_cleaned_dataset.csv        # Cleaned dataset
├── potato_yield_prediction.ipynb                   # Full ML workflow
├── requirements.txt
└── .gitignore
```


Dataset Description

The target variable used for prediction is yield.

Raw dataset includes original agricultural and reservoir features.

Cleaned dataset includes processed features after:

Missing value handling

Data cleaning and formatting

Feature selection and preprocessing

Preprocessing Summary

Missing values handled

Categorical encoding (where applicable)

Feature scaling using StandardScaler or MinMaxScaler

Train-test split for model training and validation

Models Implemented
Classical Machine Learning Models

RandomForestRegressor 

XGBRegressor

Ensemble Model
Combined predictions from RandomForestRegressor and XGBoost using averaging

RandomForestRegressor + GridSearchCV
Hyperparameter tuning to improve baseline performance

Deep Learning Models

LSTM

Bidirectional LSTM (BiLSTM)

Evaluation

All models are evaluated using standard regression metrics:

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Root Mean Square Error (RMSE)

Coefficient of Determination (R² Score)

Model performance is also visually inspected using:

Residual/Error-based plots

Actual vs Predicted comparisons (where available)

Workflow Summary

Import and analyze data

Apply feature engineering and scaling

Train multiple ML models

Optimize using hyperparameter tuning (GridSearchCV for RFR)

Train LSTM/BiLSTM with sequential input structure

Evaluate and compare models using metrics and plots

Results

Performance metrics and model-wise comparison are recorded in the notebook cell outputs.
(Values may be updated as model improvements continue.)

Setup and Execution

Install dependencies:

pip install -r requirements.txt


Open and run the notebook:

jupyter notebook potato_yield_prediction.ipynb


Ensure dataset paths are correctly referenced based on your environment.

Future Enhancements

Improve deep learning architecture with additional layers and dropout regularization

Introduce external climatic features (rainfall, temperature, humidity)

Deploy best-performing model as an interactive web tool

Add SHAP/feature importance explanations for interpretability

Author

Varanasi Sai Madhav
B.Tech – Computer Science and Engineering (AI & ML)

