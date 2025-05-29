# 🎓 Student Academic Behavior & Performance Analysis

> **Project Type**: Data Cleaning • Exploratory Data Analysis (EDA) • Predictive Modeling  
> **Dataset Size**: 80,000 synthetic student records  
> **Focus**: Identifying behavioral and lifestyle factors that influence GPA and exam performance.

---

## 📦 Dataset Overview

This project utilizes a **synthetic dataset** simulating academic and lifestyle behaviors of 80,000 students, capturing factors such as:

- 🎯 **Academic Behavior**: study hours, attendance, GPA, exam scores  
- 🧠 **Psychological Indicators**: stress, mental health, exam anxiety  
- 🏃‍♂️ **Lifestyle Factors**: sleep, exercise, screen time, social media use  
- 👪 **Background & Support**: family income, parental education/support, tutoring access  
- 📚 **Learning Preferences**: learning style, study environment, motivation, time management

> The dataset was generated using statistical models, Gaussian distributions, and conditional rules to reflect realistic student data.

🗂️ [Original Dataset on Kaggle](https://www.kaggle.com/datasets/aryan208/student-habits-and-academic-performance-dataset)

---

## 🧼 Data Cleaning Summary

Performed in Microsoft Excel and Python, data cleaning involved:

| Column                        | Transformation Description                                 |
|------------------------------|------------------------------------------------------------|
| `social_media_hours`         | Weekly → daily average (`÷ 7`)                             |
| `netflix_hours`              | Weekly → daily average (`÷ 7`)                             |
| `exercise_frequency`         | Weekly → daily frequency (`÷ 7`)                           |
| `exam_anxiety_score`         | Normalized from range 5–10 → 0–5                           |
| `gender`                     | Standardized to lowercase (`Male` → `male`)               |
| `part_time_job`              | Encoded to binary (`Yes` → 1, `No` → 0)                   |
| `access_to_tutoring`         | Encoded to binary (`Yes` → 1, `No` → 0)                   |
| `attendance_percentage`      | Kept as string to reflect actual percentage format         |
| `*_hours` columns            | Renamed for clarity (`*_per_day` / `*_average`)           |

Detailed steps in: `data_cleaning_notes.md`

---

## 📊 Exploratory Data Analysis

Exploration goals included:

- 📉 Correlation between habits and performance (`study_hours_per_day` vs `GPA`)
- 🧘‍♀️ Lifestyle impact (sleep, exercise, anxiety) on exam results
- 📚 External support influence (tutoring, parental support) on academic success
- 🧩 Demographics: age, gender, or major in relation to performance

Visualized using `matplotlib`, `seaborn`, and `plotly`.

---

## 🤖 Modeling Objectives

### 🔁 Regression
- **Target**: `exam_score`
- **Approach**: Predict using behavioral, psychological, and lifestyle features

### 🚦 Classification
- **Target**: `dropout_risk` (0/1)
- **Approach**: Predict risk of dropping out using stress, motivation, attendance

**Models used:**
- Linear Regression, Random Forest Regressor  
- Logistic Regression, Random Forest Classifier

---

## 🎯 Project Goals

- ✅ Create a clean, analysis-ready dataset  
- ✅ Understand behavioral and psychological drivers of performance  
- ✅ Develop machine learning models to:
  - Predict academic scores
  - Identify at-risk students
- 📈 Generate actionable insights for educational institutions

---

## 📁 Repository Structure

📦 student-performance-project
├── raw_data.csv
├── new_cleaned_data.csv
├── outlier_summary.csv
├── data_cleaning_notes.md
├── Exploratory Data Analysis (EDA).md
├── model_training.md
├── eda_notebook.ipynb
├── model_training_revised.ipynb
├── README.md


---

## 🛠️ Tools & Libraries

- Microsoft Excel (data cleaning)
- Python (Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn)
- Jupyter Notebook, Google Colab
- Git + GitHub

---

## 📓 Notebook Links

- 📓 [Exploratory Data Analysis Notebook](https://colab.research.google.com/drive/12_r25CkAcZLfnu8N0DvDLoy8YQ7XPwXp?usp=drive_link)  
- 🤖 [Model Training Notebook](https://drive.google.com/file/d/1SQUiXk6FLTwP9OjejNruoLQZBy-zTtS3/view?usp=sharing)

---

## 💼 Real-world Impact

This project can help educational institutions to:

- Detect at-risk students early
- Allocate support resources more effectively
- Improve outcomes through behavior-informed interventions

---

## 🙋 Author

This project is managed by **Rayhan Ananda Resky**.  
Feel free to contribute, raise issues, or fork for your own research and learning.
