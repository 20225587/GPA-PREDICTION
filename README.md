# GPA Prediction Based on Lifestyle Choices
https://github.com/20225587/GPA-PREDICTION.git
Welcome to the **GPA Prediction Based on Lifestyle Choices** project! Here, we explore how everyday choices—like sleep, study time, diet, exercise, and social activities—might be shaping students' academic performance. By predicting GPA based on lifestyle factors, we hope to provide data-driven insights for students and school management to help foster a healthier, balanced approach to academic life.

## Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Data Used](#data-used)
- [Approach](#approach)
- [Modeling and Evaluation](#modeling-and-evaluation)
- [Key Takeaways](#key-takeaways)
- [Recommendations](#recommendations)
- [Getting Started](#getting-started)
- [Future Improvements](#future-improvements)

---

## Project Overview

This project investigates how different lifestyle factors influence GPA, using machine learning to quantify and rank their impact. By analyzing patterns in habits, we can draw actionable insights to help students make lifestyle adjustments that positively affect their academic outcomes.

## Objectives

Our main goals are to:
1. Predict GPA based on students’ daily habits and lifestyle factors.
2. Identify which factors—such as sleep, study hours, exercise, diet, and social time—have the most influence on GPA.
3. Offer recommendations for schools to support students in developing balanced, GPA-boosting lifestyles.

## Data Used

The dataset captures various lifestyle factors for each student:
- **Sleep Duration** (in hours): Average hours of sleep per night.
- **Study Hours** (in hours): Average daily study time.
- **Physical Activity** (frequency): Frequency of physical exercise per week.
- **Diet Quality**: A qualitative measure of dietary habits (e.g., balanced vs. fast food-heavy).
- **Social Activity** (in hours): Time spent on socializing per day.

We use these factors to predict GPA and analyze the influence of each habit on academic performance.

## Approach

The workflow includes the following steps:

### 1. Data Exploration and Preprocessing
   - We begin by inspecting the data for missing values, outliers, and relationships between variables.
   - Missing values are handled through imputation where necessary, categorical variables (like diet quality) are converted to numeric values, and continuous variables are scaled to ensure balanced model training.

### 2. Model Selection
   - We evaluate several models:
     - **Linear Regression**: Serves as our baseline model, offering insights into straightforward relationships between lifestyle factors and GPA.
     - **Decision Tree Regressor**: Allows us to capture non-linear interactions within the data.
     - **XGBoost Regressor**: Known for its strong performance in predictive tasks, XGBoost boosts accuracy by combining multiple trees in a way that reduces errors and overfitting.
   
   - We also utilize **SHAP (SHapley Additive exPlanations)** values with XGBoost to better understand the influence of each lifestyle factor on GPA, providing an interpretable breakdown of feature importance.

### 3. Model Evaluation
   - We evaluate each model using:
     - **Mean Absolute Error (MAE)**: Represents the average difference between predicted and actual GPAs.
     - **Mean Squared Error (MSE)**: Penalizes larger errors, giving us insights into any significant outliers.
     - **R-squared (R²)**: Indicates how well our models explain GPA variance based on lifestyle factors.
   
   - The **XGBoost model with SHAP values** was the top-performing model, not only for its accuracy but also for its ability to reveal which factors were the most influential in GPA predictions.

## Modeling and Evaluation

Each model sheds light on the relationships between GPA and lifestyle factors. The XGBoost model, in particular, provided the best performance, with the SHAP analysis revealing that:

- **Sleep Duration** is a major predictor of GPA, with more consistent and adequate sleep linked to higher GPAs.
- **Study Hours** have a strong positive correlation with GPA, showing the importance of regular, focused study.
- **Diet Quality** and **Physical Activity** also contribute to higher GPA, suggesting that good nutrition and moderate exercise support cognitive function and learning.
- **Social Activity** has a mixed impact: while some social interaction is beneficial, excessive social time appears to correlate with lower GPA, indicating the need for balance.

## Key Takeaways

- **Sleep and Study Hours**: These are the top two factors influencing GPA. Encouraging consistent sleep patterns and steady study routines can boost academic performance.
- **Balanced Diet and Exercise**: Nutrition and physical health play a significant role in supporting cognitive abilities and focus.
- **Social Life Balance**: Moderate social activity is beneficial, but too much can detract from academic focus.

## Recommendations

Based on our findings, we recommend the following actions for school management:

1. **Wellness Programs**: Offer workshops and resources promoting sleep hygiene, balanced diets, and exercise habits.
2. **Academic Support**: Provide guidance on time management and effective study habits to help students maintain regular study schedules.
3. **Flexible Timetables**: Consider flexible schedules to support balanced lifestyles, especially during high-stress periods like exams.
4. **Extracurricular Management**: Encourage a balanced approach to extracurricular and social activities, helping students integrate academic and personal growth effectively.

## Getting Started

To get started with this project:

### 1. Clone the Repository
   ```
   git clone <repository-url>
   cd predicting-gpa-using-lifestyle-factors
   ```

### 2. Install Dependencies
   ```
   pip install -r requirements.txt
   ```

### 3. Run the Project
   Open the Jupyter Notebook and run the analysis:
   ```
   jupyter notebook predicting-gpa-using-lifestyle-factors.ipynb
   ```

## Requirements

The project requires these Python libraries:
- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`
- `xgboost`
- `shap`

Install them with:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn xgboost shap
```

## Future Improvements

To expand this analysis, future work could include:
- **Incorporating Additional Factors**: Include factors like mental health, screen time, or financial stress for a more holistic view of influences on GPA.
- **Longitudinal Data Analysis**: Study lifestyle factor impacts over time to see how changes in habits affect GPA in the long run.
- **Testing More Models**: Try other machine learning models like Gradient Boosting Machines (GBMs) and Support Vector Machines (SVMs) for potential improvements in accuracy.

---
