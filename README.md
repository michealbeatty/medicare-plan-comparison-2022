# Medicare Advantage vs Traditional Medicare: Utilization Disparities (2022)

Statistical analysis reveals Medicare Advantage patients receive 5.6 fewer medical visits annually than Traditional Medicare patients with identical health profiles.
This repository contains a reproducible analysis of the 2022 Medicare Current Beneficiary Survey (MCBS) Cost Supplement data, comparing medical provider visit frequency between Medicare Advantage (MA) and Traditional Medicare (TM) enrollees.

## Key Findings
- Medicare Advantage enrollees received **approximately 5.6 fewer medical provider visits per year** than their Traditional Medicare counterparts.
- This result remains **statistically significant (p < 0.001)** after adjusting for:
  - Number of chronic conditions
  - Age group
  - Sex
  - Income level
  - **Dual eligibility (Medicare + Medicaid):** Examined but excluded from final model due to lack of explanatory power.
- Disparities persist **even among patients with multiple chronic conditions**, suggesting systemic differences in care delivery.
- This finding affects approximately 27 million Medicare Advantage enrollees nationwide and raises questions about care access disparities in privatized Medicare.

## Methodology
- Data Source: MCBS 2022 Cost Supplement Public Use File (PUF)
- Survey-weighted linear regression model
- Outcome variable: `MPAEVNTS` (Medical Provider Events)
- Covariates: `CSP_NCHRNCND`, `CSP_AGE`, `CSP_SEX`, `CSP_INCOME`
- Plan flag: `plan_ma` (binary indicator for Medicare Advantage)

## Data Access
The analysis uses publicly available data from the Centers for Medicare & Medicaid Services (CMS):

- **Dataset**: Medicare Current Beneficiary Survey (MCBS) 2022 Cost Supplement Public Use File  
- **Download URL**: [CMS.gov MCBS Data Tables](https://www.cms.gov/Research-Statistics-Data-and-Systems/Research/MCBS/Data-Tables)

**Note:** Due to CMS data use restrictions, the dataset (`cspuf2022.csv`) is not included in this repository. Users must download the file directly from CMS and agree to the terms of use. Once downloaded, place the CSV in the `/data` folder to reproduce results.

## Reproducibility
To recreate the analysis:

```bash
# Create conda environment
conda env create -f environment.yml
conda activate medicare2022

# Start Jupyter
jupyter notebook
```

Open `medicare_analysis_2022.ipynb` and execute all cells.

## Contents
- `medicare_analysis_2022.ipynb`: Main analysis notebook
- `environment.yml`: Python dependencies (including pandas, seaborn, statsmodels)
- `LICENSE`: MIT license
- `.gitignore`: Standard ignores for Jupyter and Python temp files

## License
MIT License — see `LICENSE` file for details.

## Contact
For questions or media inquiries, contact:  
**Micheal Beatty**  
Data Quality Analyst specializing in healthcare policy research
