# Churn Analysis and Prediction Dashboard

## 📝 Brief One Line Summary
End-to-end customer churn analysis and prediction system using SQL Server, Power BI, and Machine Learning.

## 📌 Overview
This project addresses customer attrition by developing a robust churn analysis pipeline. The system integrates an ETL process in SQL Server, exploratory data analysis, visualizations in Power BI, and customer churn prediction using a machine learning model (Random Forest). This helps businesses identify customers likely to churn and implement strategies to retain them.

## ❓ Problem Statement
Customer retention is more cost-effective than acquiring new customers. This project aims to:
- Understand the profile of churned customers.
- Explore data across demographic, geographic, service, and account levels.
- Predict future churners using historical data and help businesses take proactive steps to reduce churn.

## 📊 Dataset
The dataset includes:
- Demographic data: Age, Gender, Marital Status
- Account info: Contract type, Payment Method, Monthly Charges, Tenure
- Services: Internet, Streaming, Backup, etc.
- Churn-related data: Customer Status, Churn Reason, Churn Category

Sources: CSV file loaded into SQL Server using import wizard.

## 🛠️ Tools and Technologies
- **SQL Server** (ETL and data cleaning)
- **Power BI** (Dashboard and visualization)
- **Python (Jupyter Notebook)** (Machine Learning - Random Forest)
- **Libraries**: Pandas, NumPy, Seaborn, Scikit-learn, Joblib

## 🔍 Methods

### ETL in SQL Server
- Created database and imported CSV
- Staged and cleaned data using SQL
- Handled NULLs, added derived columns, and inserted cleaned data into production table
- Created two views:
  - `vw_ChurnData` – for historical churned/stayed customers
  - `vw_JoinData` – for newly joined customers (used for prediction)

### Power BI Data Transformations
- Created Age Group, Tenure Group mapping tables
- Added derived columns (Churn Status, Monthly Charge Range)
- Unpivoted service columns for flexible visualization

### Model Creation in Python
- Encoded categorical data
- Trained a Random Forest Classifier
- Evaluated with accuracy, confusion matrix, and classification report
- Predicted churn for newly joined customers and saved results

## 📈 Key Insights
- Older customers and those with shorter tenures are more likely to churn
- Customers with contracts < 12 months and paperless billing showed higher churn
- Certain states showed more attrition
- Streaming services and payment methods correlate with churn

## 📊 Dashboard/Model/Output

### Power BI Summary Page:
- KPIs: Total Customers, New Joiners, Total Churn, Churn Rate
- Charts by: Gender, Age Group, Tenure Group, Payment Method, State
- Churn Category and Reasons
- Services used vs Churn

### Prediction Page:
- Grid of at-risk customers
- Churn breakdown by demographic, account info, and geographic dimensions

## ▶️ How to Run this Project?

### SQL Setup:
1. Import CSV into SQL Server using import wizard
2. Run SQL scripts to clean and prepare data
3. Create views `vw_ChurnData` and `vw_JoinData`

### Machine Learning:
1. Load Excel file in Jupyter (exported from SQL views)
2. Run the Python script to train model and predict churn
3. Save predictions to CSV

### Power BI:
1. Connect Power BI to SQL Server or CSV
2. Create custom columns and measures
3. Build pages as described above

## ✅ Results & Conclusion
- The Random Forest model accurately predicted future churners
- Business can now focus campaigns on high-risk segments
- Dashboard gives comprehensive insight into churn behavior

## 🚀 Future Work
- Improve model with more features (sentiment, support tickets)
- Automate model retraining using pipeline
- Add real-time dashboard alerts

## 👨‍💻 Author & Contact
**Name:** Pranav Soni  
**Email:** pranavsoni9596@gmail.com  
**GitHub:** [@pranavsoni95](https://github.com/pranavsoni95)  
**LinkedIn:** [Pranav Soni](https://www.linkedin.com/in/pranav-soni-826a43222/)  
**Date:** August 05, 2025
