# RETAIL ANALYTICS DASHBOARD: SALES, PROFITABILITY & CUSTOMER INSIGHTS

## Introduction
This dashboard was developed for Axis and Oak, a U.S.-based retail store dealing in books, clothing, electronics, and other consumer goods. The goal is to provide a clear snapshot of the store’s current business performance and uncover insights that will help executives determine where to focus effort and resources for maximum impact. The goal is to:

◼ Financial Overview
 - Evaluate overall financial performance, including revenue, profit, and trend over time.
 - Assess the total number of transactions and analyze the ratio of sales to returns to measure efficiency.

◼ Product and Store Insights
 - Identify the most profitable product categories and subcategories.
 - Compare product and store performance in terms of sales volume, profit margin, and contribution to total revenue.

◼ Customer Insights
 - Analyze the average number of transactions per customer to gauge engagement and loyalty.
 - Measure sales contribution by gender and distribution of customers by state.
 - Determine the most profitable age group to guide marketing and inventory decisions.

---
## 🔄 Process Flow

◼ Data Preparation (MySQL):
 - The raw retail data was cleaned and transformed in MySQL.  
 - See script [here](https://github.com/andyababio/RETAIL-ANALYTICS/blob/main/mysql_script_retail_store).


◼ Data Modeling (Power BI):
 - The cleaned datasets were imported into Power BI for data modeling.

◼ Data Visualization & Analysis:
 - I then developed interactive visuals and KPIs in Power BI using **DAX** to highlight trends, relationships, and performance metrics.

---

## 🗂️ Dataset Overview

🟥 Fact Table: Transactions
 - Transaction_ID – Unique identifier for each transaction
 - Cust_ID – Links each transaction to a specific customer
 - Tran_Date – Transaction date (used to connect with the Date table)
 - Prod_Cat_Code / Prod_Sub_Cat_Code – Identify product category and subcategory
 - Qty, Rate, Tax, Total_Amt – Metrics for financial calculations
 - Profit_Margin_%, Profit – Indicators of product-level profitability
 - Store_Type – Channel or store type (e.g., online, in-store)
 - Transaction_Status – Indicates sale or return

🟥 Dimension Table: Customer
 - Customer_ID, DOB, Gender, City_Code

🟥 Dimension Table: Product_Category
 - Prod_Cat_Code, Prod_Cat, Prod_Sub_Cat_Code, Prod_SubCat, Profit_Margin_%

🟥 Dimension Table: Date_Table
 - Date, Month, Quarter, Year, MonthNumber, DayOfWeek

Relevant relationships were then established between the above table to produce the following data model:
 <p align="center">
 <img alt="Data Model" src="https://github.com/andyababio/RETAIL-ANALYTICS/blob/main/Images/Retail%20Data%20Model.png" width="60%" />
 </p>
 
 ---
 
## 📊 Dashboard Overview  

<h3 align="center">Summary Page</h3>
<p align="center">
   <img src="https://github.com/andyababio/RETAIL-ANALYTICS/blob/main/Images/Dashboard.png" 
        alt="Dashboard" width="60%" />
</p>

<h4 align="center">Products & Customer Page</h4>
<p align="center">
      <img src="https://github.com/andyababio/RETAIL-ANALYTICS/blob/main/Images/Products.png" 
           alt="Products" width="45%" />
      <img src="https://github.com/andyababio/RETAIL-ANALYTICS/blob/main/Images/Customer.png" 
           alt="Customer" width="45%" />
</p>


---
## Key Insights
### Summary Page:
<p> Overall Business Performance (Sales, Revenue, and Trends) </p>

- Axis and Oak demonstrates strong overall business performance, generating a cumulative **$54 million** in revenue and **$14 million** in profit since its inception in 2011.
 - The business achieves its peak performance in January, contributing the highest shares of **revenue (9%)**, **profit (9.01%)**, and **transactions (8.8%)**, indicating strong customer activity at the start of the year.
 - However, product returns have a notable financial impact, reducing total revenue by approximately 10%. Return volumes are highest in January and July, highlighting potential issues related to post-holiday or mid-year product cycles that may warrant closer review.

<p align="center">
   <img src="Images/Overview.png" 
        alt="Dashboard"/>
</p>

<p> ◻ Year-on-Year Profit Growth </p>
Profits were consistent between 2011–2013, averaging $4.6–4.8 million annually, but dropped sharply to $683K in 2014 — an ~85% decline. This suggests possible operational, pricing, or product-mix changes that severely impacted overall performance.

Recommended Action:
 - Conduct a root cause review of 2014’s decline (e.g., increased returns, reduced prices, or loss of key product lines).
 - Establish annual performance benchmarks and early-warning indicators to prevent similar profit erosion.


<p> ◻ Revenue and Profit by Product Category </p> 
The Books and Electronics categories are the top revenue generators, together accounting for over 40% of total sales, while Footwear delivers the highest profit margin (≈30%), signaling efficient pricing and cost control.

Recommended Action:
 - Sustain strong performers (Books, Electronics) through targeted upselling or bundle offers.
 - Expand Footwear marketing or new product lines given its high margin potential.
 - Reassess Bags and Clothing strategies—lower revenue might be improved through promotions or assortment refreshes.


<p> ◻ Transactions by Product Category </p>
Customer activity is concentrated in Books (6,039 transactions) and Electronics (4,878). Bags have the lowest transaction volume (1,985), reinforcing earlier profit insights about limited demand.

Recommended Action:
 - Continue optimizing top-selling categories through targeted advertising and inventory prioritization.
 - Revitalize underperforming categories (e.g., Bags and Clothing) with refreshed product designs, limited-time offers, or influencer partnerships.
 - Conduct product demand analysis to align inventory levels with high-interest categories and reduce overstock risk.

<p> ◻ Transactions by Gender </p>
 Female customers account for 57% of total transactions (13,148 vs. 9,787), indicating stronger engagement and purchasing behavior among women.

Recommended Action:
 - Tailor marketing campaigns and loyalty programs toward female shoppers to sustain engagement.
 - Identify opportunities to increase male customer participation through personalized product recommendations or male-focused categories.
 - Leverage demographic insights to refine promotional messaging for balanced customer outreach.

<p align="center">
   <img src="Images/Proft and Returns MOM.png" 
        alt="Dashboard"/>
</p>

<p> ◻ Profit Trends (Month-on-Month) </p> 
Monthly profit levels remain relatively stable, averaging around $1.2 million. January ($1.33M) and October ($1.32M) are top-performing months, mirroring transaction peaks, while June ($1.12M) records the lowest profit.

Recommended Action:
 - Align inventory and marketing strategies with peak months to sustain profitability.
 - Strengthen promotional and sales strategies in months with declining profits to boost revenue consistency and mitigate seasonal dips.

<p>◻ Returns by Month</p>
Monthly return rates remain relatively stable throughout the year, fluctuating between **8.3% and 9.5%**. The highest return rates occur in **February (9.5%)** and **January (9.4%)**, suggesting potential post-holiday return activity or seasonal purchase adjustments.

Recommended Action:
 - Investigate product or category trends driving returns during Q1.
 - Implement clearer product information or flexible exchange policies during peak return months.
 - Leverage insights to reduce returns ahead of future seasonal peaks.











### Product Page
<p align="center">
   <img src="Images/Product - KPI.png" 
        alt="Dashboard"/>
</p>
<p> ◻ Key Product Performance Indicators </p>
Books remain the top-selling product category, driven primarily by the Women’s subcategory, while the e-Shop leads as the highest-performing sales channel, reflecting the growing strength of digital retail engagement.

Recommended Action:
 - Introduce cross-category promotions for top-performing segments (Books + Women’s Subcategory).
 - Leverage online behavioral data to refine product recommendations and optimize conversion.


<p align="center">
   <img src="Images/product 2.png" 
        alt="Dashboard"/>
</p>


<p> ◻ Profit by Store Type </p>
The e-Shop delivers the highest profit ($6.0M), outperforming physical stores by a significant margin. However, all store types contribute meaningfully, with consistent profitability across Flagship, MBR, and TeleShop outlets.

Recommended Action:
 - Strengthen digital-first strategies, such as personalized online offers and streamlined checkout experiences.
 - Benchmark operational efficiency from e-Shop processes to enhance Flagship and MBR performance.
 - Explore hybrid retail initiatives combining online and offline experiences to maximize reach.

<p> ◻ Product Performance Matrix </p>
Across categories, Footwear demonstrates the highest average profit margin (≈29.7%), while Books lead in both volume and total profit ($3.8M). Lower performers like Bags and Home & Kitchen show opportunities for pricing or assortment optimization.

Recommended Action:
 - Reinforce strong categories (Books, Electronics, Footwear) through bundled promotions and restock prioritization.
 - Review pricing and cost structures for lower-margin items like Home & Kitchen.
 - Streamline the Bags product line or introduce new collections aligned with current customer preferences.

<p> ◻ Returns by Age Group </p>
Customers aged **45–54 (9.8%)** and **25–34 (9.1%)** record the highest return rates, indicating potential dissatisfaction among both mature and younger adult demographics.

Recommended Action:
 - Investigate category-specific reasons for returns within these age brackets.
 - Refine product descriptions, sizing information, and quality assurance for high-return segments.
 - Introduce satisfaction surveys or targeted follow-ups to identify underlying causes of product dissatisfaction.

<p> ◻ Returns by Store Type </p>
The e-Shop records the highest return rate (11.6%), nearly double that of TeleShop (6.5%), suggesting online purchasing friction or product expectation gaps.

Recommended Action:
 - Audit e-Shop product listings for clarity (e.g., images, specifications, delivery timelines).
 - Enhance pre-purchase communication and introduce “try-before-you-buy” or easy returns policies.
 - Analyze return reasons by category to identify root causes specific to online transactions.

<p align="center">
   <img src="Images/product 3.png" 
        alt="Dashboard"/>
</p>


<p>◻ Returns by Product Category</p>
Books and Electronics recorded the highest number of returns, accounting for over **40% of all product returns**, aligning with their position as top-selling categories. However, **Bags** show a notably high return rate relative to total sales volume, suggesting possible issues with product quality, sizing, or customer expectations.

Recommended Action:
 - Conduct product-specific return analysis, particularly for Bags, to identify recurring issues.
 - Improve product descriptions, quality checks, or images for frequently returned items.
 - For Books and Electronics, introduce clearer return policies or customer education to reduce preventable returns.

<p>◻ Returns by City</p>
Pennsylvania (10.6%) and Georgia (9.5%) show the highest return rates among all customer locations. This may reflect regional preferences, shipping issues, or mismatched product expectations.

Recommended Action:
 - Review fulfillment and delivery experiences for customers in Pennsylvania and Georgia.
 - Evaluate whether specific product categories or stores are driving higher returns in these regions.
 - Tailor regional marketing and support to improve post-purchase satisfaction and reduce return rates.










 

### Customer Page

<p align="center">
   <img src="Images/Customer overview.png" 
        alt="Dashboard"/>
</p>


<p>◻ Customer Overview</p>
The customer base consists of 5,647 distinct customers**, each generating an average of ₵9.64K in revenue and completing around 4 transactions on average. This indicates strong engagement and purchase frequency across customer segments.

Recommended Action:
 - Identify and reward high-value repeat customers with loyalty programs.
 - Investigate lower-activity segments for targeted re-engagement campaigns


<p align="center">
   <img src="Images/customer 2.png" 
        alt="Dashboard" />
</p>


<p>◻ Returns by Age Group</p>
Return rates are slightly higher among the **45–54** group (**9.8%**) and **25–34** (**9.1%**), suggesting possible issues with product expectations or fit for these demographics.

Recommended Action:
 - Review return reasons among these age groups.
 - Optimize product descriptions, sizing, or return policies for improved satisfaction.

<p>◻ Sales by Age Group</p>
The **35–44** and **25–34** age groups dominate transactions, contributing over **70% of total sales volume**, confirming their position as the primary consumer demographic.

Recommended Action:
 - Maintain targeted marketing for 25–44-year-olds.
 - Design promotions to attract the 55+ group, who show potential for higher revenue per purchase despite fewer transactions.

<p>◻ Profit by Gender</p>
Across all months, **female customers consistently generate higher profits**, averaging around **20–25% more** per month compared to male customers.

Recommended Action:
 - Continue focusing marketing efforts on female buyers.
 - Conduct sentiment or behavioral analysis to identify products with higher male engagement potential.



<p align="center">
   <img src="Images/Customer 3.png" 
        alt="Dashboard" />
</p>

<p>◻ Revenue and Profit by Age Group</p>
The **35–44** and **25–34** age groups not only lead in sales volume but also deliver the highest profit contributions — **₵6.38M** and **₵5.85M**, respectively.

Recommended Action:
 - Prioritize product recommendations and campaigns for these two groups.
 - Develop age-tailored offers (e.g., family bundles for 35–44, lifestyle products for 25–34).

<p>◻ Sales by State</p>
Georgia, Illinois, and Florida lead in both transactions and revenue, jointly contributing over **40% of total sales**, highlighting them as the most active and profitable markets. Conversely, **California, North Carolina, and Pennsylvania** show the lowest figures, indicating potential for targeted growth strategies.

Recommended Action:
 - Strengthen marketing and loyalty programs in Georgia, Illinois, and Florida to sustain momentum.
 - Investigate customer preferences and sales channels in California and North Carolina to uncover barriers to conversion.
 - Introduce region-specific promotions or partnerships to improve performance in underperforming states.

 <p>◻ Customer Distribution by Region</p>
Customer presence is concentrated in **Georgia, Illinois, and Florida**, each exceeding **850 active customers**. This reflects strong penetration in key states, while **California** and **North Carolina** represent growth opportunities.

Recommended Action:
 - Strengthen presence in top-performing states through regional partnerships or local ads.
 - Explore expansion strategies in underrepresented markets (e.g., California, North Carolina).





---





## Conclusion

The analysis provides a holistic view of the business’s sales, profitability, and customer behavior across products, channels, and demographics. Overall, the company demonstrates strong performance driven by the Books and Electronics categories, a robust e-Shop channel, and a loyal customer base aged 25–44. Profitability trends indicate effective pricing and cost control, particularly within Footwear, while consistent female-driven profit contributions highlight a reliable customer segment.

However, the data also reveals areas for optimization — notably, higher return rates in specific stores (e-Shop) and age groups (45–54), as well as lower revenue contributions from categories like Bags and Clothing. Addressing these will help balance the business’s revenue mix and improve overall customer satisfaction.
