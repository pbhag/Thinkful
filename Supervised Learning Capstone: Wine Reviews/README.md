# Predicting Wine Ratings and Prices

[Presentation slides](https://github.com/pbhag/Thinkful/blob/master/Supervised%20Learning%20Capstone:%20Wine%20Reviews/Wine%20Reviews%20powerpoint.pptx)

[Jupyter notebook - analysis](https://github.com/pbhag/Thinkful/blob/master/Supervised%20Learning%20Capstone:%20Wine%20Reviews/Wine%20Reviews.ipynb)

[Jupyter notebook - modeling](https://github.com/pbhag/Thinkful/blob/master/Supervised%20Learning%20Capstone:%20Wine%20Reviews/Wine_Reviews_Analysis_Final.ipynb)

### Toolkit
* Python 3, NumPy, Pandas, Matplotlib, Seaborn, SciPy, SKLearn, NLTK (Natural language tool kit)

### Topics 
* EDA, data cleaning, preprocessing, visualization
* Feature engineering,  dimensionality reduction
* Predictive modeling

## Introduction
* Project goal: to create models that will try to predict the price of a bottle of wine or the points rating of a wine, based on wine review data
* Dataset: Scraped from Wine Enthusiast Magazine by Zach Thoutt, and posted on [Kaggle](https://www.kaggle.com/zynicide/wine-reviews). 
  * 83,495 rows of data
  * 41 different countries represented 
  * 352 provinces 
  * 947 regions 
  * 442 varieties of wine
* Target Variables: 
  * Wine Rating (between 80-100 points)
  * Wine Price (between $4-$1000 USD)

## Data Preprocessing
#### Summary of Preprocessing
* Outliers removed, missing data imputed and then dropped
* Feature engineering
  * Created a feature called `origin` to consolidate hierarchial geographical features
  * Analyzing wine descriptions
    * Text processing with regular expressions
    * Vectorization of wine descriptions using Term frequency-inverse document frequency (TF-IDF)
* Dimensionality reduction
  * Singular-Value Decomposition (SVD) to reduce size of TF-IDF vector
  * Principal Component Analysis (PCA) to reduce size of features independent of wine descriptions

## Modeling
* 80-20 train-test split on dataset
* 5-fold cross validation for parameter tuning on linear regression models
* Evaulation metric: RMSE
#### Target: Price
* Best model: Random Forest Regressor (100 estimators)
  * RMSE of +/- $1.22 per bottle of wine
#### Target: Point rating
* Best model: Random Forest Regressor (100 estimators)
  * RMSE of +/- 1.06 points in rating for wine, with no basis on the cost of the wine

