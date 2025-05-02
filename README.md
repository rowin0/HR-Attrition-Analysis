# HR Attrition Analysis
Compiled by: Roxana Windsor
## Project Background and Overview
Lines Retail is a U.S.-based e-commerce company, established in 2018, specializing in office supplies and office furniture sold through its website and mobile app. Over the past two years, the company has experienced rapid growth, which may have led to unintended consequences for employees, including decreased engagement and job satisfaction. This analysis aims to examine HR attrition data and develop key metrics to help identify the underlying reasons employees are leaving the organization.

Insights and recommendations will be provided in the following key areas:
  * Attrition trends – Identifying key metrics to help leadership understand the primary reasons employees are leaving the organization.
  * Utilizing logistic regression and random forest models to predict the probability of employee attrition.
    
The Python exploratory data analysis (EDA) phase can be found [here](https://github.com/rowin0/HR-Attrition-Analysis/blob/main/P2%20EDA.pdf).\
Python-generated graphs highlighting key metrics directly correlated with attrition are available here.\
This section presents the predicted probability of employee attrition using two predictive models.

## Data structure
The EDA process typically begins by loading the necessary libraries for data manipulation, visualization, preprocessing, and modeling, we also load Attrition csv.file and take a look at the data. 
![image](https://github.com/user-attachments/assets/96f3266b-7087-4122-979f-54b708ba9044)

## Executive summary
#### Metrics directly correlated with Attrition 
Lines Retail attrition counts show that 83.9% of employees remain with the company, while 16.1% have left. Generally, businesses strive to maintain an attrition rate of 10% or lower. In this case, the attrition rate is moving towards 20%, which is notably higher and requires further investigation.\
![image](https://github.com/user-attachments/assets/1ae493e1-eef0-4bb9-bddc-17d8b7f229cb)\
Doing a heatmap can help us understand positive and negative correlation between Attrition and other factors in the dataset. As Attrition is a binary variable (Yes/No), the correlations can be interpreted as follows: \
•	positive correlation indicates employees more likely to leave\
•	negative correlation suggests employees, more likely to stay.\
Top negative correlations are:\
•	PerformanceRating: -0.92, indicating that high performers are more likely to stay.\
•	WorkLifeBalance: -0.71, strongly suggesting that a better work-life balance correlates with lower attrition.\
•	JobSatisfaction: -0.45, implying that higher job satisfaction leads to lower attrition.\
•	YearsWithCurrManager: -0.44, suggesting that employees with stable relationships with their managers tend to stay longer.\
On the other hand, variables such as HourlyRate, PercentSalaryHike, StandardHours, and Education do not show strong direct correlations with attrition.\
![image](https://github.com/user-attachments/assets/bf209564-dde0-422d-9a5c-95b7e77e1de4)\
Additional metrics and their correlation with attrition can be found here.

#### Predicting the probability of employee attrition
The two predictive models utilize selected features or metrics identified through Recursive Feature Elimination (RFE),a method that picks features by importance and removes the least significant ones, this increases model efficiency and performance, as can be seen here.\
![image](https://github.com/user-attachments/assets/22270582-c625-4567-97d5-9ceb53c2fd69)\

The Logistic Regression model performs well overall, achieving an accuracy of 95%. Its precision is 82%, meaning that when the model predicts an employee will leave, it's correct 82% of the time. The recall is 87%, indicating that it successfully identifies 87% of all actual attrition cases.\
The Random Forest model performs well overall, achieving an accuracy of 95%. Its precision is 79%, meaning that when the model predicts an employee will leave, it's correct 79% of the time. The recall is 90%, indicating that it successfully identifies 87% of all actual attrition cases.\

![image](https://github.com/user-attachments/assets/c2fd58ad-4d68-4239-b244-1dc47f721a96) ![image](https://github.com/user-attachments/assets/e1300ec1-0b4e-41a4-b4be-0e5665e9d711)

Using the logistic regression model, an employee data from the Attrition file was tested. In this example, was evaluated employee number 282 to estimate the probability of leaving the company. The model predicted an attrition probability of 0.98, indicating a very high risk—98% chance—that this employee may leave.

![image](https://github.com/user-attachments/assets/cad237b0-a2d8-45ea-9140-31192721557b)













