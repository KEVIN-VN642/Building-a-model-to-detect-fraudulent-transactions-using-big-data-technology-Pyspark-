# Software Requirement
In order to execute this project, you need an account from Databrick platform which used for Big Data computation. A community edition of Databricks can be found [here](https://community.cloud.databricks.com/login.html). You also need knowledge about Pyspark, SQL and Python programming. Databricks allows you to execute Python, Pyspark, SQL and R on the same notebook.

#######################################################################################################################################

# Introduction

Consumer credit cards are a vital part of the economic infrastructure in the modern world, and are ubiquitous in usage in most countries. In the United States alone, over $3 trillion dollars moved through credit cards in 2021, with over 72% of adults having at least one credit card. 
Fraudulent transactions pose a risk to both customers and credit card companies, and their impact on the business is significant. Fraud across all customer cards worldwide is estimated to be 6.81 cents per $100 in total volume in 2020, with a total of $10.24 billion fraud losses in 2020 for the United States alone. As such, credit card companies are faced with the challenge of processing and identifying transactions as valid or fraudulent in real time to provide the best customer experience and maintain their reputation. 

The goal of our project was to build a strongly predictive machine learning classification model using Spark’s MLLib library to identify fraudulent transactions, while dealing with class imbalanced data.

# Data
The dataset we used for this project contains European cardholders’ credit card transactions, which spanned over two days of September 2013. The data can be found on [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). 
This dataset had 492 frauds out of a total of 284,807 transactions. As expected, fraud occurs a small percentage of the time, a total of 0.172% of all transactions, creating a dataset that is highly imbalanced. This presented us with a technical challenge that is realistic to a real-world scenario and different enough from the challenges we’ve faced in class assignments, making this topic that much more interesting to us.

# Methodology

The dataset was highly imbalanced, with 577 non-fraudulent transactions for every 1 fraudulent transaction. While this represents a hopeful reality with only a small minority of transactions being fraudulent, applying machine learning algorithms to this data in its current form would yield poor results. We used the oversampling method on the training dataset to correct for the data imbalance, which consists of synthetically duplicating fraudulent transactions, to increase the counts.I did not apply oversampling to the test dataset.
In order to perform data analysis and modeling, we chose Databricks as the working platform and leveraged Spark’s MLLib library to build our classification models. After carefully exploring the data - accounting for missing values, relationships between features and data distribution of features, I built predictive models using the training data. Various classification algorithms such as Logistic Regression, Random Forest and Gradient Boosted Tree were applied to find the best model. We used Grid Search and Cross Validation techniques to find optimal hyper-parameters for each model. 

# Modeling
The dataset was highly imbalanced, with about 99.83% of transactions being non-fraudulent. Meaning that it would be incorrect to strongly rely on accuracy to measure the success of our models, given that if our model predicted all transactions as non-fraudulent, we would have an accuracy level of 99.83%, which seems high, but wouldn’t detect any fraudulent activity. 
Given the nature of our dataset, it was more suitable to use precision, recall, f1-scores, area under ROC curve and area under PR curve to measure model performance. Recall and precision are reliable metrics to assess the predictive strength of fraud detection models.
The strongest model we built was a random forest model, which achieved a precision of 82.0% and a recall of 82.6%. Since the community version of Databricks has limited computation power, hyper-parameter tuning was challenging, with models taking hours to run. However, this model has the power to help financial institutions reduce time and workload to find fraudulent transactions and mitigate financial impacts to their customers. 

# Conclusion
Fraudulent activities aren’t going anywhere and creating strongly predictive fraud detection models is extremely important for financial institutions and their clients. With fraudsters becoming more and more imaginative, financial institutions need to heavily rely on machine learning and the advancements in big data management systems and tools to face these threats.

