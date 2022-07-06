## Data Science Project : Ecommerce Profit-Sales RFM Customer Clustering and Analysis Overview
* Dataset of one of Ecommerce sited in US with a customer's purchase history over the course year of 2015.
* Analyse which products / categories's as well as product segment which provide the most inerms of profit and sales.
* Analyze and filter out which countries / regions which satisfies the 80% of sales / profit.
* Using Recency, Frequency and Monetary strategies to segment customers into certain groups based on the RFM scoring / metric.
* Build unsupervised K means model to further improve / confirm customer segmentation.

![alt text](https://github.com/ELSady/Clustering-Airflight-Customer-Segmentation-and-Analysis/blob/main/667307.jpg) <br>

RFM analysis is a data driven customer behavior segmentation technique. RFM stands for recency, frequency, and monetary value. The idea is to segment customers based on when their last purchase was, how often they’ve purchased in the past, and how much they’ve spent overall. All three of these measures have proven to be effective predictors of a customer's willingness to engage in marketing messages and offers. While RFM analysis was born in direct-mail, it is a powerful tool for eCommerce stores to use today. RFM analysis allows us to make sense of all the customer data our store captures as part of interactions with the brand and customer transactions from the store. <br>


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
* Monetary is a measure of how much customers have spent purchasing on the store.

* Determining score for Recency, Frequency and Monetary. With a scale of 1 to 4.
* A higher number Recency score, means customer have purchased something very recently. The same applies to frequency and moentary score. Higher frequency score means customers have a history of purchasing frequently / several perhaps dozen times, whilst higher score of monetary means customers are generating higher profit stream for ecommerce. Most of the times, higher frequency correlates also with higher monetary.

### RFM Score Distribution / Comparison

Color in Red stands for Recency Distribution, Green stands for Frequency Distribution and Blue stands for Monetary Distribution. <br>
* We can clearly see a rightly skewed distribution. Indicating that the majority customers in the last 15 days, many customers have recently purchased from the ecommerce. This is very good sign, customers are still highly-engaged to the store. 
* For frequency (green in color), we can see a good normally distributed plot. Majority of each customers has purchased around 40 to 60 times. 
* Monetary distribution (blue in color) is alos in a ver good shape of normal one. It is clearly seen that majority of each customers have spent around 20000 to 25000 US dollar.

### Customer Segmentation based on RFM joint Score

Customer here are segmented into 5 different categories as follows:
* Loyal : Customers with the highest RFM Score of 444 point.
* Champion : Customers with two 4 points of RFM score, having highest possibility to turn into loyal customer which is a very valuable assets for the company.
* Average : Customers with an average score, having at least two 3 score or a combined of 3 & 4 score each.
* At Risk : Customers with double 1, 2, or both point of RFM Score and without any of 4 on their RFM, for these type of customers, the company must handle this seriously so taht they dont turn to lost customers.
* Ghost or Lost : Customers with the lowest RFM Score. <br>

Based on our analysis, we divide the customers into 5 group, based on their RFM joint score. We may want to further anlyse the cluster using K means, checking to see if the model has similar outcome as our analysis here.

### K Means Cluster Modeling
* Using pycaret as preprocessing tool, the setup si as follows

* Create a default 4 different groups / cluster. Then, we will evaluate the model performance using elbow method.

* Elbow method provides us the means to evaluate K cluster and determine which clusters is the most optimum. For this dataset, the optimum is 4 clusters. It means we have to build another model in which the cluster groupis 5
* Build another 2 different models, one with k = 4 and k = 5.
* 
### Different Clusters Comparison 
* We can clearly see in 4 clusters, it lacks the group in which the higher value / loyal customer are. This is very reasonable, because customers who fall to this group only allocated for only a dozen if not lower than total of customers / only a handfull of customers.
* So 5 clusters are the optimum ones for this dataset.

### 5 Clusters Analysis
* Cluster 1 consists of 197 customers. Characteristics of this group of customers, average score for both frequency and monetary (at score of 3) also having low recency score (at score of 2). THe seasonal customers, one who only purchase during a certain events or large discounts. Needs to be given a stimulus to raise specificly their recency score.
* Cluster 2 consists of 92 customers. These customers are the loyal ones, characterised by a high number for all metrics. High spending, frequent purchase and very recent buys as well. Needs to be very well maintained.
* Cluster 3 consists of 171 customers. The potentially lost customers or perhaps already ones. Characterised by the low score of recency, but having an average score of both monetary and frequency. Perhaps these customers at some point are reguler buyers of the store, but at then decided to stop buying from the ecomerce. Needs marketing strategies to attract them back and start purhase from the store again.
* Cluster 4 consists of 201 customers. The current reguler customers. Having average number for all metrics (some at 4). Like the previous cluster 1, these customers need to be given stimulus aside from being well maintained. The potential to be loyal customers with the right marketing strategies.
* Cluster 5 consists of 134 customers. The new customers. Characterised by the low number for both frequency and monetary, but high in terms of recency. Same as previous one, need further stimulus and or discount to attract them more and make them reguler ones.

### Conclusion
* Two types / product categories makes up for the 80% of profit and sales, those categories are fashion and home / furnitures. With Fashion makes up to 65% of profit / sales, while home and furnitures makes up to 17&.
* Two customers segment makes up to 80% of profit / sales for ecommerce. End user consumers dominates the segment with a whooping 50% of profit / sales, followed by corporate at 30% and home office at 20%.
* A total of 1084 cities already meets the 80% of profit / sales of ecommerce, while for states there are 257%.
* There are 29 countries which already makes up the 80% of profit / sales. United states are on top at 19%, followed by Australia, France and Mexico.
* 7 Region makes up the total 80% of profit / sales. With Central on top at 22%, followed by SOuth region, EMEA and North one.
* 5 different customer clusters were dettermined based on RFM joint score. There's Loyal, Champion, Reguler, At risk and Lost / ghost customers.
* 5 diferentt customers segment is also determined based on K means model. 
