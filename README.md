# HR Analytics — Employee Attrition Analysis

## 📌 Project Overview

This project performs **HR Analytics and Exploratory Data Analysis (EDA)** on employee data to identify patterns related to **employee attrition, salary, overtime, job satisfaction, departments, job roles, and work experience**.

The analysis is implemented in Python using **Pandas, NumPy, Matplotlib, and Seaborn**. The workflow covers data loading, preprocessing, cleaning, filtering, aggregation, exploratory analysis, visualization, and extraction of HR-related insights.

## 🎯 Objectives

- Understand the structure and characteristics of the HR dataset.
- Clean and preprocess employee data.
- Identify and handle missing values and duplicate records.
- Remove irrelevant columns where appropriate.
- Analyze employee attrition patterns.
- Compare employee groups based on department, overtime, income, distance from work, and job role.
- Calculate group-level HR metrics using aggregation.
- Visualize important employee and attrition patterns.
- Derive actionable insights that can support HR decision-making.

## 📂 Project Structure

```text
HR-Analytics/
│
├── HR_Analysis.ipynb       # Main analysis notebook
├── HR_Analytics.csv        # HR employee dataset
└── README.md               # Project documentation
```

> **Note:** The notebook currently loads `HR_Analytics.csv` from a Google Drive path in Google Colab. Update the file path if you are running the project locally.

## 🗃️ Dataset

The dataset contains employee-level HR information with **38 columns**, including attributes such as:

- Employee ID
- Age and Age Group
- Attrition
- Business Travel
- Department
- Distance From Home
- Education and Education Field
- Job Role
- Monthly Income
- OverTime
- Job Satisfaction
- Relationship Satisfaction
- Total Working Years
- Years at Company
- Years in Current Role
- Years Since Last Promotion
- Years With Current Manager
- Work-Life Balance

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data analysis and programming |
| Pandas | Data loading, cleaning, filtering and aggregation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Google Colab | Notebook execution environment |

## 🔄 Analysis Workflow

```text
Dataset
   ↓
Loading
   ↓
Initial Overview
   ↓
Data Cleaning & Preprocessing
   ↓
Duplicate Removal
   ↓
Irrelevant Column Removal
   ↓
Filtering
   ↓
Aggregation
   ↓
EDA
   ↓
Visualization
   ↓
Insights & Conclusion
```

## 🧹 Data Preprocessing

The project checks the dataset for missing values and performs data cleaning before analysis.

The notebook identifies missing values using Pandas and handles missing values in `YearsWithCurrManager` using a median-based replacement.

The cleaning process also includes duplicate removal and removal of irrelevant columns where required.

## 🔎 Filtering

The analysis creates focused employee groups using conditions such as:

- Employees who left the company: `Attrition == 'Yes'`
- Employees working overtime: `OverTime == 'Yes'`
- Employees with high monthly income: `MonthlyIncome > 10000`
- Employees living more than 10 units away from the workplace: `DistanceFromHome > 10`

These filters help examine specific employee segments and their HR characteristics.

## 📊 Aggregation

Group-wise analysis is performed using Pandas aggregation functions such as `groupby()`, `mean()`, `count()`, and `sum()`.

Examples include:

- Number of employees by department
- Average monthly income by department
- Average monthly income by job role
- Attrition by department
- Attrition by overtime status
- Average job satisfaction by department

## 📈 Exploratory Data Analysis & Visualization

The project uses Matplotlib and Seaborn to visualize employee and HR patterns.

Visualizations include:

- Employee Attrition Distribution
- Employees by Department
- Attrition-related comparisons
- Department-level analysis
- Job-role-level attrition analysis
- Salary and income comparisons
- Job satisfaction analysis

These visualizations make it easier to identify relationships and differences across employee groups.

## 💡 Key Analysis Areas

The notebook focuses particularly on:

### Employee Attrition
Examines which employee groups are more likely to leave the organization.

### Overtime
Compares attrition patterns between employees who work overtime and those who do not.

### Income
Analyzes monthly income across departments and job roles and examines high-income employee groups.

### Job Satisfaction
Compares job satisfaction across departments.

### Department & Job Role
Examines employee distribution and attrition across different organizational groups.

### Experience
Uses total working years, years at the company, current-role tenure, promotion history, and manager tenure as part of the HR analysis.

## 🧪 Example Pandas Operations

```python
# Check missing values
df.isnull().sum()

# Filter employees who left
df[df["Attrition"] == "Yes"]

# Filter overtime employees
df[df["OverTime"] == "Yes"]

# Department-wise employee count
df.groupby("Department").size()

# Average income by department
df.groupby("Department")["MonthlyIncome"].mean()

# Attrition by department
pd.crosstab(df["Department"], df["Attrition"])
```

## 📌 Outcome

The project demonstrates an end-to-end **HR data analysis workflow** using Python. It transforms raw employee data into structured summaries and visualizations that can help identify patterns in **attrition, income, overtime, job satisfaction, department, job role, and employee experience**.

## 🚀 How to Run

### 1. Clone or download the project

Place the following files in the same project directory:

```text
HR_Analysis.ipynb
HR_Analytics.csv
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

### 3. Open the notebook

```bash
jupyter notebook HR_Analysis.ipynb
```

Or open the notebook in **Google Colab**.

### 4. Update the dataset path

For local execution:

```python
file_path = "HR_Analytics.csv"
```

For Google Colab with Google Drive:

```python
file_path = "/content/drive/MyDrive/HR_Analytics.csv"
```

## 📚 Skills Demonstrated

- Data Cleaning
- Data Preprocessing
- Missing Value Handling
- Duplicate Detection and Removal
- Data Filtering
- GroupBy and Aggregation
- Exploratory Data Analysis
- Data Visualization
- HR Analytics
- Business Insight Generation
- Python Data Analysis

## 👨‍💻 Author

**Evan Punnen Jacob**

B.Tech Computer Science & Engineering

---

**Project Type:** Data Analysis / HR Analytics  
**Primary Language:** Python  
**Notebook:** `HR_Analysis.ipynb`
