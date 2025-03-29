## Project Overview
Hospital readmissions are costly and often preventable. This project analyzes hospital readmission patterns using patient encounter data, with the goal of identifying high-risk groups and proposing actionable interventions. It also includes a predictive modeling component to improve early identification of patients at risk of readmission.

## Objectives
- Identify key factors associated with hospital readmission
- Provide actionable suggestions for reducing readmission rates
- Build and improve predictive models to flag high-risk patients early

## Data
- **Source**: [UCI Diabetes Readmission Dataset](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008)
- **Size**: 100,000+ patient records
- **Key variables**:
  - `number_inpatient`: Number of inpatient visits in the past year
  - `number_outpatient`: Number of outpatient visits
  - `discharge_disposition_id`: Discharge destination
  - `readmitted`: Whether the patient was readmitted within 30 days
## Analysis
Exploratory data analysis revealed that **patients with ≥4 inpatient visits in the past year** have significantly higher readmission rates.

- Patients with `number_inpatient >= 4` were defined as the **high-risk group**
- A chi-squared test confirmed that readmission rates between high-risk and non-high-risk groups were **statistically significantly different**

### Key Findings

1. **High-risk patients have ~3x higher readmission rates**
   - Readmission:  
     - High-risk group: **32%**  
     - Others: **~11%**
   - 📊 *Chi-squared test showed a statistically significant difference*

2. **Follow-up care appears insufficient**
   - Average number of outpatient visits in high-risk group: **< 1**
   - Despite being high-risk, patients aren't receiving enough post-discharge care

3. **Home discharge is common among high-risk patients**
   - **71.3%** of high-risk patients are discharged to home
   - Of these, **32%** are readmitted → indicates need for better follow-up programs

### Recommendations
Based on the insights above, the following strategies are proposed:

- Implement **automatic follow-up appointment scheduling** for high-risk patients
- Provide **discharge education and case manager support** at the point of discharge
- Introduce a **post-discharge phone check-in system** targeting high-risk home discharge patients

## Predictive Model (In Progress)
A predictive model is being developed using:

- Logistic Regression, Random Forest, and other classifiers

The goal is to **identify at-risk patients earlier**, allowing hospitals to intervene before readmission occurs.

## Project Structure
