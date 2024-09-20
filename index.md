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

References: [Improving livability planning process](https://thy0212.github.io/amvest_smart_service)

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
  
- Model evaluation: Accuracy, recall and F1 score of the the two SVM models are significantly higher than the baseline, indicating high performance.
  
**Skills**: Image Analysis, R, Machine Learning.

---
## Time Series Analysis


---
## Recommendation System
