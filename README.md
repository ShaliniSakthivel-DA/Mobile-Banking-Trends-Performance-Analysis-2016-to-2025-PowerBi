# Mobile-Banking-Trends-Performance-Analysis (2016 to 2025)

This project analyzes mobile banking data using Excel and Power BI to understand transaction trends, customer behavior, and bank performance. It highlights growth patterns, compares bank types, and provides insights into digital adoption, helping transform raw data into meaningful business decisions.

**1. Project Objective:**
The objective of this mini project is to perform real-world financial data analysis using:

•	Microsoft Excel for data cleaning, transformation, and preparation

•	Power BI for interactive dashboard creation and insight generation

This project focuses on analyzing mobile banking statistics to assess:

•	Transaction volume and value distribution

•	Customer activity and engagement levels

•	Bank-wise performance (Public, Private, Co-operative)

•	Transaction frequency and average value trends

•	Risk indicators and adoption patterns

The goal is to transform raw mobile banking transaction data into meaningful insights for decision-making, highlighting customer behavior, banking sector performance, and digital adoption trends.

**2. Data Sources:**

•	Sources: India Data Portal https://indiadataportal.com/p/reserve-bank-of-india/r/rbi-bankwise_mobile_banking_transactions-in-mn-aaa

•	Timeline: January 2016 to December 2025

•	Domain: Financial Analytics

**3. Problem Statement:**

The rapid growth of mobile banking makes it important to analyze transaction data and customer usage patterns.

This project focuses on evaluating Mobile banking performance using metrics like transactions, transaction value, and active customers across different states and bank types.

It also aims to identify trends and customer behavior to improve banking services and support better decision-making.

**Bank Performance Analysis**

To measure overall bank performance using transactions, transaction value, and active customers. 

•	To find top and low performing banks based on transaction volume and value. 

•	To compare performance across Public, Private, and Cooperative banks. 

•	To understand customer distribution across different banks. 

•	To check efficiency using average transaction value and transaction frequency. 

•	To understand each bank’s share in total mobile banking activity. 

**Customer Behavior & Regional Insights** 

•	To study customer distribution across states and identify adoption levels. 

•	To understand customer segments (Small, Medium, Large) and their contribution to transactions. 

•	To observe transaction patterns across different states and categories. 

•	To identify states with highest and lowest mobile banking usage. 

•	To compare spending behavior using average transaction value across states. 

**Trend & Time Analysis** 

•	To study transaction trends over time and overall growth pattern. 

•	To measure Year-over-Year (YoY) growth in transactions. 

•	To observe monthly trends and seasonal changes in usage. 

•	To identify long-term patterns for future forecasting. 

•	To compare performance over different time periods using historical data. 

**4.	Attribute Details:**

The dataset includes fields such as id, date, month, year, bank name, state, number and amount of transactions, active customers, transaction category, bank type, average transaction value, customer tier, and transaction frequency per customer, used to analyze mobile banking performance and customer behavior.

**5.	Tools & Technologies:**

Microsoft Excel & Power Query:

•	Excel 

•	Power Query 

•	Power BI

**6.	Data Pre-Processing (Excel / Power Query/ Power BI):**

Tasks Performed:

•	Data Cleaning & Transformation: Removed duplicate records, handled missing values, standardized formats, and ensured correct data types for all columns. 

•	Handling Missing Values: Imputed missing values in no_of_active_customers using bank-wise logic to maintain data consistency and accuracy. 

•	Power Query Transformations: Applied transformations such as changing data types, creating custom columns, and automating data preparation steps. 

•	Feature Engineering (New Columns Added):

**Created additional columns such as:** 

•	Transaction Category: Classified transactions into small, medium, and large categories.

•	State: Added a column to capture the state where the bank operates.

•	Month and Year: Extracted from the Date column to enable time based analysis.

•	Average Transaction Value: Calculated the average value per transaction.

•	Customer Tier: Segmented customers into small, medium, and large tiers.

•	Transaction Frequency per Customer: Derived the average number of transactions per customer.

•	Calendar Table Creation: Created a separate date table to enable time-based analysis such as Year, Month, and support time intelligence functions.

