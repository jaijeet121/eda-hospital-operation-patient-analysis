# Hospital Operations & Patient Analytics

## 🏥 Project Overview
The hospital manages tens of thousands of patient encounters every year across several care settings (ambulatory, outpatient, wellness, urgent care, emergency, and inpatient). Each encounter is billed through different payers or involves uninsured patients. This project provides a consolidated analytical view of patient volume trends, cost drivers, payer coverage efficiency, and patient behavior to help hospital management plan capacity, control costs, protect revenue, and improve the quality of care.

## 🎯 Objectives
Using four core datasets (encounters, patients, procedures, payers), this project aims to:
1. **Understand Encounter Trends:** Analyze yearly volume, the mix of encounter classes (e.g., ambulatory, emergency), and patient length of stay.
2. **Analyze Cost and Coverage:** Evaluate the share of encounters with zero payer coverage, identify the most frequent and expensive procedures, and calculate the average claim cost by payer.
3. **Study Patient Behavior:** Track quarterly inpatient admissions, 30-day readmissions, and the demographic profile (age group, city, race, gender, marital status) of the patient base.
4. **Actionable Recommendations:** Turn data findings into strategic recommendations for capacity planning, revenue protection, and readmission reduction.

## 📂 Datasets Used
The analysis relies on four relational datasets, automatically downloaded within the notebook via Google Drive (`gdown`):
* **`encounters.csv`**: Records of patient hospital visits, including encounter class, timestamps, base cost, total claim cost, and payer coverage.
* **`patients.csv`**: Patient demographic information, including birthdate, gender, race, marital status, and geographical location.
* **`payers.csv`**: Information on insurance providers and payers (e.g., Medicare, Medicaid, Dual Eligible, Private Insurance, No Insurance).
* **`procedures.csv`**: Detailed logs of medical procedures performed during patient encounters, including base costs and reason codes.

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Statistical Analysis:** `scipy`
* **File Downloading:** `gdown`

## 📊 Key Analytical Modules

### 1. Data Setup & Quality Assurance
* Data type casting (converting string dates to standard `datetime` objects).
* Null value identification and handling.
* Duplicate record checks across all relational tables.

### 2. Encounters Overview
* **Yearly Volume:** Bar chart tracking the total number of hospital encounters year-over-year.
* **Encounter Class Mix:** Stacked bar chart analyzing the percentage breakdown of encounter types (ambulatory vs. outpatient vs. emergency, etc.) over time.
* **Length of Stay:** Categorization and pie chart distribution comparing encounters lasting over 24 hours versus under 24 hours.

### 3. Cost & Coverage Insights
* **Zero Payer Coverage:** Identification of the proportion of patient visits that received absolutely no insurance coverage (e.g., identifying uncompensated care).
* **Claimed vs. Unclaimed Costs:** Financial breakdown of the total hospital claim costs versus the actual amount covered by payers.
* **Top Procedures:** Aggregation of the top 10 most frequently performed procedures and their average base costs.

## 🚀 How to Run the Project

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/hospital-operations-analytics.git](https://github.com/your-username/hospital-operations-analytics.git)
   cd hospital-operations-analytics
