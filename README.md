# Telcom company client churn prediction

![alternative text](reports/img/churn.png)


#### -- Project Status: Completed

## Project Intro/Objective
The purpose of this project was to apply learned data science and more specifically machine learning concepts to a problem of predicting which clients will churn.


### Methods Used

* Machine Learning
* Data Visualization

### Technologies
* Python
* Pandas, jupyter, sklearn, H20, FLAML,  Pycaret


## Project Description
We obtained the kaggle dataset of clients of a telecommunication company (https://www.kaggle.com/datasets/blastchar/telco-customer-churn). The data consists of individual client's data with each row representing one client and a series of features(columns) and a dependant variable "Churn" which is either "yes" when the client churned in the time period of tha dataset or "no" otherwise.

We cleaned and performed an initial exploratory analysis of the data, generating different visualizations to get an initial understanding of the data and problem. We coninued generating initial classifier models with Pycaret and H20 ML modules and contiued from there. We generated various models XGB, Logistic Regression with various hyperparameters. We tried out various feature engineering approaches, but were largely not that impactful. The biggest impact came from using a "class weights = balanced" or SMOTE resampling in order to balance the different classes in the dataset as there is a  ~75/25 split in no churn vs churn. We came to the business solution of having a two model approach. One model that identifies wih high probability all cases at the expense of having substantial false positives (Logistic regressor) and another model (GBM) to identifiy with a higher probability clients that would churn (i.e. low amount of false positives). This way the business can target with low cost methods (e.g. mass email) clients in the first bucket while having a more bespoke approach to the second bucket. 



## Featured Notebooks/Analysis/Deliverables
* Business slides: reports/Telcom_Churn_Prediction.pdf
* Various Jupyter Notebooks used in the notebooks folder


## Team Members: 
 - [Pedro](https://github.com/PedroIglesias2)
 - [Sebastian](https://github.com/Sdrozo)
 - [P](https://github.com/w011e)
 - [Raphael](https://github.com/RP077)
