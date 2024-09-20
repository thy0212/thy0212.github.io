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
**Objective**: Monthly beer sales is provided in millions of barrels in the period of 192 months. Fit the model to the data to forcast the sale of beer.

**Method**: 
- Pre-processing the time-series data:
1. Perform EDA to examine stationarity, trend, and seasonality of the data.
2. Detrend the data because there is a significant overall increasing trend
3. Examine the ACF and PACF plots for de-trended data. The detrended beer sales is seasonality and no trend, hence, it is suggested to apply SARMA.

- Model selection: _Specific to general_
   1. Estimate an ARMA(2, 0) model with 1 seasonal lag
   2. Based on the residual diagnostics (ACF and Q-Q plot of the residuals and the p-values of the Ljung-Box test), increase the AR lags to higher numbers, until the residual plots do not show major problems.
  
**Results and Business Recommendation**: 
- Compare Bayesian Information Criteria (BIC) of all models, ARMA(4,0) model is the best performance model, meaning that beer sales of a given month depends on the he last 4 months' sales.

For the R code of the solution, please read [here](https://github.com/thy0212/descriptive-predictive-analysis/blob/main/tutorial%203/tutorial3.Rmd)
  
---
## Recommendation System
