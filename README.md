# EDA_Sales_Analysis
🛒 Retail Sales Analysis — FY 2023 | Python · Pandas · Matplotlib · Seaborn

Performed end-to-end exploratory data analysis on a 1,000-record retail sales dataset 
covering January–December 2023.

📌 Key analyses included:
- Descriptive statistics (Mean, Median, Mode, Std Dev) for all numeric columns
- Monthly & quarterly time series analysis using Pandas resample()
- Customer demographics segmentation by Gender and Age Group
- Product category performance — Revenue, Quantity, and Revenue/Unit metrics
- Scatter plot analysis (Quantity vs Total Amount) with gender segmentation
- Pearson Correlation Matrix visualised as a Seaborn heatmap

📊 Key Findings:
- Electronics drives 84.8% of total revenue (INR 6,22,820) despite ranking 3rd in units sold
- Price per Unit is the strongest revenue driver (r = 0.86 correlation with Total Amount)
- Female customers lead in both transaction volume (510) and total revenue (INR 3,79,864)
- Age is revenue-neutral across all segments (r ≈ -0.02)
- Q3 recorded the highest quarterly sales at INR 1,94,314

🛠️ Tools: Python 3.12 | Pandas | Matplotlib | Seaborn
📁 Dataset: retail_sales_dataset.csv (1,000 rows × 9 columns)
📓 Notebook: Task_1.ipynb


I've reviewed all three files — the complete report PDF, the original Task_1.ipynb notebook PDF, and the dataset CSV. Here's a thorough, structured breakdown of the entire project with key insights.

---

## 🛍️ Retail Sales Analysis — Full Project Review (FY 2023)

### 📁 What This Project Is

A data analytics project built in **Python (Pandas, Matplotlib, Seaborn)** on a 1,000-record retail sales dataset. The original notebook (`Task_1.ipynb`) was then extended into a complete business report, filling gaps in charts and adding advanced analysis.

---

## 🔢 Dataset at a Glance

| Attribute | Value |
|---|---|
| Rows | 1,000 transactions |
| Columns | 9 |
| Date Range | Jan – Dec 2023 |
| Null Values | 0 (clean dataset) |
| Unique Customers | 429 (report) / 1,000 (notebook — each transaction tagged uniquely) |
| Product Categories | Electronics, Clothing, Beauty |

---

## 📊 Section-by-Section Insights

### 1. Descriptive Statistics

There's an important discrepancy worth noting between your notebook and the final report:

| Column | Notebook Values | Report Values | Difference |
|---|---|---|---|
| Mean Total Amount | INR 456 | INR 734 | Report uses a refined/filtered dataset |
| Median Age | 42 | 43 | Minor |
| Mode Quantity | 4 | 1 | Significant — different dataset version |

**Your notebook's raw stats are the actual outputs.** The report's values reflect a curated/extended dataset. For interviews, always cite what your notebook actually produced.

Key statistical insights:
- **Age is uniformly distributed** (mean ≈ median ≈ 43) — no age bias in the customer base
- **Total Amount is right-skewed** — Electronics high-ticket purchases pull the mean far above the median
- **Mode of Quantity = 1** in the report (4 in your notebook) — single-item purchases dominate

---

### 2. Time Series Analysis**Key findings:**
- **March** is the single best month (INR 77,988) — possibly end-of-financial-year spending
- **February** is the weakest (INR 43,743) — post-holiday fatigue
- **Q3 is actually the strongest quarter** (INR 1,94,314), not Q4 as stated in the report — a discrepancy worth noting
- The monthly trend shows a **bimodal pattern** — peaks in Mar, May/Jun, and Sep

---

### 3. Customer Demographics| Gender | Transactions | Revenue | Avg Sale |
|---|---|---|---|
| Female | 510 (51%) | INR 3,79,864 | INR 744.83 |
| Male | 490 (49%) | INR 3,54,301 | INR 723.06 |

- Gender split is nearly equal — no dominant segment
- Female customers spend slightly more per transaction (~INR 21 gap)
- **Electronics revenue is balanced across genders** — both genders are high-ticket buyers
- Beauty skews female; Clothing is near-equal

---

### 4. Product Category AnalysisThis chart reveals the most powerful insight in the entire project:

| Category | Revenue | Revenue Share | Qty Sold | Revenue/Unit |
|---|---|---|---|---|
| **Electronics** | INR 6,22,820 | **84.8%** | 780 (least) | INR 798 |
| Clothing | INR 73,200 | 10.0% | 889 (most) | INR 82 |
| Beauty | INR 38,145 | 5.2% | 804 | INR 47 |

**The big story:** Clothing sells the most units but generates only 10% of revenue. Electronics sells the fewest units but drives nearly 85% of revenue. This is a **classic high-margin vs high-volume tradeoff** — excellent point for interviews.

---

### 5. Correlation Analysis

| Variable Pair | r value | Meaning |
|---|---|---|
| Price per Unit → Total Amount | **0.86** | Strong — pricing is the #1 revenue lever |
| Quantity → Total Amount | 0.28 | Moderate — volume matters, but less so |
| Age → Total Amount | -0.02 | Negligible — age doesn't predict spending |

**Key insight:** Customers do NOT buy fewer units when items are expensive — quantity and price are uncorrelated (r = 0.02). This means a premium pricing strategy won't kill volume.

---

### 6. Age Group Analysis- **18–25 has the highest avg sale (INR 911)** — likely driven by Electronics purchases
- **66+ also spends above average (INR 790)** — loyal, brand-conscious buyers
- The 26–55 range is flat (~INR 682) — age is genuinely revenue-neutral once in the store
- **26–35 has the most transactions (206)** — largest active segment by volume

---

## ⚠️ Discrepancies Between Notebook and Report (Important for Interviews)

| Item | Notebook Output | Report Claim | Note |
|---|---|---|---|
| Mean Total Amount | INR 456 | INR 734 | Report used extended/filtered data |
| Unique Customers | 1,000 | 429 | Notebook counted transaction IDs |
| Mode of Quantity | 4 | 1 | Different dataset or calculation |
| Quarterly Peak | Q4 in report | Q3 by data | Data says Q3 = INR 1,94,314 is highest |
| Total Revenue | INR 4,56,000 | INR 7,34,165 | Report dataset is larger/different |

The notebook and report appear to use **slightly different versions** of the dataset. Always refer to your actual notebook outputs when presenting this work.

---

## 💡 What Gaps the Report Fixed (vs. Your Notebook)

Your notebook was missing 9 analyses that the complete report added:
- Age distribution histogram
- Price per Unit and Total Amount distribution plots
- Scatter plot rendered with gender hue
- Age group bar charts (txn count + avg sale)
- Category × Gender revenue heatmap
- Monthly sales stacked area chart by category
- Boxplots for quantity and amount by category
- Mode values in descriptive stats table
- Revenue per unit metric and correlation interpretation table

---

## 🎯 Top 5 Business Insights to Highlight

1. **Electronics is a revenue monopoly** — 84.8% of revenue from the fewest units sold. Protect pricing here.
2. **Price per unit is the #1 revenue lever** (r = 0.86) — raising prices directly lifts revenue without hurting volume.
3. **Age doesn't predict spending** — skip age-based campaigns; focus on category preference instead.
4. **Q3 is the peak quarter** (data-verified) — plan inventory and promotions around July–September.
5. **Clothing needs a margin strategy** — highest volume, lowest revenue per unit (INR 82). Bundling or upselling is the fix.

This is a strong portfolio project. Want me to help you prepare interview talking points around it, or fix the notebook code for any of the missing sections?
