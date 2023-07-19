# BUSINESS UNDERSTANDING
This project aims to develop a predictive model that can help SyriaTel identify all the customers that they are at risk of losing. By analyzing customer data, including demographics, usage patterns, complaints, and billing records, we hope to uncover patterns and factors that contribute to churn.

#### * objectives
   The following were the main objectives we sort about fulfilling to allow us to answer our business question
        1. To check how the frequency of customer service calls affects the churning rate
        2. To check how the total cost affects the customers
        3. To check how international charge affects the churning rate.

## The Data
The data used for the project can be found here(https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset).

During the data cleaning, and exploratory data analysis:
* We found that the data had 3333 rows and 20 columns
* The data did not contain any missing data, duplicates, or placeholders for missing data.
* Because the data was binary, it was not feasible to look for outliers.


## Data Preprocessing and Modelling
During the exploratory data analysis, we realised that these columns had a high correlation:

* **Total day minutes & Total day charge** - correlation 1 

* **Total eve minutes & Total eve charge** - correlation 1 

* **Total night minutes & Total night charge** - correlation 1

* **Total intl minutes & Total intl charge** - correlation 1 

We choose to drop these columns since they had the least to contribute to our project objective:

1. Total day minutes 
2. Total eve minutes 
3. Total night minutes 
4. Total intl minutes 

We then used the train_test_split method to divide our data into the training and testing data we need to perform our modeling.
After performing our logistic regression we realised that our data was imbalanced so we set about using the **SMOTE** method to create synthetic data that mirrored our data and helped balance it thus allowing us to model our data better.

We used four different models:
* Logistic Regression.
* Decision trees
* Random Forest
* KNearest Neighbour(KNN)
  
## Conclusion
We then choose the **Random Forest model** for the following reasons:
* High recall score of 0.83: The model accurately identifies 83% of customers likely to
  churn, aligning with our objective of effective churn mitigation.
* Accuracy score of 0.94: The model correctly predicts churn cases with 94% accuracy
  providing reliable insights for decision-making.
* Balanced F1 score of 0.81: The model strikes a good balance between precision and recall,
 accurately identifying churn cases while minimizing false positives and false negatives
* (AUC score: 0.897290): The model effectively distinguishes between customers likely to churn
  and those who are not, showcasing its ability to make informed predictions.
  
  ![download](https://github.com/WatiriVivian/Customer_Churn_Phase3/assets/118829983/2d956eac-a14b-47e3-8412-59aea6a6474c)

With this graph, we can identify the features that have the most effect on our model 


## Recommendation
To reduce customer churn at Syria Tel, implement the following measures:

1. Lower call costs: Reduce the overall cost of calls, especially during peak hours, to make the service more affordable and attractive.

2. Improve customer service: Address customer issues promptly and provide excellent customer support to enhance satisfaction and loyalty.

3. Promote international plan adoption: Incentivize customers to join the international plan with discounted rates or inclusive minutes.

4. Reduce international call costs: Lower rates for international calls or introduce cost-effective calling packages to retain customers.

Monitor the effectiveness of these measures through ongoing analysis, and adapt based on customer feedback and market trends. Consider personalized offers, loyalty programs, and targeted marketing campaigns to further improve customer satisfaction and loyalty.
