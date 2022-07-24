## Q1: Mention three ways to make your model robust to outliers?

## A1:
investigating outliers is often the first step in understanding how to treat them. Once you understand the nature of why the outliers occurred, there are several possible methods we can use:

* Add regularization: Reduces variance, For Eg L1 and L2 regularization.
* Try different models: Can use a model that is more robust to outliers. For Eg, tree-based models(random forests, gradient boosting) are generally less affected by outliers than linear models.
* Winsorize data: Winsorization is the process of replacing the extreme values of statistical data in order to limit the effect of the outliers on the calculations or the results obtained by using that data. We can cap the data at various arbitrary thresholds. For Eg, at a 90% winsorization, we can take the top and bottom 5% of values and set them to the 95th and 5th percentile of values respectively
* Transform data: For Eg, do a log transformation when the response variable follows an exponential distribution or is right skewed.
Change the error metric to be more robust: For Eg, for MSE, change it to MAE or Huber loss.
* Remove Outliers: Only do this if you're certain that the outliers are true anomalies not worth incorporating into the model. This should be the last consideration, since dropping data means losing information on the variability in the data.


## Q2: Describe the motivation behind random forests and mention two reasons why they are better than individual decision trees?
 
 The motivation behind random forest or ensemble models can be explained easily by using the following example: Let’s say we have a question to solve. We gather 100 people, ask each of them this question, and record their answers. After we combine all the replies we have received, we will discover that the aggregated collective opinion will be close to the actual solution to the problem. This is known as the “Wisdom of the crowd” which is, in fact, the motivation behind random forests. We take weak learners (ML models) specifically, decision trees in the case of random forest, and aggregate their results to get good predictions by removing dependency on a particular set of features. In regression, we take the mean and for classification, we take the majority vote of the classifiers.

Generally, you should note that no algorithm is better than the other. It always depends on the case and the dataset used . Still, there are reasons why random forests often allow for stronger prediction than individual decision trees:

* Decision trees are prone to overfit whereas random forest generalizes better on unseen data as it uses randomness in feature selection and during sampling of the data. Therefore, random forests have lower variance compared to that of the decision tree without substantially increasing the error due to bias.
* Generally, ensemble models like random forests perform better as they are aggregations of various models (decision trees in the case of a random forest), using the concept of the “Wisdom of the crowd.”