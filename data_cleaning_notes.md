
# 🧼 Data Cleaning Notes

This document outlines the data cleaning and preprocessing steps applied to the original dataset `raw_data.csv` to produce the cleaned version `cleaned_data.csv`.

---

## ✅ General Cleaning Actions

- Verified data types and value ranges.
- Removed unnecessary inconsistencies in categorical columns.
- Standardized column names to reflect transformations applied (e.g., `_average`, `_per_day`).

---

## 🔄 Column-Specific Cleaning Steps

| Column                     | Transformation Description                                                   |
|----------------------------|-------------------------------------------------------------------------------|
| `social_media_hours`       | Converted from weekly total to **daily average** by dividing by 7.           |
| `netflix_hours`            | Converted from weekly total to **daily average** by dividing by 7.           |
| `exercise_frequency`       | Converted from weekly total to **daily fraction** (range 0–1).               |
| `exam_anxiety_score`       | Normalized from range 5–10 to **0–5** to simplify ordinal interpretation.     |
| `part_time_job`            | Converted from `Yes`/`No` to **1** (Yes) and **0** (No).                     |
| `access_to_tutoring`       | Converted from `Yes`/`No` to **1** (Yes) and **0** (No).                     |
| `gender`                   | Standardized values to lowercase (`Male` → `male`, etc.)                    |
| `attendance_percentage`    | Retained as string with `%` symbol (e.g., `88.4%`) for clarity.              |

---

## 📌 Column Renaming

| Original Column               | Renamed To                      |
|------------------------------|----------------------------------|
| `study_hours_per_day`        | `study_hours_per_day_average`    |
| `social_media_hours`         | `social_media_hours_average`     |
| `netflix_hours`              | `netflix_hours_average`          |
| `sleep_hours`                | `sleep_hours_average`            |
| `exercise_frequency`         | `exercise_frequency_weekly`      |

---

## 📝 Notes

- All changes were made using Microsoft Excel.
- No rows were deleted during cleaning.
- Dataset shape remains unchanged: **80,000 rows × 31 columns**
- `previous_gpa` values for semester 1 students were retained since all contained valid values.
- `screen_time` unit assumption: per day. No transformation applied.

---

For future processing or model training, consider:
- Normalizing numerical values.
- One-hot encoding categorical columns such as `learning_style`, `study_environment`, and `major`.

