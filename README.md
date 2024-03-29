# Providing data-driven suggestions for HR 

**Overview**

In this project, I analyzed a dataset and built predictive models that can provide insights to the Human Resources (HR) department of a large consulting firm.

I used different machine learning models to predict whether or not an employee will leave the company. I then compared their performance and chose the champion model for deployment

**Business Understanding**

The HR department at Salifort Motors wants to take some initiatives to improve employee satisfaction levels at the company. They collected data from employees, but now they don’t know what to do with it. They want to be provided with data-driven suggestions based on the data. They have the following question: what’s likely to make the employee leave the company?

My goals in this project are to analyze the data collected by the HR department and to build a model that predicts whether an employee will leave the company.

If we can predict employees likely to quit, it might be possible to identify factors that contribute to their leaving. Because it is time-consuming and expensive to find, interview, and hire new employees, increasing employee retention will benefit the company.

**Data Understanding**

In this [dataset](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv), there are 14,999 rows, 10 columns. The features included information on employee-reported job satisfaction levels [0–1], the score of the employee's last performance review [0–1], the number of projects the employee contributes to, the average number of hours the employee worked per month, Whether or not the employee left the company. 

The visualization below shows a stacked boxplot showing `average_monthly_hours` distributions for `number_project`, comparing the distributions of employees who stayed versus those who `left`
![images/monthly_hours_vs_#projects.png](https://github.com/RedaGrace/Providing-data-driven-suggestions-for-HR/blob/main/images/monthly_hours_vs_%23projects.png)

The scatterplot below shows the `average_monthly_hours` versus `satisfaction_level`, comparing employees who stayed versus those who `left`
![images/monthly_hours_evaluation_score.png](https://github.com/RedaGrace/Providing-data-driven-suggestions-for-HR/blob/main/images/monthly_hours_evaluation_score.png)

A stacked histogram to compare department distribution of employees who left to that of employees who didn't
![images/counts of stayed or left by department.png](https://github.com/RedaGrace/Providing-data-driven-suggestions-for-HR/blob/main/images/counts%20of%20stayed%20or%20left%20by%20department.png)

A heatmap to visualize how correlated variables are. Considering which variables we're interested in examining correlations between.
![images/heatmap.png](https://github.com/RedaGrace/Providing-data-driven-suggestions-for-HR/blob/main/images/heatmap.png)

**Modeling and Evaluation**

A random forest model comprising 300 decision trees was used to determine feature importance in who will leave the company. The plot below shows that in this random forest model, `last_evaluation`, `number_project`, `tenure`, and `overworked` have the highest importance, in that order. These variables are most helpful in predicting the outcome variable, `left`, and they are the same as the ones used by the decision tree model. The overall model performed with 94% AUC and 90% recall.
![images/feature-importances.png](https://github.com/RedaGrace/Providing-data-driven-suggestions-for-HR/blob/main/images/feature-importances.png)

**Conclusion**

This model can benefit the HR department in knowing if an employee is likely to leave the company. The model also can help to identify factors that contribute to their leaving and then the HR department will increase employee retention in the company because it is time-consuming and expensive to find, interview, and hire new employees. 
