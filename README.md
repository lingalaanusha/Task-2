# 📊 Superstore Sales Analysis - EDA & Business Intelligence

## 🎯 Project Overview
A comprehensive business intelligence project analyzing the Superstore dataset to uncover actionable insights, patterns, and trends. This project demonstrates proficiency in SQL, data visualization, and business analysis through exploratory data analysis (EDA) and dashboard creation.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-1.5%2B-green)](https://pandas.pydata.org)
[![SQL](https://img.shields.io/badge/SQL-SQLite%2FMySQL-yellow)](https://sqlite.org)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](LICENSE)

## 📁 Project Structure
```
superstore-analysis/
├── data/                                # Data files
│   ├── superstore.csv                   # Original dataset
│   └── processed_superstore.csv         # Cleaned and processed data
├── notebooks/                           # Jupyter notebooks
│   └── superstore_eda.ipynb             # Complete EDA analysis
├── sql/                                 # SQL queries and scripts
│   └── business_queries_superstore.py   # Python script to run SQL queries
├── visualizations/                      # Generated charts and plots
│   ├── categorical_distribution.png
│   ├── sales_profit_distribution.png
│   ├── time_series_analysis.png
│   ├── correlation_matrix.png
│   ├── scatter_plots.png
│   ├── category_analysis.png
│   ├── segment_analysis.png
│   └── regional_analysis.png
├── sql_visualizations/                  # Charts from SQL analysis
│   ├── monthly_sales_trend.png
│   ├── category_sales_pie.png
│   └── segment_performance.png
├── dashboard/                           # Dashboard materials
│   └── index.html                       # Static dashboard 
├── output/                              # Analysis outputs
│   ├── sql_query_results.xlsx           # All SQL query results
│   └── superstore.db                    # SQLite database
├── requirements.txt                     # Python dependencies
└── README.md                            # This file
```

## 📊 Dataset Information
- **Dataset**: Superstore Sales Data (Tableau Sample Dataset)
- **Source**: [Plotly GitHub Repository](https://github.com/plotly/datasets)
- **Rows**: 9,994 transactions
- **Columns**: 21 features
- **Time Period**: 2014-2017
- **Size**: ~1.4 MB

### Key Features:
- **Order Details**: Order ID, Order Date, Ship Date, Ship Mode
- **Customer Information**: Customer ID, Customer Name, Segment, Country, Region, State, City, Postal Code
- **Product Information**: Product ID, Category, Sub-Category, Product Name
- **Sales Metrics**: Sales, Quantity, Discount, Profit

## 🎯 Objectives
1. Perform descriptive statistics and univariate analysis
2. Answer key business questions using SQL
3. Conduct multivariate analysis and correlation studies
4. Create static dashboard mock-up with key KPIs
5. Generate actionable business insights and recommendations

## 🛠️ Technologies Used
- **Programming**: Python 3.8+
- **Data Analysis**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Database**: SQLite, MySQL (optional)
- **SQL**: Advanced queries with CTEs, window functions, joins
- **Tools**: Jupyter Notebook, VS Code, Excel, PowerPoint

## 🚀 Quick Start

### Prerequisites
```bash
Python 3.8 or higher
pip (Python package manager)
```

### Installation & Setup

#### Method 1: Automatic Setup (Recommended)
```bash
# Clone or download the project files
# Run the setup script
python setup_superstore.py
```

#### Method 2: Manual Setup
```bash
# 1. Create project directory
mkdir superstore-analysis && cd superstore-analysis

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn openpyxl

# 3. Download the dataset
curl -o superstore.csv https://raw.githubusercontent.com/plotly/datasets/master/superstore.csv

# 4. Run the EDA notebook
jupyter notebook notebooks/superstore_eda.ipynb

# 5. Run SQL queries
python sql/business_queries_superstore.py
```

## 📈 Key Analysis Performed

### 1. Descriptive Statistics & Univariate Analysis
- Distribution analysis of sales, profit, and quantities
- Categorical variable distribution (categories, regions, segments)
- Summary statistics for all numerical columns

### 2. SQL Business Questions Answered
The project answers 10 key business questions using SQL:

1. **Top 5 products by sales** in the last 6 months
2. **Monthly sales trend** with growth rate calculation
3. **Region with highest profit margin** and detailed analysis
4. **Customer segment performance** across categories
5. **Shipping mode analysis** and impact on profitability
6. **Category and sub-category performance** breakdown
7. **Top 10 customers by lifetime value**
8. **Discount impact analysis** on profit margins
9. **Monthly seasonality patterns** and insights
10. **Profitability analysis** by various dimensions

### 3. Multivariate Analysis & Correlation
- Correlation matrix of numerical variables
- Scatter plots exploring relationships (sales vs profit, discount vs margin)
- Time series analysis with trend lines
- Pair plots for multivariate relationships

### 4. Advanced Analytics
- Customer segmentation analysis
- RFM (Recency, Frequency, Monetary) analysis
- Cohort analysis for customer retention
- Profit margin optimization insights

## 📊 Key Insights Discovered

### 🔥 Top Findings:
1. **Revenue Distribution**: Technology category generates 37% of total sales with highest profit margins (16.8%)
2. **Seasonal Patterns**: December shows highest sales (holiday season), February lowest
3. **Customer Behavior**: 28% customer repeat rate, Home Office segment has highest average order value ($241)
4. **Regional Performance**: West region leads with 32% of total sales and highest profitability
5. **Discount Impact**: Discounts above 20% significantly reduce profit margins
6. **Shipping Efficiency**: Same Day shipping has highest profit margins despite lower usage

### 📈 Performance Metrics:
- **Total Sales**: $2,297,200.86
- **Total Profit**: $286,397.00
- **Average Profit Margin**: 12.46%
- **Average Order Value**: $229.86
- **Customer Repeat Rate**: 28.04%

## 📋 SQL Queries Overview

### Complex Queries Implemented:
```sql
-- Window functions for growth calculations
SELECT month, sales,
       (sales - LAG(sales) OVER (ORDER BY month)) / 
       LAG(sales) OVER (ORDER BY month) * 100 as growth_rate
FROM monthly_sales;

-- CTEs for complex calculations
WITH cohort_analysis AS (
    SELECT customer_id, MIN(order_date) as cohort_date
    FROM orders GROUP BY customer_id
)
SELECT * FROM cohort_analysis;

-- Advanced JOIN operations
SELECT c.segment, p.category, 
       SUM(o.sales) as total_sales,
       AVG(o.profit/o.sales)*100 as avg_margin
FROM orders o
JOIN customers c ON o.customer_id = c.customer_id
JOIN products p ON o.product_id = p.product_id
GROUP BY c.segment, p.category;
```

### Query Features:
- ✅ Common Table Expressions (CTEs)
- ✅ Window Functions (LAG, RANK, SUM OVER)
- ✅ Complex JOIN operations
- ✅ Conditional Aggregations (CASE WHEN with SUM)
- ✅ Date functions and calculations
- ✅ Subqueries and nested queries

## 📱 Dashboard & KPIs

### Proposed Dashboard KPIs:
1. **Monthly Sales Growth** (%) - Target: >10%
2. **Overall Profit Margin** (%) - Target: >12%
3. **Customer Repeat Rate** (%) - Target: >35%
4. **Average Order Value** ($) - Target: >$250
5. **Top Category Performance** - Technology
6. **Regional Sales Distribution** - West: 35%
7. **Shipping Efficiency** - Same Day: 95% on-time delivery

### Dashboard Components:
- **Executive Summary**: Key metrics at a glance
- **Sales Trends**: Monthly and quarterly trends
- **Category Performance**: Sales and margin by category
- **Customer Analysis**: Segment performance and retention
- **Regional Heatmap**: Geographical performance
- **Top Performers**: Best products and customers
- **Recommendations**: Actionable insights

## 💡 Business Recommendations

### Immediate Actions:
1. **Focus on Technology**: Increase inventory and marketing for Technology category
2. **Optimize Discounts**: Cap discounts at 20% for low-margin products
3. **Target Corporate Clients**: Develop B2B sales strategy with premium offerings

### Medium-term Strategies:
4. **Customer Loyalty**: Implement rewards program for repeat buyers
5. **Regional Expansion**: Invest in West region operations and marketing
6. **Shipping Optimization**: Improve Standard Class delivery times

### Long-term Initiatives:
7. **Product Bundling**: Create bundles of top-selling products
8. **Data-Driven Decisions**: Implement regular EDA and reporting cycles
9. **Customer Segmentation**: Personalized marketing based on segment behavior

## 🎬 Video Presentation Guide

### LinkedIn Video (5-7 minutes):
1. **Introduction** (30 sec): Project overview and objectives
2. **Data Overview** (1 min): Dataset description and cleaning process
3. **Key Insights** (2 min): Top 3 findings with visualizations
4. **SQL Demonstration** (1.5 min): Walkthrough of complex query
5. **Dashboard Preview** (1 min): Show KPI dashboard mockup
6. **Conclusion** (30 sec): Learnings and business impact

### Video Script Highlights:
- Show correlation between discounts and profit margins
- Demonstrate SQL window function for growth calculations
- Present actionable recommendations for business improvement
- Highlight technical skills learned during the project

## 📊 Expected Outputs

### Files Generated:
1. **Processed Data**: `data/processed_superstore.csv`
2. **SQL Database**: `output/superstore.db`
3. **Query Results**: `output/sql_query_results.xlsx`
4. **Visualizations**: 11+ charts in `visualizations/` and `sql_visualizations/`
5. **Dashboard**: `dashboard/dashboard_mockup.pptx`

### Console Output Includes:
- Descriptive statistics summary
- Key business metrics
- Top products and customers
- Insights and recommendations

## 🧪 Running the Analysis

### Step 1: EDA Analysis
```bash
# Open and run the Jupyter notebook
jupyter notebook notebooks/superstore_eda.py

# Or run as Python script
python notebooks/superstore_eda.py
```

### Step 2: SQL Analysis
```bash
# Run all SQL queries and generate results
python sql/run_sql_queries.py

# Output: sql_query_results.xlsx and visualizations
```

### Step 3: Generate Dashboard
```bash
# Review and customize the PowerPoint template
# Update with your specific insights and KPIs
```

## 📚 Learning Outcomes

### Technical Skills Developed:
- ✅ Advanced SQL query writing and optimization
- ✅ Data cleaning and preprocessing with Pandas
- ✅ Statistical analysis and hypothesis testing
- ✅ Data visualization with Matplotlib and Seaborn
- ✅ Business intelligence and KPI definition
- ✅ Dashboard design and presentation

### Business Skills Developed:
- ✅ Translating data insights into business recommendations
- ✅ Identifying key performance indicators
- ✅ Analyzing customer behavior and segmentation
- ✅ Understanding profitability drivers
- ✅ Making data-driven decisions

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Areas for Improvement:
- Add machine learning models for sales forecasting
- Implement interactive dashboard with Tableau/Power BI
- Add more advanced statistical tests
- Include customer lifetime value prediction

