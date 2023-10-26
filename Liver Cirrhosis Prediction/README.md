# Cirrhosis Prediction Project

This project encompasses three distinct phases, each contributing to the development of an effective cirrhosis prediction model. The following provides an overview of the key steps and outcomes in each phase:

---


## Phase 1: CatBoost Model for Cirrhosis Prediction

Phase 1 focuses on building a predictive model for cirrhosis using the CatBoost algorithm. This phase involves data preprocessing, exploratory data analysis (EDA), model development, and performance evaluation. 

<details>
<summary>Click to Expand - Phase 1 Details</summary>

### Importing Libraries
Essential libraries for data processing, visualization, and machine learning are imported.

### Loading Dataset
The cirrhosis dataset ('cirrhosis.csv') is loaded, forming the foundation of our predictive model.

### Data Preprocessing
Missing values are handled, categorical variables are encoded, and numerical features are standardized.

### Exploratory Data Analysis (EDA)
EDA includes histograms, box plots, feature selection, data splitting, model training, and performance evaluation with mean squared error (MSE).

</details>

---


## Phase 2: Decision Tree Classifier for Cirrhosis Prediction

In Phase 2, the Decision Tree Classifier is employed to enhance the cirrhosis prediction model. This phase encompasses data loading, extensive EDA, feature selection, data splitting, model training, and evaluation.

<details>
<summary>Click to Expand - Phase 2 Details</summary>

### Importing Libraries
Essential libraries for data analysis, visualization, and machine learning are imported.

### Loading Dataset
The cirrhosis dataset ('cirrhosis.csv') is loaded to facilitate the construction of the predictive model.

### Exploratory Data Analysis (EDA)
This phase includes visualizations such as histograms, box plots, count plots, and pairplots for an in-depth understanding of the dataset.

### Feature Selection
Relevant features ('Age', 'Bilirubin', and 'Albumin') are chosen for modeling.

### Splitting Data
The dataset is split into training and test sets for model evaluation.

### Model Training
The Decision Tree Classifier undergoes training to capture complex relationships in the data.

### Model Evaluation
Performance metrics, including accuracy, a confusion matrix heatmap, and a comprehensive classification report, are employed for assessment.

</details>

---


## Phase 3: Survival Analysis and Artificial Neural Network (ANN) for Cirrhosis Prediction

Phase 3 introduces survival analysis and an Artificial Neural Network (ANN) for advanced cirrhosis prediction. It involves data loading, extensive data preprocessing, exploratory data analysis, target variable definition, data splitting, model building, and comprehensive performance evaluation.

<details>
<summary>Click to Expand - Phase 3 Details</summary>

### Importing Libraries
Essential libraries are imported for efficient dataset management and advanced machine learning model development.

### Loading Dataset
The 'cirrhosis.csv' dataset is loaded into a Pandas DataFrame to serve as the foundation for this phase.

### Data Preprocessing
Handling missing values, encoding categorical variables, and standardizing numerical features are crucial steps in preparing the dataset for advanced modeling.

### Exploratory Data Analysis (EDA)
EDA includes visualizations like Kaplan-Meier survival curves, log-rank tests, and survival probability heatmaps to gain deeper insights.

### Defining Target Variable
The target variable, 'time_to_event,' represents the time until an event occurs, typically the time to death.

### Splitting Dataset
Data splitting is essential for model development and evaluation, ensuring the dataset is appropriately divided.

### Model Building & Compiling
An Artificial Neural Network (ANN) model tailored for survival analysis is constructed and compiled with an appropriate loss function and optimizer.

### Model Training
The ANN model undergoes training on the training data.

### Model Predictions
The trained ANN model is applied to the testing data for predictions, and its performance is assessed using the concordance index (C-index).

### Model Performance Evaluation
A binary classification threshold is introduced, and key performance metrics, including accuracy, precision, recall, F1-score, and ROC AUC score, are calculated for a comprehensive model evaluation.

</details>

---

In summary, this project encompasses three phases, each building upon the previous one, to develop an effective cirrhosis prediction model. These phases encompass data preprocessing, exploratory data analysis, model development, and thorough performance evaluation.


## How to Run
To run this project on your local environment, follow these steps:

1. **Ensure you have the required libraries installed.** You can install them using pip:
   
       pip install pandas numpy tensorflow scikit-learn matplotlib seaborn catboost lifelines

2. **Download the dataset 'cirrhosis.csv' and place it in the project directory.

3. **Execute the provided Python script to run the project.**


## Additional Model Performance Metrics
This project goes beyond basic accuracy and incorporates advanced performance metrics. These include:

- **ROC Curves:** Receiver Operating Characteristic curves offer a graphical representation of the model's ability to distinguish between classes. We calculate the ROC curve and Area Under the Curve (AUC) to assess the model's binary classification performance.

- **Precision-Recall Curves:** Precision-Recall curves provide insights into the precision and recall trade-off. They are particularly important for imbalanced datasets and are used alongside the ROC curve for comprehensive model evaluation.


## Next Steps
To further enhance this project, consider the following actions:

- **Hyperparameter Tuning:** Optimize hyperparameters such as learning rate, batch size, and the number of hidden layers to improve model performance.

- **Feature Engineering:** Experiment with feature selection and engineering techniques to identify the most informative features for the model.

- **Different Architectures:** Explore various neural network architectures, such as convolutional neural networks (CNNs) or recurrent neural networks (RNNs), to assess their impact on predictive accuracy.
