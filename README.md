# SC1015 Mini-Project - Determining Breast Cancer on tumors &amp; Rate of Survivability

## About 
This is the mini project for SC1015 - Introduction to Data Science and Artificial Intelligence (DSAI) which focuses on data of breast cancer from both [breast-cancer-wisconsin](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data) and [breast-cancer](https://www.kaggle.com/datasets/homayoonkhadivi/breast-cancer-datasets)

#### Members
- Ng Hoe Ping
- Yao Sheng
- Edmund Yeo


### Problem Motivation
Even with the advanced in technology in today's society, many patients find out that they are diagnosed with breast cancer too late. In hope of getting patients to start treatment early for early-staged breast cancer, it is important for them to do self-examination to detect for breast cancer early. Therefore, they would expect these features estimates to be as precise as possible. Inaccurate estimates can lead to panic or fear in patient.

### Problem Definition
- Are we able to predict if a breast tumor is benign or malignant based on its features?
- Can we predict the survivability of someone with a malignant breast tumor based on their lifestyle?
- Which model would be the best to predict it?

### Resources (found in this folder) @@havent update@@

- [Original Dataset](https://github.com/Georgetxm/SC1015/blob/main/breast-cancer.csv)
- [Death Dataset](https://github.com/Georgetxm/SC1015/blob/main/death.csv)
- [Recovered Dataset](https://github.com/Georgetxm/SC1015/blob/main/recovered.csv)
- [Under Treatment Dataset](https://github.com/Georgetxm/SC1015/blob/main/under_treatment.csv)
- [Presentation Slides](https://github.com/Georgetxm/SC1015/blob/main/SC1015-MiniProj.pdf)
- Video can be assessed from this [link](https://www.youtube.com/watch?v=ZABvxkkY4mM)

### Walk-Through @@havent update@@
1. [Data Preparation and Cleaning](https://github.com/Georgetxm/SC1015/blob/main/Data_Preparation_Cleaning.ipynb)
    - Outliers (Age/Ratings/Latitude/Longitude)
    - Empty/NaN/Null Data
    - Column Names were all renamed to Camel Case

2. [Exploratory Data Analysis, Data-Driven Insights & Recommendations](https://github.com/Georgetxm/SC1015/blob/main/Exploratory_Data_Analysis.ipynb)
    - Distribution/Correlation of Numeric Columns
    - Plotting of orders geographically with a heatmap
    - Using a line chart to observe the average delivery time throughout the day.
    - Feature Engineering - Distance, Speed
   
3. [Machine Learning Techniques to solve the problem](https://github.com/Georgetxm/SC1015/blob/main/Machine_Learning_without_distance.ipynb)
4. [Machine Learning with engineered feature: distance](https://github.com/Georgetxm/SC1015/blob/main/Machine_Learning_V2_w_distanceipynb)
    - Predicting Time Taken
    - Using Numerical Data
        - Univariate/Multivariate LinReg
    - Both categorical and numerical data
        - ANOVA Test & One-Hot Encoding
        - Decision Trees
        - Random Forest
        - Lasso Regression
        - XGBoost
    - Model Evaluation
        - Results with Engineered Feature (Comparison between the Old & New R^2 and MSE Score) 

    We have 2 notebooks showcase the differences of our models with and without the engineered feature. Please use [4](https://github.com/Georgetxm/SC1015/blob/main/Machine_Learning_V2_w_distanceipynb) to grade us as 3 is merely to showcase our thought process.

### Conclusion
- We were able to find a strong relation between these 5 features (concave points, area, perimeter, radius, and concavity) and diagnosis of breast tumor (benign or malignant).
- Factors that could **greatly** affect **Survivability** of malignant tumor patient includes:
    - Numerical Columns 
        - Age (Positive Correlation)
        - Weight (Positive Correlation)
        - Thickness of Tumor (Positive Correlation)
        - Number of Times the Person Gave Birth (Positive Correlation)
    - Categorical Features 
        - Blood Type
        - Breast Pain
        - Radiation History
        - Hereditory History
        - Smoking
    
- The SMOTE model we implemented to estimate survivability has a 90% accuracy!!
- From our findings, we can suggest that individuals can self-examine by looking at the 5 features mentioned earlier (concave points, area, perimeter, radius, and concavity), if suspected to be a malignant tumor, they can go to the hospital to get it checked and diagnosed early, if positive. Lastly, those with malignant tumor is able to lower the possibility of dying by having an active lifestyle and eating healthily, as well as reduce or quit smoking.

### Key Learning Points
1. input
2. input
3. input
4. Implementation of K-Nearest Neighbors Classifier(KNN), Support Vector Classifier(SVC), Random Forest Classifier, Gaussian Naive Bayes, and Synthetic Minority Overlapaping Technique(SMOTE)

### Contributors
- Ng Hoe Ping: Data Cleaning, EDA, Feature Engineering, Machine Learning, Data Driven Insights from EDA and ML, Presentation Slides, Video
- Yao Sheng: Data Cleaning, EDA, Feature Engineering, Machine Learning, Data Driven Insights from EDA and ML, Presentation Slides, Video
- Edmund Yeo: Data Cleaning, EDA, Feature Engineering, Machine Learning, Data Driven Insights from EDA and ML, Presentation Slides, Video

### References @@havent update@@
1. [Data-to-Viz](https://www.data-to-viz.com/)
2. [Outliers: Keep or Drop](https://towardsdatascience.com/outliers-keep-or-drop-892b599b8ab6)
3. [Guidelines for removing outliers](https://statisticsbyjim.com/basics/remove-outliers/)
4. [Regularisation in Machine Learning](https://towardsdatascience.com/regularization-in-machine-learning-76441ddcf99a)
5. [L1, L2 Norm and Regularisation](https://www.analyticssteps.com/blogs/l2-and-l1-regularization-machine-learning)
6. [Random Forest Regression](https://towardsdatascience.com/random-forest-regression-5f605132d19d)
7. [Lasso Regression](https://www.mygreatlearning.com/blog/understanding-of-lasso-regression/#:~:text=Lasso%20regression%20is%20a%20regularization,i.e.%20models%20with%20fewer%20parameters)
8. [Introduction to XGBoost Algorithm](https://www.analyticsvidhya.com/blog/2018/09/an-end-to-end-guide-to-understand-the-math-behind-xgboost/)
9. [XGBoost Algorithm](https://towardsdatascience.com/https-medium-com-vishalmorde-xgboost-algorithm-long-she-may-rein-edd9f99be63d)
