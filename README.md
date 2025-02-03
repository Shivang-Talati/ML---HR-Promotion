# Problem Statement:  
Your client is a large MNC and they have 9 broad verticals across the organisation. One of the problem your client is facing is around identifying the right people for promotion (only for manager position and below) and prepare them in time. Currently the process, they are following is:  
1. They first identify a set of employees based on recommendations/ past performance  
2.  Selected employees go through the separate training and evaluation program for each vertical. These programs are based on the required skill of each vertical  
3.  At the end of the program, based on various factors such as training performance, KPI completion (only employees with KPIs completed greater than 60% are considered) etc., employee gets promotion.
     
For above mentioned process, the final promotions are only announced after the evaluation and this leads to delay in transition to their new roles. Hence, company needs your help in identifying the eligible candidates at a particular checkpoint so that they can expedite the entire promotion cycle.   
They have provided multiple attributes around Employee's past and current performance along with demographics. Now, the task is to predict whether a potential promotee at checkpoint in the test set will be promoted or not after the evaluation process.  

# Expectations and Evaluation:  
We expect the candidate to build a model upon training data (70% of the train_hr.csv) and evaluate the model on the validation data, (30% of the train_hr.csv). Use the random_state=10 while splitting the data. Use the model to predict upon the test_hr.csv.     
Evaluation metric for this competition is F1_Score on the validation data.

# Steps Followed:
1️⃣ Data Import & Exploration: Loaded the dataset (hr), checked its shape, dimensions, and descriptive statistics.  
2️⃣ Data Preparation: Created a copy (hr1), checked for duplicates (found none).  
3️⃣ Feature Selection & Preprocessing: Dropped two irrelevant columns, handled missing values, and detected outliers using boxplots.  
4️⃣ Model Preparation: Defined X (features) and Y (target), scaled the data, and split it into training and validation sets.  
5️⃣ Model Building: Implemented Logistic Regression as the initial model and evaluated its performance.  
6️⃣ Error Analysis: Identified high Type II errors in the confusion matrix, leading to model tuning.  
7️⃣ Model Tuning: Optimized threshold values (0.43 & 0.44) to improve accuracy and reduce errors.  
8️⃣ Test Data Processing: Applied the same preprocessing steps to test data (excluding Y since it's unavailable).  
9️⃣ Final Prediction: Used the trained model to make predictions on the test set for evaluation purposes—ensuring the model's performance is measured accurately without re-training on test data.  
