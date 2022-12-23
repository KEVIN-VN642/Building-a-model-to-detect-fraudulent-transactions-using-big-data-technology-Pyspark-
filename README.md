# Credit-Card-Fraud-Detection-with-Pyspark

# Introduction

Consumer credit cards are a vital part of the economic infrastructure in the modern world, and are ubiquitous in usage in most countries. In the United States alone, over $3 trillion dollars moved through credit cards in 2021, with over 72% of adults having at least one credit card. 
Fraudulent transactions pose a risk to both customers and credit card companies, and their impact on the business is significant. Fraud across all customer cards worldwide is estimated to be 6.81 cents per $100 in total volume in 2020, with a total of $10.24 billion fraud losses in 2020 for the United States alone. As such, credit card companies are faced with the challenge of processing and identifying transactions as valid or fraudulent in real time to provide the best customer experience and maintain their reputation. 

The goal of our project was to build a strongly predictive machine learning classification model using Spark’s MLLib library to identify fraudulent transactions, while dealing with class imbalanced data.

# Data
The dataset we used for this project contains European cardholders’ credit card transactions, which spanned over two days of September 2013. The data can be found on [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). 
This dataset had 492 frauds out of a total of 284,807 transactions. As expected, fraud occurs a small percentage of the time, a total of 0.172% of all transactions, creating a dataset that is highly imbalanced. This presented us with a technical challenge that is realistic to a real-world scenario and different enough from the challenges we’ve faced in class assignments, making this topic that much more interesting to us.

