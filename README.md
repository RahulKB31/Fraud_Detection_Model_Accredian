# Fraud Detection Model_Accredian

This repository contains the implementation and evaluation of a fraud detection model, built using machine learning techniques. The model is designed to detect fraudulent financial transactions using various features and algorithms, and has been tested for accuracy, recall, and precision.

## Project Structure
- **`data/`**: Contains the raw and processed transaction data used for model training and evaluation.
- **`notebooks/`**: Jupyter notebooks used for exploratory data analysis (EDA), feature engineering, model selection, and evaluation.
- **`models/`**: Contains the trained models and relevant performance metrics.
- **`src/`**: Python scripts for data preprocessing, model training, and evaluation.
- **`README.md`**: Overview of the project, including key details of the fraud detection model.

## Key Components

### 1. Data Collection and Preparation
- **Data**: Includes transaction features such as transaction type, amount, account balances, and fraud indicators.
- **Preprocessing**: 
  - Handled missing values and errors.
  - Normalized numerical features.
  - Encoded categorical variables.
  - Generated new features like `isSuspicious` and `customer_info_Dest`.

### 2. Feature Engineering
- Key features selected based on domain knowledge and exploratory analysis.
- Created additional features like `isSuspicious` and `type_numeric` to enhance predictive power.

### 3. Model Selection
- Multiple algorithms were evaluated:
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - Gradient Boosting
  - Convolutional Neural Networks (CNNs)
- Models were compared using accuracy, recall, ROC AUC score, and precision.

### 4. Model Training and Evaluation
- The data was split into training, validation, and test sets.
- Cross-validation and hyperparameter tuning were applied.
- **Top-performing models**:
  - Decision Tree and Random Forest were the most effective, achieving high accuracy, balanced precision-recall, and robust fraud detection performance.

### 5. Performance Metrics
- **Decision Tree**:
  - Accuracy: 99.97%
  - ROC AUC: 0.9344
  - Recall for fraud detection: 87%
- **Random Forest**:
  - Accuracy: 99.97%
  - ROC AUC: 0.8920
  - Precision for fraud detection: 97%

## Key Predictors of Fraudulent Transactions
- **`oldbalanceOrg`**: Origin account balance before the transaction.
- **`newbalanceDest`**: Destination account balance after the transaction.
- **`type_numeric`**: Type of transaction.
- **`amount`**: Transaction amount.

## Recommendations
- **Security Enhancements**:
  - Implement multi-factor authentication.
  - Real-time transaction monitoring.
  - Regular updates to security protocols.
- **Effectiveness Assessment**:
  - Monitor the rate of fraudulent transactions before and after security updates.
  - Review the model's false positive and false negative rates regularly.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/fraud-detection-model.git
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the model training and evaluation scripts:

   ```bash
   python src/train_model.py
   ```

## Contributions
Contributions are welcome! Please open an issue or submit a pull request for any improvements.

---

Feel free to explore the model and adapt it to your own fraud detection needs!