•	Time Intelligence: Implemented measures like YoY Growth % and MoM Growth % to analyze performance trends over time.

•	Filtering & Sorting: Organized and filtered data to focus on relevant records for analysis. 

•	Bank-wise Aggregation: Created a calculated table to derive bank-wise transaction counts, enabling efficient comparison of bank performance.

**7.	Fact and Dimension Table Creation:**
     
•	Fact Table: Mobile Banking Statistics 

•	Dimension Tables: Calendar Table

**7.1 Classification of Fact and Dimension Tables:**

The mobile banking dataset was structured using a star schema model.

•	The Mobile Banking Statistics table was treated as the Fact Table since it contains measurable attributes such as the number of transactions, average transaction value, number of active customers, and customer tier.

•	The Calendar table was treated as a Dimension Table because it provides descriptive time attributes such as year, month, and quarter, which are essential for filtering and trend analysis.

**8.	Data Modelling and DAX (Power BI):**

**Data Model**

•	Established relationships between the Mobile Banking Statistics table and the Calendar table.

•	Defined one to many relationships between the Calendar table and the fact table.

•	Ensured proper cardinality for accurate aggregation and filtering.

**9. DAX Measures & Calculated Columns:**

**Calculated Measure:**

Implemented DAX measures for key metrics, including:

•	Total Transactions – Represents the total number of transactions 

•	Total Amount – Represents the overall transaction value 

•	Total Active Customers – Shows the number of customers actively performing transactions 

•	Total Customers – Represents the total number of customers in the dataset 

•	Total Banks – Represents the total number of unique banks 

•	Transaction Value – Indicates the average value per transaction 

•	Growth Percentage – Measures the percentage change between current and previous period 

•	YoY Growth % – Measures the year-over-year percentage change in performance 

•	Cumulative Transactions – Displays the running total of transactions over time

**Calculated Columns:**

•	Month: Represents the month of the transaction.

•	Year: Represents the year of the transaction.

•	State: Identifies the state where the bank operates.

•	Transaction Frequency per Customer (Integer): Calculates the average number of transactions per customer.

•	Customer Tier: Segmented customers into small, medium, and large tiers.

•	Transaction Frequency per Customer: Derived the average number of transactions per customer.

•	Data Categorization:

Classified data based on Transaction Category, Bank Type, and Customer Tier for better segmentation and analysis. 

**Table Creation:**

1.	Built a Calendar table with attributes like Year, Month, Quarter, and Day to enable time based filtering and trend analysis.
   
**Relationship Establishment**

•	A Many to One relationship was established between:

•	Mobile Banking Statistics [Date] → Calendar [Date]

•	This relationship enabled:

•	Monthly trend analysis

•	Year wise comparison

•	Drill down functionality

•	Time intelligence calculations

3.	Created a BankWiseCount table to store aggregated bank level information such as Record Count, Total Transactions, and Total Amount.
   
**10.	 Analysis and Visualizations (Power BI):**

**Bank Performance Analysis**

**Visuals Used:**

•	KPI Cards (Total Transactions, Total Transaction Amount, Active Customers, Transaction per Customer, Total Banks).

•	Bar Chart (Transactions by Bank)

•	Column Chart (Transaction Amount by Bank)

•	Donut Chart (Bank Type Distribution)

•	Scatter Plot (Active Customers vs Transaction Amount – Efficiency Analysis).

•	Page Navigator

**Interactive Features:**

•	Slicers (Bank Type, Bank Name, State, Year)

•	Button Navigation (custom buttons for page switching)

•	Edit Interactions (controlled slicer impact on visuals and cards)

•	Consistent Layout and Color Theme

**Customer Behavior & Regional Insights** 

**Visuals Used:**

•	Bar Chart (Customers by State) – shows regional customer distribution

•	Donut Chart (Customer Tier Distribution) – displays segmentation (Small / Medium / Large).

•	Matrix / Heatmap (State vs Transaction Category) – highlights usage patterns across regions.

•	Map (State-wise Transactions) – visualizes geographic transaction distribution

•	Line / Column Chart (Avg Transaction Value by State) – shows spending behavior across states.

**Interactive Features:**

