# Student Performance Analysis (Exploratory Data Analysis Project)

## Overview

This project analyzes a dataset of 1 million students' academic performance to extract trends and insights. The dataset contains information such as weekly self-study hours, attendance percentage, class participation, total score, and final grades. The goal is to explore relationships between these factors and academic performance using Python.

---

## Dataset

- Source: [Kaggle - Student Performance Dataset](https://www.kaggle.com/kayhanh/student-performance-1-million)
- Columns:
  - `student_id` : Unique ID for each student
  - `weekly_self_study_hours` : Hours spent in self-study per week
  - `attendance_percentage` : Attendance in percentage
  - `class_participation` : Score for class participation
  - `total_score` : Total academic score
  - `grade` : Letter grade (A, B, C, etc.)

---

## What I Did

1. **Data Loading and Exploration**
   - Loaded dataset using Pandas.
   - Checked the dataset shape, column names, and types using `.shape`, `.columns`, and `.info()`.
   - Obtained statistical summary of numeric columns with `.describe()`.
   - Checked for null values and duplicate rows.

2. **Feature Engineering**
   - Converted continuous numeric features into **categorical grades** for easier analysis:
     - `attendance_percentage` → `attendance_grade`
     - `weekly_self_study_hours` → `weekly_study_grade`
     - `class_participation` → `class_participation_grade`
   - Used `pd.cut()` with defined bins and labels (F–A) to create these categorical features.

3. **Visualization**
   - Plotted **distribution of grades**.
   - Plotted **distribution of attendance, weekly study, and participation grades**.
   - Used Seaborn and Matplotlib for clear visualizations.
   - Optional extensions (for better insight):
     - Boxplots/scatterplots showing relationships between features and grades.
     - Correlation heatmaps to visualize how numeric features relate to total score.

---

## Tools Used

- Python (Pandas, NumPy)
- Data Visualization (Matplotlib, Seaborn)
- Google Colab for development

---

## Insights

- Most students are concentrated in grades B and A.
- Higher attendance percentages correspond to higher academic grades.
- Weekly self-study and class participation positively correlate with total score.
- This analysis highlights the key factors contributing to academic success.

---

## How to Run

1. Clone or download the notebook.
2. Ensure all required libraries are installed (`pandas`, `numpy`, `matplotlib`, `seaborn`).
3. Open the notebook in Google Colab or Jupyter Notebook.
4. Run all cells sequentially.

---

## Next Steps / Improvements

- Add advanced visualizations like pairplots or violin plots.
- Perform predictive modeling to predict grades using features.
- Include more datasets or merge with demographic data for richer analysis.
