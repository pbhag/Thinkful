# Reuters-21578 Text Classification
[Jupyter notebook](https://github.com/pbhag/Thinkful/blob/master/Unsupervised%20Learning/Unsupervised%20Learning%20Capstone/Unsupervised%20Learning%20Capstone.ipynb)
* Note: if notebook is not rendering on GitHub, try [this](https://nbviewer.jupyter.org/github/pbhag/Thinkful/blob/master/Unsupervised%20Learning/Unsupervised%20Learning%20Capstone/Unsupervised%20Learning%20Capstone.ipynb)

### Topics: 
* Text (article) classification using the Reuters-21578 dataset
* Text cleaning and processing
* Dimensionality reduction
* Clustering:
* Supervised classification models

### Toolkit:
* Python 3, numpy, pandas, matplotlib, seaborn, scipy, sklearn, xgboost, nltk, re

## Overview:
* Project goal: utilize unsupervised machine learning algorithms to categorize article topics based on their text
* Dataset: Reuters-21578 from NLTK corpus
  * The documents in the Reuters-21578 collection appeared on the Reuters newswire in 1987. The documents were assembled and indexed with categories by personnel from Reuters Ltd.
  
  

## Data Processing:
* 90 distinct categories, articles can have more than one category label
  * Focused on articles with a single label
* Text cleaning: remove special characters and digits, lowercase text
* Feature generation: tf-idf vectorization
* Dimensionality reduction:
  * LSA (Latent Semantic Analysis): truncated SVD method in SKLearn

## Modeling
* Trained & tested algorithms on binary classes as well as a 8-category classification 
* __Unsupervised Classification (Clustering):__ suboptimal performance, visualizing ground truth clusters suggested that topics may not be very separable
* Clustering Models:
  * k-means, minibatch k-means
  * spectral clustering
  * mean-shift
  * affinity propagation
* Evaluation: Adjusted Rand Index (ARI), ground truth

* __Supervised Classification:__ much better performance, even before hyperparameter tuning, supervised classifiers did quite well
  * Trained & tested algorithms on binary classes as well as an 8-category classification
* Evaluation: mean accuracy, f1 score (10 fold cross validation)
* Models tested for binary and 8-category classification:
  * KNN 
  * Logistic Regression
  * Random Forest
  * XGBoost
  * Multi-Layer Perceptron


