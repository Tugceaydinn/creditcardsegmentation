# creditcardsegmentation

K-Means Customer Segmentation (due to cradit card behaviour)
About Project
The number of people who do not use credit cards nowadays is very small. But how efficiently do we use it? To us, this question may sound like a social question. But for banks, this question refers to the risk they take or the opportunities they can seize. In order to evaluate these risks and opportunities, they need to analyze the situation of their customers well. That's why customer segmentation is essential.

Our aim in this project, which examines the status of customers according to credit card behaviors, is to determine which customer we should approach and how. To put it another way, in this case we will develop a customer segmentation to define marketing strategy.

Our sequence of actions is as follows: Answering questions such as how customers spend, who gets more cash, who buys more expensive, who buys more in installments etc. According to the answers to these questions we asked, we can take actions such as which customer's limit will be increased or decreased, which customers should we inform about the installment opportunities.


The classes I clustered are as follows

Cluster 7 People with average to high credit limit who don't usually make one of purchases

Cluster 6 People with high spenders and high credit limit

Cluster5 People with average to high credit limit who make all type of purchases

Cluster4 This group has more people with due payments who take advance cash more often

Cluster3 Less money spenders with average to high credit limits who purchases mostly in installments

Cluster2 People with low credit limit who take more cash in advance

Cluster1 High spenders with high credit limit who make expensive purchases

Cluster0 People who don't spend much money and who have average to high credit limit

Before using PCA to transform data to 2 dimensions for visualization, first we took cosine distance before PCA because cosine distance kills the magnitude of vectors and focuses on relationships only.

Finally after PCA, I visualized our data reduced to x and y tags, expressing the clusters with different colors, grouping them according to their labels with the .groupby function to observe.

Required Libraries
pandas (load and manipulate data and for One-Hot Encoding)

numpy (calculate the mean and standard deviation)

seaborn (helping with some visualization techniques)

matplotlib.pyplot (some graphs)

matplotlib.ticker (for specifying the axes thick format)

sklearn.preprocessing , StandartScaler (scaling)

sklearn.cluster , KMeans (k-means algorithm library)

sklearn.decomposition , PCA (applying principal component analysis)

sklearn.metrics.pairwise , cosine_similarity (normalised dot product between two vectors (preparing for PCA))

io (reading files for all systems)

About dataset
The sample Dataset summarizes the usage behavior of about 9000 active credit card holders during the last 6 months. The file is at a customer level with 18 behavioral variables.

Following is the Data Dictionary for Credit Card dataset :

CUSTID : Identification of Credit Card holder (Categorical)

BALANCE : Balance amount left in their account to make purchases (

BALANCEFREQUENCY : How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)

PURCHASES : Amount of purchases made from account

ONEOFFPURCHASES : Maximum purchase amount done in one-go

INSTALLMENTSPURCHASES : Amount of purchase done in installment

CASHADVANCE : Cash in advance given by the user

PURCHASESFREQUENCY : How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)

ONEOFFPURCHASESFREQUENCY : How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)

PURCHASESINSTALLMENTSFREQUENCY : How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done)

CASHADVANCEFREQUENCY : How frequently the cash in advance being paid

CASHADVANCETRX : Number of Transactions made with "Cash in Advanced"

PURCHASESTRX : Numbe of purchase transactions made

CREDITLIMIT : Limit of Credit Card for user

PAYMENTS : Amount of Payment done by user

MINIMUM_PAYMENTS : Minimum amount of payments made by user

PRCFULLPAYMENT : Percent of full payment paid by user

TENURE : Tenure of credit card service for user

Dataset link: https://www.kaggle.com/arjunbhasin2013/ccdata

Conclusion
Different actions can be taken according to the 8 clusters we have separated. For example,(for Cluster3) we can encourage users who shop in installments by increasing their special installment options or (for Cluster2), customers who withdraw and spend cash can be provided with low commission cash via credit card or (for Cluster5) we can increase their loyalty with special offers for people with high limits and all kinds of spending.
