# Donor_Choose
Various machine-learning algorithms are applied on donor-choose data set. k-NN, logistic regression, Naive Bayes, SVM (support vector machine), decision tree, some ensemble model (like Random Forest and gradient boosting decisiont tree). Files naming is done as per the process that have been done.

## EDA_TSNE.ipynb
The file "EDA_TSNE.ipynb" contains exploratory-data-analysi and T-SNE plots. T-SNE plots are used to visualize high dimension data into lower dimension data. 

Other files are named as "model_name.ipynb". Here "model_name" can be k-NN, Naive Bayes, Logistic Regression, support vector machine, Decision Tree, Random Forest etc. If file name is 'k-NN.ipynb' then this file is related to how the k-NN is perfomed on Donor-choose dataset, what is the performance of k-NN model on this data. 

## Clustering.ipynb
Various clustering models like K-Means, hierarichal clustering and DBSCAN are applied on this dataset. This is unsupervised learning scheme (means no labeled data). Different clusters are made and randomly few datapoints are picked from clusters and found the polarity of each cluster.

## TruncatedSVD.ipynb
SVD is implemented on this data. Found the best the model and vectorizer (which resulted in best AUC value) from applied models. Found the top 2k features of that model was selected and made co-occurence matrix was created with window widht = 5 using top 2k features.

## Co-occurence Matrix (C)
let's say we've corpus = ["abc def ijk pqr", "pqr klm opq", "lmn pqr xyz abc def pqr abc"] and we want to create and co-occurence matrix with window width = 2 with top words as ["abc", "pqr","def"], then this is how it'll look like:

|   |abc|pqr|def|  
|---|---|---|---|
|abc| 0 | 3 | 3 |
|pqr| 3 | 0 | 2 |
|def| 3 | 2 | 0 |

Diagonal elements will be set to 0. For non-diagonal element C<sub>ij</sub> (where i ≠ j) means how many times word *i* occurs around word *j* in window width = 2 (both side).
