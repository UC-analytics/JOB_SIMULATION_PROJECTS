# :purple_square: TATA iQ: Data Visualization and Business Insights
A Forage job simulation: online retail analytics for a CEO and CMO, built in Tableau to reveal customer purchasing trends across multiple regions and countries, and presented effectively to the executives to generate insights for the company.

---

## :clipboard: Project Overview
In this simulation, I assumed the role of a data analyst for an online retail store. The CEO and CMO needed to understand how the business was performing, where demand was strongest, and which markets and customers offered the best expansion opportunities. This work covered the full analytics process: deciphering the right questions to answer, cleaning the data, building visuals, and presenting the findings to leadership. <br> 
For context: The two executives mainly focused on growth, profitability, Geographical Expansion, and customer retention. The CEO looks at the business through the lenses of revenue, market trends, and expansion. The Chief Marketing Officer (CMO) evaluates it from the perspectives of the customers, product demand, and sales. My job was to turn one transactional dataset into clear answers for both, to guide decision-making.

---

## ::  Dataset description and source
The TATA Group provided the dataset for this job simulation. It features:
- Online retail transactions from December 2010 to 9 December 2011
- About 536642 rows after cleaning, covering customers in the UK and 35 other countries
- Key fields: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

---

## :interrobang: Tasks and approach
### Task 1: Framing the Business Scenario
I drafted eight questions, four for each leader (Both CEO and CMO), reflecting their different priorities.

For the CEO (questions around growth, profitability, geography, and business performance):
- How has revenue changed over time, and are there clear monthly or seasonal trends that could influence future sales forecasting and business planning?
- Which countries generate the highest revenue and sales volume, and which international markets show the strongest opportunities for further expansion?
- How concentrated is the company’s revenue among its top customers, and how dependent is the business on a relatively small number of high-value customers?
- What proportion of sales is being lost through cancellations or returned items, and which products, customers, or markets contribute most to these losses?
      For the CMO (questions around customers, products, demand, and marketing opportunities):
- Which products generate the highest sales volume and revenue, and how does demand for these products change across different periods of the year?
- Who are the highest-value and most frequently purchasing customers, and how can customers be segmented based on recency, frequency, and monetary value for more targeted marketing?
- Which products are most popular in each country, and how could these geographic differences in customer preferences be used to tailor promotions and product positioning?
- What patterns exist in repeat purchases and customer buying behaviour, such as purchase frequency, basket size, and commonly purchased products, that could be used to improve customer retention and cross-selling?

### Task 2: Choosing the Right Visuals
This was a preliminary task where I needed to identify the most suitable type of visualization for various business questions. The CEO provided multiple visualization requests, and I selected the visuals that would convey the data and insights in the clearest way possible. Since data can be presented in a variety of charts, it is crucial to choose the one that best displays the information effectively.

