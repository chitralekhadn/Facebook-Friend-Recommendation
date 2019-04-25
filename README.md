## Problem Statement:
Given a directed social graph, have to predict missing links to recommend users (Link Prediction in graph)

## EDA:
1) Display a subgraph of nodes using networkx
2) Get a number of unique persons networkx
3) PLot a graph for number of followers for each p[erson.
4) plot a box plot and pdf , percentile for number of followers for each person.
5) Similarly, plot for number of people each person is following, both followers+following.

## For Classification:
6) Generated some edges which are present in graph for classification,Generated Bad links from graph which are not in graph and whose shortest path is greater than 2.
7) Split data for train and test, Removed edges from Graph and used as test data and after removing used that graph for creating features for Train and test data.
                                                   
### Featurization:
8) Calculate similarity features for both followees and followers like jaccard distance, cosine distance,preferential attachment,
9) Caculate ranking measures like page rank.PageRank computes a ranking of the nodes in the graph G based on the structure of the incoming links.
10) Calculate graph features like shortest path, getting weekly connected edges from graph, adar index,is person following back,                                                   
    katz centrality, hits score, 
11) Add set of features in dataframe.                                                   
12) Create SVD features for both source and destination 
13) Calculate weight features like 
weight of incoming edges
weight of outgoing edges
weight of incoming edges + weight of outgoing edges
weight of incoming edges * weight of outgoing edges
2*weight of incoming edges + weight of outgoing edges
weight of incoming edges + 2*weight of outgoing edges 

## Models 
14) Hyperparameter tunning for random forest classifier and train a model on best parameters 
15) Get f1 score and feature iportance, plot confusion matrix..                                                   
Train f1 score 0.9642664714792561
Test f1 score 0.9252861426701018   
16) Similarly for XGBoost Classifier  
Train f1 score 0.97975431064889
Test f1 score 0.9274423919253475
17) XGBoost Clssifier giving slightly more performace than random forest classifier,  
18) hubs_s and page rank are in top fatures for random forest and its are not in top for XGBoost.
