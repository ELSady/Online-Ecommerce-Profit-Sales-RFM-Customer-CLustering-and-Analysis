## Data Science Project : Ecommerce Profit-Sales RFM Customer Clustering and Analysis Overview
* Dataset of one of Ecommerce sited in US with a customer's purchase history over the course year of 2015.
* Analyse which products / categories's as well as product segment which provide the most inerms of profit and sales.
* ANalyze and filter out which countries / regions which satisfies the 80% of sales / profit.
* Using Recency, Frequency and Monetary strategies to segment customers into certain groups based on the RFM scoring / metric.
* Build unsupervised K means model to further improve / confirm customer segmentation.



RFM analysis is a data driven customer behavior segmentation technique. RFM stands for recency, frequency, and monetary value. The idea is to segment customers based on when their last purchase was, how often they’ve purchased in the past, and how much they’ve spent overall. All three of these measures have proven to be effective predictors of a customer's willingness to engage in marketing messages and offers. While RFM analysis was born in direct-mail, it is a powerful tool for eCommerce stores to use today. RFM analysis allows us to make sense of all the customer data our store captures as part of interactions with the brand and customer transactions from the store. 


### Business Questions:
* Which products / categories of product and segment generate the most of sales-profit?
* Which Cities, Stattes and Countries generate the most of sales and profit? 
* How are thecumulative sum of 80% of sales / profit for all parameters?
* How is the customer segmentation based on RFM analysis? 
* How is the behaviour / specific traits for each customer group?

### Projects Frame work / step by steps:
* Dataset Profiling
* Dataset Inspection, checking for any missing / abnormal values
* Datascet Cleaning, should there be any missing values
* Feature Engineering
* Visualization / Analysis
* RFM Analysis / Segmentation
* K Means Model Building

### Resources Package Used:
* Pandas
* Numpy
* Matplotlib / Seaborn
* Scikit Learn
* PyCaret

### Dataset Profiling
* Dataset consists of 51288 observations and 23 features, with a total dataset size of 1179624.

### Feature Types
* Majrity of features fall to the categorical types, meanwhile the rest of 6 are numerical ones.

### Data Cleaning
* There are no missing values detected.
* Further look at distinct values for each of categorical features aswell, abnormal values were non to be found.
* Dataset is perfectly clean.

### Feature Engineering
* Parsing Date time feature for ORder Date and Shipping Date. This is done to obtain tthe range of date of dataset. 
* As above, the date ranges over the courses of year 2015.
* Creating new feature GMV (Gross Market Value).

### Visualization
Product Categories

* Seems like the customers are keen on fashion related proiducts, evidence by the higher number of sales  / profit. It satisfies almost up to 65 % amount of sales / profit for the ecommerce. Meanwhile, home furniture only satisfies about 17 %, auto-accessories around 14% and lastly Electronic only around 5%. <br>

Segment 

* Half of the customers are your typical end user consumer, which allocates for a 50% profit and sales for ecommerce, followed by corporate around 30% and home office around 20%. <br>

City

* Of all the total 3636 cities, about one-third of them satisfie the 80% sales and profit. <br>

States

* Meanwhile for the tates, 258 already satisfie the 80% profit and sales. <br>

Country

* Moving on to countries, we can already see united states top the the list in terms of sales and profit, satisfying almost of 20%, much much more than any other countries. Followed by Australia, France and Mexico in which satisfies around 7%,6% and 5% respectively. There are 29 of total countries which makes up the 80% profit and sales. <br>

Region

* Central seems the biggest contributors for the Ecommerce when it comes to profit and sales, makes up to 21% of it, followed by South, EMEA and north in which the 33 makes out around 13%, 10% and 9% for sales and proft respectively. <br>

### Recency, Frequency, Monetary
* First, filter out dataset including countries which makes up the 80% of profit and sales. As given previously, there are 29 total.
* Next, grouping dataset based on the Customer Name / ID, this is to obtain the Recency, Frequency and Monetary values for each customers.
* Recency is the distance between last purchase to the latest ones, measured in days.
* Frequency is how often customers have purchased from the ecommerce.
* Monetary is a measure of how many 
