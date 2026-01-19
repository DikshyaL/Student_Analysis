# Student Performance Analysis & Grade Prediction (EDA + Machine Learning)

## Overview

This project analyzes a dataset of 1 million students' academic records to uncover patterns influencing academic performance and to predict student grades using machine learning. The project combines exploratory data analysis (EDA), feature engineering, data visualization, and supervised learning to understand and model student outcomes.

---

## Dataset

- **Source:** [Kaggle – Student Performance Dataset](https://www.kaggle.com/kayhanh/student-performance-1-million)
- **Size:** 1,000,000 records

### Columns
- `student_id` – Unique identifier for each student  
- `weekly_self_study_hours` – Hours spent on self-study per week  
- `attendance_percentage` – Attendance rate (%)  
- `class_participation` – Participation score  
- `total_score` – Overall academic score  
- `grade` – Final grade (A, B, C, D, F)

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Loaded and inspected the dataset using Pandas.
- Analyzed dataset structure, data types, and statistical properties.
- Checked for missing values and duplicate entries.
- Explored grade distributions and performance trends.

### 2. Feature Engineering
- Converted continuous variables into categorical grades using binning:
  - `attendance_percentage` → `attendance_grade`
  - `weekly_self_study_hours` → `weekly_study_grade`
  - `class_participation` → `class_participation_grade`
- Enabled clearer categorical analysis and visualization.

### 3. Data Visualization
- Visualized grade distributions using count plots.
- Analyzed distributions of attendance, weekly self-study, and class participation.
- Used Matplotlib and Seaborn for clear and interpretable visualizations.

### 4. Machine Learning – Grade Prediction
- Framed grade prediction as a multi-class classification problem.
- Selected features:
  - Weekly self-study hours
  - Attendance percentage
  - Class participation
- Encoded grades using `LabelEncoder`.
- Split data into training and testing sets.
- Trained a Random Forest classifier.
- Evaluated model performance using accuracy score, classification report, and confusion matrix.

### 5. Model Interpretation
- Analyzed feature importance from the Random Forest model.
- Found weekly self-study hours to be the most influential feature, followed by attendance percentage and class participation.

---

## Key Insights
- Higher self-study hours strongly correlate with better academic performance.
- Attendance plays a significant role in grade prediction.
- Class participation has a comparatively smaller impact.
- The model captures realistic academic performance patterns.

---

## Tools & Technologies
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- scikit-learn  
- Google Colab  

---

## How to Run
1. Clone or download the repository.
2. Open the notebook in Google Colab or Jupyter Notebook.
3. Install required libraries if needed:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
