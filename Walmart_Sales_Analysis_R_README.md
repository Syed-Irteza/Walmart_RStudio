# Walmart Sales Data: Comprehensive Analysis and Strategic Decision-Making Report (R)

## 📌 Purpose of the Project

This project analyzes **Walmart’s weekly sales data (2010–2012)** using **R** to uncover insights into sales seasonality, store performance, and external economic factors.  
It provides data-driven recommendations for **strategic financial planning**, **marketing optimization**, and **store management**.

The main objectives are:
- To identify **quarterly and seasonal sales patterns**.  
- To evaluate **store performance variations** and operational consistency.  
- To assess **holiday impacts** and **economic factor correlations**.  
- To segment stores using **K-Means clustering** for targeted strategies.

---

## 📁 Folder Structure

```
Walmart-Sales-Strategic-Analysis-R/
│
├── 📂 data/
│   └── walmart_sales_data.csv
│
├── 📂 scripts/
│   └── Walmart_Sales_Analysis.Rmd
│
├── 📂 images/
│   ├── Seasonal_Trends.png
│   ├── Store_Performance_Boxplot.png
│   ├── Holiday_Impact_Chart.png
│   ├── Correlation_Heatmap.png
│   ├── Time_Series_Decomposition.png
│   ├── Cluster_Profiles.png
│
├── 📂 reports/
│   ├── Walmart_Sales_Analysis_Report.html
│   ├── Walmart_Sales_Analysis_Report.pdf
│   └── Walmart_Sales_Insights.docx
│
├── README.md
├── .gitignore
```

---

## 📌 Steps to Use This Project

1. Clone the repository:
```bash
git clone https://github.com/your-username/Walmart-Sales-Strategic-Analysis-R.git
```

2. Navigate to the folder:
```bash
cd Walmart-Sales-Strategic-Analysis-R
```

3. Open the R Markdown file in **RStudio**:
```r
Walmart_Sales_Analysis.Rmd
```

4. Click **Knit** to generate the report in HTML, PDF, or Word format.

---

## 🔍 Analysis Performed

### 1. **Data Preparation**
- Cleaned dataset with **6,435 observations** and **8 variables**.  
- No missing or duplicate entries.  
- Added derived time features (Month, Quarter, Year).

### 2. **Seasonal Trends and Forecasting**
- Q4 (holiday quarter) consistently **~60% higher sales** than other quarters.  
- **2012 Q4** showed unexpected decline — flagged for further analysis.  

**Recommendations:**
- Allocate **40–50% of marketing and inventory budgets** to Q4.  
- Strengthen supplier coordination by late Q3.  
- Set **steady growth targets** for Q1–Q3.

---

### 3. **Store Performance**
- **Store #20** leads in total sales; lowest-performing stores show inconsistent results.  
- High standard deviation indicates variance in management and operations.

**Recommendations:**
1. **Benchmark** Store #20, #4, and #14 for best practices.  
2. Conduct **root-cause analysis** for bottom 5 stores.  
3. Link **manager incentives** to consistency and total sales performance.

---

### 4. **Holiday and Promotion Impact**
- Holiday weeks show **24% higher average sales**, statistically significant (p < 0.001).  
- **Thanksgiving** and **Christmas** are the most profitable periods.  

**Recommendations:**
- Prioritize **November–December** for marketing.  
- Launch **doorbuster promotions** pre-holiday.  
- Increase ad spending justified by the 24% uplift metric.

---

### 5. **Economic Factors and Correlation**
| Factor | Correlation with Weekly Sales | Insight |
|--------|-------------------------------|----------|
| **Unemployment** | -0.20 | Higher unemployment → Lower sales |
| **CPI** | +0.19 | Higher cost of living → More Walmart shopping |
| **Fuel Price** | ≈ 0 | Minimal impact |
| **Temperature** | ≈ 0 | No significant influence |

**Recommendations:**
- **Plan for recessions** with a focus on value-brand products.  
- Highlight Walmart’s **“Fight Inflation”** message in campaigns.  
- Avoid overreacting to fuel price fluctuations.

---

### 6. **Time Series Analysis**
- Clear **yearly seasonality (period = 52 weeks)** detected.  
- Sales trend is **stable with slight growth** between 2010–2012.  
- Residuals show random noise → strong model fit.  

**Forecasting Tools Used:**
- `ts()` and `decompose()` for seasonal decomposition.  
- Future extensions could include **ARIMA** or **Prophet** for prediction.

---

### 7. **Store Clustering**
Used **K-Means clustering** to classify stores by performance and local economic conditions.

| Cluster | Description | Strategy |
|----------|--------------|-----------|
| **Cluster 2 – High Performers** | High sales, low unemployment | Test premium products, focus on loyalty |
| **Cluster 0 – Average Performers** | Stable mid-tier stores | Apply best practices from Cluster 2 |
| **Cluster 1 – Low Performers** | Low sales, high unemployment | Optimize for essential goods & discounts |

---

## 📊 Key Insights Summary

| Category | Key Finding |
|-----------|--------------|
| **Seasonality** | Q4 accounts for 60% higher sales. |
| **Holiday Effect** | +24% uplift during holiday weeks. |
| **Top Store** | Store #20 leads sales rankings. |
| **Economic Influence** | CPI (+) and Unemployment (–) affect sales. |
| **Clustering** | Three store segments with distinct strategies. |

---

## 💡 Recommendations Summary

1. Focus budgets and stock buildup on **Q4**.  
2. Use **Store #20’s** model to uplift weaker stores.  
3. **Boost marketing** during major holidays.  
4. Maintain **recession resilience** through value branding.  
5. Apply **time series forecasting** to guide strategic planning.

---

## 📈 Monitoring Metrics

- Quarterly and monthly sales trends.  
- Store-wise variance in performance.  
- Holiday season uplift ratios.  
- CPI and Unemployment correlations.  
- Cluster-based store performance KPIs.

---

## 🧰 Technologies Used

- **R:** dplyr, ggplot2, tidyr, forecast, stats, factoextra  
- **Visualization:** ggplot2 (trendlines, boxplots, heatmaps)  
- **Clustering:** K-Means via `kmeans()`  
- **Time Series:** `ts()`, `decompose()`, `acf()`, `pacf()`  
- **Reporting:** R Markdown (HTML / PDF / Word output)

---

## 📈 Business Impact

This R-based analysis enables Walmart to:
- **Forecast demand** using seasonality insights.  
- **Optimize resource allocation** across stores and quarters.  
- **Benchmark and replicate** high-performing store practices.  
- **Reinforce pricing and promotional** strategies through data-driven evidence.
