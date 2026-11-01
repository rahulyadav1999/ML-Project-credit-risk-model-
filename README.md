# Credit Risk Prediction System

A Machine Learning-powered web application that evaluates loan applicants' credit risk by estimating their probability of default and generating a credit score with a corresponding risk rating.

Built using **Python, Scikit-learn, and Streamlit**, this project demonstrates how machine learning can support credit risk assessment through an interactive web interface.

## Project Overview

Credit risk assessment is an important part of the lending process. Financial institutions need to evaluate whether a loan applicant is likely to repay a loan or potentially default.

This application takes applicant and loan-related information as input and uses a pre-trained machine learning model to estimate default probability and calculate a credit score.

### Key Features

- **Default Probability Prediction:** Estimates the probability that a loan applicant may default.
- **Credit Score Calculation:** Generates a credit score on a scale of 300–900.
- **Credit Rating Classification:** Categorizes applicants into Poor, Average, Good, or Excellent ratings.
- **Interactive Web Interface:** Provides an easy-to-use interface built with Streamlit.
- **Input-Based Risk Assessment:** Evaluates applicant information such as income, loan amount, credit utilization, and delinquency history.

## Application Preview

Run the application locally to explore the interface and test different loan applicant profiles.

## Input Features

The application accepts the following information:

| Category | Input Features |
|---|---|
| Applicant Details | Age, income |
| Loan Information | Loan amount, loan tenure |
| Credit History | Average DPD, delinquency ratio |
| Credit Utilization | Credit utilization ratio, open loan accounts |
| Applicant Profile | Residence type |
| Loan Details | Loan purpose, loan type |

The application also calculates the loan-to-income ratio based on the applicant's income and requested loan amount.

## How It Works

1. **User Input:** The applicant's financial and loan-related details are entered through the Streamlit interface.
2. **Data Preparation:** Input features are transformed into the format expected by the trained model.
3. **Feature Scaling:** Selected numerical features are scaled using the saved scaler.
4. **Prediction:** The pre-trained classification model estimates the probability of default.
5. **Credit Score Calculation:** The estimated probability is converted into a credit score between 300 and 900.
6. **Risk Classification:** The applicant receives a rating based on the calculated score.

### Credit Rating Categories

| Credit Score | Rating |
|---|---|
| 300–499 | Poor |
| 500–649 | Average |
| 650–749 | Good |
| 750–900 | Excellent |

## Technology Stack

- **Programming Language:** Python
- **Machine Learning:** Scikit-learn
- **Data Processing:** Pandas, NumPy
- **Model Serialization:** Joblib
- **Web Application:** Streamlit

## Project Structure

```text
ML-Project-credit-risk-model/
│
├── artifacts/
│   └── model_data.joblib
│
├── main.py
├── prediction_helper.py
├── requirements.txt
├── README.md
└── .gitignore
```

### File Descriptions

- `main.py` – Streamlit application interface.
- `prediction_helper.py` – Input preprocessing, model prediction, and credit score calculation.
- `artifacts/model_data.joblib` – Saved model, scaler, feature names, and scaling configuration.
- `requirements.txt` – Python dependencies required to run the application.

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/rahulyadav1999/ML-Project-credit-risk-model-.git
```

### 2. Navigate to the Project Directory

```bash
cd ML-Project-credit-risk-model-
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Mac/Linux**
```bash
source venv/bin/activate
```

**Windows**
```bash
venv\Scripts\activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the Application

```bash
streamlit run main.py
```

The application will open in your browser, typically at:

```text
http://localhost:8501
```

## Future Improvements

- Add model performance evaluation metrics.
- Include confusion matrix and classification report.
- Improve input validation and preprocessing.
- Add explainability to understand the factors influencing predictions.
- Deploy the application for public access.

## Application Screenshot

![Credit Risk Prediction Application](credit-risk-app.png)

## Disclaimer

This project is developed for educational and demonstration purposes. Its predictions should not be used as the sole basis for real-world lending or financial decisions.

## Author

**Rahul Yadav Nethula**

Data Scientist | AI & Machine Learning Engineer

- **GitHub:** [rahulyadav1999](https://github.com/rahulyadav1999)
- **LinkedIn:** [Rahul Yadav Nethula](https://www.linkedin.com/in/rahul-yadav-nethula/)
