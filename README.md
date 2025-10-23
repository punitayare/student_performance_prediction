# Linear Regression – Student Performance Prediction

## 📌 Project Overview
This project predicts students’ **Performance Index** based on study habits, previous scores, sleep patterns, extracurricular activities, and practice intensity using **Linear Regression**. The pipeline includes data preprocessing, train-test splitting, model training, evaluation, and feature interpretation.

## 🗂 Dataset
- **Columns:**
  - `Hours Studied` – Number of hours studied daily  
  - `Previous Scores` – Score achieved in previous exams  
  - `Extracurricular Activities` – Participation in activities (Yes/No)  
  - `Sleep Hours` – Average hours of sleep per day  
  - `Sample Question Papers Practiced` – Number of practice question papers attempted  
  - `Performance Index` – Target variable representing overall performance  
- **Rows:** Large dataset (thousands of records)  
- **Source:** Internal CSV file (`your_dataset.csv`)  

## 🛠 Features & Preprocessing
1. **Numeric Features:** Standardized using `StandardScaler`  
2. **Categorical Features:** One-hot encoded (`Extracurricular Activities`)  
3. **Missing Values:** Imputed with median (numeric) or most frequent value (categorical)  

## ⚡ Implementation Steps
1. **Import and preprocess dataset** using `pandas` and `sklearn` pipelines  
2. **Split data** into train (80%) and test (20%) sets  
3. **Fit Linear Regression model** (`sklearn.linear_model.LinearRegression`)  
4. **Evaluate model** using:
   - Mean Absolute Error (MAE)  
   - Mean Squared Error (MSE)  
   - Root Mean Squared Error (RMSE)  
   - R² Score  
5. **Plot regression line**: Actual vs Predicted Performance  
6. **Interpret model coefficients** to understand feature impact  

## 📊 Model Evaluation (Example)
| Metric | Value |
|--------|-------|
| MAE    | 1.61  |
| MSE    | 4.08 |
| RMSE   | 2.02  |
| R²     | 0.9890  |

> Note: Metrics vary depending on dataset size and distribution.

## 🔹 Feature Importance
Top influential features based on regression coefficients:
1. `Hours Studied` – Positive impact on performance  
2. `Previous Scores` – Strong indicator of future performance  
3. `Sample Question Papers Practiced` – Improves exam readiness  
4. `Sleep Hours` – Balanced sleep contributes positively  

## 📈 Visualization
- Scatter plot comparing **Actual vs Predicted Performance Index**  
- Helps to visually inspect model accuracy and fit  

## 💾 Saving Predictions
- Predictions are saved to:  
`linear_regression_performance_predictions.csv`  
- Includes:  
  - Actual Performance  
  - Predicted Performance  

## 🧰 Libraries Used
- pandas, numpy, matplotlib, seaborn  
- scikit-learn (Pipeline, ColumnTransformer, LinearRegression, preprocessing, metrics)  

## 🔗 How to Run
1. Clone the repository:  
```bash
git clone https://github.com/yourusername/linear-regression-performance.git
