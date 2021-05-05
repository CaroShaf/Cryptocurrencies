# Cryptocurrencies Analysis
For this project, we have chosen to use unsupervised machine learning, with the K-means model, to create a classification system for a bank client to analyze the cryptocurrency
market as a new investment for its customers. There are over 1200+ cryptocurrencies in our dataset which were processed, clustered, and features reduced by using principal
component analysis (PCA). This modified dataset was filtered for cryptocurrencies that are tradable and then run through the K-means clustering unsupervised machine learning
algorithm and grouped into four clusters.  The data visualizations that accompany this study reveal some possible choices for these new investment porfolios.

Resources used to conduct this study: Python 3.7, Pandas, Jupyter Notebook, Scikit-learn, CSV file provided by Accountability Accounting

## Overview 
Four steps were performed in order to produce meaningful results for Accountability Accounting.

1. Preprocessing the Data for PCA - this step consisted of removal of null values (to increase performance and accuracy of ML algorithm), filtering out cryptocurrencies that are
 not tradeable, whittling down the number of cryptocurrencies from over 1,200 to 533.  Also data was standardized by scaling so that the classification of the cryptocurrencies into groups by similarities was more accurate. 
 
2. Reducing Data Dimensions Using PCA -- the PCA algorithm reduced down over 100 factors to just three of the primary components.  This makes for more managable and more 
meaningful data in preparation for clustering which is conducted by the K-means algorithm in the next step.  The number of clusters (k) was determined by creating an elbow 
curve, using the principal components.  The elbow curve determined that four was the optimum number of clusters as can be seen in the graph below.

    Elbow Curve [https://github.com/CaroShaf/Cryptocurrencies/blob/main/images/elbow%20curve.png]

3. Clustering Cryptocurrencies Using K-means - the K-means algorithm is popular for unsupervised clustering.  Because we didn't know how to group the cryptocurrencies outright,
we used unsupervised machine learning to determine meaningful groupings, but we calculated the most meaningful number of clusters to group the data within as was done in the
preprocessing and PCA steps in 1 and 2.

4. Visualizing Cryptocurrencies Results - Using the three principal components, along with other associated data, a scatter plot, a 3d scatter plot and an interactive table
helps us to see how the different cryptocurrencies stack up against each other.  The scatter plots are also interactive in that hovering is activated over the data points so
different aspects, such as the name of the cryptocurrency and algorithm it uses is displayed in a pop-up box.  Screenshots of these visualizations are available by following the 
links below.

## Results
* Scatter plot [https://github.com/CaroShaf/Cryptocurrencies/blob/main/images/scatter%20plot.png] - this two-dimensional plot may be the least useful of the three
      visualizations since the color of the data points is the only distinguishing feature and only alludes to the 3rd dimension by showing different colored dots on top of
      others.  This plot does, however, have a hover feature so that individual data points can be examined for further information.
      
* 3d scatter plot [https://github.com/CaroShaf/Cryptocurrencies/blob/main/images/3d%20showing%20bittorrent.png] - this three-dimensional plot is quite interesting as it can
      be rotated and zoomed in and out to see the groupings more clearly.  This plot also has hover features and the image shows the hover feature activated for BitTorrent,
      which is clearly an "outlier," in a class of its own.
      
 * Hvplot table [https://github.com/CaroShaf/Cryptocurrencies/blob/main/images/hvplot%20table.png] - this table, as shown in the image, is very useful in that it is
      interactive and as such CoinName can be alphabetized or algorithms or classes can be "grouped" by sorting on the column of choice.


## Summary

These results are left to interpretation, but a January 2021 article in Investopedia [https://www.investopedia.com/tech/most-important-cryptocurrencies-other-than-bitcoin/] 
names 10 cryptocurrencies that are "most important."  A full half of this ten are not listed in our data set, as can be determined by using the HVplot table.  Furthermore, our
dataset has nearly half of it removed due to non-tradeable status.  However, according to Investopedia [https://www.investopedia.com/news/does-your-financial-advisor
speak-crypto/], as of April 2021, there are over 9,000 peer-to-peer cryptocurrencies which are actively transferring data and value.

Since the point of cryptocurrency is to elminate the middleman (i.e., the bank) by using blockchain technology as the validation/trustworthy agent for financial (and other
legal) transactions, it may not be the best business for banks to be getting in, as interesting as it may be for financial advisors.  Most financial advisors are actually
likening investment in cryptocurrency to gambling.  They aren't recommending it.

However, that being said, much more data analysis would be required before Accountability Accounting should get into this game.  Even with this machine learning algorithm, or
others, with this dataset, the results are fairly inconclusive except that of the five (of ten) most important cryptocurrencies present in our dataset, three were Proof of Stake
algorithms and two were Proof of Work.  The first article cited above indicates a trend of endorsements for cryptocurrencies that use proof-of-stake algorithms that increase
transactions per second over other algorithms.  With this key feature in our dataset but with such a very small subset of data that does not contain market capitalization values
or token values it does seem somewhat like gambling rather than investing.
