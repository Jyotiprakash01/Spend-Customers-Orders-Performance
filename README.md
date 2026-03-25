# Spend-Customers-Orders-Performance
This dashboard was built to provide a holistic view of marketing performance and business growth, focusing on:  Marketing Spend efficiency, Customer acquisition &amp; behavior, Order and revenue performance  Profitability at first-order level for a business.

The goal was to enable stakeholders (marketing, growth, and leadership teams) to make faster, data-driven decisions on budget allocation, CAC optimization, and revenue growth.

# What This Dashboard Shows

<img width="1920" height="1080" alt="@jyotiprakash (1)" src="https://github.com/user-attachments/assets/81f4956c-0e9b-41d4-bf66-768dd01c9a95" />


This dashboard connects the below funnel:

Spend - Sessions - Customers - Orders - Revenue - Profitability

It answers key business questions like:
- Are we spending efficiently?
- Are we acquiring quality customers?
- Is revenue growing profitably?
- Are repeat customers improving over time?

What it shows:
- Total Customers, New Customers
- CAC (Customer Acquisition Cost)
- Net Revenue & Gross Profit
- Spend
- First Order AOP (Average Order Profit)
- Contribution Profit

Business Value:
- Provides a quick executive snapshot
- Enables YoY comparison (Vs Previous Year)
- Helps leadership identify:
Growth vs profitability trade-offs
Efficiency of acquisition strategies

<img width="1920" height="1080" alt="@jyotiprakash (2)" src="https://github.com/user-attachments/assets/84d59cf7-caec-4734-a994-18a036de9eb7" />
<img width="1920" height="1080" alt="@jyotiprakash (3)" src="https://github.com/user-attachments/assets/09575257-5f17-4e40-9039-537ddcf076b2" />
<img width="1920" height="1080" alt="@jyotiprakash (4)" src="https://github.com/user-attachments/assets/2e6ec80b-490a-4076-af68-115190e0fd81" />
<img width="1920" height="1080" alt="@jyotiprakash (5)" src="https://github.com/user-attachments/assets/9fbd3b0e-b1cc-4537-af2b-b33ac019cf4e" />


# Spend vs CAC Trend

Insight:
- Shows how efficiently marketing spend converts into customers
- Rising CAC indicates diminishing returns

Business Impact:
- Helped optimize budget allocation across channels
- Identified periods of inefficient spending

# Spend vs Orders

Tracks relationship between marketing investment and order volume

Insight:
Ideally both should grow together
If spend increases but orders decreases → inefficiency

Business Impact:
Helped identify low-performing campaigns
Enabled ROI-based spend decisions

# Spend vs New Customers

Tracks acquisition efficiency

Insight:
Plateau in customers despite higher spend - market saturation or targeting issue

Business Impact:
Improved audience targeting strategy
Reduced wasted spend

# Revenue vs AOV vs Profit (New vs Existing Customers)

Combines:
Net Revenue
Average Order Value (AOV)
First Order Profit

Insight:

Differentiates between customer quality vs quantity

Business Impact:
Helped business shift focus to high-value customers
Improved unit economics

# Contribution Profit vs New Customers (Moving Average)

Tracks profitability vs acquisition trend

Insight:
Increase in customers but drop in profit - unsustainable growth

Business Impact:
Balanced growth vs profitability strategy

# Contribution Profit vs Spend
Shows how spend impacts actual profit

Insight:
Critical for identifying over-spending scenarios

Business Impact:
Helped reduce loss-making campaigns

# New Customers vs CAC

Tracks acquisition cost efficiency

Insight:
CAC rising faster than customers = scaling inefficiency

Business Impact:
Used for CAC benchmarking & control

# CVR (Conversion Rate) vs CAC

Measures funnel efficiency

Insight:
Low CVR + High CAC = poor funnel performance

Business Impact:
Triggered landing page & funnel optimizations

# New vs Repeat Customers
Tracks retention

Insight:
Repeat customers are more profitable

Business Impact:
Helped invest in retention strategies (CRM, lifecycle marketing)

# CAC vs Cost Per Session

Breaks down acquisition cost into traffic efficiency

Insight:
High session cost but low CAC → good conversion
Low session cost but high CAC → poor conversion

Business Impact:
Helped optimize media buying + funnel performance together

# Sessions vs Impressions
Tracks top-of-funnel efficiency

Insight:
High impressions but low sessions = weak creatives/CTR

Business Impact:
Improved ad creatives & targeting

# Spend vs Repeat Customers
Tracks retention efficiency vs spend

Insight:
Spend typically drives new customers, not repeat

Business Impact:
Encouraged investment in retention channels (email, CRM)


# Tabular View (Detailed Breakdown)
What it shows:
Day-level breakdown of:
CAC
Profit
Customers
Orders
Revenue

Business Impact:
Enabled deep-dive analysis
Helped identify:
Daily anomalies
Campaign-level issues

# Data Sources Used

This dashboard integrates multiple data sources:

1. Marketing Platforms

Facebook Ads
Google Ads
TikTok / YouTube

Data captured:
Spend
Impressions
Clicks

2. Web Analytics (GA4 - BigQuery)

Sessions
Users
Conversion events

3. Order Database (from app to SQL database)

Orders
Revenue
Customer IDs
Repeat vs New customers

4. Attribution / Mapping Tables

Channel mapping
Campaign classification
Customer segmentation



# Data Engineering & Automation (Python + Power BI)
Incremental Data Pipeline
To handle large-scale data efficiently, I built an incremental refresh pipeline using Python:

Step 1: Data Extraction
APIs / database queries pulled:

Ad spend data from Meta
Order data from app

Step 2: Incremental Logic

Only new data (last X days) is fetched
Historical data remains unchanged

Step 3: Data Transformation (Python)
Cleaned and joined datasets:
Mapped sessions → orders → campaigns

Calculated:
CAC
AOV
Contribution Profit
Repeat vs New customers

Step 4: Data Storage
Stored processed data in:
BigQuery / SQL tables (partitioned by date)

Step 5: Power BI Integration
Connected Power BI to processed tables

Enabled:
Incremental refresh
Faster performance
Reduced load time



# Business Impact

- Cost Optimization
Identified high CAC channels → reduced wasted spend

- Revenue Growth
Focused on high AOV & repeat customers

- Profitability Improvement
Balanced growth vs contribution margin

- Better Decision Making
Enabled:
Budget reallocation
Campaign optimization
Funnel improvements
