# Employee Churn Prediction Project

## Overview
The goal of this project is to build a machine learning model to predict employee churn, which refers to employees leaving the organization. This helps in identifying employees who are at risk of leaving, enabling proactive measures to retain valuable talent.

## Dataset Chosen
We used two datasets for this project:

- **Training Dataset (`employee_data.csv`)**: This dataset contains historical data on employees, including features such as department, salary, recent promotions, complaints, etc., with the target variable indicating whether an employee has left the company (status).
- **Unseen Dataset (`unseen_employee_data.csv`)**: This dataset contains new employee data without the target variable, which we aim to predict using our trained model.

## Data Cleaning and Preprocessing
The data cleaning and preprocessing steps are crucial for preparing the datasets for machine learning. The steps include:

1. **Loading the Data**: Datasets were loaded into pandas DataFrames for easy manipulation and analysis.
2. **Handling Missing Values**: Missing values were handled using `SimpleImputer` with a mean strategy for numerical data.
3. **Encoding Categorical Features**: Categorical features (e.g., department, salary, recently promoted, filed complaint) were encoded using `OrdinalEncoder`.
4. **Encoding the Target Variable**: The target variable `status` was encoded for model training.
5. **Splitting the Data**: The training dataset was split into training and test sets to evaluate model performance.
6. **Scaling Numerical Features**: Numerical features were standardized using `StandardScaler`.

## Models Used
We utilized a `RandomForestClassifier` from scikit-learn to build our predictive model. The Random Forest algorithm is an ensemble method that improves accuracy and robustness by combining multiple decision trees.

## Model Training and Evaluation
The model training and evaluation process involved:

1. **Training the Model**: The `RandomForestClassifier` was trained on the preprocessed training data.
2. **Making Predictions**: The trained model was used for predictions on the test set and the unseen dataset.
3. **Evaluating the Model**: Performance was assessed using:
   - **Accuracy**: The ratio of correctly predicted instances to total instances.
   - **Classification Report**: Detailed metrics including precision, recall, and F1-score for each class.
   - **Confusion Matrix**: Visualized with a heatmap, showing true positives, true negatives, false positives, and false negatives.

## Results
The Random Forest model achieved an accuracy of **[insert accuracy value here]** on the test set, demonstrating its effectiveness in predicting employee churn. The confusion matrix and classification report provided insights into the balance between precision and recall for each class.

## Predictions on Unseen Data
The trained model was used to predict employee churn on the unseen dataset, indicating which employees are at risk of leaving the company.

## Conclusion
This project successfully developed a machine learning model to predict employee churn, offering valuable insights for human resources to implement proactive retention measures. The thorough data cleaning, preprocessing, and evaluation steps ensured the model's reliability and accuracy in making predictions.
