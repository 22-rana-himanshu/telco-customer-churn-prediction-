# 📊 Telco Customer Churn Prediction Using Machine Learning

A machine learning project that predicts whether a telecommunications customer is likely to leave a service using customer information and a Random Forest classification model.

## 📌 Project Overview

Customer churn occurs when customers stop using a company's products or services. Identifying customers who may leave can help businesses understand retention risks and develop better customer retention strategies.

This project uses the Telco Customer Churn dataset to build a supervised machine learning model that predicts whether a customer will churn or remain with the company.

## 🎯 Project Objectives

- Analyze customer information and service usage data.
- Clean and preprocess missing or inconsistent values.
- Encode categorical variables for machine learning.
- Train a Random Forest classification model.
- Evaluate model performance using classification metrics.
- Predict churn status and estimated churn probability for a new customer.

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning:** Scikit-learn
- **Algorithm:** Random Forest Classifier
- **Preprocessing:** One-Hot Encoding, StandardScaler
- **Evaluation:** Accuracy, Precision, Recall, F1-score, Confusion Matrix
- **Environment:** Jupyter Notebook / Google Colab

## 📂 Dataset

**Dataset:** Telco Customer Churn

The dataset contains information about telecommunications customers, including:

- Customer demographics
- Account and contract details
- Internet and phone services
- Tenure and billing information
- Customer churn status

The notebook expects the dataset file:

`WA_Fn-UseC_-Telco-Customer-Churn.csv`

Dataset source: [IBM Sample Data Sets](https://community.ibm.com/community/user/businessanalytics/blogs/steven-macko/2019/07/11/telco-customer-churn-1113)

Ensure that the dataset is available locally or in your notebook environment before running the code.

## ⚙️ Project Workflow

### 1. Data Loading and Cleaning
- Load the CSV dataset using Pandas.
- Remove the unique `customerID` column.
- Convert `TotalCharges` to a numeric format.
- Replace missing `TotalCharges` values with the median.
- Convert the target variable `Churn` into binary labels.

### 2. Feature Engineering and Preprocessing
- Identify categorical columns.
- Apply one-hot encoding using `pandas.get_dummies()`.
- Separate input features from the target variable.
- Split the dataset into 80% training and 20% testing data.
- Standardize features using `StandardScaler`.

### 3. Model Training
Train a Random Forest Classifier using:
- `n_estimators = 150`
- `max_depth = 10`
- `random_state = 42`

### 4. Model Evaluation
Evaluate predictions using:
- Accuracy
- Precision
- Recall
- F1-score
- Classification report

### 5. Customer Churn Prediction
The prediction function accepts a new customer profile and returns:
- Predicted status: `CHURN` or `RETAINED`
- Estimated churn probability as a percentage

## 📈 Model Results

The notebook prints the model's accuracy and classification report after training.

**Actual performance:** Add your measured accuracy, precision, recall, and F1-score after running the notebook. No performance values are assumed in this README.

## 💻 Installation

Install the required libraries:

```bash
pip install pandas numpy scikit-learn
```

## 🚀 How to Run

1. Clone or download this repository.
2. Place the CSV dataset in the notebook's working directory.
3. Install the required Python libraries.
4. Open the notebook in Jupyter Notebook or Google Colab.
5. Run the cells in order to preprocess the data, train the model, and evaluate performance.

## 🔍 Example Prediction

The notebook includes a sample customer profile with contract, service, tenure, and billing details.

The model returns a prediction in this format:

```text
Test Customer Prediction: CHURN (probability%)
```

The actual status and probability depend on the trained model and dataset.

**Note:** The predicted probability is a model estimate, not a guarantee that a customer will leave.

## ⚠️ Limitations

- Model performance depends on dataset quality and representativeness.
- The sample dataset may not reflect current real-world customer behavior.
- The probability estimates have not necessarily been calibrated.
- The model should be evaluated on additional data before being used for business decisions.

## 👨‍💻 Author

**Himanshu Rana**  
M.Sc. Data Science Student

- GitHub: https://github.com/22-rana-himanshu

---

⭐ This project demonstrates practical skills in data preprocessing, feature engineering, supervised machine learning, model evaluation, and customer churn prediction.
