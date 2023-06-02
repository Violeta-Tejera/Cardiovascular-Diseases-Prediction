### Cardiovascular-Heart-Disease-Prediction

The aim of this project is to develop an AI model based on classifier trees to predict the presence of heart diseases in patients based on specific characteristics, like cholesterol levels, age of the individual or whether or not they smoke. Please note that I am a beginner in this field, so there might be flaws in my model or code, or a better way to approach this problem, I'm constantly learning. Should you have any recommendations, suggestions, or would like to engage in further discussion, please contact me via email through vtejmun@gmail.com.

## Introduction

Cardiovascular diseases (CVDs) are the leading cause of death globally, although most CVDs can be prevented by addressing unhealthy habits. It is important to detect CVDs as soon as possible in order to avoid a fateful outcome. (Source: World Health Organization)

Bearing this in mind, my objective with this project is to design a classifier forest model that is able to predict whether or not a patient of certain characteristics such as age, body mass index or tobacco consumption suffers from any cardiovascular disease or not.

## Dataset

The dataset used for training and validation of the model was retrieved from Kaggle and uploaded by Chaitnya Pol, Subhajeet Das and Asit Patel. This dataset contains data from 70 000 individuals, equally distributed between patients with and without cardiovascular diseases.

![image](https://github.com/Violeta-Tejera/Cardiovascular-Heart-Disease-Prediction/assets/80209320/4e575703-871d-431b-819c-5e1dd899413c)

![image](https://github.com/Violeta-Tejera/Cardiovascular-Heart-Disease-Prediction/assets/80209320/c971cb4c-c90e-40d2-8848-711622eb86ef)


# Data preprocessing

- Age was presented in days, so it was modified into years, considering that all years have 365 days.

- A new column, BMI (Body Mass Index) was added to the dataframe by calculating it over heigth and weigth.

## Methodology

Random forests use many decision trees and makes a prediction by averaging the individual prediction of each of its components, this way, not only the accuracy of the model is improved but also we can prevent over-fitting the model. The prediction target y es 'cardio', a binary variable that indicates if a patient suffers from cardiovascular diseases (1) or not (0). The set of features X is composed by the following variables:

- Age: Age in days of the patient 
- Gender: Gender of the patient (0 = male, 1 = female)
- Height: In centimetres
- Weight: In kilograms
- Ap_Hi: Systolic blood pressure (int)
- Ap_Lo: Diastolic blood pressure (int)
- Cholesterol: 1: Normal, 2: Above normal, 3: Well above normal
- Gluc: Glucose levels. 1: Normal, 2: Above normal, 3. Well above normal
- Smoke: Tobacco consumption. (0 = no, 1 = yes)
- Alco: Alcohol intake. (0 = no, 1 = yes)
- Active: Whether or not the patient is active (0 = no, 1 = yes)

Using the operation train_test_split from scikit learn, data was divided between the train values and the validation values.

## Results

Being the random state of the random forest classifier 9, our predictions off by aproximately 0.2959. The metric used for this was mean absolute error.

Furthermore, after analysing the data presented, the following plots were constructed which showed that the prevalence of CVD increases from the age 53 onwards, with a low occurrence among individuals under the age of 40; and overweight, obese and extremely obese individuals tend to suffer from CVD more than those with lower body mass indexes.

![image](https://github.com/Violeta-Tejera/Cardiovascular-Heart-Disease-Prediction/assets/80209320/c4325d5e-7387-4667-aeea-0ce9ccf5e552)

![image](https://github.com/Violeta-Tejera/Cardiovascular-Heart-Disease-Prediction/assets/80209320/06183686-30f6-450b-ab2b-35e28311755e)
