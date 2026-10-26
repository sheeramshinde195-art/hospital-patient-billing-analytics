# 🏥 Hospital Patient & Billing Analytics

> **Turning hospital data into actionable insights for better patient experience, operational efficiency, and financial visibility.**

## 📌 Project Overview

This healthcare analytics project explores patient demographics, hospital visits, waiting times, patient satisfaction, and billing performance.

Using Python and exploratory data analysis (EDA), it transforms raw hospital datasets into meaningful insights to support data-driven decision-making.

**Workflow:** Business Problem → Data Cleaning → Feature Engineering → EDA → Insights → Recommendations

## 🎯 Business Objectives

- **Patient Demographics:** Analyze age groups, cities, and insurance distribution.
- **Healthcare Demand:** Explore chronic conditions and visit patterns.
- **Department Performance:** Compare demand and waiting times across departments.
- **Patient Satisfaction:** Examine satisfaction across waiting-time groups.
- **Financial Analysis:** Understand billing amounts, insurance coverage, and payment statuses.
- **Business Recommendations:** Identify opportunities to improve hospital operations.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Python | Data analysis |
| Pandas | Data cleaning and manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| SciPy | Statistical analysis |
| Jupyter Notebook | Interactive analysis |
| SQL, Excel, Power BI | Further analysis and reporting |

*Python is the primary analysis tool documented in this project. Other tools should be listed as completed components only when their work is available.*

## 📂 Dataset Description

### `patients.csv`
Patient demographics and health information, including `patient_id`, `gender`, `age`, `city`, `blood_group`, `insurance_status`, `chronic_condition`, `bmi`, and `registration_date`.

### `visits.csv`
Hospital visit details, including `visit_id`, `patient_id`, `visit_date`, `department`, `diagnosis`, `visit_type`, `waiting_time_minutes`, `length_of_stay_days`, and `satisfaction_score`.

### `billing.csv`
Billing and payment details, including `bill_id`, `visit_id`, `patient_id`, `bill_amount`, `insurance_covered_amount`, `patient_paid_amount`, `payment_method`, and `payment_status`.

### 🔗 Data Relationships

- `patients.patient_id` → `visits.patient_id`
- `visits.visit_id` → `billing.visit_id`
- `billing.patient_id` → `patients.patient_id`

These relationships enable integrated analysis of patient, visit, and billing data.

## 🧹 Data Cleaning & Preprocessing

- Inspected dataset structure, data types, missing values, and duplicates.
- Standardized gender and city values.
- Converted date and numeric columns to appropriate data types.
- Identified invalid ages and BMI values.
- Handled missing values using context-aware strategies.
- Applied median imputation where appropriate.
- Validated duplicate records and dataset relationships.
- Merged related datasets for analysis.

## 📊 Exploratory Data Analysis (EDA)

- **Patient Analytics:** Age groups, chronic conditions, insurance mix, and city distribution.
- **Operational Analytics:** Average and median waiting times, long-wait percentages, and department comparisons.
- **Patient Experience:** Satisfaction patterns across waiting-time groups.
- **Billing Analytics:** Billing amounts, insurance coverage, patient payments, and payment statuses.

## 🔍 Preliminary Key Findings

The notebook reports the following observations, which should be revalidated after final data cleaning.

| Metric | Reported Result |
|---|---:|
| Highest-contributing age group | 40–60 years |
| Visits in that age group | Approximately 3,682 |
| Most frequent chronic condition | Hypertension |
| Visits associated with hypertension | Approximately 2,225 |
| Insured share of visits | Approximately 49.9% |
| Average waiting time | Approximately 45.4 minutes |
| Median waiting time | Approximately 44.5 minutes |
| Visits with waiting time over 60 minutes | Approximately 15.2% |
| Visits from Hyderabad | Approximately 5,225 |

These are preliminary observations, not independently audited final results.

## 💡 Business Insights & Recommendations

1. **Waiting-Time Management:** Compare waiting times across departments and visit types to identify operational bottlenecks.
2. **Chronic-Care Planning:** Use condition trends to support follow-up and preventive-care planning.
3. **Capacity Planning:** Analyze visit patterns by age group and city.
4. **Patient Satisfaction:** Investigate satisfaction patterns across waiting-time groups without assuming causation.
5. **Financial Visibility:** Monitor billing, insurance coverage, patient payments, and outstanding payments.

## 📈 Project Workflow

1. Load the three CSV datasets.
2. Inspect data quality and structure.
3. Clean missing, duplicate, and invalid records.
4. Integrate datasets using common identifiers.
5. Create features such as age groups and waiting-time bands.
6. Perform EDA and create visualizations.
7. Interpret findings and develop recommendations.

## 📁 Repository Structure

```text
hospital-patient-billing-analytics/
├── hospital_patient_billing_analytics.ipynb
├── patients.csv
├── visits.csv
├── billing.csv
└── README.md
```

Update the notebook filename if yours differs.

## ▶️ How to Run

**Prerequisites:** Python 3.x and Jupyter Notebook.

**1. Clone the repository**

```bash
git clone https://github.com/YOUR-USERNAME/hospital-patient-billing-analytics.git
cd hospital-patient-billing-analytics
```

**2. Install the libraries**

```bash
pip install pandas numpy matplotlib scipy jupyter
```

**3. Launch Jupyter Notebook**

```bash
jupyter notebook
```

Open the notebook and execute its cells in order. Keep the CSV files in the same directory unless you update their paths.

## 🚀 Future Enhancements

- Build an interactive Power BI dashboard.
- Add SQL queries for operational and billing analysis.
- Create Excel reports using PivotTables and charts.
- Automate data-quality checks
