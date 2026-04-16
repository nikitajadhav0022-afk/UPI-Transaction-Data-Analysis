# UPI-Transaction-Data-Analysis-PowerBI-Dashboard

### Dashboard Link : https://app.powerbi.com/links/RIYV7JtXgt?ctid=91577f61-0170-494b-a390-0f33a2bb8755&pbi_source=linkShare

## Problem Statement

This dashboard analyzes **UPI (Unified Payments Interface) transaction data for the year 2024** across multiple Indian cities. It helps businesses and analysts understand transaction volume trends, city-wise and currency-wise transaction amounts, remaining balances, and customer spending patterns across different demographics, payment methods, and merchant categories.

The dashboard enables stakeholders to identify peak transaction months, compare city-level performance, and filter data across 10 dimensions — making it a powerful tool for financial data analysis.

---

## Project Highlights

- 2-page interactive Power BI report built on UPI transaction data (Year 2024)
- **10 slicers** synced across pages for seamless filtering experience
- **4 bookmark buttons** for switching between Line chart and Column chart views for both Amount and Balance
- **Conditional Formatting** applied on Matrix visual
- **Calculated column** added for Age Groups in Power Query
- Published to **Power BI Service**

---

## Data Source

- **Power BI Desktop** (data loaded directly)
- Dataset: UPI Transaction records for Year 2024
- Records: **20,000 rows**, 20 columns
- All columns: **100% Valid, 0% Error, 0% Empty** ✅

| Column | Distinct Values |
|---|---|
| TransactionID | 20,000 unique |
| TransactionDate | 60 distinct dates |
| Amount | 19,054 distinct |
| BankNameSent | 4 (SBI, ICICI, Axis, HDFC) |
| BankNameReceived | 4 (SBI, ICICI, Axis, HDFC) |
| RemainingBalance | 19,781 distinct |
| City | 4 (Delhi, Bangalore, Hyderabad, Mumbai) |

**Full column list:** TransactionID, TransactionDate, TransactionTime, TransactionType, Amount, RemainingBalance, BankNameSent, BankNameReceived, City, Currency, DeviceType, Gender, CustomerAge, Age Groups, MerchantName, MerchantAccountNumber, CustomerAccountNumber, PaymentMethod, PaymentMode, Purpose, Status

---

## Steps Followed

### Data Loading & Profiling

- **Step 1:** Loaded UPI transaction dataset into Power BI Desktop.
- **Step 2:** Performed **Data Profiling** — checked Column Distribution, Column Quality, and Column Profile based on **entire dataset** (not just top 1000 rows).
- **Step 3:** All columns showed **100% Valid, 0% Error, 0% Empty** — no data quality issues found.

### Data Transformation in Power Query Editor

Applied Steps:
- **Promoted Headers** — set first row as column headers
- **Changed Type** — set correct data types for all columns
- **Split Column by Delimiter** — split a combined column into separate fields
- **Removed Columns** — dropped unnecessary columns
- **Renamed Columns** — standardized column names (e.g. CustomerAccountNumber, MerchantAccountNumber)
- **Added Conditional Column** — created **Age Groups** column to segment customers by age

### Power Query Editor Snapshot

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/ea86bad2-f3f9-4071-89d3-97296ef4dab0" />

*Power Query Editor showing 20,000 rows, 20 columns, all 100% valid with applied transformation steps*

### Report Building — Page 1 (Transaction Trends)

- **Step 4:** Added and formatted **10 slicers** across the report:
  - BankNameSent, BankNameReceived, City, DeviceType, Gender
  - Age Groups, MerchantName, PaymentMethod, Purpose, TransactionType
- **Step 5:** Configured **slicer sizes, positions, and formatting** for consistent UI layout.
- **Step 6:** **Synced all slicers** across Page 1 and Page 2 so filters apply on both pages simultaneously.
- **Step 7:** Built a **Line Chart** showing Transactions (Amount) by Month for Year 2024.
- **Step 8:** Added **4 Bookmark buttons** to allow users to toggle between views:
  - 📈 Line Chart — Amounts
  - 📊 Column Chart — Amounts
  - 📈 Line Chart — Remaining Balance
  - 📊 Column Chart — Remaining Balance

### Report Building — Page 2 (Matrix View)

- **Step 9:** Built a **Matrix Visual** showing:
  - Rows: Month (January to December)
  - Columns: City (Bangalore, Delhi, Hyderabad, Mumbai) × Currency (EUR, USD, GBP, INR)
  - Values: Transaction Amount and Remaining Balance
