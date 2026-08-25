# 👥 HR Analytics & Employee Churn Analysis

An end-to-end **HR Analytics project** focused on analyzing employee attrition, workforce dynamics, compensation fairness, and employee flight risk at **XDA**, a mid-sized technology company undergoing strategic expansion.

The project combines **Python-based exploratory data analysis (EDA), statistical analysis, ad-hoc business analytics, SQL analysis, and Power BI visualization** to provide HR leaders with actionable insights for improving employee retention, satisfaction, compensation, and organizational health.

## 📊 Project Overview

The analysis focuses on answering key HR business questions such as:

- What is the overall employee churn rate?
- Which departments have the highest churn?
- Which job roles have the highest turnover?
- Is there a relationship between overtime and employee churn?
- How does employee satisfaction relate to attrition?
- Does higher performance correspond to higher compensation?
- Which tenure groups are most likely to leave?
- Are there potential compensation fairness issues?
- Which employees may be at higher flight risk?
- Does manager feedback correlate with promotions and retention?
- Which hiring cohorts have the highest churn?

---

## 🔗 Dashboard

[View the live Power BI dashboard](https://app.powerbi.com/view?r=eyJrIjoiM2M1Mzk5MzEtMDhhZi00NDdkLTk0NmMtNjQ3MWY2ZDQyMDU3IiwidCI6IjM3MGZiM2I4LTMzMDYtNDg5MC05MDYzLWNjMDhiZTc4ODI1NyIsImMiOjEwfQ%3D%3D)

The Power BI dashboard provides an interactive overview of employee attrition patterns across demographic, organizational, and workforce dimensions.

### Key Dashboard Features

- Total employees, retained employees, and attritted employees
- Overall employee turnover rate
- Turnover rate by department
- Turnover rate by job role
- Turnover rate by gender and marital status
- Employee age distribution
- Attrition breakdown by department and job role
- Interactive filtering and drill-through analysis
- Workforce and retention indicators

---

## 🧹 Data Preparation

The employee dataset contains information covering:

- Employee demographics
- Job role and department
- Employment tenure
- Compensation
- Performance
- Training
- Overtime
- Satisfaction
- Absenteeism
- Manager feedback
- Promotions
- Employee churn

### Data Cleaning

The analysis includes preparation steps such as:

- Loading the employee dataset using Pandas
- Inspecting dataset structure using `info()`
- Checking unique values
- Checking duplicated records
- Checking missing values
- Removing the `work_life_balance` column
- Converting variables to appropriate data types
- Creating derived analytical features such as:
  - `tenure_band`
  - `performance_band`
  - `feedback_band`
  - `tenure_decile`
  - `hire_year`
  - `risk_score`

---

## 🔍 Exploratory Data Analysis

The project uses Python for exploratory analysis before building the dashboard.

### Distribution Analysis

Distribution analysis is performed for numerical variables using:

- Histograms
- KDE plots
- Boxplots

This helps identify:

- Data distribution
- Central tendency
- Skewness
- Potential outliers
- Differences in workforce characteristics

Employee churn distribution is also analyzed using count plots and percentage breakdowns.

### Correlation Analysis

Pearson correlation is used to investigate relationships between numerical variables.

A correlation heatmap is created to examine relationships between variables such as:

- Satisfaction level
- Overtime hours
- Salary
- Performance rating
- Absenteeism
- Promotions
- Tenure
- Average monthly working hours
- Manager feedback score
- Churn

Categorical variables are also encoded using one-hot encoding to enable additional correlation analysis.

> **Note:** Correlation indicates statistical association and does not by itself establish causation.

---

## 🧠 Ad-hoc HR Analytics

The notebook also answers a series of real-world HR business questions.

### 1. Overall Churn Rate

Calculates the percentage of employees who have left the company.

**Business question:**  
> What is the company's overall employee churn rate?

### 2. Churn by Department

Calculates:

- Total employees
- Churned employees
- Churn rate

for each department.

This helps identify departments experiencing particularly high employee turnover.

### 3. Compensation Analysis by Job Role

For every job role, the analysis calculates:

- Number of employees
- Average salary
- Minimum salary
- Maximum salary
- Salary range

This provides a foundation for compensation auditing.

### 4. Gender × Churn Analysis

Creates an employee matrix by:

- Gender
- Churn status

and calculates churn rates for each gender group.

This allows HR teams to investigate potential differences in employee retention.

### 5. Tenure × Churn Analysis

Employees are divided into four tenure groups:

- **Under 1 year**
- **1–3 years**
- **3–5 years**
- **Over 5 years**

Churn rate is then calculated for each group to identify the stages of the employee lifecycle where attrition is highest.

### 6. Performance × Compensation Analysis

Performance ratings are grouped into:

- **Low:** 1–2
- **Medium:** 3
- **High:** 4–5

The analysis compares:

- Number of employees
- Average salary
- Minimum salary
- Maximum salary
- Churn rate

This helps investigate whether compensation reflects employee performance.

### 7. Overtime × Churn Analysis

Employees are segmented according to overtime hours to investigate whether excessive overtime is associated with higher employee churn.

This analysis supports investigation of potential **workload and burnout risks**.

### 8. Absenteeism Analysis

Departments are ranked according to average absenteeism.

The analysis identifies:

- Average absenteeism
- Maximum absenteeism
- Number of employees
- Churn rate

This can help HR identify departments requiring further workforce investigation.

### 9. Manager Feedback × Promotion Analysis

Manager feedback scores are divided into:

- **Low:** 1–4
- **Medium:** 5–7
- **High:** 8–10

For each group, the analysis evaluates:

- Average number of promotions
- Average salary
- Churn rate

This supports an investigation into potential **performance evaluation and promotion fairness**.

### 10. Potential Flight Risk Employees

Employees whose salary is **more than 25% below the average salary for their job role** are flagged as potential flight-risk employees.

The analysis compares:

- Employee salary
- Role average salary
- Salary gap %
- Performance rating
- Churn status

This provides a starting point for compensation review and retention intervention.

### 11. Tenure Decile Analysis

Employees are divided into **10 tenure deciles** using `pandas.qcut()`.

For each decile, the analysis calculates:

- Minimum tenure
- Maximum tenure
- Number of employees
- Churned employees
- Churn rate

This helps identify potential **retention sweet spots** and periods of elevated attrition.

### 12. Employee Composite Risk Score

A composite employee risk score is created using:

- Overtime
- Satisfaction
- Absenteeism
- Promotions

Each factor is converted into a score and combined into an overall:

**Employee Risk Score**

The top 100 employees with the highest risk scores are then identified for potential early intervention.

> This score is an analytical prioritization tool, not a definitive prediction of employee behavior.

### 13. Hiring Cohort Analysis

Employee tenure is used to derive an estimated `hire_year`.

The analysis calculates churn rates by hiring cohort to determine whether particular cohorts experienced significantly different retention outcomes.

### 14. Compensation Fairness / Underpaid Employees

Employees whose salary is **more than 10% below the average salary of their job role** are flagged for compensation review.

The analysis provides:

- Employee ID
- Job role
- Department
- Current salary
- Peer average salary
- Salary gap %
- Performance rating
- Churn status

This can help identify potential compensation inequities and retention risks.

---

## 🛠️ Tools & Technologies

### Python

- **Pandas** – data manipulation and analysis
- **NumPy** – numerical computation
- **Matplotlib** – data visualization
- **Seaborn** – statistical visualization
- **Jupyter Notebook** – exploratory analysis and documentation

### SQL

SQL queries are used to reproduce and validate several HR business analyses, including:

- Churn rate
- Department turnover
- Compensation analysis
- Gender × churn
- Tenure cohorts
- Performance bands
- Employee risk scoring
- Compensation gaps

### Power BI

- Advanced DAX
- Interactive dashboard design
- Data visualization
- Filtering and drill-through
- HR KPI reporting
- Dark-mode dashboard UI

### Power Query

Used for:

- Data cleaning
- Data transformation
- Data shaping
- Preparing data for dashboard analysis

---

## 📈 Analytical Workflow

```text
Raw Employee Dataset
        ↓
Data Cleaning & Validation
        ↓
Exploratory Data Analysis
        ↓
Distribution Analysis
        ↓
Correlation Analysis
        ↓
Ad-hoc HR Business Questions
        ↓
Feature Engineering
        ↓
Risk & Compensation Analysis
        ↓
Power BI Dashboard
        ↓
HR Insights & Recommendations
```

---

## 💡 Business Value

The project provides HR teams with a data-driven framework to:

- Identify high-turnover departments and job roles
- Understand employee attrition patterns
- Identify potential retention risks
- Investigate overtime and workload issues
- Evaluate compensation fairness
- Examine the relationship between performance and compensation
- Identify potential underpaid employees
- Prioritize employees for retention intervention
- Analyze workforce trends across tenure and hiring cohorts
- Support evidence-based HR policy decisions

---

## 📂 Project Files

```text
HR-Analytics/
│
├── HR_churn_Analyst.ipynb
├── employee_churn.csv
├── HR_Analytics_Dashboard.pbix
├── preview.png
└── README.md
```

### File Description

| File | Description |
|---|---|
| `HR_churn_Analyst.ipynb` | Python EDA, correlation analysis, ad-hoc HR analytics and risk analysis |
| `employee_churn.csv` | Employee-level HR dataset |
| `HR_Analytics_Dashboard.pbix` | Interactive Power BI dashboard |
| `preview.png` | Dashboard preview |
| `README.md` | Project documentation |

---

## 🚀 Key Takeaway

This project demonstrates an end-to-end **HR Data Analytics workflow**, combining **Python, SQL, and Power BI** to transform employee-level data into actionable insights.

The analysis goes beyond simply reporting employee churn by investigating **why attrition may occur, which employee groups are most exposed to risk, and where HR teams can focus retention and compensation efforts.**
