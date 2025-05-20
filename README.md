# 🎓 Student Academic Behavior & Performance Analysis

> **Project Type**: Data Cleaning + Exploratory Data Analysis (EDA) + Predictive Modeling  
> **Dataset Size**: 80,000 synthetic student records  
> **Focus**: Identifying behavioral and lifestyle factors that influence GPA and exam performance.

---

## 📦 Dataset Overview

This project utilizes a **synthetic dataset** simulating academic and lifestyle behaviors of 80,000 students.  
It captures multiple factors such as:

- 🎯 **Academic Behavior**: study hours, attendance, GPA, exam scores  
- 🧠 **Psychological Indicators**: stress, mental health, exam anxiety  
- 🏃‍♂️ **Lifestyle Factors**: sleep, exercise, screen time, social media use  
- 👪 **Background & Support**: family income, parental education/support, tutoring access  
- 📚 **Learning Preferences**: learning style, study environment, motivation, time management

> The dataset was generated using statistical models, Gaussian distributions, and conditional rules to reflect realistic student data.

🗂️ [Original Dataset on Kaggle](https://www.kaggle.com/datasets/aryan208/student-habits-and-academic-performance-dataset)

---

## 🧼 Data Cleaning Summary

Cleaning was performed using Microsoft Excel and involved several transformations to normalize and harmonize the data:

| Column                        | Transformation Description                                 |
|------------------------------|------------------------------------------------------------|
| `social_media_hours`         | Converted from weekly total → daily average (`÷ 7`)       |
| `netflix_hours`              | Converted from weekly total → daily average (`÷ 7`)       |
| `exercise_frequency`         | Converted from weekly total → daily frequency (`÷ 7`)     |
| `exam_anxiety_score`         | Converted from range 5–10 → 0–5 (ordinal)                  |
| `gender`                     | Lowercased for consistency (`Male` → `male`)              |
| `part_time_job`              | Encoded as binary (`Yes` → 1, `No` → 0)                   |
| `access_to_tutoring`         | Encoded as binary (`Yes` → 1, `No` → 0)                   |
| `attendance_percentage`      | Preserved as string (e.g., `88.4%`) to indicate percentage |
| `*_hours` columns            | Renamed to explicitly indicate `*_per_day` or `*_average` |

All transformations are documented in `data_cleaning_notes.md`.

---

## 📊 Exploratory Data Analysis (Planned)

The cleaned dataset will be used to explore the following:

- 📉 Correlation between habits and performance (`study_hours_per_day` vs `GPA`)
- 🧘‍♀️ Impact of lifestyle (sleep, exercise, anxiety) on exam results
- 📚 Influence of external support (tutoring, parental support) on academic success
- 🧩 Demographic analysis: Does age, gender, or major influence performance?

Visualizations will be created using Python libraries such as `matplotlib`, `seaborn`, or `plotly`.

---

## 🤖 Modeling Objectives

### 🔁 Regression Model
- **Goal**: Predict `exam_score` or `previous_gpa` based on behavior, psychology, and lifestyle factors.

### 🚦 Classification Model
- **Goal**: Predict `dropout_risk` (Yes/No) based on stress, motivation, attendance, and engagement.

Models may include:
- Linear Regression, Random Forest Regressor
- Logistic Regression, XGBoost Classifier, or Neural Networks

---

## 🎯 Project Goals

By the end of this project, we aim to:

- ✅ Build a clean, analysis-ready dataset
- ✅ Understand key drivers of student success and risk
- ✅ Develop machine learning models to:
  - Predict academic performance
  - Identify at-risk students for early intervention
- 📈 Provide actionable insights for academic institutions or educators

---

## 📁 Repository Structure

```
📦 student-performance-project
├── raw_data.csv
├── cleaned_data.csv
├── data_cleaning_notes.md
├── eda_notebook.ipynb
├── model_training.ipynb
└── README.md
```

---

## 🛠️ Tools Used

- Microsoft Excel (data cleaning)
- Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn)
- Jupyter Notebook
- Git + GitHub

---
## 📓 Notebook links


- 📓 [Exploratory Data Analysis Notebook](https://colab.research.google.com/drive/12_r25CkAcZLfnu8N0DvDLoy8YQ7XPwXp?usp=sharing)
- 🤖 [Model Training Notebook](link-to-notebook)

---

## 💼 Real-world Impact

This type of analysis can be applied in schools and universities to:

- Detect at-risk students early
- Allocate support resources more effectively
- Improve academic performance through behavior-based interventions

---

## 🙋 Author

This project is managed by Rayhan Ananda Resky.  
Feel free to contribute, suggest improvements, or fork for your own research.

