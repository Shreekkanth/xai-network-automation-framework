# Raw Data

## Overview

This directory contains the original (raw) datasets used in the capstone project:

> **An Explainable AI Framework for Telemetry-Driven Closed-Loop Enterprise Network Automation**

The datasets are preserved in their original form and are **not modified**. All preprocessing, feature engineering, feature selection, model training, and evaluation are performed programmatically within the project's Jupyter notebooks and Python modules to ensure reproducibility.

---

## Data Source

**Dataset:** UNSW-NB15

**Publisher:** Australian Centre for Cyber Security (ACCS), UNSW Canberra

**Official Dataset Repository:**

* https://research.unsw.edu.au/projects/unsw-nb15-dataset

**Official Dataset Files (UNSW SharePoint):**

* https://unsw-my.sharepoint.com/personal/z5025758_ad_unsw_edu_au/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fz5025758%5Fad%5Funsw%5Fedu%5Fau%2FDocuments%2FUNSW%2DNB15%20dataset%2FCSV%20Files

**Feature Dictionary:**

* https://unsw-my.sharepoint.com/:x:/r/personal/z5025758_ad_unsw_edu_au/_layouts/15/Doc.aspx?sourcedoc=%7B975B24E4-7E36-4CE1-B98A-9FBE4BB521B7%7D

> **Note:** The raw datasets are maintained in their original form. No modifications are made to these files. All preprocessing and feature engineering are performed programmatically within the project notebooks to ensure reproducibility.

**Original Publication:**

Moustafa, N., & Slay, J. (2015). *UNSW-NB15: A Comprehensive Data Set for Network Intrusion Detection Systems*. IEEE Military Communications and Information Systems Conference (MilCIS).

---

## Files

| File                         | Purpose                                                                                                                                                                          | Status   |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| `UNSW_NB15_training-set.csv` | Training dataset used for exploratory data analysis, feature selection, machine learning model development, and explainable AI analysis.                                         | Required |
| `UNSW_NB15_testing-set.csv`  | Independent testing dataset used for model evaluation, performance comparison, and decision threshold optimization.                                                              | Required |
| `NUSW-NB15_features.csv`     | Feature dictionary containing metadata and descriptions of the network telemetry variables used throughout the study.                                                            | Required |
| `NUSW-NB15_GT.csv`           | Ground truth reference file provided by the dataset authors. Included for completeness and potential validation but not directly used in the analyses conducted in this project. | Optional |

---

## Directory Structure

```text
data/
└── raw/
    ├── README.md
    ├── UNSW_NB15_training-set.csv
    ├── UNSW_NB15_testing-set.csv
    ├── NUSW-NB15_features.csv
    └── NUSW-NB15_GT.csv
```

---

## Data Usage within the Project

| Research Question                                   | Dataset Usage                                                         |
| --------------------------------------------------- | --------------------------------------------------------------------- |
| **RQ1 – Telemetry Feature Significance**            | Training dataset and feature dictionary                               |
| **RQ2 – Telemetry Processing Optimization**         | Training dataset                                                      |
| **RQ3 – Model Selection for Enterprise Deployment** | Training and testing datasets                                         |
| **RQ4 – Explainability and Operator Trust**         | Trained model outputs and feature dictionary                          |
| **RQ5 – Operational Risk Management**               | Testing dataset for threshold optimization and performance evaluation |

---

## Data Integrity

The raw datasets must remain unchanged throughout the project.

All data preprocessing—including categorical encoding, feature engineering, feature selection, normalization (where applicable), and train/test preparation—is implemented within the project notebooks to ensure complete reproducibility.

---

## Notes

* The official training and testing datasets already contain the target variables (`label` and `attack_cat`) required for binary and multi-class classification.
* The feature dictionary is used to interpret telemetry variables and support explainable AI (SHAP) analyses.
* The ground truth file is retained for reference and future research but is not required for the core machine learning workflow implemented in this study.

---

## Attribution

The UNSW-NB15 dataset was developed by the **Australian Centre for Cyber Security (ACCS), UNSW Canberra** and is used in this project in accordance with its published research documentation.

For complete dataset documentation and the original research publication, please refer to the **References** section of this repository or the accompanying capstone report.
