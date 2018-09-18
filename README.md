# Sentiment-Analysis
Sentiment classification of movie reviews using decision trees and forests

# Decisions Trees and Forests
Implementing the ID3 decision tree algorithm. The goal is to predict the sentiment of a movie review.
Used the Large Movie Review Dataset from Stanford for running our experiments. The core dataset 
contains 50,000 reviews split into train and test sets. This is a large dataset and therefore to make
it easier to handle, we will only work with a random subset of 1000 instances from the dataset. We will 
use the labeledBow.feat files in the train and test directories of the dataset.Each line in the file 
refers to a single review. The first entry in the line is the rating of the review on a scale of 1-10. 
We will also consider positive reviews to have ratings >= 7 and negative reviews to have a rating <= 4.

The important step of the ID3 algorithm involves choosing an attribute for creating the decision
function at every node in the decision tree. Use information gain as the measure to select the best
attribute for splitting a node.
1. Create a training set containing a random sample of 1000 observations, and a test set
containing the 1000 instances from the train and test directories. Ensure that there are equal
number of positive and negative instances in both the train and test sets. We will sample the
data points at random to obtain our mini train and test sets only once. This random subset will
then be used to run all the experiments. This way, we will be able to perform experiments that
can be reproduced with the same sample.
2. Use the training set to learn a decision tree. Discuss the statistics of the learned tree, for
example, effect of early stopping on the number of terminal nodes, effect of early stopping on
the prediction accuracy on the training dataset and the left out test dataset, attributes that are
most frequently used as split functions in the internal nodes of the tree, etc.
3. Let us add some noise to the dataset and observe its effect on the decision tree. Add 0.5, 1, 5
and 10% noise to the dataset. You can add this noise by randomly switching the label of a
proportion of data points. Construct the decision tree for each noise setting and quantify the
complexity of the learned decision tree using the number of nodes in the tree. Document and
discuss your observations about the quality of the model learned under these noise conditions.
4. Produce a pruned tree corresponding to the optimal tree size by computing the prediction
accuracy on the test set. Use a post-pruning strategy to prune the tree that has been learned
without applying any early stopping criteria. Document the change in the prediction accuracy
as a function of pruning (reduction in the number of nodes or rules/clauses obtained from the
tree).
5. Learn a decision forest that uses feature bagging. Use majority voting for predicting the label
for a test data point. Study the effect of number of trees in the forest on the prediction accuracy
of the test data set.

# Reference
[1] Andrew L. Maas, Raymond E. Daly, Peter T. Pham, Dan Huang, Andrew Y. Ng, and Christopher
Potts. (2011). Learning Word Vectors for Sentiment Analysis. The 49th Annual Meeting of the
Association for Computational Linguistics (ACL 2011).
[2] http://ai.stanford.edu/~amaas/data/sentiment/index.html
