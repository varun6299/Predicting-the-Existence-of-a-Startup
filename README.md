# Predicting-the-Existence-of-a-Startup
A Machine Learning project to build a classification model to predict the survival or acquisition of a Startup.


## **Business Case**
Establishing a startup is a highly risky move which involves a lot of sustaining efforts due to the high failure rates associated and unpredictable nature of the business environment. Hence, in order to survive and grow in the market, before setting up or during early stages, a startup needs to consider several factors like market, location, finances, competition, technology, etc. Taking the right or wrong decision in respect to these factors can impact chances of survival of the organization. It could also affect the ability to get funds from several sources.

## **Approach to the Case**
To build a classification model to identify the startups, based on their market, location and finances acquired, which are going to continue to operate, get acquired or in a worst case scenario, be forced to close down.

## **Dataset Used**
To build this model, the dataset used was taken from Kaggle. This dataset has been built from CrunchBasewhich is a platform to find information about private or public companies, and uploaded to Kaggle by Andy M.

The link to the dataset is here - https://www.kaggle.com/arindam235/startup-investments-crunchbase

** The several tasks performed during the project were as follows**

## **Data Understanding**
- No. of records, features, data types of variables, size of the dataset, variables involves, missing values and count of unique categories/ values initially checked.

## **Data Cleaning**
- Several Issues found in the data
- Datatypes of several variables wrongly identified
- Rows with missing values across all variables were found.
- Unwanted characters in certain variables preventing conversion to correct datatype.
- Invalid dates preventing processing of variables and causing date range errors.

## **Exploratory Data Analysis**
- Univariate analysis conducted to understand characteristics of each variables.
- Bi-variate analysis conducted to understand relationship of predictors with the target feature.
- Multi-variate analysis conducted to understand the relationship between several features at once.
- Key insights derived : Imbalance in dataset, high skewness in numerical features, difficulty in identifying of patterns as trends clearly skewed towards majority class, not much multi-collinearity found.

## **Data Preprocessing and Feature Engineering**
- Treatment of variables with missing values done case by case.
- Feature Engineering adopted to create new features for original variables which couldnt be imputed.
- Cardinality of categories checked for catogorcial features before taking decision to drop or retain.
- Final categorical features retain were subject to grouping minor categories getting grouped into a new cateogry - "others"
- Data split into train test using stratified shuffle split to retain proportion of target classes and prevent data leakage during required transformations.
- KNN Imputer used to impute missing values across all remaining features after encoding and scaling.
- Transformation applied to numerical features to treat outliers and lack of normality.
- One Hot encoding adopted to encode categorical features for the purpose of business interpretation.

## **Model Building**
- Several models built such Logistic regression, Naive Bayes, Tree based algorithms and Booting algorithms.
- Models perform poorly on minority classes due to imbalance in target classes.
- SMOTE applied on train to oversample instances of minority classes and resulted in improving results across both train and test.
- XGB chosen for reasons of good performance and stability in results on comparison with train and test results and also during cross validations.
- Further, Feature Selection and Hyperparameter tuning performed to improve model.
- Final model selected is a baseline model which uses 20 features and produces macro F1 score of 0.50 on test sample.
