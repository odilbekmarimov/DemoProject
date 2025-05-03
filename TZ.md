# Banking ETL and Dashboard Project

This project simulates a real-world banking analytics scenario. You will work with encoded CSV files representing banking data, decode them using mapping rules, clean and transform them using Python and SQL, and build insights in Power BI.

---

## Project Goals

* Decode and interpret encoded banking data
* Clean and transform the data using Python (pandas) and SQL Server
* Track each data ingestion process via a metadata table
* Visualize insights using Power BI dashboard (2 pages)

---

## Data Sources

You will be provided with several encoded CSV files, named as:

* `t01.csv` – Users
* `t02.csv` – Cards
* `t03.csv` – Transactions
* `t04.csv` – Logs (derived from transaction failures or pending)
* `t05.csv` – Reports (aggregated from transactions)
* `t07.csv` – Scheduled Payments

Column names follow the format `tableID-columnID`, e.g., `01-01`, `03-04`.

You will also receive a JSON file (`column_map.json`) to decode column names.

---

## Tasks Breakdown

### 1. Data Ingestion & Decoding (Python)

* Retrieve the encoded CSV files using `pandas.read_csv()`
* Use the mapping dictionary (`column_map.json`) to rename the columns to human-readable names
* Split the combined data into logical tables (users, cards, transactions, etc.)

### 2. Data Cleaning (Python + pandas)

* Convert columns to proper data types (dates, booleans, integers)
* Handle missing or invalid values (e.g., phone numbers, email)
* Flag rows that exceed card limit or transaction thresholds

### 3. Data Upload (SQL Server)

* Upload cleaned data to SQL Server tables
* Create relational constraints (e.g., foreign keys between cards and users)

### 4. Metadata Tracking

* Each ingestion must insert a row into a table called `retrieveinfo`, containing:

  * `retrieve_id`
  * `source_file`
  * `retrieved_at`
  * `total_rows`, `processed_rows`, `errors`, `notes`

### 5. Data Transformation (SQL)

Write SQL queries or views for:

* Fraud detection (flagged transactions)
* VIP user identification (based on transaction volume or balance)
* Blocked user listing (based on card/user status)
* Daily summary reports

### 6. Dashboard Creation (Power BI)

**Page 1 – Users & Cards Overview:**

* Total users, VIP %, average balance
* Bar chart of card types by balance
* Pie chart: user status distribution

**Page 2 – Transaction & Fraud Insights:**

* Timeline of transactions by type
* Flagged transaction count and value
* Highlight high-risk users or transactions
* Automate daily ingestion.
* Create stored procedures to insert new transactions or reports
* Use Python logging to track ETL steps

---

##  Deliverables

* Python script(s) for decoding, cleaning, uploading
* SQL scripts for schema creation and transformations
* Power BI file with 2 pages of analysis

