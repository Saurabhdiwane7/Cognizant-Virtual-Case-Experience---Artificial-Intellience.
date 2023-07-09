# Cognizant-Virtual-Case-Experience---Artificial-Intellience.

First Of, I would like to thank [Forage](https://www.theforage.com/) and [PWC Switzerland](https://www.pwc.ch/en.html) for this excellent virtual case experience program.

With this program i've solve a problem statement for gala groceries store with machine learning algorithms.

![l](https://i0.wp.com/themileses.com/wp-content/uploads/2018/04/straight-line.png)

## Problem Statement :

“Can we accurately predict the stock levels of products based on sales data and sensor data on an hourly basis in order to more intelligently procure products from our suppliers?”

### Task 1 = Exploratory data analysis :

Dataset : sales_data

Insights from the datasets :

• Fruit & vegetables are the 2 most frequently bought product categories 

• Non-members are the most frequent buyers within the store 

• Cash is the most frequently used payment method 

• 11am is the busiest hour with regards to number of transactions 


### Task 2 = Strategic Plan of Action

As we have mentioned in the PPT File.


### Task 3 = Feacture Engineering And Feacture Selection

Now we have the following datasets
`Sample_Sales_data`
`Sensor_stock_level`
`Sensor_storage_temperature`

Steps to be followed :

• Merge the data

• Convert timestamp with Dayofweek, hour, weekday column

• Convert all categorical columns to numeric 

• Scale the data 

### Model Building

 We will use a supervised machine learning model, and we will use `estimated_stock_pct` as the target variable, since the problem statement was focused on being able to predict the stock levels of products on an hourly basis.

Whilst training the machine learning model, we will use cross-validation, which is a technique where we hold back a portion of the dataset for testing in order to compute how well the trained machine learning model is able to predict the target variable.

Finally, to ensure that the trained machine learning model is able to perform robustly, we will want to test it several times on random samples of data, not just once. Hence, we will use a `K-fold` strategy to train the machine learning model on `K` (K is an integer to be decided) random samples of the data.

We have used `Randomforestregressor` as our machine learning algorithm  which is an instance of a Random Forest. These are powerful tree based ensemble algorithms and are particularly good because their results are very interpretable.

We are using a `regression` algorithm here because we are predicting a continuous numeric variable, that is, `estimated_stock_pct`. A `classification` algorithm would be suitable for scenarios where you're predicted a binary outcome, e.g. True/False.

We've calculated the `MAE` = mean absolute error to check and evaluate the accuracy we can see that the `mean absolute error` (MAE) is almost exactly the same each time. This is a good sign, it shows that the performance of the model is consistent across different random samples of the data, which is what we want. In other words, it shows a robust nature.

The `MAE` was chosen as a performance metric because it describes how closely the machine learning model was able to predict the exact value of `estimated_stock_pct`.

Even though the model is predicting robustly, this value for MAE is not so good, since the average value of the target variable is around 0.51, meaning that the accuracy as a percentage was around 50%. In an ideal world, we would want the MAE to be as low as possible. This is where the iterative process of machine learning comes in. At this stage, since we only have small samples of the data, we can report back to the business with these findings and recommend that the the dataset needs to be further engineered, or more datasets need to be added.

As a final note, we can use the trained model to intepret which features were signficant when the model was predicting the target variable. We will use `matplotlib` and `numpy` to visualuse the results, so we should install and import this package.


With the help of visualization we've cam across the following insights :

• The unit price and temperature are most important for predicting the stocks

• The hour of day was also important for predicting stock.

• Temperature is also significant feacture contributing for the accuracy of the model

• With the help of additional feactures like weather and deliveries we can improve the accuracy.

To enroll this Program please Visit the Forage Link!

