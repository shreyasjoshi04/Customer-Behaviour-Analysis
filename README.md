📊 Customer Shopping Behavior Analysis

An end-to-end Data Analytics portfolio project demonstrating the complete analytics workflow using Python, PostgreSQL, SQL, and Power BI. This project transforms raw customer shopping data into actionable business insights through data cleaning, exploratory data analysis, SQL-based business analysis, and an interactive dashboard.

📌 Overview 

The objective of this project is to simulate a real-world data analytics workflow followed in organizations. Starting from raw customer shopping data, the project focuses on preparing the data, answering business questions, and presenting insights through an interactive Power BI dashboard.

The project covers:

Data Loading
Exploratory Data Analysis (EDA)
Data Cleaning
PostgreSQL Database Integration
SQL Business Analysis
Power BI Dashboard Development
📂 Dataset
The dataset contains customer shopping behavior information, including:

Customer ID
Age
Gender
Category
Item Purchased
Purchase Amount
Location
Size
Color
Season
Review Rating
Subscription Status
Payment Method
Shipping Type
Discount Applied
Promo Code Used
Previous Purchases
Preferred Payment Method
Frequency of Purchases
🛠️ Tools & Technologies
Tool	Purpose
Python	Data Loading, Cleaning & Analysis
Pandas	Data Manipulation
PostgreSQL	Database Management
SQL	Business Analysis
Power BI	Dashboard & Reporting
Jupyter Notebook	Python Development
Git & GitHub	Version Control
🚀 Project Workflow
Step 1 — Load the Dataset
Import the CSV dataset using Pandas.
Explore the dataset structure.
Inspect rows, columns, and data types.
Step 2 — Exploratory Data Analysis (EDA)
Perform an initial analysis to understand the dataset.

Tasks performed:

Dataset overview
Statistical summary
Missing value analysis
Duplicate value detection
Distribution analysis
Correlation analysis
Step 3 — Data Cleaning
Prepare the dataset for further analysis.

Cleaning steps include:

Handling missing values
Removing duplicate records
Correcting inconsistent data
Formatting columns
Preparing the final cleaned dataset
Step 4 — SQL Analysis (PostgreSQL)
Load the cleaned dataset into PostgreSQL and answer business questions using SQL.

The project includes SQL concepts such as:

SELECT
WHERE
ORDER BY
GROUP BY
Aggregate Functions
CASE Statements
HAVING
Subqueries
Common Table Expressions (CTEs)
Example business questions:

Total revenue by gender
Revenue by product category
Average purchase amount
Customers using discounts
Most preferred payment methods
Seasonal shopping trends
Shopping frequency analysis
Step 5 — Power BI Dashboard
Create an interactive dashboard to visualize customer shopping behavior.

Dashboard includes:

Total Revenue
Total Customers
Average Purchase Amount
Revenue by Category
Revenue by Gender
Revenue by Season
Purchase Frequency
Payment Method Distribution
Discount Analysis
Interactive Filters & Slicers
📈 Dashboard Preview
Overall Dashboard
Dashboard

Revenue by Category
 

Revenue by Gender


Shipping Type Analysis
 

📊 Key Insights
Identified the highest revenue-generating product categories.
Compared customer spending across different demographic groups.
Evaluated the impact of discounts on purchasing behavior.
Analyzed seasonal shopping trends.
Explored customer purchasing frequency.
Built an interactive dashboard for business decision-making.
📁 Project Structure
customer_shopping_behavior_analysis/
│
├── dataset/
│   └── customer_shopping_behavior.csv
│
├── images/
│   ├── dashboard.png
│   ├── category1.png
│   ├── category2.png
│   ├── gender.png
│   ├── shippingtype1.png
│   └── shippingtype2.png
│
├── notebooks/
│   └── Data_cleaning.ipynb
│
├── powerbi/
│   └── customer_behavior_dashboard.pbix
│
├── sql/
│   └── customer_behavior_sql_queries.sql
│
├── .gitignore
├── LICENSE
└── README.md
▶️ How to Run
1. Clone the Repository
git clone https://github.com/awadhanisiddhi/customer_shopping_behavior_analysis.git
2. Install Required Libraries
pip install pandas psycopg2
3. Run the Python Notebook
Open:

Data_cleaning.ipynb
Execute all cells to:

Load the dataset
Perform EDA
Clean the data
Export data to PostgreSQL
4. Execute SQL Queries
Create a PostgreSQL database.
Import the cleaned dataset.
Run the SQL queries from:
sql/customer_behavior_sql_queries.sql
5. Open the Power BI Dashboard
Launch:

powerbi/customer_behavior_dashboard.pbix
Refresh the data connection if required.

💼 Skills Demonstrated
Data Cleaning
Exploratory Data Analysis (EDA)
Python Programming
SQL Query Writing
PostgreSQL
Business Analytics
Data Visualization
Power BI Dashboard Development
Business Insight Generation
End-to-End Data Analytics Workflow
📄 License
This project is intended for learning and portfolio purposes.

🙏 Acknowledgements
This project was built as part of my learning journey by following the YouTube tutorial "COMPLETE Data Analytics Portfolio Project in 6 EASY Steps | Python + SQL + Power BI" by Amlan Mohanty. I implemented the data cleaning, SQL analysis, and Power BI dashboard while following the tutorial to gain hands-on experience with an end-to-end data analytics workflow.

About
End-to-end customer shopping behavior analysis using Python, PostgreSQL, SQL, and Power BI.

Resources
Readme
MIT license
Activity
Stars
0 stars
Watchers
0 watching
Forks
0 forks
