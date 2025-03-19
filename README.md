# AI-Powered Financial Insights and Recommendations

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Data Generation](#data-generation)
- [Technologies Used](#technologies-used)
- [Machine Learning Pipeline](#machine-learning-pipeline)
- [Installation & Setup](#installation--setup)
- [API Endpoints](#api-endpoints)
- [Folder Structure](#folder-structure)
- [Future Enhancements](#future-enhancements)
- [Contributors](#contributors)
- [License](#license)

## Overview
This project is an **AI-powered financial assistant** designed to:
- Provide **personalized financial insights** based on customer demographics and transaction history.
- Recommend suitable financial products such as **Credit Cards, Home Loans, and Personal Loans**.
- Predict loan amounts and credit limits using machine learning models.
- Serve as a Flask-based **API and web interface** for user-friendly interactions.

## Features
- **Customer Segmentation**: Uses **K-Means clustering** to group customers.
- **Product Recommendation**: Predicts the best financial product using a **Multi-Output Classifier**.
- **Loan/Credit Limit Prediction**: Estimates loan amounts & credit limits using **Random Forest Regressors**.
- **Financial Insights Generation**: Generates **natural language insights** with **LLM (Hugging Face Transformer Model)**.
- **Flask Web API**: Provides an interface for insights & recommendations.

## Data Generation
This project generates **synthetic customer data** using `Faker`. It includes:
### 1. Customer Demographics
   - Name, age, gender, marital status, education, occupation, salary, etc.
### 2. Financial Behavior
   - Loan amount, credit utilization, EMI paid, tenure, default status, credit limit.
### 3. Enquiries Data (Last 3 months)
   - Recent credit inquiries, product type, amount, approval/rejection status.
### 4. Transaction History (Past 6 months)
   - Transaction descriptions, account balance, salary credits, hobby-based spending.

## Technologies Used
- **Python (Flask)** – Web framework for API and frontend.
- **Pandas, NumPy** – Data processing and analysis.
- **Scikit-Learn** – ML models for clustering, classification, and regression.
- **Hugging Face Transformers** – AI-generated financial insights.
- **Matplotlib** – Visualization (for development and testing).
- **Joblib** – Model persistence.

## Machine Learning Pipeline
### 1. Pre-trained Models
   - `KMeans`: Customer segmentation.
   - `StandardScaler`: Data normalization.
   - `MultiOutputClassifier`: Predicts product suitability.
   - `RandomForestRegressor`: Predicts loan amounts & credit limits.
### 2. LLM-Based Insights
   - Uses a **fine-tuned transformer model** for personalized financial insights.
### 3. Flask Web Application
   - Accepts customer data and returns **product recommendations & financial insights**.

## Installation & Setup
### Prerequisites
- **Python 3.x** installed.
- Install dependencies:
  ```bash
  pip install -r requirements.txt
  ```

### Running the Application
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo.git
   cd your-repo
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Flask app:
   ```bash
   python app.py
   ```
4. Open the web interface in your browser:
   ```
   http://127.0.0.1:5000/
   ```

## API Endpoints
### 1. Generate Insights
- **Endpoint**: `/`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
    "customer_data": { ... }
  }
  ```
- **Response**:
  ```json
  {
    "insights": "Customer is financially stable with high credit utilization..."
  }
  ```

### 2. Generate Recommendations
- **Endpoint**: `/`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
    "customer_data": { ... }
  }
  ```
- **Response**:
  ```json
  {
    "recommended_product": "Credit Card",
    "predicted_limit": 50000
  }
  ```

## Folder Structure
```
📦 project-directory
├── models/                  # Pre-trained ML models (saved using joblib)
├── templates/
│   ├── index.html           # Web UI template
├── static/
│   ├── styles.css           # UI styles
├── app.py                   # Main Flask application
├── requirements.txt         # Dependencies
├── README.md                # Project documentation
└── data/                    # (Optional) Sample datasets
```

## Future Enhancements
- **Integration with Real Banking APIs** for live transaction analysis.
- **Reinforcement Learning** for self-improving recommendation models.
- **Advanced Customer Profiling** using deep learning techniques.

## Contributors
- **Your Name** – Developer

## License
This project is licensed under the **MIT License**.

---
For any issues or queries, please raise a **GitHub issue** or contact **[Your Email]**.

