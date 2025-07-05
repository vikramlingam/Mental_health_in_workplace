# Mental Health in the Workplace: A Data-Driven Analysis of Burnout and Well-being

## Project Overview

This project explores a synthetic dataset simulating survey responses from 3,000 professionals across diverse roles and countries. The goal is to shed light on mental health trends, burnout risks, and factors influencing productivity and satisfaction in the workplace. Through comprehensive data analysis and predictive modeling, I aim to uncover key insights and suggest ways to foster a healthier work environment.

## Getting Started

### Data Loading and Initial Inspection

The first step involved loading the dataset and performing initial checks to understand its structure, data types, and identify any missing values. This foundational step is crucial for preparing the data for subsequent analysis.

### Exploratory Data Analysis (EDA)

#### Univariate Analysis

I started by examining each variable individually. For numerical features like 'Age' or 'BurnoutLevel', histograms and box plots helped visualize their distributions and identify potential outliers. For categorical features such as 'Gender' or 'Department', count plots showed the frequency of each category, providing insights into the dataset's composition.

![image](https://github.com/user-attachments/assets/8939ef86-50d9-42f5-be69-f35752f30392)

#### Bivariate Analysis

Next, I explored relationships between pairs of variables. A correlation heatmap was generated for all numerical features to quickly identify strong positive or negative linear relationships. Scatter plots were used to visualize how selected numerical features relate to key well-being indicators like 'JobSatisfaction' and 'BurnoutLevel'. For categorical features, box plots illustrated their relationship with numerical target variables, showing differences in medians and spread across groups.

![image](https://github.com/user-attachments/assets/218d2163-14e1-4f22-91b0-bb933aaad798)


![image](https://github.com/user-attachments/assets/659c0651-7ef6-4070-8300-47193dea3a09)

![image](https://github.com/user-attachments/assets/2a763b1e-db20-4e00-acb9-c2917ead7b89)

#### Multivariate Analysis

To explore relationships involving more than two variables, I created a pair plot for a subset of important numerical features, colored by 'BurnoutRisk'. This visualization provided a hint of how different groups relate across multiple factors simultaneously.

![image](https://github.com/user-attachments/assets/a07a2f6d-6384-4be6-a351-8c8b590c8186)

## Predictive Analytics

### Predicting Who is at Burnout Risk

One of my main goals was to predict `BurnoutRisk`. I trained a machine learning model (Random Forest Classifier) for this task. The model performed exceptionally well, accurately identifying employees at risk. The feature importance analysis revealed that `BurnoutLevel` was the overwhelmingly dominant predictor, suggesting a direct relationship between an employee's current burnout level and their categorized burnout risk in this dataset.

![image](https://github.com/user-attachments/assets/e2cdb8bc-a344-4db4-92e4-e6e6c1c34a37)

### Understanding What Causes Burnout (Predicting Burnout Level)

While knowing who is at burnout risk is important, I also wanted to understand *what causes* an employee's `BurnoutLevel` to be high in the first place. For this, I built another machine learning model (Random Forest Regressor) to predict the continuous `BurnoutLevel`.

Although this model didn't predict the exact burnout level with very high precision (indicated by a low R-squared), its feature importance analysis still provided valuable insights into which factors the model considered most influential. The key factors that emerged were:

* **Manager Support Score:** Highlighting the critical role of management in employee well-being.
* **Productivity Score:** Suggesting a complex interplay between perceived productivity and burnout.
* **Work-Life Balance Score:** Emphasizing its fundamental importance in preventing burnout.
* **Job Satisfaction:** A core component of employee well-being that impacts burnout.
* **Career Growth Score:** Indicating that opportunities for advancement and development contribute to lower burnout.

These findings suggest that a supportive work environment, good work-life balance, feeling productive, and having opportunities to grow are important for keeping burnout levels in check.

![image](https://github.com/user-attachments/assets/49094e0d-11b4-4f08-82e6-79b22fa90177)

## Conclusion and Next Steps

This analysis provides a robust starting point for understanding mental health in the workplace. I've seen how various factors contribute to burnout and highlighted the importance of things like manager support and work-life balance. For companies, these insights can be a guide to creating better, healthier environments for their employees.

Future work could involve looking at how these factors change over time if I had more longitudinal data, or combining these insights with real-world observations to build even more effective well-being programs.
