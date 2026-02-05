# 📊 Superstore Sales Analysis - EDA & Business Intelligence (Indian Rupees Version)

## 🎯 Project Overview
A comprehensive business intelligence project analyzing the Superstore dataset to uncover actionable insights, patterns, and trends. This project demonstrates proficiency in SQL, data visualization, and business analysis through exploratory data analysis (EDA) and dashboard creation.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-1.5%2B-green)](https://pandas.pydata.org)
[![SQL](https://img.shields.io/badge/SQL-SQLite%2FMySQL-yellow)](https://sqlite.org)

## 📁 Project Structure
```
superstore-analysis-inr/
├── data/                                # Data files
│   ├── superstore.csv                   # Original dataset
│   └── processed_superstore.csv          # Cleaned 
├── notebooks/                           # Jupyter notebooks
│   ├── superstore_eda.ipynb         # Complete EDA analysis 
├── sql/                                 # SQL queries and scripts
│   └── business_queries_superstore.py   # SQL queries
├── visualizations/                      # Generated charts and plots
│   ├── categorical_distribution.png
│   ├── sales_profit_distribution_inr.png
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
│   ├── index.html                   # Static dashboard 
├── output/                              # Analysis outputs
│   ├── sql_query_results.xlsx       # All SQL query results 
│   ├── superstore.db                    # SQLite database
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

### Key Features (INR Converted):
- **Order Details**: Order ID, Order Date, Ship Date, Ship Mode
- **Customer Information**: Customer ID, Customer Name, Segment, Country, Region, State, City, Postal Code
- **Product Information**: Product ID, Category, Sub-Category, Product Name
- **Sales Metrics**: Sales (₹), Quantity, Discount, Profit (₹)

## 🎯 Objectives
1. Perform descriptive statistics and univariate analysis 
2. Answer key business questions using SQL 
3. Conduct multivariate analysis and correlation studies
4. Create static dashboard mock-up with key KPIs 
5. Generate actionable business insights and recommendations for Indian market

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

#### Method 1: Automatic Setup 
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
pip install pandas numpy matplotlib seaborn openpyxl forex-python 

# 3. Download the dataset
curl -o superstore.csv https://raw.githubusercontent.com/plotly/datasets/master/superstore.csv

# 5. Run the EDA notebook 
jupyter notebook notebooks/superstore_eda.ipynb

# 6. Run SQL queries with INR
python sql/business_queries_superstore.py
```

## 📈 Key Analysis Performed (INR Converted)

### 1. Descriptive Statistics & Univariate Analysis
- Distribution analysis of sales (₹), profit (₹), and quantities
- Categorical variable distribution (categories, regions, segments)
- Summary statistics for all numerical columns 

### 2. SQL Business Questions Answered (INR)
The project answers 10 key business questions using SQL :

1. **Top 5 products by sales** in the last 6 months (₹ values)
2. **Monthly sales trend** with growth rate calculation (₹)
3. **Region with highest profit margin** and detailed analysis (₹)
4. **Customer segment performance** across categories (₹)
5. **Shipping mode analysis** and impact on profitability (₹)
6. **Category and sub-category performance** breakdown (₹)
7. **Top 10 customers by lifetime value** (₹)
8. **Discount impact analysis** on profit margins (₹)
9. **Monthly seasonality patterns** and insights (₹)
10. **Profitability analysis** by various dimensions (₹)

### 3. Multivariate Analysis & Correlation
- Correlation matrix of numerical variables
- Scatter plots exploring relationships (sales vs profit in ₹, discount vs margin)
- Time series analysis with trend lines (₹ values)
- Pair plots for multivariate relationships

## 📊 Key Insights Discovered (INR Values)

### 🔥 Top Findings (Converted to INR):
1. **Revenue Distribution**: Technology category generates ₹6.94 Crores (37% of total) with highest profit margins (16.8%)
2. **Seasonal Patterns**: December shows highest sales (₹2.32 Crores - holiday season), February lowest (₹1.45 Crores)
3. **Customer Behavior**: 28% customer repeat rate, Home Office segment has highest average order value (₹20,000)
4. **Regional Performance**: West region leads with ₹1.87 Crores (32% of total) and highest profitability
5. **Discount Impact**: Discounts above 20% significantly reduce profit margins in INR terms
6. **Shipping Efficiency**: Same Day shipping has highest profit margins (15.2%) despite lower usage

### 📈 Performance Metrics (INR):
- **Total Sales**: ₹19.07 Crores ($2,297,200.86 × 83)
- **Total Profit**: ₹2.37 Crores ($286,397.00 × 83)
- **Average Profit Margin**: 12.46%
- **Average Order Value**: ₹19,090 ($229.86 × 83)
- **Customer Repeat Rate**: 28.04%
- **Exchange Rate Used**: 1 USD = ₹83

### 🏆 Top 5 Products by Sales (INR):
1. **Canon imageCLASS 2200**: ₹51.13 Lakhs sales, ₹10.96 Lakhs profit
2. **Fellowes PB500 Electric**: ₹35.19 Lakhs sales, ₹8.13 Lakhs profit  
3. **HP Designjet T7100ps**: ₹33.03 Lakhs sales, ₹6.97 Lakhs profit
4. **Samsung Galaxy Note 4**: ₹31.37 Lakhs sales, ₹6.31 Lakhs profit
5. **Cisco TelePresence System**: ₹28.64 Lakhs sales, ₹5.73 Lakhs profit
   
```

## 📱 Dashboard & KPIs

### Dashboard KPIs (Indian Rupees):
1. **Monthly Sales Growth** (%) - Target: >10%
2. **Overall Profit Margin** (%) - Target: >12%
3. **Customer Repeat Rate** (%) - Target: >35%
4. **Average Order Value** (₹) - Target: >₹20,000
5. **Top Category Performance** - Technology: ₹6.94 Crores
6. **Regional Sales Distribution** - West: 32% (₹6.08 Crores)
7. **Shipping Efficiency** - Same Day: 95% on-time delivery

### Dashboard Components:
- **Executive Summary**: Key metrics 
- **Sales Trends**: Monthly and quarterly trends 
- **Category Performance**: Sales and margin 
- **Customer Analysis**: Segment performance and retention
- **Regional Heatmap**: Geographical performance 
- **Top Performers**: Best products and customers

## 💡 Business Recommendations 

### Immediate Actions:
1. **Focus on Technology**: Increase inventory and marketing for Technology category - highest ROI at 16.8% margin
2. **Optimize Discounts**: Cap discounts at 20% for low-margin products to protect profitability
3. **Target Corporate Clients**: Develop B2B sales strategy with premium offerings targeting corporate segment

### Medium-term Strategies:
4. **Customer Loyalty**: Implement rewards program for repeat buyers with benefits
5. **Regional Expansion**: Invest in West region operations and marketing (highest sales at ₹6.08 Crores)
6. **Shipping Optimization**: Improve Standard Class delivery times while maintaining cost efficiency

### Long-term Initiatives:
7. **Product Bundling**: Create bundles of top-selling products to increase average order value above ₹20,000
8. **Data-Driven Decisions**: Implement regular EDA and reporting cycles with INR metrics
9. **Customer Segmentation**: Personalized marketing based on segment behavior and spending patterns

### India-Specific Recommendations:
10. **Festival Sales**: Leverage Diwali, Dussehra, and other festival seasons for special promotions
11. **Regional Pricing**: Consider regional pricing strategies based on state-level economic factors
12. **Payment Options**: Integrate popular Indian payment methods (UPI, Net Banking, EMI options)

### Step 1: EDA Analysis 
```bash
# Run EDA 
python notebooks/superstore_eda.py

### Step 2: SQL Analysis 
```bash
# Run all SQL queries 
python sql/business_queries_superstore.py

# Output: sql_query_results.xlsx and INR visualizations

### Step 3: Generate Dashboard
```bash
# Open the HTML dashboard
open dashboard/index.html

## 📊 Expected Outputs 

### Files Generated:
1. **Processed Data**: `data/processed_superstore_.csv`
2. **SQL Database**: `output/superstore.db` 
3. **Query Results**: `output/sql_query_results.xlsx` 
4. **Visualizations**: 11+ charts in `visualizations/` and `sql_visualizations/`
5. **Dashboard**: `dashboard/index.html` (Static dashboard)

### Console Output Includes:
- Descriptive statistics 
- Key business metrics 
- Top products and customers 
- Insights and recommendations 

## 📚 Learning Outcomes 

### Technical Skills Developed:
- ✅ Advanced SQL query writing with currency conversion
- ✅ Data cleaning and preprocessing with Pandas including currency conversion
- ✅ Statistical analysis with multi-currency considerations
- ✅ Data visualization with Indian currency formatting
- ✅ Business intelligence with localization for Indian market
- ✅ Dashboard design with INR KPIs and metrics

### Business Skills Developed:
- ✅ Translating data insights into business recommendations for Indian market
- ✅ Understanding currency impact on business metrics
- ✅ Analyzing customer behavior in local currency context
- ✅ Understanding profitability drivers in INR terms
- ✅ Making data-driven decisions with currency considerations



**Disclaimer**: Currency conversion is for analytical purposes only. Actual financial calculations should use current, verified exchange rates.
