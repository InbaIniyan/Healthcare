# Phase 1: CatBoost Model for Cirrhosis Prediction

## Introduction
Phase 1 of this project focuses on developing a predictive model for cirrhosis using the CatBoost algorithm. This phase entails comprehensive data preprocessing, exploratory data analysis (EDA), model development, and rigorous performance evaluation. Below is a detailed account of the steps taken in this phase.

## 1. Importing Libraries
In the initial stage of our project, we imported the following libraries to facilitate data processing, visualization, and machine learning:

- **pandas**: Used for data manipulation and management.
- **matplotlib and seaborn**: Employed for data visualization and creating insightful plots.
- **sklearn (Scikit-learn)**: Provides various machine learning tools, such as train-test splitting and standardization.
- **catboost**: Utilized for training the CatBoost regression model, a powerful gradient boosting algorithm.

## 2. Loading Dataset
We began by loading the cirrhosis dataset from the 'cirrhosis.csv' file using pandas. This dataset contains valuable information for our predictive modeling task.

## 3. Data Preprocessing
### i) Handling Missing Values for Numeric Columns
To address missing values in numeric columns, we applied the following steps:

- Identified numeric columns in the dataset.
- Calculated the mean for each numeric column and imputed missing values with the corresponding means. This approach preserves the statistical characteristics of the data.

### ii) Handling Missing Values for Categorical Columns
For categorical columns, the process involved:

- Identifying categorical columns in the dataset.
- Replacing missing categorical values with the mode (most frequent value) of each respective column.

### iii) Encoding Categorical Variables
To prepare the dataset for machine learning, we one-hot encoded the categorical variables, transforming them into a numerical format. This step ensures that the model can utilize these features effectively.

## 4. Data Splitting
To evaluate our model's performance, we split the dataset into training, validation, and test sets. We used the following split ratios:

- 70% of the data for training.
- 15% for validation.
- 15% for testing.

## 5. Feature Scaling
Feature scaling is a crucial preprocessing step to ensure that all features have a similar scale. We utilized the StandardScaler from sklearn to standardize the features, making them suitable for CatBoost.

## 6. Exploratory Data Analysis (EDA)
### i) Histogram for Numeric Variables
To gain insights into the distribution of numeric variables, we created histograms with 20 bins. These visualizations allow us to assess data density and observe data spread.

### ii) Boxplots for Numeric Variables
Box plots were constructed for numeric variables, providing a comprehensive view of the data's central tendency, spread, and potential outliers. Understanding the distribution of numeric features is essential for model development.

### iii) Count Plots for Categorical Variables
For categorical variables, count plots were generated, focusing on the "Status" feature. This enabled us to visualize the distribution of cirrhosis statuses.

## 7. Correlation Analysis
We conducted a correlation analysis to identify relationships between variables. The correlation matrix was visualized using a heatmap, providing a clear view of variable dependencies and interactions.

## 8. Target Variable Distribution
We used a count plot to visualize the distribution of the target variable, "Stage." Understanding the distribution of cirrhosis stages is essential for model evaluation and interpretation.

## 9. Feature Relationships
### i) Scatter Plots for Numeric Features
To explore the relationship between "Bilirubin" and the target variable "Stage," we created scatter plots. This visualization helps us understand how "Bilirubin" affects cirrhosis stage.

### ii) Categorical Feature Analysis
We conducted a categorical feature analysis by creating contingency tables for gender ("Sex") and "Stage." These tables provided insights into how gender relates to cirrhosis stage.

## 10. Outlier Detection
We utilized box plots to detect outliers in the "Age" column. Identifying outliers is essential for model robustness and accurate predictions.

## 11. Feature Engineering
Feature engineering is a crucial step in model development. In this phase, we engineered a new feature, "BMI," based on "Age" and "Cholesterol." This feature enhances the dataset's predictive power.

## Building Model using CatBoost Algorithm
### Model Training
We created and trained the CatBoost model with 1000 iterations and a learning rate of 0.1. This state-of-the-art gradient boosting algorithm is ideal for regression tasks.

### Model Evaluation
Predictions were made on the validation set, and model performance was evaluated using the mean squared error (MSE). The CatBoost MSE on the validation set was calculated and recorded.

### Make Predictions
Predictions were extended to the test set, allowing us to assess the model's predictive capability. The CatBoost MSE on the test set was also computed and documented.

### Predicted vs. Actual Values
A scatter plot was generated to visualize the relationship between actual and predicted values. This visualization aids in assessing the model's accuracy and identifying any patterns or discrepancies.

### Overall MSE for Catboost Algorithm
The overall weighted MSE was calculated across all sets (training, validation, and test) to determine the model's overall performance. The result was recorded to provide a comprehensive evaluation of the CatBoost algorithm's effectiveness in predicting cirrhosis.
