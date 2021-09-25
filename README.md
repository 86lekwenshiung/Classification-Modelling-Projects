# **Classification Modelling Projects**

## 1.0 Repo Objectives
The main objectives of this repo is to document various type of classification modelling projects during my data science learning journey. This serve not only to documents the learning journey, but more importantly it archives various methodology used so that one can quickly referenced back for inspiration on the thinking process when working on new , unknown projects.

## 2.0 Datasets and Additional resources
- UCI Machine Learning Repository. https://archive.ics.uci.edu/ml/datasets/heart+Disease
- Kaggle : https://www.kaggle.com/ronitf/heart-disease-uci
- Learning ML and DS Bootcamp 2021 by Daniel Bourke : Udemy
 

<a id = 'content'><a/>
## 3.0 Notebook Summary
| Project Name | Problem Statement | Notebook Key Feature | Dataset |
|:---:|:---:|---|:---:|
| [Heart Problem Classification](https://github.com/86lekwenshiung/Classification-Modelling-Projects/blob/main/Credit_Card_Default.ipynb) | Given clinical parameters about a patient, can we predict whether or not they have heart disease? | 1. Introductory EDA<br>2. Modelling : KNN , Logistic Regression , RandomForest<br>3. Hyperparameter tuning : GridSearchCV , RandomizedSearchCV | Heart Disease Dataset from UCI ML Repo |
| [Credit Risk Classification](https://github.com/86lekwenshiung/Classification-Modelling-Projects/blob/main/Credit_Card_Default.ipynb) | Given Customer payment activities and demographic , are they risky or not risky? | 1. Imbalanced Data<br>2. Modelling : Logistic Regression<br>3. Data tuning : Smote , ROS , RUS | Credit Risk Dataset from Kaggle |
| [Telco Churn Classification](https://github.com/86lekwenshiung/Classification-Modelling-Projects/blob/main/Imbalanced%20Classification%20on%20Telco%20Churn.ipynb) | Given customer profile and demographic , are we able to predict potential churn?|  1. Imbalanced Data<br>2. Modelling : Logistic Regression<br>3. Data tuning : Smote || 

## 4.1 Heart Disease Classification
[(back to top)](#content)
- 4.1.1 Models Used for Exploration
    - Logistic Regression
    - KNN
    - Random Forest
 
 - 4.1.2 Findings
    - Modelling Choices to focus on : KNN
    - Evaluation Matrix : If we can reach 95% accuracy at predicting whether or not a patient has heart disease during the proof of concept, we'll pursure this project.
    - Result : We did not meet the evaluation metric set at 95%. Our various model so was slightly 90%
  
  - 4.1.3 Whats Next
    - Continue to tune the hyperparameter for the best model so far
    - Collect more data
    - Another model, possibly
    - The main takeaway for the next step is given sufficient time , we can continue to try to improve our model or try out other Various model, if more data might not be avaliable at the moment
___

## 4.2 Credit Risk Classification
[(back to top)](#content)
- 4.2.1 Models Used for Exploration
    - Logistic Regression
    - SmoteENN , Random Under Sampler   

- 4.2.2 Findings
    - For imbalanced Data , the model will simply predict the majority, resulting in many False Negative or Positive. Though the Accuracy is high , it is a false indication.
    - Other metrics such as f1 score should be used instead.
    - Imbalanced data are required to be tune via undersampling the minority or oversampling the majority.
    
<p align = 'center'>
    <img src = 'https://github.com/86lekwenshiung/Classification-Modelling-Projects/blob/main/Image/Smote_Method.png'>
<p/>

<p align = 'center'>
    <img src = 'https://github.com/86lekwenshiung/Classification-Modelling-Projects/blob/main/Image/classification_metrics.PNG' width =35%>
<p/>

 - 4.1.3 Whats Next
   - Continue to test out various under or oversampling methodology
   - Explore with various imbalance dataset
___

## 4.3 Telco Churn Prediction
[(back to top)](#content)

 #### Data Imbalance Ratio
 * Churn : 30%
 * No Churn : 70%
 
#### Key Insights
* Oversampling on Random Forest Classifier for this paticular dataset does not appear to significantly inprove the F1 Score.
* Undersampling and Hybrid Sampling like SMOTEENN does actually improve the Randform Forest Performance. 
* Oversampling on Logistic Regression do improve the F1 score , however model score performed badly across all metrics.

| Log Reg (No SMOTE) | Logistic Regression | Random Forest (No SMOTE) | Random Forest Classifier |  |
|---|---|---|---|---|
| Accuracy | 0.711600 | 0.590623 | 0.721331 | 0.715249 |
| Precision | 0.491803 | 0.364958 | 0.647260 | 0.538847 |
| Recall | 0.023024 | 0.568304 | 0.072525 | 0.082502 |
| F1 Score | 0.043988 | 0.444478 | 0.130435 | 0.143095 |
| AUC Score | 0.615507 | 0.614876 | 0.660334 | 0.643889 |
| Gini Score | 0.231013 | 0.229752 | 0.320669 | 0.287778 |
 
#### Next Step
* Use other classification technique like XGBoost
* Try other SMOTE Technique like undersampling or combined under and over sample.
* Use Hyperparameter tuning to improve model.
* Remove more outliers before parsing through model.
* Focus on top features and do a polynomial transform.
* Collect data for more distinct features that are better able to differentiate between churn and no churn.
 
