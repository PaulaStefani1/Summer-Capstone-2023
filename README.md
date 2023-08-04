# Summer-Capstone-2023

Overview: 
This Repository is used in order to track and save the different EDA, modeling and analysis processes performed during the completion of the Kaggle Home Credit Default Risk project during the MSBA Capstone Project for Summer 2023.

## Business Problem Statement
A vast amount of people have difficulty in verifying and providing proof of credit accountability when getting loans. This is a reflection of insufficient or non-existent credit histories and variance among people’s financial historical data. Without sufficient financial and credit histories, it becomes harder for lenders to identify and predict which customers are at risk of default and which are not, which can lead to mis-identifications between both groups, as well as a reduction of possible future customers that would be in fact reliable borrowers.

The purpose of the proposed project is to create a supervised analytical model to help Home Credit predict how capable each applicant is of repaying a possible loan. The analytics approach in solving this issue will be to use the different features for the current application vs. previous applications and create a supervised model based on multiple regression, and machine learning techniques like k-Fold Cross-Validation, Gaussian Mixture Model, and/or Artificial Neural Networks. Our team will also use the different transaction datasets available in order to improve the performance of the predictive model.

The main deliverable for this project will the creation of a predictive model that can be used to identify defaulters and non-defaulters and support future analysis, and a formal determination of which variables are more important when determining the prediction of the repayment ability of enterprise loans.This will benefit the lenders by providing them more reliable models and also will benefit the customers by delivering greater access to financial services that could not be available for them due to the lack of historical financial data.

Our team is composed of three students in the University of Utah MSBA program. The project will be completed by August 2, and will be separated in three main milestones: Exploratory Data Analysis, Modeling, and Final Model Presentation. The benchmark for success on this project is to be able to deliver the predictive model in a way that is reliable, effective, and cost efficient, in which we can use the current data collected without needing to expend more resources collecting future information.

##  Data and Target Variable

The target variable as identified by the data provider is called “TARGET” in the application_{train|test}.csv dataset. It’s a binary variable represented by a 1 or a 0. A 1 indicates that the borrow is experiencing is either delinquient or in default. The lateness and number installment range vary. Approximately 8.1% of all borrowers in the dataset fit the target category. This suggests a significant classification imbalance that will need to be considered in future modeling/feature selection. In the next project phase (modeling), this target variable will be predicted in the testing data set. Three variables, in particular are common requirements for lenders to evaluate credit worthiness: income, credit amount, and annuity payments. These are all necesarily intertwined and we evaluated the interplay between these and other variables throughout this document. 

## Modeling

For modeling we used 3 types of modeling tools: Logistic Regression Naive Bayes and Random Forest. 
The approach for the Logistic Regression Model was to increase model complexity and amount of variables while checking model accuracy and predictive efficiency.
Three Naive Bayes models were created for better model comparisons. First two models use the existing class imbalance and the third will up-sample the target = 1 class. Our last models are a creation of a simple tree model to see if we could gain any initial insight, followed by random forest models with increased complexity and cross-validation.

## Solution and Findings: 

Our tuned Random Forest models perform the best of all the models that we tried; logistic regression, Naive Bayes and Decision Tree or default Random Forest model. We were able to manipulate the logistic regression and Naive Bayes model to be better models than just the default settings; however, even after upsampling the training set that our models were built on to have the same proportion of the target classes, these models ultimately were not as strong as the tuned Random Forest. We believe much of this can be attributed to the fact that these models did not have a wide variety of information to predict the target class of “1” as the samples that already existed in the data set were just sampled randomly to make up for the imbalance in the data set. Regardless of this challenge in our modeling process, we were able to create a Random Forest model that actually predicted the minority class through tuning parameters such as reducing the number of trees and increasing the node size and try values from the default. Through cross-validation, we were able to iterate through our model multiple times and plotted the AUC which, on the training set clearly is overfitting the model, but on the test set is showing a curve that we would expect. Our Kaggle score ended up being .63974 as a private score and .61927 as a public score. We did run into some inconsistencies between the application set and the dataset that we ran our analysis on, in particular, we had to leave out a day’s credit from our Kaggle submission although we were able to include it in this model which we feel could contribute to a better score.

## My contribution to the project and Learnings.

I believe my main contribution to this project was through the creation of the logistic regression models created for the Modeling Phase, as well as support on EDA creation and the creation of the presentation itself. Overall I learned so much with this on hands project and it was very interesting opportunity to work and learn with different individuals in the area of data analytics. I not only think it was a great opportunity for me to develop my analytical skills but also to understand more about how they are applicable to real-world scenarios and context challenges, while also learning how to better communicate and use data knowledge exchange tools to support the efficiency and communication/collaboration of the work project. 

## Business Value of Solution / Project 

I believe the main business value we brought for this challenge was the creation of a model that can be helpful to identify the strongest predictors of default fo the population studied in the case, while also providing Home Credit recommendations on how to improve predictive models for their business case and hw to use their data on a more efficient way, for example by indicating that Home Credit should create a Currency ID to better help future analysis of the case, or for example by recommending that they focus on dedicating resources to contextualized data that is more reflective of underserved populations.

Lastly, we were able to identify that our model had a $505,160,164 estimated greater ROI of random forest model over majority classifier performance in normalized currency value, which shows how our model and project created could benefit Home Credit and increase ROI. 



