# Business Project Portfolio

---

## Business Intelligence and Smart Service: Shorten livability planning process

<img src="images/amvest.png?raw=true" alt="Smart Service" width="90%"/>

**Objective**: Given demographic features of an area, the dashboard shows the predicted the number of amenities that will maximize the livability for an area.

**Information shown**:
- Predicted livability score
- Sufficient number of amenities
  
**Applied case**: Urban planning.

**Challenges**: Missing values, data transformation, and inconsistent data.

**Skills**: Excel, Tableau, R, ETL, Exploratory Data Analysis, Hyperparameter Tuning, Git.

For detailed report: [Improving livability planning process](https://thy0212.github.io/amvest_smart_service)

---
## Image Analysis: Product-Brand Detection

**Objective**: Given an image of a clothing item, detect the brand name and product type (e.g., shoes or earrings) of the item.

**Method**: 
- Image Pre-Processing:
  1. Process colorful images, retaining the RGB and HSV color histograms while removing the alpha channel, which captures transparency, from the image.
  2. Extract the RGB and HSV color histograms.
  3. Extract the shape of items by transforming the images to grayscale, applying the Canny algorithm, and then applying the Hough Line Detection algorithm.
  4. Encode textures using local binary patterns.
   
- Algorithm Development: Develop two predictive models (brand detection and product type detection) using support vector machines (SVM).
  
**Results**: Accuracy, recall and F1 score of the the two SVM models are significantly higher than the baseline, indicating high performance.
  
**Skills**: Image Analysis, R, Machine Learning.

---
## Time Series Analysis: Beer Sale Forcast
**Objective**: Monthly beer sales data is provided in millions of barrels over a period of 192 months. The goal is to fit a model to the data in order to forecast beer sales.

**Method**: 
- Pre-processing the time-series data:
1. Perform exploratory data analysis (EDA) to examine the stationarity, trend, and seasonality of the data.
2. Detrend the data to address the significant overall increasing trend.
3. Examine the ACF and PACF plots for the detrended data. The detrended beer sales has seasonality with no trend; therefore, it is recommended to apply a SARMA model.

- Model selection: _Specific to general_
   1. Estimate an ARMA(2, 0) model with 1 seasonal lag
   2. Based on the residual diagnostics (ACF and Q-Q plot of the residuals, and the p-values from the Ljung-Box test), increase the AR lags until the residual plots do not show major issues.
  
**Results and Business Recommendation**: 
- Compare the Bayesian Information Criterion (BIC) across all models. The ARMA(4, 0) model shows the best performance, indicating that beer sales in a given month depend on the sales of the last four months.

For the R code of the solution, please read [here](https://github.com/thy0212/descriptive-predictive-analysis/blob/main/tutorial%203/tutorial3.Rmd)
  
---
## Recommender System

**Objectives**: The dataset includes ratings from 100 customers for various products on the website. The goal is to build a recommender system using KNN algorithm.

**Method**: 
- Clean the data by removing missing values.
- Calculate recommendations by applying user-based KNN.
- Fine-tune the model by testing various values of K and evaluate the model's prediction accuracy using MAE and RMSE.

**Results and Business Recommendation**: 
- Models with K values between 20 and 30 show the highest performance.
- Besides highly rated products, it is suggested that the system should also display new items. Since users want to explore new options, the recommender system may not be valuable to them if it only recommends similar items.


