# Quantifying-Hyperarousal
Quantifying hyperarousal using massive dataset compiled by the University of Houston, as a part of the University of Houston Computer science REU program. 

The supervised learning file contains the results of applying some basic supervised methods (GradientBoost, RandomForest, etc.) on the data; particularly, to predict heart rate. Heart rate was normalized by finding the baseline heart rate of each individual when not driving. 

The Cross-Modality Markov Network file first builds a graph between features such that every edge is weighted by the mutual spearman p-value between the features and applies the Louvain community detection algorithm 1000 times to find communities. Then, it creates a Markov network based on an estimated inverse covariance matrix found using Graphical Lasso. A lot of the heart rate data in the file was originally NaNs, so I used a random forest model with R-square score of 0.86 to predict those missing values based on the remaining data. 
