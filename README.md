# Power-BI-Oil-and-Gas-Production-Profitability-Analysis 
Project Overview - 
This project analyzes oil and gas production, profitability, operational efficiency, and well-level performance across a portfolio of 18 wells operating across six oil fields.
The goal of the analysis was to build an interactive Power BI dashboard that allows users to evaluate production trends, financial performance, downtime, maintenance costs, and individual well performance.
The project was designed around a key business question:
Which wells and fields are performing well, and where may operational inefficiencies be creating opportunities for improvement? 

Business Questions - 
The analysis focuses on the following questions:
How is overall oil production and profitability trending?
Which fields generate the most production and operating profit?
Which wells are the highest performers?
Which wells have the highest downtime?
How does maintenance spending compare with production?
Are there indications that operational downtime or maintenance costs are associated with weaker well performance?
Which assets may warrant additional management attention? 

Dataset - 
The dataset contains 1,800 daily operational records across 18 wells and six fields.
Each record represents the daily activity of a single well and includes production, financial, and operational information.
Key data categories:
Production
-Oil production
-Gas production
-Water production
Financial
-Revenue
-Operating costs
-Maintenance costs
-Oil and gas prices
-Operating profit
Operational
-Downtime hours
-Production efficiency
-Production status
Well characteristics
-Well ID
-Field
-Region
-Well type
-API gravity
-Well age
 Note: The dataset is a fictional/synthetic dataset created for portfolio and analytical demonstration purposes.

Data Model - 
The Power BI model uses a basic star schema consisting of a central fact table supported by dimension tables.
                               DimDate--->FactProduction<---DimWell
FactProduction
Contains the daily operational and financial measurements for each well.
DimWell
Contains descriptive attributes for each well, including:
-Field
-Region
-Well Type
-API Gravity
-Well Age
DimDate
Contains the calendar attributes used for time-based analysis:
-Date
-Year
-Month
-Quarter
-Month Year
A separate staging query was also used in Power Query to prepare the source data before loading the analytical tables.

Tools & Technologies -
-Power BI
-Power Query
-DAX
-Data Modeling / Star Schema
-Microsoft Excel/CSV source data

Dashboard - 
The Power BI report contains three primary analytical pages.
1. Executive Overview
Provides a high-level view of:
-Total oil production
-Revenue
-Operating profit
-Operating margin
-Production trends
-Profitability by field
-Revenue by field
-Production by region
2. Well & Field Performance
Focuses on asset-level performance, including:
-Top 10 wells by oil production
-Top 10 wells by operating profit
-Production vs. downtime
-Well-level profitability
-Production efficiency
-Field and regional filtering
3. Operational Efficiency
Examines:
-Downtime by field
-Maintenance costs by field
-Production efficiency by well
-Production vs. maintenance spending

Key Findings - 
Overall Performance
Across the analyzed period, the portfolio generated approximately:
Oil Production:	668.7K BBL
Revenue:	$46.0M
Operating Profit:	$31.8M
Operating Margin:	69.0%
Total Downtime:	2,733 hours
Maintenance Cost:	$1.89M
Average Production Efficiency:	93.1%
The portfolio generated a relatively strong overall operating margin, while maintaining average production efficiency above 93%.

Field Performance -
The two Permian fields were the strongest producers.
Permian South produced approximately 140.0K barrels, while Permian North produced approximately 139.9K barrels.
Together, the two Permian fields accounted for roughly 42% of total oil production.
Permian North generated the highest operating profit at approximately $8.95M, followed closely by Permian South at approximately $8.62M.
This indicates that the Permian assets were the primary contributors to overall portfolio profitability. 

Well Performance - 
W-007 was the highest-producing well, generating approximately 63.0K barrels during the analyzed period.
It also generated approximately $3.14M in operating profit, making it one of the strongest overall assets in the portfolio.
Other high-performing wells included:
W-002
W-013
W-014
W-018
The consistency between high production and high profitability among several top-performing wells suggests that production volume was an important driver of financial performance in this dataset.

Operational Efficiency - 
The analysis also identified areas where operational performance warrants additional investigation.
Bakken North had the highest total downtime at approximately 632 hours, substantially above the portfolio average.
It also had the lowest average production efficiency among the six fields at approximately 91.6%.
By comparison, Eagle Ford had the highest average efficiency at approximately 94.3% while experiencing considerably less downtime.
This makes Bakken North a potential area for further operational investigation.

Maintenance vs. Production - 
Maintenance spending was not uniformly distributed across the fields.
Bakken North had the highest maintenance cost per barrel among the six fields, while the Permian fields generated substantially more production with lower maintenance cost per barrel.
This suggests that maintenance spending should be evaluated alongside production output rather than viewed in isolation.
A high maintenance cost is not necessarily a problem if it supports high production, but assets with comparatively high maintenance spending and weaker production may deserve closer review.

Recommendations - 
Based on the analysis, management could consider:
-Prioritize review of high-downtime assets
Bakken North contains several wells with relatively high downtime and lower efficiency. These assets could be reviewed to determine whether maintenance scheduling, equipment reliability, or other operational factors are contributing to lost production capacity.
-Continue monitoring high-performing Permian assets
The Permian fields are major contributors to both production and profitability. Maintaining operational reliability across these assets should remain a priority because disruptions could have a meaningful impact on overall portfolio performance.
-Evaluate maintenance spending relative to output
Maintenance costs should be evaluated alongside production and profitability. Identifying wells with high maintenance costs but comparatively low output could help prioritize future operational improvements.

Project Takeaways - 
This project demonstrates the ability to:
Transform and prepare operational data using Power Query
Design a dimensional/star-schema data model
Create DAX measures for financial and operational KPIs
Build interactive Power BI dashboards
Analyze production and profitability at the field and well levels
Identify potential operational efficiency opportunities
Translate data into business-oriented recommendations
