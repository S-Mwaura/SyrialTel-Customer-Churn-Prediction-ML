## Machine Learning Model for Predicting Syriatel Customer Churn

### Project Overview
This project aims to help SyriaTel, a telecommunications company, predict customer churn using machine learning. The goal is to identify customers likely to discontinue services so that proactive retention strategies can be implemented.
By leveraging historical customer data, we build and evaluate classification models that help reduce churn, improve customer satisfaction, and increase business profitability.

### Business Understanding
SyriaTel is experiencing increasing customer attrition, which threatens revenue and market share. Understanding why customers leave is critical for improving retention strategies.

### Problem statement
How can SyriaTel identify customers at risk of churn early enough to take preventive action?

### Objectives:
* Identify key drivers of customer churn
* Build predictive machine learning models
* Evaluate and compare model performance
* Recommend data-driven retention strategies

### Data Understanding
* Data Source: Kaggle (Telecom Customer Churn Dataset)
* Records: 3,333 customers
* Features: 21 attributes
* Target: churn (Yes/No)
### Key Features:
* Call usage (day, evening, night, international)
* Charges and minutes
* Customer service interactions
* Subscription plan details

### Data preparation.
* No missing values or duplicates found during data cleaning
* Categorical variables encoded using one-hot encoding
* Train-test split applied
* SMOTE used to handle class imbalance
* Feature scaling applied via pipeline
* Multicollinearity reduced by removing redundant charge-related features

### Exploratory Data Analysis (EDA)
#### Target
Churn is used as the Target

#### Key Insights
* Churn is imbalanced across classes
* Strong correlation between minutes and charges (expected relationship)
* Weak correlation between most features and churn as shown:
![alt text](images/image-4.png)

Some features have skewed distribution
 - Appropriate scaling and normalization done
* Slight positive relationship between:
   - Day minutes
   - Customer service calls
   - International usage
The distribution of the target variable is shown below:
![alt text](images/image-2.png)

### Feature Engineering and Data Preprocessing
* Removed multicollinear features (charges vs minutes)
* Encoded categorical variables using one-hot encoding
* Applied SMOTE for class imbalance
* Standardized numerical features

### Modelling
The following models were trained and evaluated:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
The bar graph represents the 3 models evaluated. 
![alt text](images/image-6.png)

The ROC Curves and AUC calculations for the different models are also shown.
![alt text](images/image-7.png)

The metrics is as shown. 
![alt text](<images/Models Metrics.png>)

### The Random Forest model was selected as the best-performing model due to:
- Highest overall accuracy (91%)
- Strong F1-score (66%)
- Balanced precision and recall
- Best ROC-AUC performance

### Conclusion
Machine learning models can effectively predict customer churn at SyriaTel. The Random Forest model provides the most reliable predictions and should be used for deployment.

By focusing on key churn drivers, SyriaTel can significantly reduce customer attrition and improve long-term profitability.

### Business recommendations for Syriatel Company
1. Improve Pricing Strategy

- Offer discounts on high-usage time periods (especially daytime).

2. Enhance Customer Support

- Reduce repeated service calls through better resolution systems.

3. Customer Retention Programs

- Identify high-risk customers early and offer personalized incentives.