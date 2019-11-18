
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

## Data Exploration
<!-- figure 1 -->
Based on the correlation heatmap above, the bottom-most row and right-most column depict the correlation of each factor with the target. From the correlation heat map, it is evident that cp, thalach are the most positively correlated with the target, and exang, oldpeak, and ca are the most inversely correlated with the target. To summarize, from the correlation heat map, the five features (cp, thalach, exang, oldpeak, ca) depict the most correlation with the target result.

<!-- figure 2 -->
The pair plot is used to understand the best set of features to explain the relationship between two variables or to form the most separated clusters.  Thus, it uses the top 5 features chosen from our feature selection ([ 'ca', 'cp’, ‘exang’, ‘old peak’, ‘thalach’]) to show their relations.

### Feature Selection
Using a chi-squared statistical test, we identified the same 5 features as having the highest correlation with the target variable.
<!-- figure 3 -->

The Extra Tree Classifier class in the scikit-learn API was used to estimate the importance of features. The five features displayed were the same as above, but the scores were different from the univariate selection.
<!-- figure 4 -->

In order to show the accuracy of the following algorithms to choose the most common risk factors for cardiovascular disease from our dataset, we tried to match it with proven medical research. Our top 5 features from the dataset includes ['ca', 'cp’, ‘exang’, ‘old peak’, ‘thalach’] which essentially breaks down to chest pain, number of major vessels, ST depressions found from an ECG, and a person’s maximum heart rate. 

On the other hand, based on research, chest pains, high blood pressure / cholesterol, shortness of breath are among the most common risk factors. We can see that chest pains are a match, as well as shortness of breath and maximum heart rate because they are both correlated to each other. Based on these results, we can see a positive correlation of matches between our dataset and research to show accurate measures.

### Normalization
### Encoding original values to categorical values

## Supervised Learning Techniques
### Neural Networks
### Decision Tree
### Support Vector Machine
### Logistic Regression

## Results

## Reference
