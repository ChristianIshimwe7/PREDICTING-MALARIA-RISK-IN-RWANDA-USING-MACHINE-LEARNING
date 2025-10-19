#PROJECT PLAN: PREDICTING MALARIA RISK IN RWANDA USING MACHINE LEARNING.

#AUTHOR: Christian ISHIMWE/ African Leadership University Rwanda.

#E_MAIL: c.ishimwe7@alustudent.com

Problem: Predicting malaria risk (high/low) in Rwandan communities using historical health and environmental data to support early interventions by the Rwanda Biomedical Centre (RBC).
Why It Matters: Malaria remains a leading cause of morbidity in Rwanda, with 1.7M cases in 2022 (WHO). Predictive models can help target resources (e.g., bed nets, sprays) to high-risk areas, especially in rural regions.
Mission Alignment: This directly supports your goal of using ML to improve healthcare access and outcomes in Rwanda.

Dataset

Source: Combine Rwanda Health Management Information System (HMIS) data (available via statistics.gov.rw) with open environmental datasets (e.g., rainfall, temperature from NASA POWER).

HMIS: Provides malaria case counts, patient demographics, and clinic locations.
NASA POWER: Offers weather data (rainfall, temperature) correlated with malaria spread.
Backup Option: If HMIS access is limited, use WHO Global Health Observatory or Kaggle malaria datasets.


Features: Rainfall, temperature, humidity, population density, historical malaria cases, age, gender.
Target: Binary classification (high/low malaria risk).
Justification: Relevant to Rwanda’s public health needs, rich for feature engineering, and not from sklearn/keras (meets assignment rules).

Methodology

Traditional ML (Scikit-learn):

Models: Logistic Regression, Random Forest, XGBoost.
Feature Engineering: Normalize weather data, encode categorical variables (e.g., province), create interaction terms (e.g., rainfall × temperature).


Deep Learning (TensorFlow):

Sequential API: Simple feedforward neural network (FNN).
Functional API: Multi-input model combining weather and demographic data.
tf.data API: Efficient data pipeline for batching and shuffling.


Experiments:

Vary hyperparameters (e.g., learning rate, number of layers, tree depth).
Test feature subsets (e.g., weather-only vs. all features).
Compare train/test splits (70/30, 80/20).


Evaluation Metrics: Accuracy, precision, recall, F1-score, ROC-AUC, confusion matrix.
Visualizations: Learning curves, confusion matrices, ROC curves.
