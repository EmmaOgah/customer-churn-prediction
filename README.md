
# ChurnGuard – Customer Churn Prediction System

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Flask](https://img.shields.io/badge/Flask-Web%20Framework-black?logo=flask)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--learn-orange?logo=scikitlearn)
![Database](https://img.shields.io/badge/Database-MySQL-blue?logo=mysql)
![Status](https://img.shields.io/badge/Status-Completed-success)

## Project Overview

ChurnGuard is a Python-based Customer Churn Prediction and Management System developed to help businesses identify customers who are likely to discontinue their services.

The application integrates machine learning algorithms with a Flask web application to analyse customer information, estimate churn probabilities, classify customer risk levels, and support data-driven customer retention decisions.

The system combines predictive analytics, customer management, database integration, and administrative functionality in one application.

## Problem Statement

Customer churn is a major challenge for businesses because losing existing customers can affect revenue, profitability, and long-term growth.

ChurnGuard addresses this challenge by applying machine learning techniques to historical customer data to identify potential churn patterns and help businesses take proactive retention measures.

## Key Features

- **Customer Churn Prediction:** Estimates the probability of a customer leaving a service.
- **Risk Classification:** Categorises customers into Low, Medium, and High risk levels.
- **Customer Management:** Supports customer registration and record management.
- **Retention Recommendations:** Provides suggested actions based on predicted customer risk.
- **Interactive Dashboard:** Provides an interface for monitoring customer information and predictions.
- **Role-Based Access Control:** Supports different administrative and operational permission levels.
- **Prediction History:** Maintains records of previous predictions.
- **Reports and Analytics:** Supports downloadable CSV reports.
- **Audit Logging:** Records administrative activities.
- **Authentication:** Includes secure password hashing, login, and password reset functionality.

## Technologies Used

### Programming Language
- Python

### Machine Learning and Data Science
- Pandas
- NumPy
- Scikit-learn
- Joblib

### Machine Learning Algorithms
The project implements and compares four classification algorithms:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier
4. Gradient Boosting Classifier

### Web Development
- Flask
- HTML
- CSS
- JavaScript
- Bootstrap

### Database
- MySQL
- MySQL Connector/Python

### Authentication and Security
- Flask-Login
- Werkzeug password hashing
- Role-based permission controls

## Machine Learning Methodology

The machine learning component follows a structured predictive modelling workflow.

### 1. Data Collection
The training pipeline loads the IBM Telco Customer Churn dataset.

### 2. Data Cleaning
- Handles missing values.
- Converts numerical fields into appropriate data types.
- Encodes the target variable into binary values.
- Prepares customer information for modelling.

### 3. Data Preprocessing
The project uses Scikit-learn preprocessing pipelines.

Numerical features:
- Median imputation
- Standard scaling

Categorical features:
- Most-frequent-value imputation
- One-hot encoding

### 4. Model Training
The dataset is divided into training and testing sets using an 80:20 split, with stratified sampling.

Four classification algorithms are trained and evaluated.

### 5. Model Evaluation
The following evaluation metrics are implemented:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

### 6. Model Selection and Deployment
The model with the highest ROC-AUC score is selected and saved using Joblib.

The Flask application loads the saved model pipeline to generate predictions for customer records.

## Application Architecture

The application is organised into modular components:

| Component | Responsibility |
|---|---|
| `app.py` | Flask application and routes |
| `config.py` | Application configuration |
| `model/` | Model training and preprocessing |
| `database/` | MySQL database operations |
| `utils/` | Validation, permissions, and helper functions |
| `templates/` | HTML application pages |
| `static/` | CSS and JavaScript assets |
| `dataset/` | Customer churn dataset |

## Installation and Setup

### Prerequisites

Ensure you have installed:

- Python 3
- MySQL Server
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/EmmaOgah/customer-churn-prediction.git
```

### 2. Navigate into the Project

```bash
cd customer-churn-prediction
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

Windows:

```bash
venv\Scripts\activate
```

Linux/macOS:

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure the Database

- Start your MySQL server.
- Create the database using the SQL script in `database/customer_churn.sql`.
- Configure your database connection settings using the variables expected by `config.py`.
- Configure a strong Flask secret key.
- Configure SMTP settings if password reset emails are required.

### 6. Prepare the Dataset

Place the IBM Telco Customer Churn CSV dataset at the configured location:

```text
dataset/customer_churn.csv
```

### 7. Train the Machine Learning Model

Run:

```bash
python model/train_model.py
```

The training process compares the four classification algorithms and saves the selected model.

### 8. Start the Application

After database configuration, model training, and creation of the initial administrator account, start the Flask application:

```bash
python app.py
```

Open the local address displayed by the Flask development server in your browser.

**Note:** The initial administrator setup is handled by `seed.py`. Review and replace its example credentials before running it. Never publish real credentials.

## Project Objectives

- Apply machine learning to customer churn prediction.
- Develop practical predictive analytics solutions using Python.
- Compare classification algorithms using appropriate evaluation metrics.
- Integrate a trained machine learning pipeline into a Flask application.
- Support customer retention through data-driven recommendations.
- Demonstrate the integration of machine learning, web development, and database management.

## Future Improvements

- Deploy the application to a cloud platform.
- Integrate additional machine learning algorithms.
- Improve model performance through hyperparameter tuning.
- Introduce advanced customer behaviour analytics.
- Add interactive visual analytics.
- Implement automated model monitoring and retraining.

## Author

**Emmanuel Ogah**

Computer Engineering Graduate | Python Developer | Data Science | Artificial Intelligence | Machine Learning

- GitHub: [EmmaOgah](https://github.com/EmmaOgah)
- LinkedIn: [Emmanuel Ogah](https://www.linkedin.com/in/emmanuel-ogah-619893218/)

---

*Developed as an independent project to demonstrate practical applications of Python, Data Science, Machine Learning, and web development.*
