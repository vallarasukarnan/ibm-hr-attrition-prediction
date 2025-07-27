# IBM HR Attrition Prediction Project

_A machine learning project using employee data to predict attrition and identify key retention factors._

---

## Objective  
Predict whether an employee is likely to leave the company using machine learning models and derive insights to support HR decisions.

---

## Dataset  
- **Source**: [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)  
- **Records**: 1,470 employees  
- **Target variable**: `Attrition` (`Yes` = 1, `No` = 0)

---

## Key Steps  
1. **Exploratory Data Analysis (EDA)**  
   - Visualized attrition trends by job role, age, overtime, etc.  
   - Identified imbalance in target classes (`Yes`: 237, `No`: 1233)  
2. **Data Preprocessing**  
   - Handled encoding with Label Encoding & One-Hot Encoding  
   - Scaled numerical features using StandardScaler  
3. **Imbalanced Data Handling**  
   - Applied **SMOTE** to oversample the minority class  
4. **Model Building**  
   - Logistic Regression  
   - Random Forest Classifier  
5. **Model Evaluation**  
   - Accuracy, Precision, Recall, F1-Score, Confusion Matrix  
6. **Feature Importance**  
   - Identified top predictors influencing attrition  

---

## Model Performance (on SMOTE data)  

| Model                  | Accuracy | Precision (1) | Recall (1) | F1-Score (1) |
|------------------------|----------|----------------|-------------|---------------|
| **LogisticRegression** | **85.37%** | 0.55           | **0.45**     | **0.50**       |
| RandomForestClassifier | 83.33%   | 0.46           | 0.23         | 0.31           |

> _Precision (1), Recall (1), and F1-Score (1) refer to the positive class: Attrition = Yes._

---

## Top Features Influencing Attrition  

| Feature               | Importance |
|------------------------|------------|
| StockOptionLevel       | 0.0666     |
| YearsWithCurrManager   | 0.0534     |
| YearsAtCompany         | 0.0475     |
| Age                    | 0.0466     |
| TotalWorkingYears      | 0.0449     |
| MonthlyIncome          | 0.0444     |

---

## Key Insights  
- Logistic Regression outperformed Random Forest in recall, making it more effective at catching potential attrition cases.  
- Employees with lower stock options, fewer years with their manager, or lower income are more prone to leave.  
- The model helps HR teams take proactive measures to reduce employee turnover.  

---

## Conclusion  
This model provides HR with a data-driven approach to identify employees at risk of attrition and supports strategic planning for employee engagement and retention.

---

## Future Work  
- Try more advanced models like XGBoost or Support Vector Machines (SVM)  
- Deploy the model as a web app using Flask  
- Integrate the insights into Power BI for real-time dashboards  

---

## Tools & Technologies  
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- Imbalanced-learn (SMOTE)  

---

## 📁 Project Structure

```
├── data/
│   └── HR_Employee_Attrition.csv
│
├── notebook/
│   └── IBMhr_project.ipynb
│
├── models/
│   └── Logistic_model.pkl
│
├── README.md
```


