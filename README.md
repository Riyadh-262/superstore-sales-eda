# Exploratory Data Analysis of Superstore Sales

A Python-based exploratory data analysis (EDA) of retail transactions, completed as a **group project** for **CSE303: Statistics for Data Science** at **East West University (Spring 2026)**.

The analysis examines sales distribution, descriptive statistics, customer and product categories, regional trends, time-based sales patterns, data quality, and shipping duration. The accompanying academic report also discusses a linear regression experiment; **the supplied Jupyter notebook does not contain that regression implementation**.

## Project overview

- **Dataset:** 9,800 rows and 18 original columns (retail transactions; source identified as Kaggle in the course report)
- **Main numerical metric:** `Sales`
- **Tools:** Python, pandas, matplotlib, seaborn, Jupyter Notebook
- **Techniques:** Descriptive statistics, histogram/density/box plots, IQR outlier detection, categorical analysis, time-series exploration, and missing-value checks

## Key observations

| Metric | Value |
|---|---:|
| Transactions | 9,800 |
| Original features | 18 |
| Average sales | 230.77 |
| Median sales | 54.49 |
| Sales standard deviation | 626.65 |
| Missing postal codes | 11 (about 0.11%) |
| Duplicate records | 0 |

The sales distribution is strongly right-skewed, with many low-value transactions and a small number of high-value transactions. **Office Supplies** is the most common product category (5,909 records), followed by Furniture (2,078) and Technology (1,813). These are **transaction counts, not category revenue totals**.

## Repository structure

```text
superstore-sales-eda/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   └── Project_train.csv
├── notebooks/
│   ├── SuperStoreSales.ipynb             # runnable EDA notebook with date/path fixes
│   └── SuperStoreSales_original.ipynb    # unchanged uploaded coursework notebook
└── reports/
    └── CSE303_Group3_Project_Report.pdf
```

## Getting started

1. Clone the repository and enter its directory:

   ```bash
   git clone https://github.com/YOUR_USERNAME/superstore-sales-eda.git
   cd superstore-sales-eda
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   ```

   **Windows PowerShell:** `.venv\Scripts\Activate.ps1`  
   **macOS/Linux:** `source .venv/bin/activate`

3. Install packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Start Jupyter:

   ```bash
   jupyter notebook
   ```

5. Open `notebooks/SuperStoreSales.ipynb` and select **Run All**. The notebook checks both typical working directories when locating the CSV.

## Analysis workflow

1. Inspect data types, columns, and first records.
2. Calculate mean, median, mode, variance, standard deviation, and IQR for Sales.
3. Visualize distribution and identify IQR-based outliers.
4. Explore categorical attributes (Segment, Category, Region, etc.).
5. Convert order dates and examine monthly sales patterns.
6. Check missing values, duplicates, and shipping-day anomalies.

## Limitations and next steps

- The report describes **linear regression experiments and RMSE figures**, but the uploaded notebook contains only EDA/data-quality cells. Treat the regression section as **report-only, not independently reproducible from this repository** until its code is added.
- The dataset is credited to **Kaggle** in the report, but its precise dataset URL and redistribution license are not supplied. **Verify the source and license before publicly distributing the CSV**; otherwise remove the CSV and provide download instructions.
- The notebook focuses on transaction counts and sales patterns, rather than causal claims or validated forecasting.

## Team and attribution

This was a **five-person group project**, not an individual project. Team members (as listed in the submitted report): **Al Zarin, Joy Dutta, Mst. Nabiha Tahsin, Riyadh Hossain, and Istiak Hasan Masfi**. Submitted for CSE303, East West University. Individual contributions have not been specified in the source material.

## Report

See [`reports/CSE303_Group3_Project_Report.pdf`](reports/CSE303_Group3_Project_Report.pdf) for the original methodology, visualizations, and the separate discussion of linear regression.

## License

No software/data reuse license is asserted here. Add a software license only after confirming the team's permission, and follow the original dataset's license separately.
