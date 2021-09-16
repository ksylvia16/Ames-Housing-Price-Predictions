# Ames Housing Data and Kaggle Challenge


## Introduction & Problem Statement

I have been hired by Ames Realty Co. to build a model that best determines sale prices for properties in Ames, Iowa. Determining the sale price of a house is often complicated due to the number of variables that influence pricing decisions. However, with enough data, a linear regression model can be created that can help determine the most important features of a home and accurately predict housing prices.

Using a housing dataset from Ames, Iowa, I've attempted to create a linear regression model that predicts housing sale prices, based on over 2000 housing observations and more than 80 features using various feature engineering, selection, and regularization techniques.

In this project, my goals were to create both a high performing and extremely generalizable model. This means the model should react to unseen sets of data without large variations in accuracy. Ultimately, I'll be looking to evaluate the performance of this model using root mean squared error (RMSE) or the measure of the differences between values predicted by the model and the values observed.

Due to the scale of this project, it is split into two Jupyter notebooks: [01 EDA and Data Cleaning](https://github.com/ksylvia16/Ames-Housing-Price-Predictions/blob/e6164434e725126b8d6a253eaaea5167bbe5436e/code/01_EDA_and_Cleaning.ipynb) and [02 Feature Engineering and Modeling](https://github.com/ksylvia16/Ames-Housing-Price-Predictions/blob/e6164434e725126b8d6a253eaaea5167bbe5436e/code/02_Feature_Engineering_%26_Modeling.ipynb).

---

### Data and Data Dictionary

**Provided Data**

* [train.csv](http://localhost:8888/doc/tree/submissions_614/Projects/project_2/datasets/given/train.csv)
* [test.csv](http://localhost:8888/doc/tree/submissions_614/Projects/project_2/datasets/given/test.csv)

**Data Dictionary**

* A detailed data dictionary can be found here: [Link](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt/)

---

## Summary of Findings and Recommendations

The different regression models used included: 1. Linear Regression; 2. Lasso Regression; 3. Ridge Regression; and 4. Elastic Net Regression.  Lasso, Ridge, and Elastic Net Regression are methods that perform feature selection, each to different degrees.  They also regularize, or scale, the Beta coefficient of each feature, manipulating the model to minimize the affect 'noise' or meaningless data has on its predictions, increasing the model's predictive accuracy.

The ridge regression model had the best predictive performance on housing sale price in Ames, Iowa, and outperformed the other linear models tested. The model revealed that Overall, Exterior, and Kitchen Quality have a high correlation with the sale price of a home. Also, categorical features that had a high correlation with sale price were poured concrete foundation, having a finished garage, and having vinyl siding for exterior covering. Features that decrease the sale price of a home include an unfinished garage, a home located within 200' of East-West Railroad, roof material of gravel and tar, and a low depression land contour.

![Predicted Price vs. Actual Price](https://github.com/ksylvia16/Ames-Housing-Price-Predictions/blob/79922a61082f7706adce773fcbca8988de00b8ce/images/actual_vs_predicted.png)

Using this final model, I am able to account for approximately 92.2% of the variation in Sale Price. With a 71% improvement from the base model, my model proves to be an efficient method of determining sale prices of homes in Ames, Iowa. With more time, an adjustment to the model would be made to increase the accuracy of predicting the sale prices in more expensive homes.

---

## Additional Links

[DSIR-614 Regression Challenge](https://www.kaggle.com/c/dsi-ames/overview)
