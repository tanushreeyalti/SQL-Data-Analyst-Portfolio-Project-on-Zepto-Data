# 🛒 Zepto E-commerce SQL Data Analyst Portfolio Project

A **real-world SQL Data Analytics portfolio project** using **Zepto's e-commerce inventory dataset**.  
This project demonstrates **end-to-end data analytics workflow**: from **data exploration and cleaning** to **business insights generation**, just like in a professional retail analytics role.

---

## 📌 Project Overview

**Objective:** Analyze e-commerce inventory data to extract meaningful business insights using SQL.  

In this project, I:

- ✅ Created a **PostgreSQL database** for Zepto’s inventory dataset
- ✅ Performed **Exploratory Data Analysis (EDA)**
- ✅ Cleaned and transformed **raw data for analysis**
- ✅ Derived **business-focused insights** for decision-making

This project is a **portfolio-ready example** to showcase **SQL and data analytics skills** to recruiters.

---

## 📁 Dataset Overview

The dataset represents **realistic e-commerce inventory data**, where each row is a **unique SKU**.  

| Column Name                | Description                                               |
|----------------------------|-----------------------------------------------------------|
| `sku_id`                   | Unique identifier for each product                        |
| `name`                     | Product name as listed on Zepto                           |
| `category`                 | Product category (Fruits, Snacks, Beverages, etc.)        |
| `mrp`                      | Maximum Retail Price (₹)                                  |
| `discountPercent`          | Discount applied on MRP (%)                               |
| `discountedSellingPrice`   | Price after discount (₹)                                  |
| `availableQuantity`        | Units available in inventory                              |
| `weightInGms`              | Product weight in grams                                   |
| `outOfStock`               | Boolean flag for stock status                             |
| `quantity`                 | Number of units per package                               |

---

## 🔧 Project Workflow

### 1️⃣ Database & Table Creation

```sql
CREATE TABLE zepto (
  sku_id SERIAL PRIMARY KEY,
  category VARCHAR(120),
  name VARCHAR(150) NOT NULL,
  mrp NUMERIC(8,2),
  discountPercent NUMERIC(5,2),
  availableQuantity INTEGER,
  discountedSellingPrice NUMERIC(8,2),
  weightInGms INTEGER,
  outOfStock BOOLEAN,
  quantity INTEGER
);

