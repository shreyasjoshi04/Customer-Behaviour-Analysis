# Customer Behavior Analysis Dashboard

A complete **Customer Behavior Analysis and Business Intelligence project** that demonstrates an end-to-end data analytics workflow using **Python, SQL, and Microsoft Power BI**.

The project starts with a raw customer dataset, cleans and prepares the data using Python, performs analytical queries using SQL, and finally presents the insights through an interactive Power BI dashboard.

---

## 📊 Dashboard Overview

The Power BI dashboard provides a high-level view of customer purchasing behavior and sales performance.

### Key KPIs
- **Number of Customers**
- **Average Purchase Amount**
- **Average Review Rating**

### Dashboard Analysis
The dashboard includes:
- Customer distribution by **Subscription Status**
- **Revenue by Category**
- **Sales by Category**
- **Revenue by Age Group**
- **Sales by Age Group**
- Interactive filters for:
  - Subscription Status
  - Gender
  - Product Category
  - Shipping Type

These visuals make it easier to identify customer trends, compare product categories, and understand purchasing behavior across different customer segments.

---

## 🔄 Project Workflow

```text
Raw Dataset
     │
     ▼
Python Data Loading
     │
     ▼
Data Cleaning & Preprocessing
     │
     ▼
Clean Dataset
     │
     ▼
SQL Analysis
     │
     ▼
Business Insights
     │
     ▼
Power BI Data Modeling
     │
     ▼
Interactive Dashboard
```

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| **Python** | Data loading, cleaning, preprocessing, and exploration |
| **Pandas** | Data manipulation and transformation |
| **NumPy** | Numerical operations where required |
| **SQL** | Data analysis and business queries |
| **PostgreSQL / SQL Database** | Storing and querying structured customer data |
| **Microsoft Power BI** | Data visualization and dashboard development |
| **Power Query** | Data transformation and preparation in Power BI |
| **DAX** | Measures and KPI calculations |

---

## 📁 Project Structure

```text
Customer-Behavior-Dashboard/
│
├── data/
│   ├── raw/
│   │   └── customer_data.csv
│   │
│   └── cleaned/
│       └── customer_data_cleaned.csv
│
├── python/
│   └── data_cleaning.py
│
├── sql/
│   └── customer_analysis.sql
│
├── powerbi/
│   └── customer_behavior_dashboard.pbix
│
└── README.md
```

> File and folder names can be adjusted according to the final GitHub repository structure.

---

# 1. 📥 Loading the Dataset Using Python

The first step is to load the raw customer dataset into Python.

Pandas is used because it provides convenient functions for reading, inspecting, cleaning, and transforming tabular data.

### Example

```python
import pandas as pd

df = pd.read_csv("customer_data.csv")

print(df.head())
print(df.shape)
print(df.info())
```

### Initial Data Inspection

The dataset is checked for:

- Number of rows and columns
- Column names
- Data types
- Missing values
- Duplicate records
- Incorrect or inconsistent values
- Possible outliers

Example:

```python
print(df.info())
print(df.isnull().sum())
print(df.duplicated().sum())
print(df.describe())
```

---

# 2. 🧹 Data Cleaning Using Python

Raw datasets often contain problems that can affect analysis and visualization.

The cleaning process includes:

### Missing Values

```python
df.isnull().sum()
```

Missing values can be handled according to the type of column and business requirement.

### Duplicate Records

```python
df.drop_duplicates(inplace=True)
```

### Data Type Correction

Columns such as customer IDs, purchase amounts, dates, and categorical fields are converted to appropriate data types.

Example:

```python
df["purchase_amount"] = pd.to_numeric(
    df["purchase_amount"],
    errors="coerce"
)
```

### Text Standardization

Categorical values are standardized to avoid inconsistencies.

```python
df["category"] = df["category"].str.strip().str.title()
```

### Final Validation

After cleaning, the dataset is checked again:

```python
print(df.info())
print(df.isnull().sum())
print(df.duplicated().sum())
```

The cleaned dataset is then used for SQL analysis and Power BI visualization.

---

# 3. 🗄️ SQL Data Analysis

After cleaning the data, SQL is used to answer business-related questions.

Typical analysis includes:

### Total Customers

```sql
SELECT COUNT(DISTINCT customer_id) AS total_customers
FROM customer;
```

### Average Purchase Amount

```sql
SELECT AVG(purchase_amount) AS average_purchase_amount
FROM customer;
```

