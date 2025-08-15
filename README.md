# ✈️ Flight Delay Prediction using XGBoost (Boosting) vs Random Forest (Bagging)

## 📖 Project Overview
This project demonstrates how to predict **flight delays** using an **XGBoost Classifier** and compares its performance with the **Random Forest Classifier** from a previous project.  

The comparison highlights:
- **Random Forest** → Ensemble **Bagging** method  
- **XGBoost** → Ensemble **Boosting** method  

The workflow covers:
- Data Loading & Cleaning  
- Exploratory Data Analysis (EDA)  
- Feature Encoding  
- Model Building (XGBoost)  
- Hyperparameter Tuning (GridSearchCV)  
- Performance Comparison with Random Forest  
- Model Evaluation & Visualization  
- Model Saving for Future Use
- Comparison

---

## 📊 Dataset
The dataset consists of:
- **10,000 sampled flight records** from `Airlines.csv`  
- **Features**:
  - Airline  
  - Flight  
  - AirportFrom  
  - AirportTo  
  - DayOfWeek  
  - Time  
  - Length  
- **Target**:
  - Delay (`0` = Not Delayed, `1` = Delayed)  

---

## 📂 Project Structure
- **data/** → Raw dataset (`Airlines.csv`)  
- **outputs/**  
  - **eda/** → Plots generated during EDA  
  - **models/** → Saved XGBoost model (`xgboost.pkl`) and RandomForest model (`randomForest.pkl`) 
  - **results/** → Evaluation metrics & plots  
- **notebooks/** → Jupyter Notebooks
- **README.md** → Project documentation  

---

## 📊 Outputs
- **EDA Plots** → `outputs/eda/`  
  - Delay class distribution pie chart  
  - Distribution plots for numerical features by delay status  
  - Correlation heatmap  
  - Delays by time of day  
- **Model Evaluation** → `outputs/results/`  
  - Confusion Matrix (default & best threshold)  
  - ROC Curve  
  - Probability distribution plots  
  - **Performance Comparison Table** → XGBoost vs Random Forest  
- **Saved Model** → `outputs/models/xgboost.pkl` and `outputs/models/randomForest.pkl` 

---

## 🛠 Technologies Used
- **Python 3.x**  
- **Pandas, NumPy** – Data manipulation  
- **Matplotlib, Seaborn** – Visualization  
- **Scikit-learn** – Model evaluation  
- **XGBoost** – Gradient Boosting model  
- **Joblib** – Model persistence  

---

## 📈 Model Performance Comparison
| Metric         | Random Forest (Bagging) | XGBoost (Boosting) |
|----------------|-------------------------|--------------------|
| Accuracy       | 0.647500                | 0.631500           |
| F1 Score       | 0.562926                | 0.430008           |
| ROC-AUC        | 0.691531                | 0.695053           |

> ✅ **Conclusion:** Random Forest showed better performance than XGBoost in terms of Accuracy and F1 Score, indicating stronger balanced classification capability on this dataset. However, XGBoost achieved a slightly higher ROC-AUC, reflecting its strength in ranking and capturing complex relationships, even if that advantage did not translate into better classification performance at the default threshold.

