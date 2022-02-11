# Cryptocurrency Clusters

## Background

* You are on the Advisory Services Team of a financial consultancy. One of your clients, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. They’ve asked you to create a report that includes what cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system for this new investment.

* You have been handed raw data, so you will first need to process it to fit the machine learning models. Since there is no known classification system, you will need to use unsupervised learning. You will use several clustering algorithms to explore whether the cryptocurrencies can be grouped together with other similar cryptocurrencies. You will use data visualization to share your findings with the investment bank.

### Data Preparation

* Read `crypto_data.csv` into Pandas. The dataset was obtained from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).

* Discarded all cryptocurrencies that are not being traded. 

* Removed all rows that have at least one null value.

* Filtered for cryptocurrencies that have been mined. That is, the total coins mined should be greater than zero.

* Since the coin names do not contribute to the analysis of the data, deleted the `CoinName` from the original dataframe.

* Converted the remaining features with text values, `Algorithm` and `ProofType`, into numerical data. 

* Standardized dataset so that columns that contain larger values do not unduly influence the outcome.

<img width="592" alt="Screen Shot 2021-10-28 at 6 29 10 PM" src="https://github.com/azmir0218/Unsupervised_Machine_Learning/blob/main/photos/transformation.png">


### Dimensionality Reduction

* Performed dimensionality reduction with PCA. Preserved 90% of the explained variance in dimensionality reduction. 

* Next, further reduced the dataset dimensions with t-SNE and visually inspected the results. 

<img width="592" alt="Screen Shot 2021-10-28 at 6 29 10 PM" src="https://github.com/azmir0218/Unsupervised_Machine_Learning/blob/main/photos/tsne.png">


### Cluster Analysis with k-Means

* Created an elbow plot to identify the best number of clusters. Used a for-loop to determine the inertia for each `k` between 1 through 10. Determined, if possible, where the elbow of the plot is, and at which value of `k` it appears.

#### Elbow curve

<img width="592" alt="Screen Shot 2021-10-28 at 6 29 10 PM" src="https://github.com/azmir0218/Unsupervised_Machine_Learning/blob/main/photos/elbow.png">

#### Different Clusters

<img width="592" alt="Screen Shot 2021-10-28 at 6 29 10 PM" src="https://github.com/azmir0218/Unsupervised_Machine_Learning/blob/main/photos/kmeans.png">


