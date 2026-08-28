Sector-wise Financial Performance Analysis using Web Scraping & EDA
Project Overview
This project focuses on sector-wise financial performance analysis using automated web scraping and exploratory data analysis. Financial data was collected from Screener.in across multiple sectors and structured into a single dataset for analysis.

The project combines Python, Web Scraping, Data Cleaning, Descriptive Statistics, Inferential Statistics, EDA, and Data Visualization to identify patterns in company size, profitability, growth, valuation, and capital efficiency.

Business Problem
Investors and analysts often find it difficult to compare the financial performance of companies across different sectors because financial information is distributed across multiple webpages.

Manual collection and comparison of metrics such as Market Capitalization, P/E, ROCE, sales growth, and profit growth is time-consuming and prone to errors.

Solution
An automated web-scraping solution was developed using Python to collect sector-wise financial data from Screener.in. The collected data was cleaned, statistically analyzed, visualized, and used to identify high-performing companies and sectors.

Project Objectives
Automate financial data collection from Screener.in.
Extract company-level financial information across multiple sectors.
Create a structured master dataset.
Perform data cleaning and preprocessing.
Analyze company and sector-level financial performance.
Apply descriptive and inferential statistics.
Identify patterns in profitability, growth, valuation, and capital efficiency.
Generate meaningful business insights through visualization.
Dataset
Metric	Value
Sectors	180
Companies	2,411
Features	12
Features
Feature	Description
S.No.	Serial number of the company
Name	Company name
CMP Rs.	Current Market Price
P/E	Price-to-Earnings ratio
Mar Cap Rs.Cr.	Market Capitalization in ₹ Crores
Div Yld %	Dividend Yield
NP Qtr Rs.Cr.	Quarterly Net Profit
Qtr Profit Var %	Quarterly Profit Variation
Sales Qtr Rs.Cr.	Quarterly Sales
Qtr Sales Var %	Quarterly Sales Variation
ROCE %	Return on Capital Employed
Sector	Sector classification
Web Scraping Process
The scraping workflow was automated using Requests, BeautifulSoup, lxml, and Pandas.

Screener.in Market Page
        ↓
Retrieve HTML using Requests
        ↓
Parse HTML using BeautifulSoup
        ↓
Extract Sector URLs
        ↓
Loop through 180 Sectors
        ↓
Extract Company Tables
        ↓
Create DataFrames
        ↓
Combine into Master Dataset
Data Understanding & Cleaning
The following checks were performed:

Dataset shape
Data types
Missing-value analysis
Duplicate-record analysis
Numerical conversion
Sector-wise missing-value treatment
Missing values were identified in P/E, NP Qtr Rs.Cr., Qtr Profit Var %, Sales Qtr Rs.Cr., Qtr Sales Var %, and ROCE %.

Missing numerical values were handled using sector-wise median imputation because financial variables can contain extreme values and financial characteristics can differ substantially between sectors.

Descriptive Statistics
Descriptive statistics were used to understand the distribution and variability of financial metrics.

The analysis included:

Mean
Median
Standard deviation
Minimum
Maximum
Quartiles
Sector-wise statistics
Mean and median were compared because financial data can be skewed by extreme observations.

Inferential Statistics
One-Way ANOVA
Business Question: Does the average ROCE differ significantly across the selected sectors?

H₀: The mean ROCE is the same across the selected sectors.

H₁: At least one sector has a different mean ROCE.

Sample
10 sectors
25 companies per sector
250 companies
Result
Statistic	Result
F-statistic	2.6186
P-value	0.00665
Significance Level	0.05
Conclusion
Since the p-value is less than 0.05, the null hypothesis was rejected.

There is statistically significant evidence that the average ROCE differs across the selected sectors.

Exploratory Data Analysis
The project uses different visualization techniques to analyze financial relationships and distributions.

Market Capitalization Distribution — Histogram
Understands the distribution of company sizes.

Market Capitalization vs ROCE — Scatter Plot
Investigates whether company size is associated with capital efficiency.

Sales Growth vs Profit Growth — Scatter Plot
Examines whether increasing sales translates into increasing profitability.

Sector-wise ROCE Distribution — Box Plot
Compares ROCE distributions and variability across sectors.

Correlation Heatmap
Identifies relationships between major financial indicators.

Business Insights
The analysis provides insights into:

Differences in financial performance across sectors.
Companies with relatively high capital efficiency.
Distribution of market capitalization across companies.
Relationship between sales growth and profit growth.
Relationship between company size and ROCE.
Relationships among major financial indicators.
Significant differences in average ROCE across selected sectors.
The analysis also demonstrates that no single financial metric is sufficient to evaluate company performance. Market capitalization, profitability, growth, valuation, dividend yield, and capital efficiency should be considered together.

Challenges
Understanding the HTML structure and locating the correct tables and links.
Extracting sector URLs dynamically rather than manually entering them.
Handling missing financial metrics.
Managing extreme values in ROCE, P/E, and growth percentages.
Converting scraped strings into numerical values.
Managing data collected from 180 sectors and 2,411 companies.
Technologies Used
Technology	Purpose
Python	Core programming language
Requests	Web requests
BeautifulSoup	HTML parsing
lxml	HTML parser
Pandas	Data manipulation
NumPy	Numerical operations
Matplotlib	Data visualization
Seaborn	Statistical visualization
SciPy	Statistical testing
Jupyter Notebook	Development and analysis
Project Structure
Sector-wise-Financial-Performance-Analysis/
│
├── Sector_Wise_Financial_Analysis.ipynb
├── sector_wise_financial_data.csv
├── Sector_Wise_Financial_Analysis.pptx
└── README.md
How to Run the Project
1. Clone the repository
git clone <your-github-repository-url>
2. Install required libraries
pip install requests beautifulsoup4 lxml pandas numpy matplotlib seaborn scipy
3. Open Jupyter Notebook
jupyter notebook
Open Sector_Wise_Financial_Analysis.ipynb.

4. Run the notebook
Web Scraping
      ↓
Data Collection
      ↓
Data Understanding
      ↓
Data Cleaning
      ↓
Descriptive Statistics
      ↓
EDA
      ↓
Bivariate Analysis
      ↓
Inferential Statistics
      ↓
Business Insights
Key Takeaway
This project demonstrates an end-to-end Data Analytics workflow, starting from automated web scraping and ending with statistical and business analysis.

It shows how publicly available financial information can be transformed into a structured dataset and analyzed using Python, EDA, descriptive statistics, bivariate analysis, and One-Way ANOVA to understand company and sector-level financial performance.

Author
K.Srikanth

Skills demonstrated: Python • Web Scraping • Pandas • EDA • Statistics • Data Visualization • Business Analysis
