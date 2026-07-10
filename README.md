# Superstore Market Performance Dashboard 📊

An enterprise-grade data visualization and business intelligence project built with **Power BI**, **SQL**, and **Python**. This project transforms raw retail transactional data into an interactive, high-impact executive dashboard tailored for market performance and operational insights.

## 🖥️ Dashboard Preview
![Superstore Dashboard](image_7fb2e8.png)

---

## 🚀 Project Overview & Scope
In modern retail management, tracking core sales velocity and macro market distribution is essential for sustainable scale. This project addresses data-driven strategy by converting multi-variable transactional structures into clear executive KPIs. 

### Key Analytics & Objectives:
- **Market Velocity Tracking:** Analyzing transaction volumes and values across major segments.
- **Product Portfolio Performance:** Isolating categorical dominance to determine key performance drivers.
- **Geographical Optimization:** Visualizing regional sales trends to isolate supply-chain or localization demands.

---

## 🛠️ Tech Stack & Methodology

### 1. Data Cleaning & Transformation (Python & SQL Context)
Before importing data into the data model, strict validation steps were executed using **SQL Data Definition/Manipulation** statements and **Python (Pandas)** processing to handle structural anomalies, format checking, and metric normalization:

#### 🐍 Python Data Pipeline:
```python
import pandas as pd

# Data normalization and locale mapping pipeline
df = pd.read_csv("SampleSuperstore.csv")
df['Sales'] = pd.to_numeric(df['Sales'], errors='coerce')
df['Quantity'] = pd.to_numeric(df['Quantity'], errors='coerce')
df['Discount'] = pd.to_numeric(df['Discount'], errors='coerce')

# Metric sanity validation
df = df.dropna(subset=['Sales', 'Quantity'])
print("Pipeline normalization completed successfully.")