### Task 3: Data cleaning and visualisation (Done using Excel and Tableau)
This task essentially required me to create the visuals around each of the four questions that the CEO and CMO have asked, using either Tableau or Power BI. This task was split into data cleaning and data visualisation. The questions included the following:
1. The CEO of the retail store is interested in viewing the time series of the revenue data for the year 2011 only. He would like to view granular data by looking into revenue for each month. The CEO is interested in viewing the seasonal trends and wants to dig deeper into why these trends occur. This analysis will be helpful for the CEO to forecast for the next year.
2. The CMO is interested in viewing the top 10 countries that are generating the highest revenue. Additionally, the CMO is also interested in viewing the quantity sold along with the revenue generated. The CMO does not want to have the United Kingdom in this visual.
3. The CMO of the online retail store wants to view the information on the top 10 customers by revenue. He is interested in a visual that shows the highest revenue-generating customer at the start and gradually declines to the lower revenue-generating customers. The CMO wants to target the higher revenue-generating customers and ensure that they remain satisfied with their products.
4. The CEO is looking to gain insights on the demand for their products. He wants to look at all countries and see which regions have the greatest demand for their products. Once the CEO gets an idea of the regions that have high demand, he will initiate an expansion strategy which will allow the company to target these areas and generate more business from these regions. He wants to view the entire data in a single view without the need to scroll or hover over the data points to identify the demand. There is no need to show data for the United Kingdom, as the CEO is more interested in viewing the countries that have expansion opportunities.
*Data Cleaning:*
I created a copy of the original data and then performed the necessary data cleaning. I removed 5268 duplicate data rows to avoid having skewed results. Then I removed negative values in the quantity and unit price sections (representing returned purchases and invalid prices) by using conditional formulas, and proceeded to filter them out. I filtered out a total of 10589 rows as a result and moved the necessary data to a new sheet.
*Data Visualisations*
I loaded the Excel file into Tableau for the required analysis and created a Revenue field (Quantity × UnitPrice).
  For the first task, I plotted a line chart showing the monthly revenue for the year 2011, using the invoice date column. From the chart, I observed that revenue fluctuated between increases and decreases each month. It started with a decline from 689,812 in mid-January to 522,546 by mid-February. This alternating pattern continued until June, after which the revenue dip in July was only half as severe as previous months. The revenue then rose steadily, peaking at 1,503,867 in mid-November. However, it fell sharply thereafter, ending at 637,790 in December, which is quite close to the initial revenue at the start of the year. I attributed this decline to a data artifact, as the invoice dates in the dataset end on December 9. Therefore, I believe that the drop reflects incomplete data rather than a decline in demand. 
  For the second task, a side-by-side chart was used to illustrate the top 10 countries generating the highest revenue along with the quantities sold. Five countries dominate this chart, excluding the UK. The UK accounts for approximately 85% of total revenue, leaving the remaining 15% to be shared among the other countries. The Netherlands, EIRE (Ireland), Germany, France, and Australia contribute to about 70% of the non-UK revenue. Spain, in sixth place, earns less than half of Australia’s revenue, resulting in a clear drop after the fifth bar on the chart.
The top two countries largely rely on a few buyers. One customer is responsible for about 98% of the Netherlands' revenue. In EIRE, two customers account for around 98% of the revenue, and in Australia, one customer generates about 90% of the revenue.
Germany and France represent healthier markets, each having approximately 90 customers and 390 to 460 orders, meaning their revenue is more evenly distributed among many buyers.
The price per unit varies across these countries. The Netherlands sells at about $1.42 per unit, while Germany and France sell at around $1.90 per unit, indicating a trend of bulk buying of lower-priced items. Spain has the highest value per unit at about $2.20.
  The Chief Marketing Officer (CMO) wanted to identify the highest revenue-generating customers to target for profit retention and growth. I visualized this using a column chart. Two customers on the chart are outliers due to unusually high order volumes compared to the others. One, Customer 12346, placed a single order of 74,215 units on January 18, while the other, Customer 16446, ordered 80,995 units on December 9, the last day of the data range. Although these outliers still contribute to overall revenue, removing them alters the picture significantly. Without these two, the top 10 customers would then include Customer 16684 (approximately 66.7k) and Customer 14096 (around 65.2k), making them the largest revenue contributors.
Most of these top customers are loyal clients who remained active throughout the year. For instance, Customer 14911 (from Ireland) placed 201 orders, which indicates the behavior of a regular repeat buyer.
In terms of geography, after cleaning the data, six of the top ten customers are located in the UK, while two are in Ireland, and one each is situated in the Netherlands and Australia. The top customer, Customer 14646 from the Netherlands, generates approximately 280k, making it the most important account in the entire non-UK business.
The top ten customers account for about 17% of all identified customer revenue across 4,339 customers. Additionally, about 16% of total revenue was generated by transactions without a customer ID and was excluded from this chart.
  To highlight the countries and regions with the highest demand for their products, I created a filled map visual that allowed them to see demand levels across different regions at a glance. The ranking by quantity aligns with revenue: the Netherlands leads with 201,000 units sold, followed by EIRE with 147,000, Germany with 119,000, France with 112,000, and Australia with 84,000. There is a significant drop in demand after this, with Sweden at 36,000, Switzerland at 31,000, Spain at 28,000, Japan at 26,000, and Belgium at 23,000. Demand is primarily concentrated in Western Europe and Australia, with Japan being the only Asian market in the top ten.
