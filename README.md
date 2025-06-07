# Medicare Advantage vs Traditional Medicare: 2022 CSPUF Analysis

This notebook analyzes data from the 2022 Consumer Survey of Medicare Beneficiaries (CSPUF) to compare key differences between Medicare Advantage (MA) and Traditional Medicare enrollees.

## 🔍 Analysis Goals

- Compare **out-of-pocket (OOP) costs** across income levels and plan types
- Assess **utilization rates** for different healthcare services
- Examine population **health status** using chronic condition counts
- Analyze **age distribution** by plan type
- Control for confounding by comparing service use **within chronic condition groups**

## 🧮 Methodology

- Weighted analysis using the **CSPUFWGT** variable for valid population-level inference
- Comparison of:
  - Inpatient (IPAEVNTS)
  - Medical provider (MPAEVNTS)
  - Outpatient (OPAEVNTS)
  - Prescription drug (PMAEVNTS) events
- Stratification by:
  - Income (`CSP_INCOME`)
  - Plan type (`PAMTCARE`, `PAMTMADV`)
  - Number of chronic conditions (`CSP_NCHRNCND`)

## 📁 Files

- `medicare_analysis_2022.ipynb`: Jupyter notebook with all code and findings
- `cspuf2022.csv`: **Not included** — you must download from the official CMS repository

## 📊 Key Findings (2022, Weighted)

- **Poor seniors** pay significantly less OOP on average than richer seniors — likely due to dual-eligibility assistance
- **MA enrollees consistently show fewer provider visits** than Traditional Medicare patients, even when controlling for chronic condition burden
- MA populations skew younger and healthier

## 🚫 Data Access

To reproduce this analysis, download the 2022 CSPUF dataset from:
- https://www.cms.gov/research-statistics-data-systems/medicare-current-beneficiary-survey-mcbs

## 👤 Author

Micheal Beatty  
Data analyst, public interest technologist, and healthcare transparency advocate.