### Revenue by Category

```sql
SELECT
    category,
    SUM(purchase_amount) AS revenue
FROM customer
GROUP BY category
ORDER BY revenue DESC;
```

### Sales by Category

```sql
SELECT
    category,
    COUNT(customer_id) AS sales
FROM customer
GROUP BY category
ORDER BY sales DESC;
```

### Customer Distribution by Subscription Status

```sql
SELECT
    subscription_status,
    COUNT(customer_id) AS customers
FROM customer
GROUP BY subscription_status;
```

### Revenue by Age Group

```sql
SELECT
    age_group,
    SUM(purchase_amount) AS revenue
FROM customer
GROUP BY age_group
ORDER BY revenue DESC;
```

SQL analysis helps convert raw customer records into meaningful business information before visualization.

---

# 4. 📊 Power BI Dashboard

The cleaned data and analytical results are brought into **Microsoft Power BI** to create an interactive dashboard.

### Dashboard Components

#### KPI Cards

The dashboard highlights:

- Number of Customers
- Average Purchase Amount
- Average Review Rating

#### Customer Subscription Analysis

A donut chart shows the percentage of customers across different subscription statuses.

#### Revenue Analysis

Column and bar charts are used to compare revenue across:

- Product categories
- Age groups

#### Sales Analysis

Sales volume is compared across:

- Product categories
- Age groups

#### Interactive Slicers

Users can filter the dashboard using:

- Subscription Status
- Gender
- Category
- Shipping Type

This allows users to explore customer behavior from different perspectives.

---

# 5. 📈 Key Business Questions

The dashboard is designed to help answer questions such as:

1. How many customers are present in the dataset?
2. What is the average amount spent by customers?
3. What is the average customer review rating?
4. Which product categories generate the highest revenue?
5. Which categories have the highest sales volume?
6. How does revenue vary across different age groups?
7. How are customers distributed by subscription status?
8. How does customer behavior change based on gender?
9. How does shipping type relate to customer purchasing behavior?
10. Which customer segments should receive more business attention?

---

# 6. 💡 Business Insights

The dashboard can be used by businesses to:

- Understand customer purchasing patterns
- Identify high-performing product categories
- Compare revenue and sales volume
- Analyze customer segments
- Understand subscription behavior
- Identify valuable customer groups
- Support data-driven business decisions

---

# 7. 🚀 How to Run the Project

### Step 1 — Clone the Repository

```bash
git clone <your-github-repository-url>
cd Customer-Behavior-Dashboard
```

### Step 2 — Install Python Libraries

```bash
pip install pandas numpy
```

### Step 3 — Load the Dataset

Place the raw dataset inside:

```text
data/raw/
```

### Step 4 — Run the Python Cleaning Script

```bash
python python/data_cleaning.py
```

The cleaned dataset will be generated inside:

```text
data/cleaned/
```

### Step 5 — Run SQL Queries

Load the cleaned dataset into your SQL database and execute:

```text
sql/customer_analysis.sql
```

### Step 6 — Open the Power BI Dashboard

Open:

```text
powerbi/customer_behavior_dashboard.pbix
```

If required, update the data source path or database connection in Power BI.

Then refresh the dataset to view the latest results.

---

# 8. 📌 Skills Demonstrated

This project demonstrates practical knowledge of:

- Python
- Pandas
- Data Cleaning
- Data Preprocessing
- Exploratory Data Analysis
- SQL
- Aggregations and GROUP BY
- Business Analysis
- Power BI
- Data Visualization
- Dashboard Design
- KPI Development
- Interactive Slicers
- Data-Driven Decision Making

---

## 🎯 Project Objective

The main objective of this project is to demonstrate an **end-to-end data analytics workflow**:

> **Raw Data → Python Cleaning → SQL Analysis → Power BI Visualization → Business Insights**

It combines programming, database querying, and business intelligence into one practical analytics project.

---

## 👨‍💻 Author

**Shreyas Joshi**

Final-Year Computer Science & Engineering Student

Interested in:

- Data Analytics
- Python
- SQL
- Power BI
- Business Intelligence
- Web Development

---

## ⭐ Project Highlights

- End-to-end analytics workflow
- Python-based data cleaning
- SQL-based business analysis
- Interactive Power BI dashboard
- KPI-driven reporting
- Customer segmentation analysis
- Category and age-group analysis
- Interactive filtering

---

## 📄 License

This project is created for **educational, portfolio, and learning purposes**.
