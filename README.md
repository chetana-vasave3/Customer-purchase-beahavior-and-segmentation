
# Customer_purchase_behaviour_segments



## Index

 - Objective 
 - Data Understanding
 - Dataset Descriprition
 - Exploratory Data Analysis
 - Conclusion




## Objective

Analyze customer spending patterns, payment habits, credit utilization, and other credit card-related metrics. Understanding these patterns and behaviors can help identify customer segments, predict default rates, or develop targeted marketing strategies, among other applications in the credit card industry.

## Data Understanding
The dataset appears to be related to credit card usage and customer behavior. It contains various features that describe the financial attributes and behaviors of customers..

 
 
##  Dataset Descriprition

#### Take a first look of our data
- CUST_ID: Unique identifier for each customer.
- BALANCE: The outstanding balance amount on the credit card.
- BALANCE_FREQUENCY: Frequency of balance updates, measured as the ratio of the number of times the balance was updated to the total number of transactions.
- PURCHASES: Total amount of purchases made on the credit card.
- ONEOFF_PURCHASES: Total amount of one-time purchases (not installments) made on the credit card.
- INSTALLMENTS_PURCHASES: Total amount of purchases made in installments on the credit card.
- CASH_ADVANCE: Total amount of cash advances taken from the credit card.
- PURCHASES_FREQUENCY: Frequency of purchases, measured as the ratio of the number of purchase transactions to the total number of transactions.
- ONEOFF_PURCHASES_FREQUENCY: Frequency of one-time purchases, measured as the ratio of the number of one-time purchase transactions to the total number of transactions.
- PURCHASES_INSTALLMENTS_FREQUENCY: Frequency of purchases in installments, measured as the ratio of the number of installment purchase transactions to the total number of transactions.
- CASH_ADVANCE_FREQUENCY: Frequency of cash advances, measured as the ratio of the number of cash advance transactions to the total number of transactions.
- CASH_ADVANCE_TRX: Number of cash advance transactions.
- PURCHASES_TRX: Number of purchase transactions.
- CREDIT_LIMIT: Credit limit on the credit card.
- PAYMENTS: Total amount of payments made.
- MINIMUM_PAYMENTS: Minimum amount of payments due.
- PRC_FULL_PAYMENT: Percentage of the full payment made on the credit card.
- TENURE: Number of months the customer has been a cardholder.

## Exploratory Data Analysis

 We checked for duplicate values, Missing values and Outliers in the dataset . We removes all the duplicate values from the daatset and filled missing values by using some statistical methods like mean, median and mode.Removed unwanted Columns like customer Id.we did univariate and bivariate anlysis on Numerical as well as categorical data.


 ## Kmeans Clustering algorithm


 We have used Kmens clustering algorithm to make clusters of the similar data points so that we can separate the customers segments..we made 4 clusters.the main task here was to find the appropriate value of k that is no. of clusters.. so we used Elbow method to find the no. of clusters.before that we used PCA algorithm to convert the datframe into 2D form so that the visualiztion will be easy for us.
 

 ## Training and Testing the model accuracy using Decision Tree Algorithm
 

 We used Decision Tree algorithm to check the model performance ..we devided the data into training and test sets.fit the data into Decision Tree model and calculate the performace with the help of the confusion matrix .. we used Performance metrics like precision, Recall and F1 score.finaly we got the accuracy above 90%.. After that we saved the model with the help of the joblib module.

#### joblib module: 
The joblib module is a part of the scikit-learn library and is used for efficiently storing and loading Python objects, such as machine learning models, to disk. It provides utilities for serializing Python objects into a binary format and deserializing them back into memory.
 

 After saving the model we created web application with the help of the software team in our orgnization and for that we used stremlit web frame wrok.

#### stremlit web framework

Streamlit is an open-source Python library used for building interactive web applications. It allows you to create data-driven applications and easily deploy them for others to access and interact with through a web browser. Streamlit simplifies the process of creating web interfaces for your Python scripts, making it ideal for prototyping, data exploration, and building interactive visualizations.

 #### To get started with Streamlit, you can follow these general steps:

- Install Streamlit: You can install Streamlit using pip, Anaconda, or any other preferred method.

- Create a Python script: Write your Python code that generates the content and functionality of your application. This can include data loading, preprocessing, visualization, and interaction logic.

- Use Streamlit API: Import the Streamlit library and use its API functions to define the elements and behavior of your application. You can add widgets, charts, text, and other interactive components.

- Run the Streamlit app: Execute the Streamlit command in your terminal or command prompt, pointing it to your Python script. Streamlit will start a local server and open your application in a web browser.

- Interact with the app: You can now interact with your Streamlit application through the web interface. Any changes you make to your Python script will automatically update the application in real-time.



## Conclusion

- We made the clusters of customers
- We created the model which predicts the customer cluster with the help of the selected features.
- In the web app we have to fill feature values after that model will tell us in which cluster that customer is belong to.