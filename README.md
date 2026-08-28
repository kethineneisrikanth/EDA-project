# 📊 Sector-wise Financial Performance Analysis using Web Scraping & EDA

## 📌 Project Overview

This project focuses on analyzing the financial performance of companies across different sectors using **automated web scraping and Exploratory Data Analysis (EDA)**.

Financial data was collected from **Screener.in** across multiple sectors and combined into a structured dataset.

The project covers the complete Data Analytics workflow:

* Web Scraping
* Data Collection
* Data Cleaning
* Data Preprocessing
* Descriptive Statistics
* Inferential Statistics
* Exploratory Data Analysis
* Data Visualization
* Business Insights

The main goal is to identify patterns in **company size, profitability, growth, valuation, and capital efficiency**.

---

## 🚨 Business Problem

Financial information of listed companies is distributed across multiple sector-wise webpages. Because of this, comparing companies manually can be difficult and time-consuming.

Analysts may need to compare metrics such as:

* Market Capitalization
* P/E Ratio
* ROCE
* Quarterly Sales
* Quarterly Profit
* Sales Growth
* Profit Growth
* Dividend Yield

Manually collecting this information from hundreds or thousands of companies can also result in errors.

### 💡 Solution

We developed an automated Python-based web scraping solution to collect financial data from Screener.in.

The collected data was then:

**Scraped → Cleaned → Structured → Analyzed → Visualized → Converted into Business Insights**

---

## 🎯 Project Objectives

* Automate financial data collection from Screener.in.
* Extract company-level financial information from multiple sectors.
* Create a structured master dataset.
* Clean and preprocess the collected data.
* Analyze company and sector-level financial performance.
* Perform descriptive and inferential statistical analysis.
* Identify patterns in profitability, growth, valuation and capital efficiency.
* Generate meaningful business insights using visualizations.

---

## 🌐 Data Source

**Source:** Screener.in

The project collected financial information from multiple sectors available on the website.

### Dataset Summary

| Metric    |     Value |
| --------- | --------: |
| Sectors   |   **180** |
| Companies | **2,411** |
| Features  |    **12** |

---

## 📋 Dataset Features

| Feature            | Description                  |
| ------------------ | ---------------------------- |
| `S.No.            | Serial number of the company |
| `Name             | Company name                 |
| `CMP Rs.          | Current Market Price         |
| `P/E              | Price-to-Earnings Ratio      |
| `Mar Cap Rs.Cr.   | Market Capitalization        |
| `Div Yld %        | Dividend Yield               |
| `NP Qtr Rs.Cr.    | Quarterly Net Profit         |
| `Qtr Profit Var % | Quarterly Profit Variation   |
| `Sales Qtr Rs.Cr. | Quarterly Sales              |
| `Qtr Sales Var %  | Quarterly Sales Variation    |
| `ROCE %           | Return on Capital Employed   |
| `Sector           | Sector classification        |

---

## 🕷️ Web Scraping Process

The scraping process was automated using:

* Python
* Requests
* BeautifulSoup
* lxml
* Pandas

### Workflow

``
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
```
```

This approach eliminated the need to manually collect financial information from each sector.

---

## 🧹 Data Understanding & Cleaning

After collecting the data, several data-quality checks were performed:

* Dataset shape
* Data types
* Missing-value analysis
* Duplicate-record analysis
* Numerical conversion
* Sector-wise missing-value treatment

### Missing Values

Missing values were found in financial columns such as:

* P/E
* Quarterly Net Profit
* Quarterly Profit Variation
* Quarterly Sales
* Quarterly Sales Variation
* ROCE

### Missing Value Treatment

Missing numerical values were replaced using **sector-wise median imputation**.

The sector-wise median was selected because financial data can contain extreme values and different sectors can have different financial characteristics.

---

## 📊 Descriptive Statistics

Descriptive statistics were used to understand the distribution and variability of the financial metrics.

The analysis included:

* Mean
* Median
* Standard Deviation
* Minimum
* Maximum
* Quartiles
* Sector-wise statistics

Mean and median were compared because financial data can be affected by extreme values.

---

## 📈 Exploratory Data Analysis

Several visualizations were created to understand relationships and patterns in the financial data.

### 1. Market Capitalization Distribution

**Chart:** Histogram

Used to understand the distribution of company sizes based on market capitalization.

### 2. Market Capitalization vs ROCE

