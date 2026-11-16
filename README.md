# E-Commerce Sales Trend & Customer Churn Analysis
**InternCircle Project 3 — Data Science & AI**  
**Author:** Ashish Balodia  

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://ashishbalodia1-streamlit--customer-churn-analysis-app-o57mmw.streamlit.app/)

---

## 🌐 Live Web Application

The interactive analytics dashboard is live and deployed on Streamlit Community Cloud:

👉 **Live Demo:** **[https://ashishbalodia1-streamlit--customer-churn-analysis-app-o57mmw.streamlit.app/](https://ashishbalodia1-streamlit--customer-churn-analysis-app-o57mmw.streamlit.app/)**

Managers and evaluators can interactively filter monthly sales, explore product category trends, inspect the Pareto 80/20 customer curve, and download the 1-page executive brief PDF in real time without running any code locally.

---

## About the Project
In this project, I performed an end-to-end sales analysis on an e-commerce retail dataset to understand revenue trends throughout the year, identify top-selling product categories, and find our most valuable customer segments. 

The goal of this project is to answer practical business questions that a store manager would ask, test the Pareto 80/20 rule, and provide simple, numbers-backed recommendations to grow sales and retain top customers.

---

## Key Highlights & Findings

- **Total Revenue:** £10.67M across 19,960 completed orders, with an average order value of £534.
- **Seasonality & Best Month:** Sales build up through autumn and peak in **November 2011 (£1.51M)** due to holiday shopping. 
- **Post-Holiday Drop:** Sales slow down sharply in **February 2011 (£523k)**, which is nearly 3 times lower than the November peak.
- **Top Product Categories:** `Home & Decor` (£2.76M) and `Kitchen & Dining` (£2.64M) make up **over 50% of total sales**, with `Seasonal & Gifts` spiking heavily during the Q4 holiday months.
- **Pareto 80/20 Rule Verified:** 
  - The **top 10% of customers (434 accounts) generate 61.4% of total sales** (£5.47M).
  - The **top 20% generate 74.6% of sales**.
  - Customer #14646 was the top buyer with over £280,000 in orders.

---

## 3 Practical Recommendations

1. **VIP Loyalty Program for Top 10% Customers:**  
   Since just 434 customer accounts bring in over 60% of our sales, losing even a few of them would significantly impact revenue. Management should offer them dedicated account support, early access to new collections, and volume discounts on repeat orders.
2. **Early Spring Restocking Clearance to Beat the February Dip:**  
   Sales drop by 24% month-over-month in February. Running a "New Year / Spring Restock" clearance in mid-January with tiered discounts (like 15% off orders over £300) will help retail shop owners restock earlier.
3. **Product Bundling at Checkout:**  
   Home and Kitchen products account for half of our revenue, while Bags sell frequently. Recommending bundles (e.g. mug sets paired with matching tote bags) at checkout can help increase the average order value.

---

## Project Structure

```text
├── app.py                           # Interactive Streamlit Web Dashboard application
├── ecommerce_sales_analysis.ipynb   # Main Jupyter notebook containing all 8 analysis steps
├── ecommerce_executive_brief.pdf     # 1-page business brief PDF for management
├── ecommerce_executive_brief.png     # Preview image of the 1-page brief
├── online_retail_II.xlsx            # Original dataset (UCI Machine Learning Repository)
├── online_retail_II.parquet         # Fast-loading cached version of the dataset
├── project-3-guide.pdf               # Project guide and instructions
├── requirements.txt                  # Python libraries used
└── README.md                         # Project documentation
```

---

## The 8 Steps Followed

1. **Understand the business question:** Formulated practical questions around seasonality, categories, and customer loyalty.
2. **Load and inspect the data:** Checked column types, missing values, duplicates, and filtered out refunds/cancellations (invoices starting with 'C').
3. **Add date features:** Calculated item revenue (`Quantity * Price`), extracted month, weekday, quarter, and categorized products into simple categories.
4. **Analyze sales trends:** Calculated monthly sales, month-over-month growth, and plotted a line chart highlighting the peak and trough months.
5. **Compare categories:** Used `groupby` for total sales and average spend, created a monthly pivot table, and plotted category sales.
6. **Find best customers:** Computed spend per customer, tested the 80/20 rule, and plotted the cumulative revenue (Lorenz / Pareto) curve.
7. **Write recommendations:** Provided 3 practical recommendations backed by our exact numbers.
8. **Present it:** Summarized everything in a one-page brief and generated `ecommerce_executive_brief.pdf`.

---

## How to Run This Project

### 1. View Live Online
Open the live dashboard directly in your browser:  
👉 **[Streamlit Live App](https://ashishbalodia1-streamlit--customer-churn-analysis-app-o57mmw.streamlit.app/)**

### 2. Run Locally
1. Clone this repository:
   ```bash
   git clone https://github.com/ashishbalodia1/streamlit--Customer-churn-analysis.git
   cd streamlit--Customer-churn-analysis
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch the dashboard:
   ```bash
   streamlit run app.py
   ```

### 3. Run the Jupyter Notebook
```bash
jupyter notebook ecommerce_sales_analysis.ipynb
```
