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
The process of finding an optimal solution started with the question of wether natural clusters could be identified within the data. Therefore two cluster methods were used: Hierarchical Clustering and DBSCAN. The methods were chosen because of the mixed data types, the data contains - i.e. nominal, ordinal and metric data. Other clustering methods can not handle mixed data types. The popular K-Means algorithm is not suitable for categorical data, because it uses euclidean distance to measure the distance between the data points and assume therefore continuous values. K-Modes and K-Prototype are also not suitable for clustering this type of data. They can handle only continuous and/or nominal data, but not ordinal data. Hierarchical Clustering and DBSCAN can use precomputed distance matrices as a metric method. For this reason the gower distance were computed and was set as a precomputed metric into the cluster algorithms. Moreover, algorithm like K-Means or K-Modes do not support precomputed matrices as input.


# 4 Recommendation