Sweden presents an unusual situation: it ranks sixth in quantity sold but only has eight customers and the lowest revenue per unit sold, approximately $1.06. The country purchases many low-priced items, which means that the quantity sold may not accurately reflect its real value. Because "demand" in this context refers to units sold, it is heavily influenced by a few bulk wholesale buyers.

### Task 4: Communicating insights and analysis
I recorded a five-minute video for the CEO and CMO explaining the data preparation, the visual choices, and my findings, with a focus on expansion opportunities and next steps to take. I related my findings to each of the four scenarios presented to me in the previous task.

---

## :hammer_and_wrench: Tools used

- Excel for data cleaning
- Tableau (data cleaning, calculated fields, visualisation and analysis)

---

## 🗂️ Project/Folder Structure

## Folder Structure
```
Tata_Data_Visualisation/
├── README.md
├── Data/
│   ├── online_retail_cleaned.csv
|   └──
├── tableau/
│   └── Tableau_visualisation.twbx
├── images/
│   ├── monthly_revenue.png
│   ├── top_10_countries.png
│   ├── top_10_customers.png
│   └── demand_map.png
└── presentation/
    └── presentation_notes.md
```
---

## :bulb: Key Findings & Insights
- *Seasonality*: Revenue was fairly flat from January to August, then climbed to a peak of about 1.5m in November, consistent with pre-holiday buying. The apparent December fall reflects incomplete data, since the dataset ends on 9 December 2011.
- *Markets*: Netherlands, EIRE, Germany, France and Australia generate about 70% of non-UK revenue. After them, revenue drops sharply.
- *Quality of demand*: Germany and France have broad customer bases (about 90 customers each). Netherlands, EIRE and Australia depend on a handful of bulk buyers, so they’re better managed as key accounts.
- *Customers*: The top 10 customers account for about 17% of identified customer revenue, and most of them bought in nearly every month of the year, which signals strong loyalty.

### Recommendations
- Prioritise Germany and France for deeper marketing investment, and treat the Netherlands, EIRE and Australia as account-managed markets (losing one customer would wipe out most of the country’s revenue).
Treat Germany and France as the proven, broad markets where marketing spend should work best.
- Consider Spain, Belgium and Switzerland as next-tier expansion candidates.
- Plan stock inventory and campaigns from late summer to prepare for the autumn peak, and run targeted ads in September and October, especially to high-value and wholesale customers, so that they order early.
- Launch promotions in the January to June periods. That’s where revenue is flat and unstable, so campaigns or bundle offers could help lift it.
- Study why the two dips (February and June) happened, then plan a strategy to fix that
- Management should give the top accounts dedicated attention: loyalty perks, early access to new stock, and a check-in if a regular buyer’s order gap grows.
- Investigate the roughly 16% of revenue with no customer ID. It could be guest checkouts, and capturing those customers would widen the retention list. 

---

## :warning: Limitations
- Returns and cancellations were removed rather than netted off, so a few very large orders that were later cancelled in the raw data can still inflate customer and monthly figures.
- December 2011 is a partial month with incomplete data
- About 16% of revenue has no customer ID and is excluded from the customer analysis.
*Next step*: analyse repeat-purchase patterns and time between orders, and compare against 2010 to confirm the seasonality.

---

## :mailbox: Contact

**Uchechukwu Esther Okwudili**  
:e-mail: [Email](ucokwudili27@gmail.com )
:briefcase: [LinkedIn](www.linkedin.com/in/uchechukwu-okwudili)
:globe_with_meridians: 

---

*⭐ If you found this project useful or interesting, feel free to star the repository!*


o	☐ Key findings and a screenshot or two
o	☐ How to reproduce the analysis
o	☐ Link to the dashboard or website write-up
•	☐ Organised folders, e.g. data/, scripts/ or notebooks/, outputs/ or images/


