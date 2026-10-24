# Customer Churn Analysis

A small portfolio project exploring customer churn, basic data quality, and dashboard reporting with Excel/CSV and Power BI.

## Project files

- `customer_churn_raw_dataset.csv` — source table supplied for this project (15 rows, 11 columns).
- `Customer_Churn_Analysis_Workbook.xlsx` — workbook with raw data, calculated summary, contract summary, and definitions/limitations.
- `Customer_Churn_Data_Quality_Report.pdf` — corrected data quality and exploratory report.
- `Customer_Churn_Dashboard.pdf` — static PDF export of the supplied Power BI dashboard.
- `Customer_Churn_Analysis.pbix` — supplied Power BI Desktop project file.
- `README.md` — project overview and interpretation.

## Objective

Review the supplied customer records, calculate basic churn and retention metrics, check data consistency, and communicate observations in a Power BI dashboard.

## Key results

| Metric | Result |
|---|---:|
| Customers in sample | 15 |
| Fields | 11 |
| Missing cells | 0 |
| Duplicate CustomerIDs | 0 |
| Average age | 39.07 years |
| Average tenure | 18.80 months |
| Churned customers | 7 |
| Retained customers | 8 |
| Churn rate | 46.67% |
| Retention rate | 53.33% |
| Sum of TotalCharges for churned records (dashboard's ~3.11K KPI) | 3,109.51 (currency not specified) |
| Sum of MonthlyCharges for churned records | 409.93 (currency not specified) |

## Data quality checks

- No missing values were found in the supplied table.
- No duplicate `CustomerID` values were found.
- `TotalCharges` matches `MonthlyCharges × TenureMonths` for all records within floating-point precision.
- Observed ranges: Age 23–60, Tenure 2–48 months, SupportTickets 0–6.
- These observed ranges are descriptive; they do not, by themselves, prove the presence or absence of statistical outliers.

## Exploratory observation

In this sample, all 7 churned customers have a Month-to-Month contract, while no churn is recorded among the One Year or Two Year contract records. This pattern is worth investigating with a larger dataset, but it must not be interpreted as proof of causation or as a reliable real-world churn estimate.

The dashboard's approximately 3.11K KPI matches the sum of TotalCharges for churned records (3,109.51). The separate sum of MonthlyCharges for churned records is 409.93. Currency is not specified in the source. These are descriptive sums, not a forecast of lost revenue or lifetime value.

## Tools

- Microsoft Power BI Desktop
- Microsoft Excel / CSV
- Basic data quality validation and exploratory analysis

## Limitations

- Only 15 customer records are included, so results are illustrative and not statistically representative.
- The original external source, sampling method, and currency were not provided.
- Before publishing publicly, confirm the data is permitted for public sharing and contains no real confidential customer information.
- The `.pbix` file is included as supplied; open it in Power BI Desktop to confirm all visuals, filters, and measures refresh and behave as expected.

## How to use

1. Open `Customer_Churn_Analysis_Workbook.xlsx` to review the data and summary.
2. Open `Customer_Churn_Analysis.pbix` in Power BI Desktop to inspect the interactive report.
3. Use the PDF files as quick previews and documentation.
