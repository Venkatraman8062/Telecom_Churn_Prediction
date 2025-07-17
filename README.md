📊 Business Objective
To identify customers at risk of churn before they actually leave — specifically, by analyzing usage data from months 6, 7, and 8 and predicting churn behavior in month 9. This helps telecom providers proactively retain customers, optimize offers, and improve service quality.

🧠 Key Highlights
📌 Identified "High-Value Customers" using average recharge amount in months 6 & 7

🧹 Cleaned and preprocessed telecom data (~100+ features)

📉 Engineered churn label based on customer inactivity in month 9

🔎 Handled multicollinearity with VIF and correlation matrix

⚙️ Feature selection using Random Forest and RFE

🤖 Trained multiple models – Logistic Regression, Random Forest (with SMOTE)

📈 Achieved 60%+ accuracy post-class imbalance handling

🏆 Ranked top 10 churn predictors, with roam_ic_mou_8 being the most influential

🗂️ Project Structure
bash
Copy
Edit
├── telecom_churn_data.csv        # Input dataset
├── telecom_churn_prediction.ipynb # Full code and analysis
├── README.md                     # Project documentation (you're here!)
🔬 Data Preparation
Removed constant and irrelevant features

Parsed and processed date columns

Derived features like days_since_last_rech

Filtered top 30% of high-value customers

Created a binary churn label based on inactivity

📌 Feature Engineering & Selection
Handled missing values (filled with 0)

Visualized correlations with a heatmap

Removed highly correlated and low-variance features

Scaled features using StandardScaler

Applied Variance Threshold and VIF for multicollinearity

Used Recursive Feature Elimination (RFE) with Random Forest

🧪 Model Building
1. Random Forest (Baseline)
Accuracy: ~94%, but model overfit due to class imbalance

Insight: Excellent for feature ranking, not great for generalization

2. Logistic Regression (Balanced)
Accuracy: ~82%

Class balancing handled with class_weight='balanced'

Still suffered from class imbalance

3. Random Forest + SMOTE
Accuracy: ~60%, better class balance

Best performing model in terms of churn detection

Used for final prediction and feature importance analysis

