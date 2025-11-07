# Customer Shopping Behavior Analysis
🧠 Overview
This project analyzes customer shopping behavior using transactional data from 3,900 purchases across various product categories. The goal is to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior to guide strategic business decisions.
### 📁 Dataset Summary
- File: shoppingDS.csv
- Rows: 3,900
- Columns: 18
- Key Features:
  - Demographics: Age, Gender, Location, Subscription Status
  - Purchase Details: Item Purchased, Category, Purchase Amount, Season, Size, Color
  - Behavioral Metrics: Discount Applied, Promo Code Used, Previous Purchases, 
	Frequency of purchases, Review Rating, Shipping Type
### 🛠️ Tools & Technologies
<br>- Python (pandas)<br>- PostgreSQL (SQL queries)<br>- Power BI (dashboard)<br>- Jupyter Notebook (documentation)
### 🚶 Project Steps
 1. Data Preparation in Python
- Loaded `shoppingDS.csv` using `pandas`
- Explored structure with `df.info()` and `df.describe(include=True)`
- Imputed missing `review_rating` values using median per category
- Renamed columns to snake_case for clarity
- Engineered features:
  - `age_group` using `pd.qcut()`
  - `purchase_frequency_days` using `.map()` logic
- Dropped `promo_code_used` after redundancy check
- Loaded cleaned DataFrame into PostgreSQL for SQL analysis
### 2. SQL Analysis in PostgreSQL
Performed structured queries to answer key business questions:
- Revenue comparison by gender
- High-spending discount users
- Top-rated products by category
- Shipping type vs. average spend
- Subscriber vs. non-subscriber revenue
- Discount-heavy products
- Customer segmentation: New, Returning, Loyal
- Top 3 products per category
- Subscription likelihood among repeat buyers
- Revenue by age group
SQL queries are documented in : customer_behavior.sql
### 3. Power BI Dashboard
Connected PostgreSQL to Power BI and built an interactive dashboard with:
- Measures:
  - Number of Customers
  - Average Review Rating 
  - Average Purchase Amount
- Visuals for customer segments, product performance, and revenue trends
Dashboard file:  retail.pbix  
### 4. Final Report
Summarized findings and recommendations in a PDF report for stakeholders.
📄 Report available : Project Report.pdf
### ✅ Key Insights
- Customers aged 30–45 contribute the highest revenue
- Promo codes boost short-term sales but reduce margins
- Loyal customers (10+ purchases) are more likely to subscribe
- Express shipping users spend more on average
- Top-rated products align with best-sellers — ideal for campaign targeting
### 💡 Business Recommendations
Boost Subscriptions: Promote exclusive benefits to increase subscriber base
Loyalty Programs: Reward repeat buyers to shift them into the “Loyal” segment
Product Positioning: Highlight top-rated and best-selling items in promotions
Targeted Marketing: Focus on high-revenue age groups and express-shipping users