•	Slicers (State, Transaction Category) – for regional and behavioural filtering

•	Slicers (Year) – To see the year wise bank performance

•	Minimalistic Design – avoids clutter and focuses on insights

•	Cross-filtering between visuals – selecting one chart updates others

•	Consistent Color theme and layout

**Trend & Time Analysis**

**Visuals Used:**

•	Line Chart (Transactions Count by Year) – The line chart shows a steady increase in mobile banking transactions from 2016 (0.8K) to 2024 (7.0K), reflecting consistent growth over the years.

•	Line Chart (Year-over-Year Growth %) – The chart shows rapid growth in mobile banking transactions between 2016 (89%) and 2018 (202%), followed by a steady decline with minor fluctuations, reaching 29% in 2024.

•	Line / Column Chart (Transaction Amount by Month-Year) – The line chart shows a sharp upward trend in transaction amounts from 2016 (5M) to 2024 (168,269M), with steady growth until 2023 followed by an exponential spike in 2024.

•	Line Chart (Count of Transactions by Year): Compares yearly transaction volumes and includes forecasting for the next 10 years.

•	Card Visual – Total Transactions: Displays the overall transaction count as a key KPI.

•	Card Visual – YoY Growth %: Shows year over year growth percentage for performance comparison.

**Interactive Features:**

•	Year Slicer: Allows filtering by specific years to analyze trends interactively.

•	Button Navigation (custom buttons for page switching)

•	Edit Interactions (controlled slicer impact on visuals and cards)

•	Consistent Layout and Color Theme

**11.	 Insights & Conclusions:**

**Bank Performance Analysis** 

•	    State Bank of India leads with ~167B transactions, followed by HDFC Bank (~55.7B) and Bank of Baroda (~41.4B), showing that a few top banks dominate transaction volume, while most other banks contribute significantly lower volumes.

•	Public Sector Banks lead with ~8.4B active customers, followed by Private Sector Banks (~4.0B) and Payment Banks (~1.6B), while other bank types have significantly lower and niche customer bases.

•	State Bank f India leads with ~5.66B active customers, followed by HDFC Bank (~1.13B), while Kotak Mahindra Bank (~0.76B), ICICI Bank (~0.73B), and Axis Bank (~0.72B) form the next tier, indicating a highly concentrated customer base among top banks.

•	Efficiency analysis shows SBI as both a high-volume and high-value performing bank. 

**Customer Behavior & Regional Insights** 

•	Maharashtra leads with (5,441) active customers, followed by Gujarat (3,681) and Karnataka (2,042), while most other states have significantly lower counts, indicating customer concentration in key economic regions. 

•	Large customers (~10.46B) contribute the most, far exceeding Small (~3.63B) and Medium (~0.47B) segments. 

•	Urban states show higher adoption rates, while rural states show steady but slower growth. 

•	Maharashtra (HQ ~175M) leads in average transactions, followed by Punjab (~59M) and Delhi (~44M), with a sharp drop across other states.

**Trend & Time Analysis** 

•	Transaction count shows steady growth from 797 in 2016 to 6,966 in 2025, indicating consistent year-over-year increase in activity, with significant acceleration after 2018.

•	YoY growth peaked in 2018 at 201.80%, followed by strong growth in 2019 (131.95%) and 2021 (111.26%), but gradually declined to 28.78% by 2025, indicating a shift from rapid expansion to a more stable growth phase.

•	Mobile banking has experienced accelerated adoption and scaling, with 2024 marking an unprecedented surge in transaction value — indicating both deeper customer engagement and rapid expansion of digital financial services.

•	Forecasting indicates continued growth in mobile banking over the coming years. Both historical and forecast data confirm a consistent upward trajectory, with monthly cumulative jumps translating into long-term growth forecasts that nearly double between 2025 and 2030.

**12.	 Conclusion:**

•	Mobile Banking Trends & Performance Analysis (2016–2025) highlights significant growth in digital transactions, customer adoption, and banking efficiency over time. 

•	The analysis provides clear insights into bank performance, regional usage patterns, and customer behavior using key KPIs. 

•	These findings support data-driven decision-making and indicate strong long-term growth potential in mobile banking services.
