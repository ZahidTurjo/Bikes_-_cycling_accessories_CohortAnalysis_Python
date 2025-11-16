# Cohort Analysis of Customer Transactions

This project performs a **Cohort Analysis** on customer transaction data to understand user retention, churn, and engagement over time. Cohort analysis allows businesses to track customer behavior and make data-driven decisions.

---

## 🔹 What is Cohort Analysis?

Cohort Analysis is a method of analyzing groups of users (called cohorts) who share a common characteristic within a defined time period.  
A cohort is a group of users who started an activity (like first purchase or signup) at the same time.  

It helps to:
- Understand retention (how long users stay active)
- Measure churn (how many users leave)
- Compare user quality across months, campaigns, or regions
- Track revenue growth, LTV, and engagement
- Identify the best-performing campaigns or months

---

## 🔹 Dataset
- Source:  [Kaggle - Customer Transaction Dataset](https://www.kaggle.com/datasets/archit9406/customer-transaction-dataset)
- Sheet: `Transactions`
- Total Records: 20,000
- Columns: `transaction_id, product_id, customer_id, transaction_date, online_order, order_status, brand, product_line, product_class, product_size, list_price, standard_cost, product_first_sold_date`

**Sample:**

| transaction_id | product_id | customer_id | transaction_date | online_order | order_status | brand       | product_line | product_class | product_size | list_price | standard_cost | product_first_sold_date |
|----------------|------------|-------------|-----------------|--------------|--------------|------------|--------------|---------------|--------------|------------|---------------|------------------------|
| 1              | 2          | 2950        | 2017-02-25      | 0            | Approved     | Solex      | Standard     | medium        | medium       | 71.49      | 53.62         | 41245                  |
| 2              | 3          | 3120        | 2017-05-21      | 1            | Approved     | Trek Bicycles | Standard  | medium        | large        | 2091.47    | 388.92        | 41701                  |

---
## 🔹 Key Steps
1. Cleaned data (filled missing numeric and categorical values)  
2. Assigned `TransactionMonth` and `CohortMonth`  
3. Calculated `CohortIndex` (months since first purchase)  
4. Built cohort table and calculated retention rates  
5. Visualized retention heatmaps using Seaborn

--- 
## 🔹 Results
- Cohort retention heatmaps show monthly retention rates per cohort
  <img width="1533" height="715" alt="image" src="https://github.com/user-attachments/assets/d70e377f-3d44-4a91-87b4-c8deec152599" />
  
## the Cohort Retention Heatmap

The heatmap shows **monthly retention rates** for each cohort of customers:

- **Rows** = CohortMonth (month when the customer made their first purchase)
- **Columns** = CohortIndex (months since first purchase)
- **Cell values** = Retention rate (% of users still active)

**Key observations:**

1. The first column of each row is always **100%**, because it represents the cohort’s first month.
2. Retention generally **declines over time**:
   - For example, January 2017 cohort starts at 100% in month 1, drops to ~36% in month 2, and fluctuates around 37–39% in later months.
3. Some cohorts show **higher retention in later months** (e.g., April 2017 month 4 = 46%), indicating strong engagement for that period.
4. Recent cohorts (e.g., October–December 2017) have fewer months of data, so retention appears only for the first few months.

**Insights:**

- Overall, **retention decreases over time**, which is common in most businesses.
- Some months have better retention than others, possibly due to **seasonal effects, promotions, or marketing campaigns**.
- The heatmap helps identify **which cohorts are most engaged** and where interventions may be needed to improve retention.
---
## 🔹 Author
[**Z.I. Turjo**](https://www.linkedin.com/in/zahidul-islam-turjo-609549320/)

