#  Heart Failure Prediction - End-to-End Machine Learning Project

This project presents a complete machine learning pipeline for predicting heart failure based on clinical and demographic features. It was developed as part of my data science learning journey to practice real-world data handling, model building, and performance evaluation.

---

##  Project Objectives
- Understand the relationship between patient features and heart disease risk.
- Build reliable models to classify patients as likely to have heart disease or not.
- Compare multiple ML models and mitigate overfitting through tuning.

---

##  Dataset
- **Features:**
  - Age, Sex, ChestPainType, RestingBP, Cholesterol, FastingBS, RestingECG, MaxHR, ExerciseAngina, Oldpeak, ST_Slope
- **Target:**
  - `HeartDisease`: 1 (positive), 0 (negative)

---

##  Exploratory Data Analysis (EDA)
- Checked **class balance** (Heart disease vs Normal)
- Analyzed **categorical feature distribution**:
  - Count plots by gender, chest pain type, ECG results, exercise-induced angina, and ST slope
- Pie charts for overall proportions
- **Correlation matrix** heatmap to detect strong predictors

---

##  Data Preprocessing
- Applied **Label Encoding** for:
  - `Sex`, `ChestPainType`, `RestingECG`, `ExerciseAngina`, `ST_Slope`
- Used **train-test split** (80/20) to avoid data leakage
- **Feature Scaling** with `StandardScaler` (fit only on training set)

---

##  Models Used
### 1. Logistic Regression  
- Baseline linear classifier  
- Pros: simple and interpretable  
- Cons: limited performance on complex patterns  

### 2. Support Vector Machine (SVM)  
- Suitable for binary classification  
- Kernel trick to handle non-linear decision boundaries  

### 3. Random Forest  
- Ensemble of decision trees  
- Tuned using `max_depth=5` to reduce overfitting  

---

##  Evaluation Metrics
- **Train/Test Accuracy**
- **Mean Absolute Error (MAE)**
- **AUC Score (ROC Curve)**
- **Confusion Matrix**
- **Classification Report** (Precision, Recall, F1-score)

---

##  Final Results

| Model              | Train Accuracy | Test Accuracy | MAE    | AUC Score |
|-------------------|----------------|---------------|--------|-----------|
| Logistic Regression | 86.1%          | 84.8%         | 0.1522 | 0.9008    |
| SVM                | 89.9%          | 86.4%         | 0.1359 | 0.9491    |
| Random Forest (tuned) | 90.5%      | 87.5%         | 0.1250 | 0.9347    |

 Best performing model: **Random Forest** (after tuning)

---

##  Tools & Technologies
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn (models, metrics, preprocessing)
- Jupyter Notebook

