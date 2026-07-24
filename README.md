# Pakistan E-Commerce Sales Analysis and Prediction

Analyzing real Pakistani e-commerce data to find sales trends and predict order revenue using Machine Learning.

---

## Dataset

| Property | Detail |
|---|---|
| Total Rows | 1,048,575 |
| After Cleaning | 572,750 valid orders |
| Time Period | 2016 to 2018 |
| Target Column | grand_total (order revenue in PKR) |

---

## Steps

| Step | What Was Done |
|---|---|
| Data Cleaning | Removed empty columns, dropped rows with zero or missing values in price, quantity, and revenue |
| EDA | Monthly revenue trend, top 10 categories, payment method distribution |
| Feature Engineering | Converted date to month period, encoded category names using factorize |
| Modeling | Random Forest Regressor trained on price, quantity, discount, and category |

---

## Model Results

| Metric | Value | Meaning |
|---|---|---|
| R² Score | 0.97 | Model explains 97% of revenue variation |
| MAE | 2096 PKR | Average prediction error per order |

> R² is high because grand_total is mathematically tied to price and quantity. The model confirms and quantifies this relationship well.

---

## Feature Importance

| Feature | Importance |
|---|---|
| qty_ordered | 89.5% |
| price | 9.7% |
| discount_amount | 0.5% |
| category_encoded | 0.2% |

Quantity ordered was by far the strongest driver of revenue.

---

## Business Insights

| Finding | Detail |
|---|---|
| Top Category | Women's Fashion and Mobiles generated the highest revenue |
| Payment Method | Cash on Delivery dominated — reflects customer trust behavior in Pakistan |
| Sales Trend | Revenue grew steadily with seasonal peaks visible in monthly chart |

---

## Tech Stack

Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

---

## Author

Zain Ali — zainzulfiqar.cs@gmail.com
