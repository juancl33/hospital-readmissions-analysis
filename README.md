# Hospital Readmissions Reduction Program Analysis

## Project Overview

This project analyzes Centers for Medicare & Medicaid Services (CMS) hospital readmissions data to evaluate differences in Excess Readmission Ratio (ERR) performance across Hospital Readmissions Reduction Program (HRRP) conditions and identify facility-level patterns that may be more useful for quality review.

The analysis was completed in Python using pandas, SciPy, and matplotlib.

## Key Findings

* 36.9% of facilities accounted for 80% of total positive ERR deviation above 1.0, indicating that above-expected readmission performance was concentrated among a subset of facilities.
* 1,055 of 2,862 facilities had at least 3 conditions with ERR above 1.0.
* 36 facilities had all 6 HRRP conditions above 1.0.
* A corrected Welch's t-test found no statistically significant difference in mean ERR between Medical and Surgical condition groups (t = -0.4650, p = 0.6419).

## Data Validation

During review, an incorrect Acute Myocardial Infarction (AMI) measure-code mapping was identified. The mapping was corrected and validation checks were added to confirm that all six CMS measures were classified correctly.

The correction restored 1,763 AMI observations to the Medical group, after which the analysis and statistical test were rerun.

## Dataset

The full dataset contained 18,510 hospital-condition records across 3,085 facilities and 6 HRRP conditions.

After filtering to records with usable Excess Readmission Ratio values, the analysis included 11,927 records across 2,862 facilities.

## Tools

* Python
* pandas
* SciPy
* matplotlib
* Jupyter Notebook

## Repository Contents

* `hospital_readmissions_analysis.ipynb` - Complete analysis, validation, statistical testing, and facility-level findings
