# ASOS Fashion Product Analysis & Stockout Revenue Estimation

## Project Overview

This project analyzes fashion product data from ASOS using Python for exploratory data analysis, brand analysis, pricing insights, and stockout revenue estimation.

The analysis focuses on understanding:

* Product pricing trends
* Brand distribution
* Stock availability
* Estimated lost revenue caused by stockouts
* Brand performance strategies

The project was developed using Jupyter Notebook and common Python data analysis libraries.

---

# Dataset

The dataset used in this project:

* **File:** `products_asos.csv`
* **Source:** Fashion product listing dataset
* **Format:** CSV

The dataset includes information such as:

* Product names
* Descriptions
* Prices
* Brand-related information
* Product sizes
* Stock availability

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

# Project Workflow

## 1. Data Loading

The dataset is imported using Pandas and cleaned for analysis.

Key preprocessing steps include:

* Handling invalid rows
* Converting price columns to numeric values
* Removing missing price values

---

## 2. Brand Extraction & Cleaning

Brand names are extracted from product descriptions and standardized.

Examples:

* `New` → `New Look`
* `River` → `River Island`
* `Miss` → `Miss Selfridge`

This helps create more accurate brand-level analysis.

---

## 3. Stockout Analysis

The notebook estimates:

* Number of out-of-stock sizes
* Stockout rate
* Potential phantom/lost revenue

A custom function is used to identify unavailable product sizes and estimate possible revenue loss.

---

## 4. Brand Strategy Analysis

Brands are analyzed based on:

* Average product price
* Average stockout count
* Stockout rate
* Estimated lost revenue
* Number of products

This provides insight into:

* High-demand brands
* Pricing strategy
* Inventory management opportunities

---

# Key Insights

* Certain brands show significantly higher stockout rates.
* High stockout rates may indicate strong customer demand.
* Lost revenue estimation highlights the financial impact of unavailable inventory.
* Pricing and inventory trends vary considerably across fashion brands.

---