**Chart:** Scatter Plot

Used to investigate whether company size is associated with capital efficiency.

### 3. Sales Growth vs Profit Growth

**Chart:** Scatter Plot

Used to examine whether increasing sales translates into increasing profitability.

### 4. Sector-wise ROCE Distribution

**Chart:** Box Plot

Used to compare ROCE distribution and variability across different sectors.

### 5. Correlation Heatmap

Used to identify relationships between major financial indicators.

---

## 🧪 Inferential Statistics

### One-Way ANOVA

A One-Way ANOVA test was performed to answer the following business question:

> **Does the average ROCE differ significantly across the selected sectors?**

### Hypotheses

**H₀:** The mean ROCE is the same across the selected sectors.

**H₁:** At least one sector has a different mean ROCE.

### Sample

* **10 sectors**
* **25 companies per sector**
* **250 companies**

### Results

| Statistic          |      Result |
| ------------------ | ----------: |
| F-statistic        |  **2.6186** |
| P-value            | **0.00665** |
| Significance Level |    **0.05** |

### Conclusion

Since the **p-value is less than 0.05**, the null hypothesis was rejected.

Therefore:

> **There is statistically significant evidence that the average ROCE differs across the selected sectors.**

---

## 💡 Business Insights

The analysis provided several important insights:

### 🏢 Company Size

Market capitalization is concentrated among a relatively small number of very large companies, while many companies fall into the small and mid-cap categories.

### 📈 Capital Efficiency

Companies with relatively high ROCE demonstrate stronger capital utilization.

### 🏭 Sector Performance

Financial performance differs across sectors, making sector-level analysis useful for understanding industry patterns.

### 💰 Sales & Profitability

The relationship between sales growth and profit growth helps determine whether increasing revenue is translating into increasing profitability.

### 📊 Multiple Financial Metrics

No single metric is sufficient to evaluate company performance.

Market capitalization, profitability, growth, valuation, dividend yield and capital efficiency should be considered together.

---

## ⚠️ Challenges

During the project, we faced several challenges:

1. Understanding the HTML structure of the website.
2. Locating the correct tables and links.
3. Dynamically extracting sector URLs.
4. Automating scraping across 180 sectors.
5. Handling missing financial values.
6. Managing extreme values in ROCE, P/E and growth percentages.
7. Converting scraped strings into numerical values.
8. Managing data from more than 2,400 companies.

---

## 🛠️ Technologies Used

| Technology       | Purpose                   |
| ---------------- | ------------------------- |
| Python           | Core programming language |
| Requests         | Web requests              |
| BeautifulSoup    | HTML parsing              |
| lxml             | HTML parser               |
| Pandas           | Data manipulation         |
| NumPy            | Numerical operations      |
| Matplotlib       | Data visualization        |
| Seaborn          | Statistical visualization |
| SciPy            | Statistical testing       |
| Jupyter Notebook | Development and analysis  |

---

## 📁 Project Structure

``
Sector-wise-Financial-Performance-Analysis/
│
├── Sector_Wise_Financial_Analysis.ipynb
├── sector_wise_financial_data.csv
├── Sector_Wise_Financial_Analysis.pptx
└── README.md
```
```
---

## ▶️ How to Run the Project

### 1. Clone the Repository

``
git clone <your-github-repository-url>
```
```

### 2. Install Required Libraries

``
pip install requests beautifulsoup4 lxml pandas numpy matplotlib seaborn scipy
```
````
### 3. Start Jupyter Notebook

``
jupyter notebook
```
```
### 4. Open the Notebook

Open:

``
Sector_Wise_Financial_Analysis.ipynb
````
````
### 5. Run the Analysis

``
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
```

```

## 🔑 Key Takeaway

This project demonstrates an **end-to-end Data Analytics workflow**, starting from automated web scraping and ending with statistical and business analysis.

It demonstrates how publicly available financial information can be transformed into a structured dataset and analyzed using:

**Python + Web Scraping + Pandas + EDA + Statistics + Data Visualization**

The project also demonstrates the use of **One-Way ANOVA** to evaluate whether average ROCE differs significantly across selected sectors.

---

## 👨‍💻 Author

**K. Srikanth**

### Skills Demonstrated

```Python` • `Web Scraping` • `Pandas` • `NumPy` • `EDA` • `Statistics` • `Data Visualization` • `Business Analysis`
