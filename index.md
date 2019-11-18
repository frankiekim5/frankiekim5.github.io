## Introduction
Cardiovascular disease is the leading cause of death globally, and it is expected to cause more than 23.6 million fatalities a year by 2030. One's survival from cardiovascular disease primarily depends on early detection and accurate diagnosis of the disease.

We can utilize Machine Learning algorithms to predict how likely one is to be diagnosed with cardiovascular disease, which can be used to improve the prevention rate and to provide critical insight for physicians to provide the correct treatment for the patient. In this project, we compare and contrast several ML algorithms for prediction of cardiovascular disease, and analyze them to identify the factors that determine which algorithm is the best fit for our given dataset.

## Methods
Heart Disease UCI has made their data available with information from 303 individuals. The dataset provides basic features such as age and sex as well as features that are crucial to diagnosing cardiovascular disease such as blood pressure, cholesterol levels, and blood sugar levels.

The data contains the following columns:
* Age - age in years
* Sex - (1 = male; 0 = female)
* Cp - chest pain type
* Trestbps - resting blood pressure (in mm Hg on admission to the hospital)
* Chol - serum cholesterol in mg/dl
* Fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false)
* Restecg - resting electrocardiographic results
* Thalach - maximum heart rate achieved
* Exang - exercise induced angina (1 = yes; 0 = no)
* Oldpeak - ST depression induced by exercise relative to rest
* Slope - the slope of the peak exercise ST segment
* Ca - number of major vessels (0-3) colored by flourosopy
* Thal - 3 = normal; 6 = fixed defect; 7 = reversible defect
* Target - have disease or not (1=yes, 0=no)

The goal is to predict the binary class ‘target’, which indicates whether or not a patient has cardiovascular disease. A value of 0 indicates a patient with cardiovascular disease while a value of 1 indicates a patient without cardiovascular disease.
We will be utilizing three different supervised learning methods to compare the performances and accuracies. Those three methods are Neural Network, Support Vector Machine, and Decision Tree.

## Expected Results
Based off of known factors that are significant to detecting cardiovascular disease, we predict that our algorithms will detect similar correlations with the given factors. Current risk factors that are commonly considered in diagnosing risk of heart disease are split into two categories: those that are considered controllable and uncontrollable. Uncontrollable risk factors for heart disease include: male sex, older age, and family history. Controllable risk factors include: high cholesterol, high blood pressure, diabetes, etc. If the tested models have predictive capabilities, it should be possible to see that these factors will correlate positively with heart disease diagnoses. 

In order to test the effectiveness of our predictive models, it is common to evaluate two metrics known as sensitivity and specificity.

Sensitivity is defined as $\frac{True Positive}{True Positive + False Negative}$

Sensitivity is defined as True PositiveTrue Positive + False Negative
Specificity is defined as True NegativeTrue Negative + False Positive 

In addition to these two single-value calculations, we will also provide the confusion matrices to visualize the accuracies of each model’s predictive capabilities. In the field of medical diagnosis, we are looking to minimize the number of false negatives, because it is more desirable to produce a false positive diagnosis that leads to further testing, rather than a false negative that could hide potentially dangerous conditions.


## Discussion

## Reference
