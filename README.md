# **Employee retention project: README**

Predicting whether an employee will leave the company.

## **Overview:**

The goal of this Project was to find out reasons why employees might be leaving the company, and to suggest measures for HR to improve employee retention. A Dataset which included different features of an employee like average monthly hours at work, work accident, years at the company and if that employee left the company was given. After Data cleaning and Exploring was done, different Machine Learning Models were built to predict if an employee is leaving the company. From the best performing models, it could be derived that most important features for the prediction were average monthly hours and last evaluation score of the employees. 

## **Business Understanding**

High employee turnover rates have several negative consequences for a company. It reduces performance and profitability; high turnover rates increase the chance of losing good employees. (paper: https://oarep.usim.edu.my/jspui/handle/123456789/20529) Losing an employee means the company has to hire a new employee which increases hiring costs, also the new employee often can't start off at the same level the previous employee worked on, a learning phase with lower productivity is nearly always needed.

## **Data Understanding**

This Dataset is a synthetic Dataset provided by the Certificate Program, it consisted of 11991 unique employee entrys and 9 features. Included features were satisfaction level, last evaluation score, number of projects worked on, average monthly hours, years at the company, work accident, left, promoted in the last 5 years, department, and salary. The Bar chart below shows how many entries of left vs. retained employees are in the Dataset.

![image](https://github.com/johannesschoch/Employee-retention-project-Google-Advanced-Data-Analytics-Certificate-Capstone-Project-/assets/118877188/33d0de0b-57e0-406c-ae35-08693877dd4f)


the split was uneven but not too uneven to require resampling (left = 1 > 10% of Data). For the final chosen Model the feature of satisfaction level was dropped because it was a highly relevant feature in the first models but might not reveal the real causes someone is leaving the company (There would be additional research required on how to improve satisfaction level, in contrary if you know people with high working hours tend to quit more often, you can already suggest measures from that).

## **Modeling and Evaluation**

The final model chosen was a Gradient Boosting Model with parameters after hyperparameter optimisation of: 300 boosting stages, 0.01 learning rate and max depth of the tree nodes of 6. The model performet with 92,6% precision, 91,7% recall and F1 score of 92,17% on the test Dataset. In the following Graph the most important features for that model are plotted. Top features were: average mothly hours, last evaluation score and number of projects.

![image](https://github.com/johannesschoch/Employee-retention-project-Google-Advanced-Data-Analytics-Certificate-Capstone-Project-/assets/118877188/dc2ed267-f259-4c22-9d64-26b58f1de1d4)



## **Conclusion**

This model can predict which employees will leave the company quite good. And therefore, some measures can be derived if you now look at the most important features from the model. 



![image](https://github.com/johannesschoch/Employee-retention-project-Google-Advanced-Data-Analytics-Certificate-Capstone-Project-/assets/118877188/7383faef-a9e2-452a-b87d-8f64bed9c810)

This image shows the most important features in the Gradient Boosting model. Blue Dots represent employees that stayed at the company vs. orange ones that left. There are two clusters of people leaving that can be observed. People with high evaluation scores and a lot of average hours as well as people with relatively low evaluation scores and low average hours. 

recommendations derived from this are:
- Don't require employees to work long hours / reward employees that do so
- make sure evaluation score is not linked to hours worked to not frustrate people working fewer hours
- maybe reward employees also based on evaluation score

![image](https://github.com/johannesschoch/Employee-retention-project-Google-Advanced-Data-Analytics-Certificate-Capstone-Project-/assets/118877188/70c5c222-ebe7-42bb-b0da-d7c3eabf3bab)

Here the third and fourth most important feature is shown. Again, blue dots for employees that stayed and orange ones for people that left. This shows that a project count of 7 always leads to an employee leaving the company. 

recommendations derived from this are:
- capping the number of projects for employees
