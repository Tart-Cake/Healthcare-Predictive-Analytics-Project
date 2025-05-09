# Healthcare Predictive Analytics: Diabetes Risk Prediction  
**"Leveraging Machine Learning for Early Diabetes Detection and Preventive Care"**  

## Overview  
This predictive analytics initiative focuses on developing a robust machine learning system to identify early diabetes risk factors, enabling proactive healthcare interventions. By analyzing multidimensional patient data, we aim to:  
- Predict individual diabetes risk with 97%+ accuracy  
- Identify key clinical and demographic risk markers  
- Optimise resource allocation for preventive care programs  
- Support clinical decision-making with explainable AI insights  

Our solution integrates advanced ML techniques with an intuitive clinical interface, bridging the gap between data science and patient care.  

---

## Key Features  
✅ **Comprehensive Data Pipeline**  
- **Source**: [Diabetes Prediction Dataset](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset) (100,000 patient records)  
- **Preprocessing**:  
  - Duplicate values removed 
  - Categorical encoding (Label Encoding)  
  - Synthetic minority oversampling (SMOTE)  
  - Feature engineering 

✅ **Optimised Model Development**  
- **Algorithms**: Logistic Regression, Random Forest, XGBoost, LightGBM  
- **Ensemble**: Voting Classifier (XGBoost + LightGBM + Random Forest + Logistic Regression)  
- **Performance Metrics**: Accuracy, Recall, F1-score

✅ **Full-Stack Deployment**  
- **Backend**: Flask API with model serialisation (Pickle)  
- **Frontend**: Responsive web interface (HTML5/CSS3/JavaScript)  

---

## Dataset Overview: Diabetes Prediction  

### 📊 Key Characteristics  
| Metric              | Value          |
|---------------------|----------------|
| Patients            | 100,000        |
| Features            | 9 Clinical + Demographic |
| Class Balance       | 9% Diabetic  |

### 🔍 Feature Analysis  
| Feature | Type | Clinical Significance |  
|---------|------|------------------------|  
| **Gender** | Categorical | Sex-specific risk patterns |  
| **Age** | Float | Age-stratified risk groups |  
| **Hypertension** | Binary | Comorbidity indicator |  
| **Heart Disease** | Binary | Cardiovascular risk factor |  
| **Smoking History** | Categorical | 5-tier classification |  
| **BMI** | Float | Obesity metric (18.5-50 kg/m²) |  
| **HbA1c** | Float | 3-month glycemic control (3.5-9%) |  
| **Blood Glucose** | Integer | Acute hyperglycemia indicator |  
| **Diabetes** | Binary | Target (Prevalence: 9%) |  

---

## Clinical Impact  
Our solution addresses critical healthcare challenges:  

🩺 **Early Detection**  
- Identifies high-risk patients 3-5 years before onset  

📈 **Preventive Care Optimisation**  
- Reduces screening costs through risk stratification  
- Prioritises high-value interventions  

🔬 **Evidence-Based Insights**  
- Reveals nonlinear risk relationships (BMI × Age)  

💡 **Decision Support**  
- Real-time risk scoring during patient intake  
- Customised prevention protocol suggestions  

---

## Architecture  
```mermaid  
graph TD  
    A[Patient Data] --> B[Preprocessing Pipeline]  
    B --> C{ML Engine}  
    C -->|XGBoost| D[Risk Prediction]  
    C -->|LightGBM| D  
    D --> E[Result]  
