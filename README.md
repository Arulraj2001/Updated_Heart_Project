# 🫀 Heart Disease Prediction and Analysis

This project is a **Machine Learning-based Web Application** that predicts the likelihood of heart disease in patients using clinical data. It combines **data preprocessing, model training, and a Django web interface** to deliver real-time predictions and insights.

## 📌 Project Overview

- Predicts the presence of heart disease using the `Heart.csv` dataset.
- Uses **Logistic Regression**, **SVM**, and **Random Forest** models.
- Integrated into a Django web application with interactive data visualizations.
- Displays prediction results with a risk percentage and health recommendations.

## 🎯 Problem Statement

Heart disease is one of the leading causes of death globally. Early detection can save lives. This project builds a system that assists healthcare professionals by accurately predicting the risk of heart disease based on patient data.

---

## 🧠 Machine Learning Workflow

### 1. **Dataset**
- Source: `Heart.csv`
- Attributes: Age, Gender, Chest Pain Type, Cholesterol, Blood Pressure, etc.
- Target: AHD (Yes/No - indicating presence of heart disease)

### 2. **Preprocessing**
- Categorical encoding (e.g., one-hot)
- Handling missing values (median/mode imputation)
- Feature scaling (StandardScaler)
- Feature selection (SelectKBest - ANOVA F-statistics)

### 3. **Models Used**
| Model | Accuracy | F1 Score | ROC AUC |
|-------|----------|----------|---------|
| Random Forest | 86.88% | 86.66% | 93.93% |
| SVM | 88.52% | 88.13% | 96.42% |
| Logistic Regression ✅ | 88.52% | 88.13% | 96.64% |

➡️ **Selected Model:** Logistic Regression (`best_heart_disease_model.pkl`)

---

## 🌐 Web Application (Django)

### 🔧 Functional Modules

- `/predict/` – Input form for users to get heart disease risk assessment.
- `/visualizations/` – Charts: Age distribution, Gender ratio, Chest Pain, Disease by age.
- `/upload_dataset/` – Upload custom datasets for analysis.
- `/download_template/` – Download sample CSV format.

### 📁 Project Structure
heart_app/ ├── templates/ │ └── heart_app/ │ ├── home.html │ ├── predict.html │ ├── visualizations.html │ ├── upload.html ├── static/ ├── views.py ├── Heart.csv media/ └── heart_datasets/ best_heart_disease_model.pkl manage.py

yaml
Copy
Edit

---

## 📊 Tools & Technologies

| Category | Tech Used |
|----------|-----------|
| ML Framework | Scikit-learn, joblib |
| Backend | Python 3.8+, Django 4.x |
| Frontend | HTML5, CSS3, Bootstrap |
| Data | Pandas, NumPy |
| Visualization | Plotly |
| Storage | Django FileSystemStorage |

---

## 🚀 How to Run This Project Locally

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/heart-disease-predictor.git
cd heart-disease-predictor
2. Create a Virtual Environment
bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
3. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
4. Run the Server
bash
Copy
Edit
python manage.py runserver
Visit http://127.0.0.1:8000/ in your browser.

🌟 Future Enhancements
✅ SHAP/LIME-based explainability

✅ Doctor login panel to manage patient reports

✅ Real-time health monitoring dashboard

✅ Mobile responsive PWA with voice input

✅ Retraining model with new uploaded data

