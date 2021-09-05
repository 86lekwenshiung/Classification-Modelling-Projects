# **Heart Problem Classification**

## 1.0 Problem Statement
- Given clinical parameters about a patient, can we predict whether or not they have heart disease?

## 2.0 Datasets and Additional resources
- UCI Machine Learning Repository. https://archive.ics.uci.edu/ml/datasets/heart+Disease
- Kaggle : https://www.kaggle.com/ronitf/heart-disease-uci
- Learning ML and DS Bootcamp 2021 by Daniel Bourke : Udemy

## 3.0 Data Dictionary
|Feature|Type|Description|
|---|---|---|
|age|int|age in years|
|sex|int|(1 = male; 0 = female)|
|cp|int|0: Typical angina: chest pain related decrease blood supply to the heart <br> 1: Atypical angina: chest pain not related to heart <br> 2: Non-anginal pain: typically esophageal spasms (non heart related) <br> 3: Asymptomatic: chest pain not showing signs of disease|
|trestbps|int|resting blood pressure (in mm Hg on admission to the hospital) : anything above 130-140 is typically cause for concern|
|chol|int|serum cholestoral in mg/dl. serum = LDL + HDL + .2 * triglycerides <br> (above 200 is cause for concern)|
|fbs|int|(fasting blood sugar > 120 mg/dl) (1 = true; 0 = false). <br> '>126' mg/dL signals diabetes|
|thalach|int|maximum heart rate achieved|
|exang|int|exercise induced angina (1 = yes; 0 = no)|
|oldpeak |int|ST depression induced by exercise relative to rest. looks at stress of heart during excercise , unhealthy heart will stress more|
|slope|int|maximum heart rate achieved|
|thalach|int|the slope of the peak exercise ST segment. <br>0: Upsloping: better heart rate with excercise (uncommon) <br>1: Flatsloping: minimal change (typical healthy heart). <br>2: Downslopins: signs of unhealthy heart|
|ca|int|number of major vessels (0-3) colored by flourosopy. colored vessel means the doctor can see the blood passing through |
|thalach|int|maximum heart rate achieved <br> 1,3: normal <br> 6: fixed defect: used to be defect but ok now <br> 7: reversable defect: no proper blood movement when excercising|

## 4.0 Approach to Problem Solving
We're going to take the following approach:
1. Problem definition
2. Data
3. Evaluation
4. Features
5. Modelling
    - Logistic Regression
    - KNN
    - Random Forest Classification 
7. Experimentation
    - Hyperparameter tuning with GridSearch CV / Randomized Search CV

## 5.0 Models used for exploration
- Logistic Regression
- KNN
- Random Forest

## 6.0 Conclusion
- Modelling Choices to focus on : KNN
- Eveluation Matrix : If we can reach 95% accuracy at predicting whether or not a patient has heart disease during the proof of concept, we'll pursure this project.
- Result : We did not meet the evaluation metric set at 95%. Our various model so was slightly 90%

### Whats next?
- Continue to tune the hyperparameter for the best model so far
- Collect more data
- Another model, possibly
- The main takeaway for the next step is given sufficient time , we can continue to try to improve our model or try out other Various model, if more data might not be avaliable at the moment
