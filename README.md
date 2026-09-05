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
