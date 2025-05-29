# 1 Background and Objective
In this project the objective is to find an optimal method to cluster customers based on ecommerce data.
<br><br>
Clustering plays a crucial step in marketing by differentiating customers based on psychological (e.g. satisfaction), demographic (e.g. age) or/and behavioural (e.g. last activity) factors. The objective of clustering is to tailor marketing activities, such as advertising or social media activities to the specific characteristics of each segment. The overall goal is to allocate ressources, particularly finacial ressources optimally.
<br><br>
The dataset stems from kaggle: https://www.kaggle.com/datasets/salahuddinahmedshuvo/ecommerce-consumer-behavior-analysis-data
<br><br>
This project is licensed under the terms of the Creative Commons Attribution 4.0 license (CC-BY-4.0)


# 2 Data Structure

The raw dataset has 1000 entries with 28 columns, which can be divided into demographic, psychological and behavioural columns:



# 3 Executive Summary
## 3.1 Initial Clustering
The process of finding an optimal solution started with the question of wether natural clusters could be identified within the data. Therefore two cluster methods were used: <b>Hierarchical Clustering</b> and <b>DBSCAN</b>. The methods were chosen because of the mixed data types, the data contains - i.e. nominal, ordinal and metric data. Other clustering methods can not handle mixed data types. The popular K-Means algorithm is not suitable for categorical data, because it uses euclidean distance to measure the distance between the data points and assume therefore continuous values. K-Modes and K-Prototype are also not suitable for clustering this type of data. They can handle only continuous and/or nominal data, but not ordinal data. Hierarchical Clustering and DBSCAN can use precomputed distance matrices as a metric method. For this reason the <b>gower distance</b> were computed and was set as a precomputed metric into the cluster algorithms. Moreover, algorithm like K-Means or K-Modes do not support precomputed matrices as input.

![Silhoutte_Plot](/assets/img/Silhoutte_Score_per_Sample.png)

Exploring the data with regard to its distribution indicated, that no natural and distinct clusters in the data could be found. Furthermore, the non significant distribution of the data made it also difficult to select appropriate features for the algorithms. At least, the correlation analysis showed that there was no intercorrelation between the features. The assumption, that no distinct clusters can be found was confirmed after performing Hierarchical Clustering and DBSCAN. In both algorithms, the Silhouette Score only showed a score of 0.0187 and -0.1612, respectively (see Plot). To reduce the effect in higher dimensions ('curse of dimensionality') a Principal Component Analysis (PCA) was performed using 2 principal components. But even there, the plot didn´t show any distinct clusters. The unsatisfying result raised the question which method can be used to cluster the data. The decision felt on the RFM-Segmentation, which will be summarized in the next part.


## 3.2 RFM Segmentation
### 3.1 Introduction

The RFM Segmentation is a popular and widely used segmentation method in marketing that relies only on three variables: (R) Last Activity (Recency); (F) Frequency Amount (Frequency); (M) Purchase Amount (Monetary). It provides a pragmatic approach to categorizing customers based on these variables. The dataset is divided in equally sized groups. The number of groups must be select in advance.

### 3.2 Segmentation with KMeans

### 3.3 Softmax Regression

# 4 Recommendation