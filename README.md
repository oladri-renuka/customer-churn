# Customer Churn Prediction

Customer churn prediction is a vital task for businesses, especially in industries with subscription-based services like telecom companies. Customer churn refers to the phenomenon where customers discontinue their relationship with a company. It is a crucial metric for businesses as retaining existing customers is often more cost-effective than acquiring new ones.

This project aims to predict customer churn in a telecom company using machine learning algorithms. By identifying customers who are likely to churn, businesses can take proactive measures to retain them, such as offering incentives, improving service quality, or providing personalized offers.
Predicting churn can help businesses understand and mitigate customer attrition, thereby improving customer retention and profitability.

## Dataset

The dataset used in this project is sourced from `telecom_churn.csv`. It contains the following columns:

1. `Churn`: Binary variable indicating whether the customer churned or not.
2. `AccountWeeks`: Number of weeks the customer has been with the company.
3. `ContractRenewal`: Whether the customer renewed their contract (binary).
4. `DataPlan`: Whether the customer has a data plan (binary).
5. `DataUsage`: Amount of data used by the customer.
6. `CustServCalls`: Number of customer service calls made by the customer.
7. `DayMins`: Total minutes of day calls.
8. `DayCalls`: Total number of day calls.
9. `MonthlyCharge`: Monthly charge for the customer.
10. `OverageFee`: Overage fee charged to the customer.
11. `RoamMins`: Total minutes of roaming calls.

## Methodology

1. **Data Preprocessing**: The dataset is preprocessed by handling missing values, encoding categorical variables, and scaling numerical features.

2. **Exploratory Data Analysis (EDA)**: Exploratory data analysis is conducted to gain insights into the dataset and understand the factors influencing customer churn. Visualizations such as histograms, pair plots, and categorical plots are utilized
- Histograms: Visualize the distribution of various features in the dataset.
- Pair Plot: Explore pairwise relationships between features, differentiated by churn status.
- Pie Chart: Illustrate the overall churn ratio in the dataset.
- Categorical Plots: Analyze the relationship between churn status and categorical features such as contract renewal, data plan, and customer service calls.
- Scatter Plots: Investigate relationships between numerical features, segmented by churn status and other criteria.
- Customer Segmentation: Divide customers into segments based on usage patterns and analyze churn behavior within each segment.
- Box Plots: Compare the distribution of numerical features between churned and retained customers.

3. **Random Under-sampling**: Since the dataset is imbalanced, random under-sampling is performed to balance the classes.

4. **Model Training**: Several machine learning algorithms are trained on the preprocessed data, including:
    - Decision Tree Classifier
    - Random Forest Classifier
    - Gradient Boosting Classifier
    - K-Nearest Neighbors Classifier

5. **Model Evaluation**: The performance of each model is evaluated using confusion matrices, classification reports, and ROC curves. Additionally, the area under the ROC curve (AUC) is calculated to measure the models' discriminatory power.

## Results

- **Decision Tree Classifier**: Achieved an accuracy of 84%, with an AUC score of 0.877.
- **Random Forest Classifier**: Achieved an accuracy of 85%, with an AUC score of 0.893.
- **Gradient Boosting Classifier**: Achieved an accuracy of 84%, with an AUC score of 0.898.
- **K-Nearest Neighbors Classifier**: Achieved an accuracy of 80%, with an AUC score of 0.860.

## Conclusion

Based on the evaluation metrics, the Gradient Boosting Classifier performs the best among the models tested, with the highest accuracy and AUC score. However, further optimization and tuning of hyperparameters could potentially improve the performance of all models.

Feel free to explore the code and experiment with different algorithms or feature engineering techniques to enhance the predictive accuracy of the churn prediction model.
