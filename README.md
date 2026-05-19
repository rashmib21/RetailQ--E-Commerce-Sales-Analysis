# RetailQ--E-Commerce-Sales-Analysis


# RetailIQ — E-Commerce Sales Analysis 🛒📊

> Analyzing 800,000+ real UK retail transactions to uncover revenue patterns, customer behaviour, and business insights using Python data science libraries.

---

## 📌 Project Overview

RetailIQ is an end-to-end data science project built on the **Online Retail II UCI dataset** — a real-world dataset containing 800K+ transactions from a UK-based non-store online retail company (2009–2011).

The goal was to answer real business questions:
- Which countries and products drive the most revenue?
- When are peak sales seasons?
- Which customers are high-value vs at-risk?
- What does the revenue distribution look like across markets?

---

## 🚀 Key Findings

- 🇬🇧 **UK dominates** — £14.7M revenue (85%+ of total across all countries)
- 📈 **November peak** — £1.16M in a single month (holiday season surge)
- 🏆 **#1 Bestseller** — "World War 2 Gliders" with 100,000+ units sold
- 🌍 **Netherlands** — highest order value variation (mix of wholesale + retail buyers)
- ⚠️ **1,151 outlier transactions** flagged above £694 — potential high-value wholesale accounts

---

## 🛠️ Tech Stack

| Library | Purpose |
|---|---|
| **Python** | Core programming language |
| **Pandas** | Data cleaning, groupby, pivot tables, RFM segmentation |
| **NumPy** | Vectorized operations, outlier detection |
| **Matplotlib** | Static multi-chart dashboard |
| **Seaborn** | Heatmap (Country × Month), Boxplot distribution |
| **Plotly** | Interactive world map, animated bar chart, sunburst chart |
| **Jupyter Notebook** | Analysis report with executive summary |

---

## 📁 Project Structure

```
retailiq-analysis/
│
├── RetailIQ_Analysis.ipynb       # Main Jupyter Notebook
├── online_retail_II.csv          # Dataset (download from Kaggle)
├── matplotlib_dashboard.png      # Static charts — 3 subplots
├── seaborn_charts.png            # Heatmap + Boxplot
├── map_chart.html                # Interactive Plotly world map
├── products_chart.html           # Interactive top products chart
├── monthly_trend.html            # Interactive monthly revenue trend
└── README.md                     # Project documentation
```

---

## 📊 Visualizations

### 1. Monthly Revenue Trend (Matplotlib)
Line chart showing revenue across 25 months — clear November peaks in both 2010 and 2011.

### 2. Top 10 Countries by Revenue (Matplotlib)
Bar chart showing UK's overwhelming dominance vs other markets.

### 3. Top 10 Products by Quantity Sold (Matplotlib)
Horizontal bar chart — "World War 2 Gliders" leads at 100K+ units.

### 4. Country × Month Revenue Heatmap (Seaborn)
Colour-coded heatmap showing which country performed in which month. UK row is consistently dark red.

### 5. Revenue Distribution by Country (Seaborn)
Boxplot comparing order value spread across top 5 countries. Netherlands has the widest box — most varied order sizes.

### 6. Interactive World Map (Plotly)
Choropleth map — hover over any country to see exact revenue. Shareable as HTML without Python.

### 7. Interactive Monthly Trend (Plotly)
Line chart with hover tooltips — exact revenue figures on mouse-over.

---

## 🔍 Data Cleaning Steps

1. Loaded 805,549 raw transactions from CSV
2. Parsed `InvoiceDate` as datetime
3. Removed cancelled orders (Invoice starting with 'C')
4. Dropped negative Quantity and Price values
5. Removed null `Description` and `Customer ID` rows
6. Created `Revenue` column = Quantity × Price (via NumPy)
7. Added `Month` and `Year` columns for time-series analysis

**Final clean dataset: 805,549 rows × 11 columns**

---

## 🧠 Business Insights

| Insight | Business Action |
|---|---|
| UK = 85% of revenue | Focus retention efforts on UK customers |
| November = peak month | Plan inventory 3 months in advance |
| 1,151 high-value outlier transactions | Assign dedicated account managers |
| Netherlands order variation | Create separate wholesale & retail strategies |
| Top 3 products are gift/novelty items | Expand gift-ware product range |

---

## ▶️ How to Run

1. Clone this repository
```bash
git clone https://github.com/rashmib21/retailiq-analysis.git
cd retailiq-analysis
```

2. Install required libraries
```bash
pip install pandas numpy matplotlib seaborn plotly openpyxl
```

3. Download the dataset from Kaggle
- Dataset: [Online Retail II UCI](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci)
- Place `online_retail_II.csv` in the project folder

4. Open the notebook
```bash
jupyter notebook RetailIQ_Analysis.ipynb
```

Or open directly in **Google Colab** — upload the CSV and run all cells.

---

## 📂 Dataset

**Source:** [Online Retail II UCI — Kaggle](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci)

**Description:** Real transactions from a UK-based online retailer selling unique all-occasion gift-ware (01/12/2009 to 09/12/2011). Many customers are wholesalers.

**Columns:** Invoice, StockCode, Description, Quantity, InvoiceDate, Price, Customer ID, Country

---

## 👩‍💻 About the Author

**Rashmi Barethiya**
Full-Stack Developer transitioning into Data Science
MCA Graduate — DAVV Indore

- 🔗 [LinkedIn](https://www.linkedin.com/in/rashmi-barethiya-2823b1227)
- 💻 [GitHub](https://github.com/rashmib21)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ If you found this project helpful, please give it a star!
