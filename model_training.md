
# 🧠 Model Training – Student Academic Behavior & Performance

This document outlines the entire machine learning pipeline used to train models for predicting student exam scores (regression) and dropout risk (classification).

---

## 🗓 1. Load Dataset

We began by loading a cleaned dataset (`new_cleaned_data.csv`) containing 80,000 student records, including academic, behavioral, psychological, and lifestyle indicators.

Key steps:
- `df.info()` and `df.describe()` used to assess data types and distributions
- Confirmed no missing values in the dataset

---

## 🔧 2. Data Preprocessing

### One-Hot Encoding:
Categorical variables were transformed into numerical format using one-hot encoding with `drop_first=True` to prevent multicollinearity.

### Boolean Conversion:
Dummy variables returned as boolean were explicitly converted to integers (0/1) for modeling compatibility:
```python
bool_cols = df_encoded.select_dtypes(include='bool').columns
df_encoded[bool_cols] = df_encoded[bool_cols].astype(int)
```

---

## 🔍 3. Feature Selection

### For Regression (`exam_score`):
Used `f_regression` to score each feature's linear relationship with the target. Features with F-score > 5 were selected.

### For Classification (`dropout_risk`):
Used `f_classif` (ANOVA) to score each feature's relation to binary dropout risk. Features with F-score > 5 were selected.

Visualizations included top 10 features and full-feature F-score barplots.

---

## 📊 4. Train-Test Split & Scaling

Separate splits were created for regression and classification tasks using `train_test_split`. 

Standardization was applied post-split using `StandardScaler` to normalize feature scales.

---

## 🎓 5. Model Training

### Regression Models:
- Linear Regression
- Random Forest Regressor

Evaluated using:
- R² Score
- Mean Squared Error (MSE)
- Scatterplot of predicted vs actual scores

### Classification Models:
- Logistic Regression
- Random Forest Classifier

Evaluated using:
- Accuracy, Precision, Recall, F1 Score
- Classification Report
- Confusion Matrix Heatmap

---

## 📈 6. Cross-Validation

5-Fold Cross-Validation was applied to both regression and classification models using `cross_val_score()`:
- Regression: scoring='r2'
- Classification: scoring='accuracy'

Provided more stable performance estimates.

---

## 🔄 7. Model Interpretation

### Regression:
Visualized coefficients from Linear Regression to show direction and magnitude of feature influence.

### Classification:
Plotted feature importances from Random Forest Classifier to reveal key predictors of dropout risk.

---

## 🌟 8. Final Evaluation Summary

### Regression Results:
- Linear Regression: R² = ~..., MSE = ~...
- Random Forest: R² = ~..., MSE = ~...

### Classification Results:
- Logistic Regression: Accuracy = ~..., F1 Score = ~...
- Random Forest: Accuracy = ~..., F1 Score = ~...

### Insights:
- Study habits and tutoring access strongly influence exam scores.
- Stress level, anxiety, and attendance are major indicators of dropout risk.

---

## 🚀 Next Steps
- Hyperparameter tuning for better performance
- Exporting models for deployment (`.pkl`/`.joblib`)
- Integration into educational dashboards or intervention systems
