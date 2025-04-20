# 🩺 Diabetes Prediction and Readmission Analysis

This project focuses on improving diabetes-related healthcare insights using machine learning techniques and statistical analysis. It is divided into two major tasks:
1. Predicting diabetes using logistic regression after data preprocessing and KNN imputation.
2. Analyzing hospital readmissions using the UCI diabetic readmission dataset.

---

## 📌 Objectives

- 🧠 Apply **KNN Imputation** to handle missing values in clinical features.
- 🔍 Train a **Logistic Regression** model to predict diabetes.
- 📈 Perform **exploratory analysis** on the diabetic readmission dataset.
- 💡 Identify how HbA1c measurement, medication changes, and diagnosis types influence readmission.

---

## 📁 File Structure

```plaintext
├── diabetes.csv                     # PIMA Indian Diabetes dataset
├── diabetic_data.csv               # UCI Diabetic Readmission dataset
├── diabetes_modeling.py            # Script for KNN imputation and Logistic Regression
├── readmission_analysis.py        # Script for readmission exploratory analysis
├── requirements.txt                # Python dependencies
└── README.md                       # You're here!

```
## 🧪 Task 1: Diabetes Prediction using Logistic Regression

### ✅ Steps:
1. **Replace invalid zero values** in clinical features (`Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`) with `NaN`.
2. **Apply KNN Imputation** to fill missing values using neighboring patient data.
3. **Standardize features** to normalize the input space.
4. **Encode Outcome** to `-1` (no diabetes) and `1` (diabetes).
5. **Train a Logistic Regression model** using the standardized data.

### 📊 Evaluation Metrics

| Metric        | Value   |
|---------------|---------|
| Accuracy      | 76.19%  |
| Precision     | 67.92%  |
| Recall        | 48.65%  |
| ROC AUC       | 83.59%  |

### 📉 Confusion Matrix

```lua
[[140  17]
 [ 38  36]]

```

# 🧪 Task 2: UCI Diabetic Readmission Analysis

This task uses the UCI Diabetic Dataset to analyze readmission trends based on **HbA1c test results** and **diagnosis types**.

---

## 🔍 Exploratory Analysis Performed:

1. **HbA1c Result vs Medication Change**  
   Analyzing the relationship between different HbA1c results and whether patients underwent medication changes.

2. **HbA1c Measured vs Readmission**  
   Comparing the readmission rates of patients whose HbA1c was measured versus those whose HbA1c was not measured.

3. **Stratified Readmission by Diagnosis Group**  
   Analyzing readmission rates based on primary diagnosis group and whether the HbA1c test was measured.

---

## 📊 Key Insights:

- **HbA1c > 8** was associated with a higher likelihood of medication change, indicating that patients with poorly controlled diabetes were more likely to undergo a change in treatment.
  
- **Measured HbA1c** was correlated with increased readmission, particularly in patients diagnosed with diabetes. This suggests that HbA1c measurement could be a key factor in monitoring patient health and predicting hospital readmission.

- **Diabetic patients without measured HbA1c** had a higher chance of being readmitted within 30 days, suggesting that lack of proper monitoring could increase readmission risk.

---

## 🖼️ Visualizations:

1. **Heatmaps**:  
   These heatmaps illustrate the relationship between **HbA1c results** and treatment changes as well as readmission trends. 

2. **Clustered Bar Charts**:  
   These bar charts visualize **stratified readmission rates** based on **whether HbA1c was measured** and **diagnosis groups** (such as diabetes, circulatory issues, respiratory issues, etc.).

---

## 📌 Dependencies

To run the code and generate the analysis, ensure you have the following dependencies installed:

```bash
pip install pandas numpy seaborn matplotlib

```

## 🔧 Future Enhancements

1. **Integrate Other Models**:  
   Add and compare additional machine learning models such as **Random Forest**, **Support Vector Machines (SVM)**, and **Gradient Boosting** to improve prediction accuracy and overall model performance.

2. **Handle Diagnosis Codes**:  
   Implement the handling of diagnosis codes by mapping them using external medical code systems like **ICD-10** for more accurate and interpretable diagnosis categorization.

3. **Deploy as a Web Application**:  
   Create a **web application** that allows healthcare professionals or users to input patient data through an interactive interface and receive real-time predictions and analysis.

---

## 🙌 Acknowledgements

- **UCI Machine Learning Repository**:  
   For providing the **Diabetes Readmission** dataset used in this analysis, which is crucial for understanding diabetes-related healthcare trends.

- **DEAP Library**:  
   For the powerful genetic algorithm-based optimization tool, which was utilized in optimizing certain aspects of the analysis.

- **Scikit-learn**, **Matplotlib**, **Seaborn**:  
   The backbone libraries in Python for machine learning, data analysis, and visualization, which made this entire analysis possible and efficient.