- **Step 10:** Applied **Conditional Formatting** on matrix values to highlight high and low transaction amounts visually.

### Publishing

- **Step 11:** Published report to **Power BI Service**.

---

## Report Snapshots

### Page 1 — Bookmark View 1: Line Chart — Transaction Amounts (Year 2024)

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/75b0411d-31f2-4b93-8e80-89945b15d7d0" />

*Line chart showing monthly transaction amounts — Peak: May (1,707K), Low: August (1,599K)*

### Page 1 — Bookmark View 2: Column Chart — Transaction Amounts (Year 2024)

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/fb301cb3-966f-47fb-bf09-843c8729a111" />

*Column chart view of monthly transaction amounts — ranging from 1.60M to 1.71M*

### Page 1 — Bookmark View 3: Line Chart — Remaining Balance (Year 2024)

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/df3c8ff0-07e8-4643-8d9c-51c46a7f4b7c" />

*Line chart showing monthly remaining balance — Peak: May (8,536K), Low: January (8,232K)*

### Page 1 — Bookmark View 4: Column Chart — Remaining Balance (Year 2024)

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/21e3b00a-d7ac-4b7f-85f0-7dc6521f2d2a" />

*Column chart view of monthly remaining balance — consistently ranging between 8.2M to 8.5M*

### Bookmarks & Selection Pane

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/e82c8385-9351-41ee-aaeb-fd3e5c82e7a3" />

*Bookmarks pane showing all 4 configured bookmarks: Line chart Amounts, Column chart Amounts, Line Chart Balance, Column Chart Balance*

### Page 2 — City & Currency Matrix with Slicer

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/949c1c01-ed7a-4868-a31b-db4f6564fb1e" />

*Matrix visual showing Amount and Remaining Balance by City (Bangalore, Delhi, Hyderabad, Mumbai), Currency, and Month with conditional formatting. City slicer shown open with all 4 cities visible.*

### Power Query Editor — Data Cleaning Steps

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/8c697e99-becc-47ba-a420-7d8d0d7c308a" />

*Power Query Editor showing 20,000 rows, 20 columns, all 100% valid with applied transformation steps*

---

## Key Metrics (Year 2024)

| Month | Transaction Amount | Remaining Balance |
|---|---|---|
| January | 1,679K | 8,232K |
| February | 1,693K | 8,252K |
| March | 1,624K | 8,442K |
| April | 1,663K | 8,222K |
| May | 1,707K ⬆ (Peak Amount) | 8,536K ⬆ (Peak Balance) |
| June | 1,653K | 8,331K |
| July | 1,610K | 8,331K |
| August | 1,599K ⬇ (Low Amount) | 8,433K |
| September | 1,667K | 8,433K |
| October | 1,691K | 8,421K |
| November | 1,642K | 8,327K |
| December | 1,646K | 8,429K |

---

## Key Insights

- **May 2024** recorded the highest transaction amount at **1,707K** — possibly driven by festive or seasonal spending.
- **August 2024** saw the lowest transaction amount at **1,599K**.
- Transactions show a clear **dip mid-year (June–August)** and recover strongly from **September onwards**.
- **Mumbai (INR)** and **Delhi (USD)** are among the most active cities by transaction volume based on the matrix data.
- The dashboard supports **multi-dimensional analysis** across 10 filters — city, bank, gender, age group, device type, merchant, payment method, purpose, and transaction type.

---

## Visuals Used

| Visual | Purpose |
|---|---|
| Line Chart | Monthly transaction amount trend (2024) |
| Column Chart | Monthly transaction amount (bookmark toggle) |
| Matrix | City × Currency × Month breakdown for Amount & Remaining Balance |
| Slicers (10) | BankNameSent, BankNameReceived, City, DeviceType, Gender, Age Groups, MerchantName, PaymentMethod, Purpose, TransactionType |
| Bookmark Buttons (4) | Toggle between Line/Column chart for Amount and Remaining Balance |

---

## Advanced Features Implemented

| Feature | Details |
|---|---|
| Synced Slicers | All 10 slicers sync across Page 1 and Page 2 |
| Bookmarks | 4 bookmarks created to toggle between 4 chart views |
| Conditional Formatting | Applied on matrix visual to highlight transaction patterns |
| Age Group Column | Calculated column added in Power Query to segment customers |
| Data Profiling | Column quality, distribution, and profile checked for entire dataset |

---

## Tools & Technologies

- Power BI Desktop & Power BI Service
- Power Query Editor (M Language)
- DAX (Data Analysis Expressions)
- Microsoft Excel (data staging)
