Employee Attrition Prediction using Machine Learning

Project Overview
This project addresses the significant challenge of employee attrition by applying data analytics and machine learning. Utilizing a dataset of 11,906 employee records, it identifies key turnover drivers and develops predictive models to enable proactive retention strategies.

Business Problem
Employee attrition increases costs related to recruitment, training, and lost productivity. This study aims to provide organizations with a tool to identify employees at risk of leaving, allowing for timely and targeted interventions to improve talent retention.

Data
The dataset, sourced from Kaggle, contains 11,906 employee records with 23 columns. It includes demographic information (Age, Gender), job-related details (Job Role, Tenure, Income, Satisfaction), and a binary 'Attrition' target indicating if an employee 'Stayed' or 'Left'. The dataset was relatively balanced (6278 'Stayed', 5628 'Left').

Methodology
A quantitative approach was used, involving Python and its data science libraries.

Data Preprocessing: Handled inconsistent columns, applied one-hot encoding for categorical variables, and split data into 80% training / 20% testing sets with stratification.

Analytical Techniques: Two supervised machine learning algorithms were employed:

Logistic Regression: Chosen for its interpretability in binary classification.

Random Forest: Selected for its ability to capture complex, non-linear relationships.

Evaluation: Models were assessed using standard classification metrics: Accuracy, Precision, Recall, F1-Score, and AUC-ROC.

Key Findings & Results
Exploratory Data Analysis (EDA) Insights:
Work-Life Balance: Poorer work-life balance strongly correlated with higher attrition.

Job Satisfaction: Lower job satisfaction directly linked to increased attrition.

Demographics & Tenure: Employees who left were generally younger, had shorter tenures, fewer promotions, and often lower income.

Job Role: Attrition rates varied significantly across different job roles (e.g., higher in Education/Healthcare than Media/Finance/Technology).

Model Performance Metrics:
Logistic Regression emerged as the slightly superior model.

Metric

Logistic Regression

Random Forest

Accuracy

0.7443

0.7326

Precision (Predicting 'Left')

0.7483

0.7405

Recall (Identifying 'Left')

0.7763

0.7588

F1-Score

0.762

0.7495

AUC-ROC

0.8291

0.8095

The Logistic Regression model's AUC-ROC of 0.8291 indicates strong discriminatory power in distinguishing between employees likely to stay or leave.

Key Predictors (from Random Forest Feature Importance):
The most influential factors in predicting attrition were:

Distance from Home

Age

Years at Company

Monthly Income

Work-Life Balance

Job Satisfaction

Number of Promotions

[Include a screenshot of your ROC Curve here, like this: ![ROC Curve - Logistic Regression](path/to/your/roc_curve_lg.png)]
[Include a screenshot of your Feature Importance plot here, like this: ![Feature Importance Plot](path/to/your/feature_importance.png)]

Business Insights & Recommendations
This analysis provides actionable strategies for HR:

Prioritize Well-being: Implement flexible work options, manage workloads, and foster a supportive culture to improve work-life balance and job satisfaction.

Foster Career Growth: Establish clear career paths, provide skill development, mentorship, and promotion opportunities, especially for younger employees.

Tailor Interventions: Investigate challenges in high-attrition roles and develop targeted support (e.g., specialized training, job design adjustments).

Leverage Predictive Analytics: Integrate the attrition_model.pkl into HR systems for proactive risk scoring, prioritizing interventions for high-risk individuals.

Ensure Ethical Use: Maintain transparency and fairness in model implementation, avoiding discrimination and retaining human oversight.

Project Artefact
The primary output is the trained Logistic Regression model, saved as attrition_model.pkl. This model is designed to predict an employee's probability of attrition based on their attributes, serving as a vital tool for data-driven HR decisions and resource prioritization.

Future Work
Hyperparameter Optimization: Fine-tune model parameters (especially for Random Forest) using cross-validation.

Feature Engineering: Explore creating new features from existing data or integrating external datasets (e.g., economic indicators).

Alternative Algorithms: Investigate advanced models like Gradient Boosting or Neural Networks for potentially higher predictive accuracy.

Causal Inference: Employ methods to understand the causal impact of interventions.

Tools & Technologies
Python 3.10

Libraries: pandas, scikit-learn, matplotlib, seaborn

Jupyter Notebook
