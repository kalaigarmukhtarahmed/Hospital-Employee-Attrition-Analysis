# 🏥 Hospital Employee Attrition Analysis

> **Exploring the factors associated with employee attrition through Python, statistics, visualization, probability, and hypothesis testing.**

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)
![SciPy](https://img.shields.io/badge/SciPy-Statistics-8CAAE6)
![Dataset](https://img.shields.io/badge/Dataset-Synthetic-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

## 📌 Project Overview

Employee attrition is an important workforce analytics problem. Understanding the factors associated with employees leaving an organization can help demonstrate how data science can be used to explore workforce patterns.

This project performs an exploratory and statistical analysis of a **synthetic hospital employee dataset** using Python.

The analysis focuses on relationships between employee attrition and factors such as:

- 💰 Salary
- 🧑‍💼 Work experience
- ⏱️ Overtime
- 😊 Job satisfaction
- ⚖️ Work-life balance
- 📈 Performance
- 👨‍💼 Manager rating
- 🎓 Education
- 🏥 Department
- 🔄 Promotions
- 🌙 Night shifts
- 📚 Training
- 📍 Distance from home

The project goes beyond basic visualization by applying statistical methods such as **correlation analysis, conditional probability, Welch's independent two-sample t-test, and Cohen's d effect size**.

---

## 🎯 Project Objectives

The main objectives of this project are to:

1. Understand the structure of the employee dataset.
2. Calculate descriptive statistics for employee salary.
3. Analyze the distribution of monthly salaries.
4. Detect potential salary outliers using the IQR method.
5. Compare salary between employees who stayed and employees who left.
6. Compare work experience across attrition groups.
7. Analyze the relationship between overtime and attrition.
8. Examine job satisfaction across attrition groups.
9. Identify correlations between numerical variables and attrition.
10. Calculate conditional attrition probability for employees with low job satisfaction.
11. Test whether salary differences between attrition groups are statistically significant.
12. Measure the magnitude of salary differences using Cohen's d.

---

## 📊 Dataset

The project uses a **synthetically generated hospital employee dataset** containing:

- **1,000 employee records**
- **33 columns**

### Dataset Features

| Feature | Description |
|---|---|
| `Employee_ID` | Unique employee identifier |
| `Hospital` | Hospital associated with the employee |
| `Department` | Employee department |
| `Job_Level` | Employee job level |
| `Job_Role` | Employee job role |
| `Location` | Employee location |
| `Gender` | Employee gender |
| `Age` | Employee age |
| `Education` | Education level |
| `Employment_Type` | Full-time, part-time, or contract |
| `Work_Mode` | Work arrangement |
| `Shift` | Day, night, or rotational shift |
| `Years_at_Hospital` | Years spent at the hospital |
| `Years_in_Current_Role` | Years in current role |
| `Total_Work_Experience` | Total professional experience |
| `Monthly_Salary_INR` | Monthly salary |
| `Annual_Salary_INR` | Annual salary |
| `Annual_Bonus_INR` | Annual bonus |
| `Job_Satisfaction` | Job satisfaction score |
| `Work_Life_Balance` | Work-life balance score |
| `Performance_Rating` | Performance rating |
| `Overtime_Hours_Month` | Monthly overtime hours |
| `Overtime` | Overtime category |
| `Night_Shifts_Month` | Monthly night shifts |
| `Training_Hours_Year` | Annual training hours |
| `Patients_Handled_Month` | Patients handled per month |
| `Projects_Count` | Number of projects |
| `Promotions_Last_5_Years` | Promotions in the last five years |
| `Manager_Rating` | Manager rating |
| `Distance_From_Home_KM` | Distance from home |
| `Salary_Growth_Potential` | Salary growth potential |
| `Attrition_Probability` | Synthetic attrition probability |
| `Attrition` | Whether the employee left |

> **Important:** This is synthetic data created for educational and portfolio purposes. It does not represent real hospital employees, hospitals, or confidential workforce records.

---

# 🔬 Analysis Performed

## 1. Descriptive Statistics

The project calculates descriptive statistics for employee salaries, including:

- Mean
- Median
- Mode
- Variance
- Standard deviation
- Coefficient of variation

These measures provide an initial understanding of the salary distribution.

---

## 2. Salary Distribution

A histogram with KDE is used to visualize the distribution of monthly salaries.

This helps identify:

- Central tendency
- Spread
- Distribution shape
- Potential skewness
- Concentration of salaries

---

## 3. Salary Outlier Detection

Potential salary outliers are detected using the **Interquartile Range (IQR)** method.

```text
IQR = Q3 - Q1

Lower Bound = Q1 - 1.5 × IQR

Upper Bound = Q3 + 1.5 × IQR
```

A box plot is also used to visually identify extreme observations.

---

## 4. Salary vs Attrition

Monthly salary is compared between:

- Employees who stayed
- Employees who left

The analysis uses grouped statistics and visualizations to examine whether salary distributions differ between the two groups.

---

## 5. Work Experience vs Attrition

The project compares `Total_Work_Experience` across attrition groups.

This provides a simple way to examine whether employees with different levels of experience show different attrition patterns in the synthetic dataset.

---

## 6. Overtime vs Attrition

A contingency table is created using:

```text
Overtime × Attrition
```

The analysis uses normalized proportions to compare attrition patterns between employees who work overtime and those who do not.

---

## 7. Job Satisfaction vs Attrition

Average job satisfaction is compared between employees who:

- Stayed
- Left

This helps examine whether satisfaction levels differ across the two groups.

---

## 8. Correlation Analysis

The categorical target:

```text
Attrition
```

is converted into a numerical flag:

```text
Yes → 1
No  → 0
```

The project then examines correlations between numerical variables and the attrition flag.

This provides an exploratory view of which numerical variables have stronger linear relationships with attrition.

> Correlation does not establish causation.

---

## 9. Conditional Probability

The project calculates the probability of attrition among employees with low job satisfaction.

The main quantity examined is:

```text
P(Attrition | Job Satisfaction ≤ 2)
```

This is compared with the overall attrition probability.

---

## 10. Hypothesis Testing

An independent two-sample **Welch's t-test** is used to compare monthly salary between the two attrition groups.

### Null Hypothesis

```text
H₀: The mean salary is equal between the two attrition groups.
```

### Alternative Hypothesis

```text
H₁: The mean salary is different between the two attrition groups.
```

A significance level of:

```text
α = 0.05
```

is used.

The notebook reports:

- t-statistic
- p-value

---

## 11. Effect Size — Cohen's d

Statistical significance alone does not describe the practical magnitude of a difference.

Therefore, **Cohen's d** is calculated to quantify the standardized difference between salary distributions.

This complements the t-test by providing an effect-size measure.

---

# 🧰 Technologies Used

| Technology | Purpose |
|---|---|
| 🐍 Python | Core programming language |
| 🐼 Pandas | Data manipulation and analysis |
| 🔢 NumPy | Numerical operations |
| 📊 Matplotlib | Data visualization |
| 📈 Seaborn | Statistical visualization |
| 🧪 SciPy | Statistical testing |
| 📓 Jupyter Notebook | Interactive analysis |
| 🔧 Git | Version control |
| 🌐 GitHub | Project hosting |

---

# 📂 Repository Structure

```text
Hospital-Employee-Attrition-Analysis/
│
├── Hospital_Employee_Attrition_Analysis.ipynb
├── hospital_employee_attrition_dataset.csv
├── requirements.txt
└── README.md
```

### Files

### `Hospital_Employee_Attrition_Analysis.ipynb`

Contains the complete Python analysis, visualizations, statistical calculations, and hypothesis testing.

### `hospital_employee_attrition_dataset.csv`

Synthetic dataset containing 1,000 hospital employee records.

### `requirements.txt`

Contains the Python libraries required to reproduce the analysis.

### `README.md`

Project documentation.

---

# ▶️ How to Run the Project

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Hospital-Employee-Attrition-Analysis.git
```

Then:

```bash
cd Hospital-Employee-Attrition-Analysis
```

---

## 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 3. Open the Notebook

Run:

```bash
jupyter notebook
```

Then open:

```text
Hospital_Employee_Attrition_Analysis.ipynb
```

---

# ☁️ Google Colab

The notebook can also be executed using Google Colab.

Upload both:

```text
Hospital_Employee_Attrition_Analysis.ipynb
hospital_employee_attrition_dataset.csv
```

The notebook loads the dataset using:

```python
pd.read_csv("hospital_employee_attrition_dataset.csv")
```

Therefore, the CSV should be available in the notebook's working directory.

---

# 🔄 Project Workflow

```text
                  ┌──────────────────────┐
                  │   Synthetic Dataset  │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Data Understanding   │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Descriptive Analysis │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Visualization / EDA  │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Outlier Detection    │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Attrition Analysis   │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Correlation &        │
                  │ Conditional          │
                  │ Probability          │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Hypothesis Testing   │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Cohen's d Effect     │
                  │ Size Analysis        │
                  └──────────────────────┘
```

---

# 💡 Data Science Skills Demonstrated

This project demonstrates practical knowledge of:

- Data loading
- Data inspection
- Data cleaning
- Descriptive statistics
- Exploratory Data Analysis
- Data visualization
- Group-by analysis
- Outlier detection
- Categorical analysis
- Correlation analysis
- Probability
- Conditional probability
- Hypothesis testing
- Welch's t-test
- Statistical significance
- Effect-size analysis
- Python-based analytical workflows
- Reproducible project organization

---

# 🚀 Future Improvements

The project can be extended into a complete machine-learning application.

### 🤖 Machine Learning

Possible models:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

### 📊 Model Evaluation

Future versions can include:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- Cross-validation

### 🧠 Explainable AI

SHAP or other explainability techniques can be added to understand model predictions.

### 🌐 Interactive Dashboard

The analysis can be converted into a dashboard using:

- Streamlit
- Plotly
- Power BI

### ☁️ Deployment

A future version could be deployed as an interactive web application for portfolio demonstration.

---

# ⚠️ Important Modeling Note

If `Attrition` is later used as the machine-learning target, do **not** use:

```text
Attrition_Probability
```

as a model input feature.

`Attrition_Probability` was generated as part of the synthetic dataset creation process and is directly related to the attrition outcome. Including it as a feature could introduce **target leakage** and produce misleading model performance.

---

# 🔐 Data & Ethics

This project uses synthetic data.

No:

- Real employee records
- Patient information
- Medical records
- Personally identifiable information
- Confidential hospital information

are included.

The analysis is intended for:

- Academic learning
- Data-science practice
- Portfolio development
- Statistical analysis demonstrations

It should not be used for actual employee hiring, termination, compensation, or risk decisions.

---

# 📌 Project Status

```text
████████████████████████████████ 100%
```

**Completed — Exploratory & Statistical Analysis**

Future development can extend the project into a machine-learning prediction system and interactive dashboard.

---

# 👨‍💻 Author

**Kalaigar Mukhtar Ahmed**

Computer Science & Engineering

**Areas of Interest**

- Data Science
- Python
- Machine Learning
- Artificial Intelligence
- Data Analytics

---

## ⭐ Support

If you find this project useful or interesting, consider giving the repository a ⭐ on GitHub.

---

### 📄 License

This project is intended for educational and portfolio purposes.
