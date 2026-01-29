#  E-commerce Business Performance Analysis


##  Project Overview
This project is an **end-to-end data analytics pipeline** designed to analyze 3 months of e-commerce data (Nov 2020 - Jan 2021). The goal was to identify revenue drivers, evaluate traffic channel efficiency, and understand user behavior differences between registered customers and guests.

**Live Dashboard:** [Tableau Public](https://public.tableau.com/app/profile/artemii.zubriichuk/viz/ProjectDashboard_17692968895970/Dashboard)

---

##  Tech Stack
* **Data Extraction:** Google BigQuery (SQL)
* **Data Cleaning & Analysis:** Python (Pandas, NumPy)
* **Statistical Hypothesis Testing:** Scipy (Mann-Whitney U, Kruskal-Wallis, Chi-Square, Pearson Correlation)
* **Visualization:** Matplotlib, Seaborn, Tableau
* **Environment:** Google Colab

---

## The Pipeline
1.  **SQL Extraction:**
    * Joined 5+ relational tables (`session`, `session_params`, `order`, `product`, `account`) using `LEFT JOIN`.
    * Extracted granular data on sessions, orders, products, and user verification status.
2.  **Exploratory Data Analysis (Python):**
    * Handled missing values (Guest users vs. Registered).
    * Analyzed price distribution (found right-skewed data with high-ticket outliers).
    * Calculated metrics: Average Order Value (AOV), Conversion Rates, Revenue per Channel.
3.  **Statistical Validation:**
    * Proved hypotheses using statistical tests to ensure insights were not random noise.
4.  **Dashboarding:**
    * Built an interactive Tableau dashboard for stakeholders.

---

##  Key Insights & Statistical Proof

### 1. User Value (Registered vs. Guest)
* **Insight:** Registered users generate consistent revenue, but Guests have a surprisingly high volume.
* **Test:** Mann-Whitney U Test.
* **Result:** `p-value < 0.05`. Confirmed a statistically significant difference in daily spending between registered users and guests.

### 2. Traffic Channel Efficiency
* **Insight:** Not all traffic sources are equal. Direct and Organic Search drive the most engaged sessions.
* **Test:** Kruskal-Wallis Test.
* **Result:** `p-value < 0.05`. Confirmed significant performance disparity between traffic channels. Marketing budget should be reallocated to top performers.

### 3. Geographic & Strategy
* **Insight:** The US market dominates revenue. Expansion into Europe requires a localized strategy.
* **Test:** Chi-Square Test.
* **Result:** `p-value > 0.05`. No significant difference in "Organic" traffic share between Europe and Americas, suggesting standard SEO strategies work across both regions, but volume differs.

### 4. Sales Correlations
* **Insight:** Strong positive correlation ($r=0.79$) between number of sessions and total revenue.
* **Recommendation:** Increasing top-of-funnel traffic will linearly scale revenue.

---

## Visualizations (Preview)

*(You can add screenshots of your Python charts here if you want)*

The final interactive dashboard allows filtering by:
*  Date Range
*  Region (Continent/Country)
*  Device Category

---

##  How to Run
1.  Clone the repository.
2.  Open the `notebook.ipynb` in Jupyter or Google Colab.
3.  Authenticate with Google Cloud (if rerunning BigQuery extraction).
4.  Run all cells to generate the `ecommerce_data_for_tableau.csv`.

---

##  Contact
**Artemii Zubriichuk**
* [LinkedIn](https://www.linkedin.com/in/artemii-zubriichuk-63b83a330/)
* [Tableau Portfolio](https://public.tableau.com/app/profile/artemii.zubriichuk)
