# Hospital Patient Data Analysis — SQL & Power BI

## Project Overview

This project analyzes a synthetic dataset of 1,000 hospital patient records using SQL and Microsoft Power BI.

The goal was to explore patient demographics, diagnoses, hospital departments, admission patterns, treatment types, length of stay, and patient outcomes.

The project demonstrates an end-to-end healthcare data analysis workflow:

**Data → SQL Analysis → Power BI Dashboard → Insights**

> **Note:** This dataset is synthetic and does not represent real patients or real hospital statistics.

---

## Questions Explored

The analysis focused on questions such as:

* Which diagnoses were most common in the dataset?
* Which hospital departments had the highest patient volumes?
* How were patients distributed by age and gender?
* What were the most common admission types?
* Which treatment types were most frequently recorded?
* What were the patient outcomes?
* Which departments had the longest average length of stay?
* Which diagnoses were associated with longer average stays?
* How did admissions change over time?
* How did outcomes vary by admission type?
* What were the overall patient and hospital-level KPIs?

---

## Dataset

The dataset contains **1,000 synthetic patient records** with the following fields:

| Column           | Description                      |
| ---------------- | -------------------------------- |
| `patient_id`     | Unique patient identifier        |
| `age`            | Patient age                      |
| `gender`         | Patient gender                   |
| `diagnosis`      | Primary diagnosis                |
| `department`     | Hospital department              |
| `admission_date` | Date of admission                |
| `discharge_date` | Date of discharge                |
| `length_of_stay` | Number of days spent in hospital |
| `admission_type` | Emergency, Elective, or Referral |
| `treatment_type` | Recorded treatment category      |
| `outcome`        | Patient outcome                  |

---

## Tools Used

* **MySQL** — data storage, validation, querying, and analysis
* **Power BI** — interactive dashboard and data visualization
* **SQL** — aggregation, filtering, grouping, conditional logic, and KPI calculations

---

## Data Validation

Before analysis, the dataset was checked for:

* Duplicate patient IDs
* Missing values
* Invalid age ranges
* Invalid length-of-stay values
* Inconsistent discharge and admission dates
* Incorrect diagnosis-to-department mappings

The dataset contained:

* **1,000 unique patient records**
* **No missing values**
* **No duplicate patient IDs**
* Length of stay consistent with admission and discharge dates

---

## Key Findings

### Patient Demographics

* Average patient age: **50.73 years**
* Age range: **2–90 years**
* Female patients: **524**
* Male patients: **476**

### Diagnoses

The most frequently recorded diagnoses were:

| Diagnosis            | Patients |
| -------------------- | -------: |
| Hypertension         |      221 |
| Diabetes             |      172 |
| Pneumonia            |      164 |
| Malaria              |      156 |
| Asthma               |      143 |
| Peptic Ulcer Disease |       85 |
| Sickle Cell Disease  |       59 |

These figures describe this **synthetic dataset only** and should not be interpreted as estimates of disease prevalence.

### Department Volume

| Department       | Patients |
| ---------------- | -------: |
| Respiratory      |      307 |
| Cardiology       |      221 |
| Endocrinology    |      172 |
| General Medicine |      156 |
| Gastroenterology |       85 |
| Hematology       |       59 |

### Patient Outcomes

| Outcome                     | Patients |
| --------------------------- | -------: |
| Discharged                  |      763 |
| Referred for Follow-up      |      121 |
| Transferred                 |       81 |
| Left Against Medical Advice |       35 |

The overall discharge rate in the synthetic dataset was **76.30%**.

### Length of Stay

Overall average length of stay was **6.39 days**.

Departments with longer average stays included:

* Hematology — **14.22 days**
* Gastroenterology — **8.13 days**
* Endocrinology — **6.33 days**
* Respiratory — **6.29 days**
* General Medicine — **5.89 days**
* Cardiology — **4.17 days**

---

## Power BI Dashboard

The Power BI report contains two main pages.

### Executive Dashboard

The dashboard provides an overview of:

* Total patients
* Average age
* Average length of stay
* Discharged patients
* Patient volume by department
* Diagnosis distribution
* Monthly admissions
* Patient outcomes
* Admission types
* Average length of stay by department

### Interactive Patient Analysis

The second page allows users to interactively filter the dataset using:

* Department
* Admission type
* Gender
* Diagnosis

It also includes dynamic KPIs, diagnosis analysis, outcomes by admission type, and a patient-level data table.

---

## Project Structure

```text
Hospital-Patient-Data-Analysis/
│
├── data/
│   └── hospital_patient_data.csv
│
├── sql/
│   └── hospital_patient_analysis.sql
│
├── powerbi/
│   └── Hospital_Patient_Analysis.pbix
│
├── screenshots/
│   ├── executive_dashboard.png
│   └── interactive_analysis.png
│
└── README.md
```

---

## Reproducing the Analysis

1. Import the CSV dataset into MySQL.
2. Create the `hospital_analysis` database and `patients` table.
3. Run the SQL validation queries.
4. Run the analysis queries in `hospital_patient_analysis.sql`.
5. Open the Power BI report to explore the dashboard and interactive analysis.

---

## Disclaimer

This project was created for educational and portfolio purposes using synthetic healthcare data.

No real patient information is included.
