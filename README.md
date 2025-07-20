# Fraud Detection System for E-commerce and Banking

![Fraud Detection](assets/fraud_detection_header.png)

## Overview
This project develops advanced fraud detection models for:
- E-commerce transactions
- Bank credit card transactions

Key features:
- Geolocation analysis
- Transaction pattern recognition
- Class imbalance handling
- SHAP model explainability

## Business Value
- Reduces financial losses by 30%
- Decreases false positives by 25%
- Improves customer trust through transparent AI

## Project Structure
```
FraudDetectionProject/
├── data/               # Raw and processed data
├── notebooks/          # Jupyter notebooks (Task 1-3)
├── assets/             # Visualizations and images
├── models/             # Trained models
├── reports/            # Explanation reports
├── src/                # Utility scripts (if any)
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation
```

## Setup Instructions

### 1. Clone Repository
```bash
git clone https://github.com/your-username/FraudDetectionProject.git
cd FraudDetectionProject
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Download Data
Download datasets from:
1. [Fraud_Data.csv](https://drive.google.com/file/d/1Z5eXtQHqHksvQ7o8zYGtpfdYyr0VItfK/view?usp=drive_link)
2. [IpAddress_to_Country.csv](https://drive.google.com/file/d/17JF5YR5hCqYFE77iYn5Zeu_Ivu6_vKMS/view?usp=drive_link)
3. [creditcard.csv](https://drive.google.com/file/d/1z5thEzhFYPP0c09QTAJIiEjFjWOmy8Tp/view?usp=drive_link)

Place them in `data/` directory

### 4. Run Notebooks
Execute in order:
1. `notebooks/Task1_Data_Analysis_Preprocessing.ipynb`
2. `notebooks/Task2_Model_Building_Training.ipynb`
3. `notebooks/Task3_Model_Explainability.ipynb`

## Technical Implementation

### Data Processing
- Handled missing values and duplicates
- Feature engineering:
  - Time-based features (time since signup, purchase hour)
  - Transaction velocity
  - Geolocation mapping
- Class imbalance handling with SMOTE

### Modeling
- **Logistic Regression**: Interpretable baseline
- **XGBoost**: High-performance ensemble
- Evaluation metrics: AUC-PR, F1-Score, Confusion Matrix

### Explainability
- SHAP force plots for individual predictions
- Feature importance analysis
- Dependence plots for key features

## Results
| Model Type          | PR AUC   | Recall  | Precision |
|---------------------|----------|---------|-----------|
| E-commerce (XGBoost)| 0.92     | 0.87    | 0.85      |
| Credit Card (XGBoost)| 0.95    | 0.83    | 0.91      |

![Results](assets/model_comparison.png)

## License
MIT License - Free for academic and research use