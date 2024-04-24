# SC1015 Mini-Project - Determining Breast Cancer on tumors &amp; Rate of Survivability

## About 
This is the mini project for SC1015 - Introduction to Data Science and Artificial Intelligence (DSAI) which focuses on data of breast cancer from both [breast-cancer-wisconsin](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data) and [breast-cancer](https://www.kaggle.com/datasets/homayoonkhadivi/breast-cancer-datasets)

#### Members
- Ng Hoe Ping
- Yao Sheng
- Edmund Yeo


## Problem Motivation
Even with the advanced in technology in today's society, many patients find out that they are diagnosed with breast cancer too late. In hope of getting patients to start treatment early for early-staged breast cancer, it is important for them to do self-examination to detect for breast cancer early. Therefore, they would expect these features estimates to be as precise as possible. Inaccurate estimates can lead to panic or fear in patient.

## Problem Definition
- Are we able to predict if a breast tumor is benign or malignant based on its features?
- Can we predict the survivability of someone with a malignant breast tumor based on their lifestyle?
- Which model would be the best to predict it?

## Resources (found in this folder)

- [Original Dataset](https://github.com/bobesaur/SC1015_MiniProj/blob/main/breast-cancer.csv)
- [Death Dataset](https://github.com/bobesaur/SC1015_MiniProj/blob/main/death.csv)
- [Recovered Dataset](https://github.com/bobesaur/SC1015_MiniProj/blob/main/recovered.csv)
- [Under Treatment Dataset](https://github.com/bobesaur/SC1015_MiniProj/blob/main/under%20treatment.csv)
- [Presentation Slides](https://github.com/bobesaur/SC1015_MiniProj/blob/main/SC1015%20Mini-Project%20Slides.pdf)
- Video can be assessed from this [link](https://youtu.be/NGaIxfxqTGs)


## Walk-Through @@havent update@@
<h3>1. Data Preparation and Cleaning</h3>
<h4>[All Datasets]</h4>

- Removed rows with NaN/NULL spaces that will affect the machine learning accuracy
- Removed unnecessary parameters like "education" and "patient ID"
- Combined "death.csv" and "recovered.csv" into a single variable in the code for machine learning

<h3>2. "original"</h3>
<h4>[variable named from "breast-cancer".csv]</h4>

- Separated into 2 variables: "meanbreast" and "worstbreast"
- Find parameters in both variables that will predict classifications Malignant("M") or Bengin ("B")
- Visualisation in Histogram/Boxplot/Violinplot

<h3>3. "survival"</h3>
<h4>[Combined variable named from "death.csv" and "recovered.csv"]</h4>

- Clean data by only focusing on relevant parameters to our problem, as well as remove any outliers
- One-hot encoding, converted the variables under "condition" from "death" to "1", and "recovered" to "0".
- Visualisation in Histogram/Correlation Heatmap
- Implementation of different classification algorithms to find the highest accuracy score

<h3>4. Machine Learning Techniques to solve the problem</h3>

- Decision Tree
- RandomForestClassifier
- Logistic Regression
- K-Nearest Neighbours (KNN)
- Support Vector Machine (SVM)
- Gaussian Naive Bayes (NB)
- Keras Neural Network


<h3>5. Model Evaluation</h3>

- Visualisations to identify imbalance data and effectiveness of Machine Learning Techniques.
- Evaluating with Precision, recall, f1 score.

## Conclusion
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
1. Concepts of different evluation methods (Precision, Recall and F1 Score).
2. Identifying false accuracy with overfitting and imbalance data.
3. Handling overfitting and imbalance data.
4. Implementation of K-Nearest Neighbors Classifier(KNN), Support Vector Classifier(SVC), Random Forest Classifier, Gaussian Naive Bayes, Logisitic Rgression and Synthetic Minority Overlapaping Technique(SMOTE)
5. Neural Network Model (Multilayer Perceptron).

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
9. [SMOTE Application](https://www.analyticsvidhya.com/blog/2020/10/overcoming-class-imbalance-using-smote-techniques/)
