
# 📊 Exploratory Data Analysis – Student Academic Behavior & Performance

This notebook presents a comprehensive exploratory data analysis (EDA) of a synthetic dataset containing academic, behavioral, and lifestyle data from 80,000 students.

---

## 🎯 Objectives

- Explore behavioral, psychological, and lifestyle factors that influence academic performance.
- Identify key relationships between features and target variables (`exam_score` and `dropout_risk`).
- Detect potential data quality issues such as outliers and encoding problems.
- Provide actionable insights that inform the modeling phase.

---

## 📂 Dataset Overview

- 📌 **Total Records**: 80,000 students
- 📈 **Features**: Academic indicators, study habits, mental health scores, lifestyle metrics, tutoring access, and demographics.
- 🧹 **Cleaning**: Conducted prior in Excel & Python, includes type normalization and feature engineering (e.g., weekly to daily conversion).

---

## 🧪 Key EDA Techniques Used

- **Univariate Analysis**: Distribution plots for all numeric features
- **Categorical Distribution**: Countplots with labels for frequency comparison
- **Correlation Analysis**: Barplots of numeric features vs `exam_score` and `dropout_risk`
- **Scatterplots**: Automated generation against both targets
- **Boxplots**: For categorical vs target variable comparisons (e.g., tutoring access, gender, part-time job)
- **Outlier Detection**: Using the Interquartile Range (IQR) method with detailed summary

---

## 🔍 Key Insights

- Students who study more than 4 hours/day tend to score higher in exams and GPA.
- Exam anxiety is **negatively correlated** with exam performance.
- Students with part-time jobs show **slightly lower** GPA and attendance.
- Access to tutoring appears **positively associated** with both GPA and exam scores.
- Gender-related performance differences are **minimal** in this dataset.
- Most students study between **2 to 5 hours per day**.
- Strong positive correlation between `exam_score` and `study_hours_per_day` as well as `access_to_tutoring`.
- Several numerical columns contain outliers that may affect model robustness.
- **Next steps** include normalization, outlier treatment, and feature selection for modeling.

---

## 📈 Visual Samples

![Example Barplot Correlation](link-to-plot1.png)  
![Example Scatterplot](link-to-plot2.png)  
> *Plots omitted here. Replace with screenshots or export if sharing publicly.*

---

## 🛠 Tools & Libraries

- Python (Pandas, NumPy, Seaborn, Matplotlib)
- `missingno` for missing value visualization
- Jupyter Notebook

---

## 🔄 Next Steps

- Develop regression and classification models based on identified key features.
- Apply normalization and encoding strategies.
- Perform model evaluation and hyperparameter tuning.

---

## 🙋 Author

Exploratory analysis by **Rayhan Ananda Resky**  
Feel free to open issues, submit suggestions, or fork this project for your own use.

---

## 🧠 Bonus Tip

To use this notebook for your own dataset:
- Replace `cleaned_data.csv` with your own file.
- Adjust target variables in the correlation and scatterplot section.
- Update insights based on your specific context.
