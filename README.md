# Sales-Prediction Project
Providing sales prediction & recommendations using the best model. The project will be a sales prediction for food items sold at various stores.

Author: 

Suhasini Tatipalli

Business problem:

The goal of this project is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales.

Data

Sales data dictionary

Item_Identifier - Item unique identifier

Item_Weight - Item weight

Item_Fat_Content - Fat content ( Low Fat or Regular )

Item_Visibility - Item visibility percentage on the shelf

Item_Type - Items sold ( Dairy, Soft Drinks, Meat, Fruits and Vegetables, Household, Baking Goods, Snack Foods, Frozen Foods, Breakfast, Health and Hygiene, Hard,  Drinks, Canned, Breads, Starchy Foods, Others, Seafood )

Item_MRP - Item price

Outlet_Identifier - Outlet unique identifier

Outlet_Establishment_Year - The year outlet established	

Outlet_Size - Size of the outlet (Small, Medium, Large )

Outlet_Location_Type - Location type (Tier 1, Tier 2, Tier 3 )

Outlet_Type - Type of outlet ( Grocery Store, Supermarket Type1, Supermarket Type2, Supermarket Type3 )

Item_Outlet_Sales - Item sales in a given outlet  

Path: /content/drive/MyDrive/Colab Notebooks/Machine Learning/Week 5/sales_predictions.csv

Methods:

1. Seaborn - Advanced Plot of Item outlet sales distribution

2. Seaborn - Multivariate exploratory visualization for Outlet sales by Item type

3. Seaborn - Multivariate visualization for Average outlet sales 

Results :

Viz 1: Sales Distribution

![image](https://user-images.githubusercontent.com/109765822/192070762-37ddc1a2-35a8-4bbb-a39f-65e33cb68868.png)

Mean Item_Outlet_Sales :$2,181.29

Median Item_Outlet_Sales :$1,794.33

Viz 2: Outlet sales by Item type 

![image](https://user-images.githubusercontent.com/109765822/192069592-a58a6cdc-64d5-4c6f-9553-9fed8641547a.png)

 The above bar graph shows that the Supermarket Type 1 sales are higher in all products compared to other outlets

 The fruites & vegetables, snack foods salses are higher than the other items on the shelf
  
 Seafood sales are low compared to all other products accross all the outlets
  
  
Viz 3: Average outlet sales

![image](https://user-images.githubusercontent.com/109765822/192069456-2700161d-c795-4e82-b3f3-ac6dba790fc8.png)

Supermarket Type3 average sales are higher than other outlets

Model:

1.Linear regression model to predict sales

Performance of the model based on r^2 is:

Train R-Squared: 0.33
Test R-Squared: 0.327

Performance of your model based on rmse is:

Train RMSE: 37.52
Train RMSE: 36.91

2. Simple regression tree model to predict sales

Performance of the regression tree model by all metrics & r^2

Training
scores: 
MAE: 22.95 
MSE: 29,760.69 
RMSE: 172.51 
R2: 0.99
Testing
scores: 
MAE: 1,189.09 
MSE: 2,818,128.61 
RMSE: 1,678.73 
R2: -0.02

The default decision tree had a much higher R^2 score on the training data than it did on the test data. This is an indication that the model is overfitting.

The model after optimization using the max_depth the performance is,

Training
scores: 
MAE: 888.40 
MSE: 1,472,257.44 
RMSE: 1,213.37 
R2: 0.50
Testing
scores: 
MAE: 890.20 
MSE: 1,492,252.84 
RMSE: 1,221.58 
R2: 0.46

3. Random forest regressor tree model to predict sales

Performance of the regression tree model by all metrics & r^2

Training
scores: 
MAE: 372.46 
MSE: 280,974.61 
RMSE: 530.07 
R2: 0.91
Testing
scores: 
MAE: 952.56 
MSE: 1,799,215.38 
RMSE: 1,341.35 
R2: 0.35

After tuning and running the model with optimized value for max_depth and with n_estimators the performance is,

Training
scores: 
MAE: 827.50 
MSE: 1,293,039.54 
RMSE: 1,137.12 
R2: 0.56
Testing
scores: 
MAE: 844.05 
MSE: 1,375,628.19 
RMSE: 1,172.87 
R2: 0.50

Recommendations:



Limitations & Next Steps:

