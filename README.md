# Walmart Retail Sales Analysis  
## End-to-End SQL + Python Data Analytics Project

---

## Project Overview

This project performs end-to-end retail sales analysis using:

- **Python (Pandas, SQLAlchemy)**
- **MySQL**
- **VS Code**
- **MySQL Workbench**
- **Kaggle API**

The objective is to simulate a real-world retail analytics workflow:

1. Data extraction using Kaggle API  
2. Data cleaning and transformation using Python  
3. Loading structured data into MySQL  
4. Performing advanced SQL analysis  
5. Extracting actionable business insights  

---

## 🛠 Tools & Technologies Used

- Python 3.8+
- Pandas
- NumPy
- SQLAlchemy
- PyMySQL
- MySQL
- MySQL Workbench
- VS Code
- Kaggle API

---

## Project Workflow

### Environment Setup
- Created structured workspace in VS Code
- Organized project folders
- Created virtual environment
- Installed required dependencies

### Kaggle API Setup
- Downloaded Kaggle API token (`kaggle.json`)
- Configured `.kaggle` directory
- Downloaded dataset using CLI

### Data Cleaning
- Removed duplicates  
- Handled missing values  
- Corrected data types  
- Validated consistency  

### Feature Engineering
- Created `total = unit_price × quantity`

### 5️⃣ Load Data into MySQL

```python
engine_mysql = create_engine("mysql+pymysql://root:YOUR_PASSWORD@localhost:3306/walmart")
df.to_sql(name="walmart_table", con=engine_mysql, if_exists="append", index=False) python
```

## SQL Business Analysis

---

### Payment Method Analysis

Digital payments contribute **~78% of total revenue**.

**Business Insight:**  
Customers strongly prefer digital payments over cash.

---

### Average Basket Size

Average items per transaction: **2.36 items**

**Opportunity:**  
Cross-selling and bundle strategies can increase overall revenue per customer.

---

### Revenue by Branch

Top-performing branches consistently generate higher revenue compared to others.

**Business Interpretation:**  
Revenue variation across branches may be influenced by:
- Location
- Customer demographics
- Product mix strategy

---

### Top 10% High-Value Transactions

Using the **NTILE window function**, premium transactions were identified.

**Insight:**  
A small customer segment contributes disproportionately high revenue.

**Business Strategy:**  
Introduce loyalty programs or premium memberships to retain high-value customers.

---

### Profit Margin Analysis

Profit margins across categories are similar (**~38–40%**).

**Conclusion:**  
Revenue differences are driven primarily by **sales volume**, not margin percentage.

---

## Skills Demonstrated

- SQL Aggregations
- Subqueries
- Window Functions (NTILE, RANK)
- Contribution Percentage Calculation
- Data Cleaning using Pandas
- SQLAlchemy Database Integration
- Business Insight Generation

---

## Project Structure
Walmart-Retail-SQL-Analysis/
│
├── data/
├── project.ipynb
├── walmart_analysis.sql
├── requirements.txt
└── README.md


---

## Future Enhancements

- Dashboard integration (Power BI / Tableau)
- Automated ETL pipeline
- Sales forecasting model
- Customer segmentation
