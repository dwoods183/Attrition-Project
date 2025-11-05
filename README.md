## Employee Attrition Prediction Model
This project outlines the development of a machine learning model to predict employee attrition. It utilizes Python, scikit-learn, and pandas within a Jupyter Notebook to analyze the factors leading to employee turnover and identify which employees are at the highest risk of leaving.

This was developed to demonstrate a practical application of data preprocessing, feature engineering, and model evaluation using a well-known HR dataset.

### Dataset
This model is trained using the publicly available WA_Fn-UseC_-HR-Employee-Attrition.csv (IBM HR Employee Attrition) dataset.

Note: This file must be located in the project's root directory to run the notebook successfully.

Project Requirements
The notebook requires Python 3 and the following core libraries:

- pandas

- scikit-learn

#### These can be installed in your environment using pip:
pip install pandas scikit-learn

### How to Run the Project
1. Clone or download the repository.

2. Place the WA_Fn-UseC_-HR-Employee-Attrition.csv file in the same directory as the notebook.

3. Launch the Attrition Project.ipynb file using Jupyter Notebook or a compatible IDE (like VS Code).

4. Execute the cells in order from top to bottom. The notebook will handle data processing, model training, and will output the results directly.

### Model Development Process
The model was built using the following workflow:

1. Data Loading & Cleaning: The CSV is loaded, and the target variable (Attrition) is converted to a binary format (1/0). Non-predictive columns like EmployeeNumber are dropped.

2. Feature Engineering: All categorical text data (e.g., Department) is transformed into a numerical format using one-hot encoding so the model can process it.

3. Data Splitting: The dataset is divided into a 75% training set and a 25% test set. This split is stratified to maintain a consistent ratio of "Yes" to "No" attrition cases in both sets.

4. Model Training: A RandomForestClassifier (a powerful ensemble model) is trained on the 75% training data.

5. Model Evaluation: The trained model's predictive power is tested on the 25% unseen test data, and its accuracy is calculated.

6. Feature Analysis: The model is analyzed to determine which features (e.g., MonthlyIncome, OverTime) had the most influence on its predictions.

### Findings and Results
The model achieved the following performance on the test set:

- Model Accuracy: 83.42%

The analysis also revealed the key drivers of attrition. The top 10 most important factors identified by the model are:

1. MonthlyIncome

2. Age

3. DailyRate

4. TotalWorkingYears

5. DistanceFromHome

6. YearsAtCompany

7. HourlyRate

8. MonthlyRate

9. OverTime_Yes

10. NumCompaniesWorked
