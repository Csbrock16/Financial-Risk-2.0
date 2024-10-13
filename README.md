# Financial Risk

### Project Review 

The Financial Risk Assessment Dataset provides detailed information on individual financial profiles. It includes demographic, financial, and behavioral data to assess financial risk.

### Data Source

Financial Risk Assessment: The primary dataset used for this analysis is the "financial_risk_assessment.csv" containing detailed information pertaining financial risk.

### Tools

- Excel - Dashboarding
- SQL Server - Data Analysis
- Tableau - Visualization

### Data Preparation

1. Import the necessary data into Excel
2. Set up your workbook
3. Add raw data to a table
4. Data analysis
5. Determine the visuals

### Exploratory Data Analysis (EDA) 

EDA involved exploring the financial risk to answer key questions, such as: 

What could go wrong? 
What is the likelihood of occurrence?
What would be the impact?
How can the business recover?

### Data Analysis

SELECT
    Age,
    Gender,
    Education_Level,
    Marital_Status,
    Income,
    AVG(Credit_Score) AS Avg_Credit_Score,
    AVG(Loan_Amount) AS Avg_Loan_Amount,
    Loan_Purpose,
    Employment_Status,
    AVG(Years_at_Current_Job) AS Avg_Years_at_Current_Job,
    AVG(Payment_History) AS Avg_Payment_History,
    AVG(Debt_to_Income_Ratio) AS Avg_Debt_to_Income_Ratio,
    AVG(Assets_Value) AS Avg_Assets_Value,
    SUM(Number_of_Dependents) AS Total_Dependents,
    City,
    State,
    Country,
    SUM(Previous_Defaults) AS Total_Previous_Defaults,
    AVG(Marital_Status_Change) AS Avg_Marital_Status_Change,
    AVG(Risk_Rating) AS Avg_Risk_Rating

FROM
    financial_data

GROUP BY
    Age,
    Gender,
    Education_Level,
    Marital_Status,
    Income,
    Loan_Purpose,
    Employment_Status,
    City,
    State,
    Country

ORDER BY
    Age, Gender, Education_Level, Marital_Status;

### Results/Findings 
Figured Out: 
  - the failure, how to succeed, and where the business is vulnerable.
  - each risk to determine how likely it is to happen.
  - how much the risk would impact the business if it occurred.
  - what steps can the business take to recover?  
