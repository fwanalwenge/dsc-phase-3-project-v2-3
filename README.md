
## PREDICTION OF SYRIATEL COMPANY CUSTOMER CHURN

![image](https://github.com/fwanalwenge/dsc-phase-3-project-v2-3/assets/134020486/3538d3d6-eccf-4a07-8021-72cc01d640b7)



### Overview
The aim of this project is to utilize machine learning to forecast the probability of customer churn for SyriaTel, a telecom company. By employing machine learning models, the project seeks to offer SyriaTel a practical plan to enhance their customer retention tactics and elevate overall customer satisfaction 


### Business Understanding
#### Business Problem
Due to heightened competition in the telecommunications industry, SyriaTel is increasingly concerned with accurately forecasting customer churn as a means to maintain a competitive edge. Customer retention is of utmost importance to the company since it is more cost-effective to keep existing customers than to acquire new ones. By leveraging data analysis and predictive analytics, SyriaTel aims to uncover trends and signals that can help them foresee customer actions and take proactive steps to minimize churn rates. Thus, SyriaTel is in search of predictive machine learning models that can anticipate whether customers are likely to churn or not. This, in turn, will enable the company to implement preemptive measures for retaining these customers. The data used for this analysis will include information about customer demographics such as location and usage patterns, including call histories and charges. It is essential for SyriaTel to continually adapt and update its models to keep pace with evolving customer behavior and changes in the market landscape to ensure the effectiveness of their customer retention strategies.

#### Methodology
This project strictly follows the CRISP-DM framework, which provides a structured path encompassing phases like comprehension, data preparation, model development, assessment, and implementation. The project will explore a range of models, commencing with a fundamental logistic regression model and advancing to more complex alternatives such as Decision Trees and Random Forest. The performance evaluation will rely on key metrics including accuracy, precision, recall, and F1-score.

#### Objectives 
* Create machine learning models that can predict customer churn by using data to analyze customer features.
* Comparing the build machine learning models and determine the most accurate model in prediction.
* The analysis aims to identify the specific features that have a significant impact on the customer churn rate in SyriaTel, provide valuable recommendations based on the findings hence help to mitigate churn rates in the company and improve customer retention.
  
### Data Understanding 
The project utilizes historical customer data, including demographic information and transactional data of SyriaTel telecom company. This data is used to build a predictive model that can classify customers as churned or non-churned. The data has 3333 rows and 21 columns and the company is based in California USA. The colunmn tites are as follows:

- State: The state where the customer resides.
- Area code: The area code associated with the customer's phone number.
- International plan: A binary variable indicating whether the customer has an international calling plan (1) or not (0).
- Voice mail plan: A binary variable indicating whether the customer has a voicemail plan (1) or not (0).
- Number vmail messages: The number of voicemail messages the customer has.
- Total day minutes: The total number of minutes the customer used during the daytime.
- Total day calls: The total number of calls the customer made or received during the daytime.
- Total day charge: The total charges incurred by the customer for daytime usage.
- Total eve minutes: The total number of minutes the customer used during the evening.
- Total eve calls: The total number of calls the customer made or received during the evening.
- Total eve charge: The total charges incurred by the customer for evening usage.
- Total night minutes: The total number of minutes the customer used during the night.
- Total night calls: The total number of calls the customer made or received during the night.
- Total night charge: The total charges incurred by the customer for night usage.
- Total intl minutes: The total number of minutes the customer used for international calls.
- Total intl calls**: The total number of international calls the customer made.
- Total intl charge: The total charges incurred by the customer for international calls.
- Customer service calls: The number of customer service calls made by the customer.
- Churn: A binary variable indicating whether the customer has churned (1) or not (0).
- Total_calls: The total number of calls made or received by the customer across all periods (day, evening, and night).
- Total_charge: The total charges incurred by the customer across all usage periods.
- 
## Data processing 
- We checked for missing values, duplicates, categorical and numerical values to ensure that data is clean and in correct format for modelling. 
- We further removed the class imbalance from the data and standardize to make date Consistent and uniformity of modelling. 
- Hence this process. This was done to ensured that the data is valid,accurate and complete for modelling
- We also dropped the outliers that can affect the data and give wrong predictions


## Data Analysis 
We visualized several columns on churn rates, voice mail and international plan relationship with churn and calls made in United States to get more insights about our data

![image](https://github.com/fwanalwenge/dsc-phase-3-project-v2-3/assets/134020486/7fdc1d52-6d5e-41d3-a6d9-a4a122a1e53a)


- It can be seen that most of the customers are loyal to the SyrialTel company
- This is because most of the counts are false based on churn rate count 

![image](https://github.com/fwanalwenge/dsc-phase-3-project-v2-3/assets/134020486/d57a1c17-e46d-4e92-90ed-714cdc472092)

- There is not much difference between people who make international calls in terms of getting international plan.
- On average there are almost the same number of people getting international plan from the most international calls compared to the ones who do not make international calls often

![image](https://github.com/fwanalwenge/dsc-phase-3-project-v2-3/assets/134020486/ce2665fd-bfc4-43a6-98ae-af7cedd46696)

- There is more customers loyalty by Voice mail plan subscribers due to lower churn rate 
* Customers have higher rate of churn and higher probabiliy to switch from Syriatel in terms of international plan.  
* This shows that customers are more happy with voice mail than international plan.   

![image](https://github.com/fwanalwenge/dsc-phase-3-project-v2-3/assets/134020486/f6eb6f95-2a8d-474e-823e-c95ffe69629e)

- There is strong relationship betwen calls and loyalty as most people making the calls are loyal to SyriaTel company
- This shows that there is lower probalility of switching among customers. 

## Modelling

We constructed three distinct models designed to predict customer churn within Syriatel company. These models include:

1. Logistic Regression: The initial Logistic Regression model achieved an accuracy rate of 89.6% on the training data and 86.0% on the testing data. After applying cross-validation with 5 folds, the testing data accuracy improved to 86.2%, while training data accuracy slightly dropped to 89.2%.
2. Decision Tree Classifier: Another model in our arsenal, the Decision Tree Classifier, exhibited an accuracy of 88.6% on the training data and 92.5% on the testing data for predicting customer churn. After fine-tuning with grid search, the training accuracy saw an improvement to 90.4%, and testing accuracy surged to an impressive 93.6%.
3. Random Forest Model: The Random Forest model achieved an initial accuracy of 87.1% on the training data and 87.2% on the testing data. Following hyperparameter tuning, the model's accuracy significantly improved to 93.6% on the training data and 92.7% on the testing data.

Having identified the Decision Tree and Random Forest as the two best-performing models, we proceeded to fine-tune their hyperparameters using grid search. This optimization not only enhanced model performance but also mitigated the risk of overfitting, ensuring more reliable predictions.

## Evaluation 
- From the above model we concluded that decison tree is the best model for be used by SyriaTel in predicting customer churn due to its good perfomance. 
- To futher check on the model perfomance we checked drew ROC curve to check for ROC accuracy and area under the curve. Here we found the roc score for logistic regression, decision tree and random forest classifier as `0.83, 0.88` and `0.91` respectively.
- After hyperparameter tuning we picked decision tree classifier is indeed the best model for predicting customer churn in SyriaTel since its accuracy imrproved after tuning with gridsearch. 
- Random forest is a good model too but its too complex, time consuming, expensive and in this case overfitted after grid search tuning.
  
![image](https://github.com/fwanalwenge/dsc-phase-3-project-v2-3/assets/134020486/c35b99a4-e521-4e7c-909b-e9452a6c516f)

## Conclusion and Recommendation
- Decision tree classifier is the best model to be used by SyriaTel company
- From this analysis SyriaTel company will be able to achieve : 
1. Precise Customer Churn Prediction: The model's high accuracy ensures the effective identification of customers at risk of churning. This capability empowers SyriaTel to take proactive steps to retain these customers, potentially reducing attrition and associated costs.

2. Cost-Efficient Strategies: With accurate churn prediction, SyriaTel can strategically allocate resources for targeted retention efforts, such as personalized offers, loyalty programs, and improved customer service, specifically for at-risk customers. This targeted approach can lead to cost savings compared to deploying retention strategies across the entire customer base.

3. Enhanced Customer Retention: Accurate churn prediction enables the company to implement proactive measures to retain valuable customers. By addressing customer concerns, resolving issues, and providing incentives before churn occurs, SyriaTel has the opportunity to maintain a loyal customer base, potentially increasing customer satisfaction and loyalty.

4. Informed Business Strategy: Accurate churn prediction offers insights into customer behavior and patterns, enabling the company to better understand the factors contributing to churn. This information informs data-driven business decisions, including product or service enhancements, improvements in the customer experience, and targeted marketing campaigns. These strategies are designed to reduce churn and enhance customer retention.

## Next Steps
- Investigate Alternative Algorithms: Explore different machine learning algorithms to enhance churn prediction accuracy.
- Augment Data Collection: Gather additional data to boost the accuracy of churn prediction models.
- Ongoing Model Assessment and Refinement: Continuously evaluate model performance, fine-tune parameters, and maintain models to ensure their accuracy and effectiveness in predicting customer churn.
