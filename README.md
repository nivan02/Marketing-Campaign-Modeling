# 📈 Customer Response Prediction – Direct Mail Campaign

This project focuses on predicting **customer responses to a direct mail campaign** and optimizing which customers should be targeted in a second wave of outreach. The work involved **building predictive models, evaluating profitability, and generating actionable mailing lists** that balance cost with expected returns.

---

## 📌 Project Overview

A large dataset of small business customers was provided, along with historical response data from the first wave of a marketing campaign. The task was to:

- Predict which customers were most likely to respond in a **second wave of mailings**.  
- Optimize the mailing strategy under budget and profitability constraints.  
- Generate a list of customer IDs to target, ensuring maximum return on investment.  

Key challenges included class imbalance (few responders vs. many non-responders), cost of mailing per customer, and the requirement to estimate **profit impact** of the mailing decision.

---

## 🔍 Methodology

1. **Data Preprocessing**  
   - Cleaned customer demographics and transaction history.  
   - Created engineered features such as recency of purchase and engagement bins.  
   - Addressed missing values and standardized categorical variables.  

2. **Model Development**  
   - Logistic Regression with L1 regularization (Lasso) for feature selection.  
   - Neural Network models for capturing complex non-linear relationships.  
   - Comparison of models based on **AUC, precision-recall, lift, and expected profit**.  

3. **Profit Optimization**  
   - Incorporated mailing costs and net revenue per responder.  
   - Applied a 50% adjustment factor to predicted probabilities to account for lower second-wave response.  
   - Selected the cutoff point that maximized **expected profit** rather than accuracy alone.  

4. **Evaluation**  
   - Split data into training and test sets (70/30).  
   - Conducted model performance comparison and sensitivity analysis.  
   - Scaled results to the full population of customers for final mailing recommendations.  

---

## 📂 Repository Contents

- `Analysis_Notebook.ipynb` – Python notebook with full modeling pipeline.  
- `customer_wave2.csv` – Output file with mailing recommendations (True/False).  
- `Report.pdf` – Executive summary of findings and recommendations.  

---

## 🛠️ Tools & Libraries

- **Python**: pandas, numpy, matplotlib, seaborn  
- **scikit-learn**: Logistic Regression, Neural Networks, evaluation metrics  
- **imbalanced-learn**: Techniques for class imbalance handling  
- **Custom evaluation metrics**: Profit, Lift, AUC  

---

