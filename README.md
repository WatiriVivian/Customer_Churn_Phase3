# The Question we were aiming to answer
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

We then choose the model with the best Recall and AUC this was the **Random Forest model**.

## Recommendation
To effectively reduce the churn rate of customers from Syria Tel, we recommend implementing the following measures:

1. Lower Total Cost of Calls: One significant factor influencing churn is the total cost of calls. By reducing the overall cost of calls for customers, especially during peak hours, you can provide them with cost-effective solutions. This strategy aims to make the service more affordable and attractive, potentially reducing the incentive for customers to switch to competitors.

2. Address Customer Service Issues: Customers who frequently contact customer service may have unresolved issues or concerns. It is crucial to prioritize addressing their problems promptly and efficiently. By providing excellent customer service and resolving issues effectively, you can improve customer satisfaction and loyalty, thereby reducing the likelihood of churn. Implementing customer feedback mechanisms and optimizing customer service processes can aid in this endeavor.

3. Encourage International Plan Adoption: Actively promoting and incentivizing customers to join the international plan can help reduce churn. By offering attractive features, such as discounted international calling rates or inclusive international minutes, you can encourage more customers to opt for the international plan. This strategy not only increases customer retention but also enhances revenue from international calling services.

4. Lower International Call Costs: High call costs for international calls can significantly contribute to customer churn. Lowering the rates for international calls or introducing cost-effective international calling packages can make Syria Tel a more appealing choice for customers who frequently engage in international communication. This measure aims to retain customers by providing competitive pricing and reducing the incentive to switch to other service providers.

It is important to monitor the effectiveness of these measures through ongoing analysis of churn rates, customer feedback, and market trends. Regularly evaluating and adapting these strategies based on customer needs and preferences will help optimize retention efforts and reduce churn effectively. Additionally, providing personalized offers, loyalty programs, and targeted marketing campaigns can further contribute to improving customer satisfaction and loyalty.
