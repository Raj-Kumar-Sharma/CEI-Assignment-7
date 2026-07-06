# 🚀 Week 7 - Delta Lake Incremental Data Processing using Apache Spark

## 📌 Project Overview

This project demonstrates **Incremental Data Processing using Delta Lake and Apache Spark (PySpark)**. The objective is to simulate a real-world data engineering pipeline where new customer data arrives periodically and needs to be merged into an existing dataset without reprocessing the entire table.

The implementation showcases how **Delta Lake's ACID transactions and MERGE operation** enable efficient updates and inserts while maintaining data consistency and reliability.

This assignment was completed as part of the **Celebal Technologies Summer Internship 2026**.

---

# 🎯 Objective

The primary objective of this project is to understand and implement **incremental data processing** using **Delta Lake**.

The workflow includes:

- Load a dataset into a Delta Table
- Perform basic data cleaning
- Handle missing values
- Remove duplicate records
- Create an incremental dataset
- Apply Delta Lake MERGE (UPSERT) operation
- Update existing records
- Insert new records
- Validate the final dataset
- Understand the concept of Slowly Changing Dimension (SCD Type 1)

---

# 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Programming Language |
| Apache Spark (PySpark) | Distributed Data Processing |
| Delta Lake | ACID Transactions & Incremental Processing |
| Google Colab | Development Environment |
| Pandas | Data Handling |
| Git | Version Control |
| GitHub | Project Hosting |

---

# 📂 Project Structure

```text
Week7_Delta_Lake_Incremental_Data_Processing/
│
├── data/
│   ├── customer_master.csv
│   └── customer_incremental.csv
│
├── notebooks/
│   └── Week7_Delta_Lake_Incremental_Data_Processing.ipynb
│
├── screenshots/
│   ├── data_loading/
│   ├── data_cleaning/
│   ├── incremental_dataset/
│   ├── merge_operation/
│   ├── validation/
│   └── final_output/
│
├── Week7_Report.pdf
│
└── README.md
```

---

# 📊 Dataset Description

The project uses a sample **Customer Master Dataset** containing customer information.

### Dataset Columns

- Customer_ID
- Customer_Name
- Email
- Phone_Number
- City
- State
- Country
- Registration_Date

A second dataset is created to simulate **incremental customer data**, where:

- Existing customer records are updated.
- New customer records are inserted.

---

# ⚙️ Project Workflow

## Step 1: Load Dataset into Delta Table

The customer master dataset is loaded into a PySpark DataFrame.

### Tasks Performed

- Read CSV dataset
- Infer schema automatically
- Verify schema
- Display sample records
- Save DataFrame as a Delta Table

### Output

- Delta Table successfully created
- Dataset loaded correctly
- Schema verified

---

## Step 2: Data Cleaning

Basic preprocessing is performed before storing the data.

### Cleaning Operations

- Check null values
- Fill missing values
- Remove duplicate records
- Validate cleaned dataset
- Save cleaned Delta Table

### Output

- Missing values handled
- Duplicate records removed
- Clean dataset stored as Delta Table

---

## Step 3: Create Incremental Dataset

A second dataset is created to simulate newly arriving customer records.

The incremental dataset contains:

- Updated information for existing customers
- Newly added customer records

This dataset mimics real-world incremental data ingestion.

---

## Step 4: Delta MERGE (UPSERT) Operation

The incremental dataset is merged into the existing Delta Table.

### Merge Logic

**When Customer_ID already exists**

- Update existing customer information

**When Customer_ID does not exist**

- Insert a new customer record

This demonstrates the implementation of **Slowly Changing Dimension (SCD Type 1)**.

### Benefits of Delta MERGE

- ACID Transactions
- Efficient Updates
- Efficient Inserts
- No Full Table Reload
- Faster Incremental Processing

---

## Step 5: Validation

The final Delta Table is validated after the merge.

### Validation Checks

- Total record count
- Duplicate records
- Updated customer details
- Newly inserted records
- Final dataset verification

---

# 🔄 Data Pipeline

```text
Customer Master CSV
        │
        ▼
Read using PySpark
        │
        ▼
Data Cleaning
        │
        ▼
Create Delta Table
        │
        ▼
Generate Incremental Dataset
        │
        ▼
Delta MERGE Operation
(Update + Insert)
        │
        ▼
Validation
        │
        ▼
Final Delta Table
```

---

# 📚 Key Concepts Covered

- Apache Spark DataFrames
- Delta Lake
- Delta Tables
- ACID Transactions
- Incremental Data Processing
- MERGE (UPSERT) Operation
- Data Cleaning
- Duplicate Removal
- Null Value Handling
- Data Validation
- Slowly Changing Dimension (SCD Type 1)
- ETL Pipeline Development

---

# 📸 Screenshots Included

The project contains screenshots for every implementation step.

- Data Loading
- Schema Verification
- Data Cleaning
- Null Handling
- Duplicate Removal
- Incremental Dataset
- MERGE Operation
- Validation
- Final Output

---

# 📦 Deliverables

- ✅ Jupyter Notebook (.ipynb)
- ✅ Customer Master Dataset
- ✅ Incremental Dataset
- ✅ Screenshots
- ✅ Assignment Report (PDF)
- ✅ README Documentation

---

# 📈 Expected Output

After successful execution, the project produces:

- Clean Delta Table
- Updated customer records
- Newly inserted customer records
- Validated final dataset
- Duplicate-free records
- Complete notebook execution
- Screenshots of every implementation step

---

# 🎓 Learning Outcomes

By completing this project, I gained practical experience in:

- Building incremental ETL pipelines
- Working with Apache Spark DataFrames
- Creating and managing Delta Tables
- Performing MERGE (UPSERT) operations
- Applying Slowly Changing Dimension (SCD Type 1)
- Cleaning and validating large datasets
- Understanding ACID transactions in Delta Lake
- Implementing efficient data engineering workflows

---

# 🚀 Future Enhancements

Future improvements for this project include:

- Implementing SCD Type 2
- Automating the pipeline using Apache Airflow
- Integrating Spark Structured Streaming
- Using Azure Data Lake Storage (ADLS) or AWS S3
- Building Power BI dashboards for analytics

---

# 👨‍💻 Author

**Pranjal Upadhyay**

**B.Tech - Artificial Intelligence & Data Science**

**Celebal Technologies Summer Internship 2026**

---