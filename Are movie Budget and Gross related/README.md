# 🎬 Gross vs Budget Correlation Analysis

## Overview

This project analyzes the relationship between a movie's **production budget** and its **gross revenue** using Python-based data analysis techniques.

The goal of the project is to determine whether higher-budget movies tend to generate higher box office revenue and to uncover patterns, trends, and correlations within the movie industry dataset.

---

# 📊 Project Objectives

* Explore relationships between movie budgets and gross earnings
* Clean and preprocess movie industry data
* Perform correlation analysis on numerical features
* Identify strong positive or negative relationships
* Create visualizations to understand financial trends in movies
* Practice exploratory data analysis (EDA) techniques

---

# 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook**

---

# 📁 Dataset

The dataset contains movie industry information including:

* Movie Name
* Genre
* Budget
* Gross Revenue
* Company
* Runtime
* Score
* Votes
* Release Year
* Director
* Star Cast

The analysis mainly focuses on:

* **Budget**
* **Gross Revenue**

---

# 🔍 Analysis Workflow

## 1. Import Required Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

These libraries are used for:

* Data manipulation
* Statistical analysis
* Visualization
* Correlation mapping

---

## 2. Load the Dataset

```python
df = pd.read_csv('movies.csv')
```

The movie dataset is loaded into a Pandas DataFrame.

---

## 3. Data Cleaning

The notebook handles:

* Missing values
* Data formatting
* Duplicate checks
* Data type conversions

Example:

```python
df = df.dropna()
```

---

## 4. Scatter Plot Visualization

A scatter plot is used to visualize the relationship between movie budgets and gross revenue.

```python
plt.scatter(x=df['budget'], y=df['gross'])
plt.title('Budget vs Gross Earnings')
plt.xlabel('Gross Earnings')
plt.ylabel('Budget for Film')
plt.show()
```

This helps identify trends and possible correlations.

---

## 5. Correlation Analysis

The project computes correlations between numerical variables.

```python
correlation_matrix = df.corr(numeric_only=True)
```

A heatmap is then created to visualize the strength of relationships.

```python
sns.heatmap(correlation_matrix, annot=True)
```

---

# 📈 Key Findings

* Movies with larger production budgets generally tend to earn higher gross revenue.
* Budget and gross revenue show a strong positive correlation.
* Some low-budget movies still achieve high earnings, indicating outliers and market variability.
* Correlation heatmaps make it easier to identify financial relationships between variables.

---

# 📊 Visualizations Included

The notebook includes:

* Scatter plots
* Correlation heatmaps
* Trend analysis charts
* Pairwise relationship exploration

---