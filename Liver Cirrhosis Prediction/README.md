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



# Phase 2: Decision Tree Classifier for Cirrhosis Prediction

## Introduction
Phase 2 of this project builds upon the foundation laid in Phase 1. In this phase, we leverage the Decision Tree Classifier to continue our journey towards accurate cirrhosis prediction. Below, we provide an intricate account of each step taken in Phase 2.

## 1. Importing Libraries
We initiate Phase 2 by importing libraries essential for data analysis, visualization, and machine learning:

- **pandas**: A versatile library for data manipulation and analysis.
- **matplotlib and seaborn**: These libraries are essential for data visualization and creating insightful plots.
- **sklearn (Scikit-learn)**: This rich library provides the Decision Tree Classifier, enabling us to build a predictive model.

## 2. Loading Dataset
Our journey continues with the cirrhosis dataset, loaded from the 'cirrhosis.csv' file using pandas. This dataset contains valuable information that will fuel our predictive modeling journey in Phase 2.

## 3. Exploratory Data Analysis (EDA)
In Phase 2, we delve deeper into data exploration:

### i) Histogram of 'Age' Column
We begin with a histogram of the 'Age' column, providing insights into the distribution of patient ages within the dataset. This visualization deepens our understanding of the age distribution within the dataset, which can be a crucial factor in cirrhosis prediction.

### ii) Box Plot for Numeric Variables
A box plot is constructed for 'Bilirubin' and 'Albumin', offering a visual representation of the central tendency and spread of these essential numeric features. Understanding the distribution of these variables is crucial for building an accurate predictive model.

### iii) Count Plot for Categorical Variables
We use a count plot to visualize the distribution of the 'Sex' variable. This visualization provides insights into the gender distribution within the dataset, an important aspect of cirrhosis prediction.

### iv) Pairplot for Numerical Variables
The exploration extends to a pairplot for 'Age', 'Bilirubin', and 'Albumin'. This pairwise visualization helps us understand the relationships between these numeric variables. It can reveal correlations and interactions that are valuable for building an accurate predictive model.

## 4. Feature Selection
Feature selection is a critical step in building an effective predictive model. In this phase, we select the following features for modeling:

- 'Age'
- 'Bilirubin'
- 'Albumin'
These features are essential for cirrhosis prediction and have been chosen based on their potential significance.

## 5. Splitting Data
Data splitting is a fundamental part of model evaluation. In Phase 2, the dataset is divided into training and test sets using an 80-20 split ratio. This division ensures that the model is trained on one portion of the data and tested on another, allowing us to assess its performance effectively.

## 6. Model Training
The Decision Tree Classifier is chosen as the machine learning model for this phase. We initiate the model training process using the training data. Decision trees are effective at capturing complex relationships in the data, making them suitable for predictive modeling.

## 7. Testing Model
The trained model is put to the test using the test dataset. This step involves making predictions for cirrhosis detection based on the features selected for modeling.

## 8. Model Evaluation
### i) Performance Metrics - Accuracy, Confusion Matrix, Classification Report
The model's performance is evaluated through essential performance metrics, including:

- Accuracy: This metric represents the model's overall correctness in making predictions. A high accuracy indicates that the model is effective in cirrhosis prediction.

- Confusion Matrix: A confusion matrix is a tabulation of true positive, true negative, false positive, and false negative predictions. It provides a detailed breakdown of the model's performance.

- Classification Report: A classification report offers a comprehensive summary of the model's performance, including metrics such as precision, recall, F1-score, and support for each class (in this case, cirrhosis status).

### ii) Confusion Matrix Heatmap
A heatmap of the confusion matrix is generated, enhancing the visual representation of the model's performance. This visualization helps in identifying true positive, true negative, false positive, and false negative predictions, which are crucial for understanding the model's performance.
