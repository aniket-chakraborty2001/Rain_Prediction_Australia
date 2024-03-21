# Rain_Prediction_Australia
This Supervised ML project deals with Rain prediction in Australia depending on over 20 mixed type of variables. This data set is cleaned so no extra preprocessing is done. Only some feature engineering processes are used to complete the whole project

<h3>Project Data Set</h3>

In this project the data set that is used is called as **'Weather_Data'** and it is attached with the project files. To get the data, click on the below name of the data frame

[Weather_Data.csv](https://github.com/aniket-chakraborty2001/Rain_Prediction_Australia/blob/main/Weather_Data.csv)

Talking about the data set, The data set contains **3271 records (rows) and 22 features**. The columns of the data frame are of mixed type. Some are categorical and Some are continuous. The discussion of each column of the data set is given in the below picture,

<p align = 'center'>
  <img width = "500" height = "600", src = "https://github.com/aniket-chakraborty2001/Rain_Prediction_Australia/blob/main/Images/Contents.png">
</p>

In this data set, the column **RainTomorrow** is the target variable (dependent variable). The other columns excluding the column **Date** are the independent variables. The data set in hand is cleaned, so no need to check for missing values. 

<h3>Feature Engineering</h3>

The term **'Feature Engineering'** means to select and transform the data that are essential for the project. In this project, droping the **Date** column and one-hot encode the categorical columnms using **pd.get_dummies()** is something that is very interesting. To copnduct the project I converted the Yes and No entries of the target column with values 1 and 0 respectively. In the last part, I converted the type of all the columns of the data frame into float using the **.astype(float)** method

<h3>Machine Learning Models</h3>

In this project, I try to fit the data in a Machine Learning Algorithm and try to predict the future values depending on the best models. The ML techniques that are used here are - 

* Linear Regression
* Logistics Regression
* K-Nearest Neighbors Classification
* Decision Tree Classification
* Support Vector Machine (SVM)

The accuracy metrics that are used to conduct this project are - 

* MAE (Mean Absolute Error), MSE (Mean Squared Error) and R2 Value for Linear Regression
* Accuracy Score, Jaccard Index, F1 Score, Log Loss, Confusion Matrix for Logistic Regression
* Accuracy Score, Jaccard Index, F1 Score for KNN classifier and Log Loss set to Not Defined
* Accuracy Score, Jaccard Index, F1 Score for Decision Tree Classifier and Log Loss set to Not Defined
* Accuracy Score, Jaccard Index, F1 Score for SVM and Log Loss set to Not Defined

<h3>Result of Linear Regression Model</h3>

As observed, the target variable of the data set is categorical type with two entries '1' and '0'. So, Binary Logistic Regression is a better choice. To prove this, I build a Linear Regression Model and calculate the performance metrics MAE, MSE and R2 value. The result is given as - 

<p align = 'center'>
  <img width = '600' height = '100' src = "https://github.com/aniket-chakraborty2001/Rain_Prediction_Australia/blob/main/Images/LinearRegression_Result.png">
</p>

From the above picture, it is clear that the model is very bad at predicting values as the R2 score is not even close to 50%

<h3>Result of Other Models</h3>

After the Linear Regression Failed, I tried the Logistic Regression Model, Classification model using KNN and Decision Tree and SVM. The result that I get from this model is given by the below picture

<p align = 'center'>
  <img width = '600' height = '150' src = "https://github.com/aniket-chakraborty2001/Rain_Prediction_Australia/blob/main/Images/OtherRegression_Result.png">
</p>

<h3>Confusion Matrix and Performance Metrics from Confusion Matrix</h3>

Defining the function that can create the confusion matrix and using the confusion_matrix function of sklearn's metrics module, I plot the Confusion matrix that helped to understand the Logistics Tregression Model in a better way. The picture of confusion matrix is given as - 

<p align = 'center'>
  <img width = '500' height = '500' src = 'https://github.com/aniket-chakraborty2001/Rain_Prediction_Australia/blob/main/Images/ConfusionMatrix.png'>
</p>

From confusion matrix different metrics like precision, recall, sensitivity, f1 score can be calculated. Using the **'classification_report'** function of sklearn's metrics module, I also get those metric values to know the performance of the model. This is given as - 

<p align = 'center'>
  <img width = '700' height = '400' src = 'https://github.com/aniket-chakraborty2001/Rain_Prediction_Australia/blob/main/Images/ResultConfMatrix.png'>
</p>

<h2 align = 'center'>This Ends the Project</h2>
