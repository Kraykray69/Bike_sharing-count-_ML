Bike Sharing Demand Prediction
Pipeline Approach Design:
|__ Import necessary libraries
|__ Fetch the dataset
|__ Data Preprocessing
    |__ Drop unnecessary columns
    |__ Separate categorical and numerical features
|__ Train and Evaluate Models
    |__ Train 5 models: Random Forest, Linear Regression, Support Vector Regressor, Decision Tree Regressor, and K-Neighbors Regressor
    |__ Evaluate models using MSE, MAE, and R2 Score
    |__ Compare metrics and select the best model
|__ Best model selected: Random Forest
|__ Save the best model pipeline for prediction
|__ Create a Gradio interface for user-friendly prediction



## Project Overview:
This project aims to predict the demand for bike rentals using a machine learning pipeline approach. The dataset contains features like temperature, humidity, windspeed, and other contextual data like time of day and weather conditions.

## Project Workflow:
1. **Import Libraries**: The necessary libraries for data manipulation, machine learning, and model evaluation are imported.
2. **Fetch the Dataset**: The dataset is fetched from the UCI Machine Learning Repository (ID: 275) using `fetch_ucirepo()`.
3. **Data Preprocessing**:
   - Unnecessary columns such as `instant` and `dteday` are dropped.
   - Features are separated into categorical and numerical for efficient preprocessing.
4. **Model Training & Evaluation**:
   - **Models used**: 
     - Random Forest
     - Linear Regression
     - Support Vector Regressor
     - Decision Tree Regressor
     - K-Neighbors Regressor
   - **Metrics used**:
     - **MSE** (Mean Squared Error)
     - **MAE** (Mean Absolute Error)
     - **R2 Score**
   - The model with the best overall performance based on evaluation metrics is selected for prediction (Random Forest in this case).
5. **Prediction Pipeline**:
   - The best model is integrated into a prediction pipeline using the `Pipeline` function from scikit-learn.
   - The pipeline preprocesses new input data and provides bike rental predictions.

6. **Gradio Interface**:
   - A simple interface built using Gradio allows users to input key features (e.g., temperature, humidity, season) and get bike demand predictions.

## Model Evaluation Results:

| Model                    | MSE          | MAE          | R2 Score  |
|---------------------------|--------------|--------------|-----------|
| Random Forest              | 1766.53      | 24.89        | 0.944     |
| Linear Regression          | 19379.83     | 104.80       | 0.388     |
| Support Vector Regressor   | 19686.60     | 89.64        | 0.378     |
| Decision Tree Regressor    | 3344.87      | 34.01        | 0.894     |
| K-Neighbors Regressor      | 2777.11      | 33.17        | 0.912     |


# Launch the project by executing the notebook or script, which will:
-Fetch and preprocess the data.
-Train and evaluate multiple models.
-Display the best-performing model based on evaluation metrics.
-Launch a Gradio interface for predictions.


## Conclusion:
The Random Forest model achieved the best performance with the highest R2 Score and lowest errors, making it the best model for predicting bike rental demand.
