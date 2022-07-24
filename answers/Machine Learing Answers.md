## Q1: Mention three ways to make your model robust to outliers?

## A1:
investigating outliers is often the first step in understanding how to treat them. Once you understand the nature of why the outliers occurred, there are several possible methods we can use:

* Add regularization: Reduces variance, For Eg L1 and L2 regularization.
* Try different models: Can use a model that is more robust to outliers. For Eg, tree-based models(random forests, gradient boosting) are generally less affected by outliers than linear models.
* Winsorize data: Winsorization is the process of replacing the extreme values of statistical data in order to limit the effect of the outliers on the calculations or the results obtained by using that data. We can cap the data at various arbitrary thresholds. For Eg, at a 90% winsorization, we can take the top and bottom 5% of values and set them to the 95th and 5th percentile of values respectively
* Transform data: For Eg, do a log transformation when the response variable follows an exponential distribution or is right skewed.
Change the error metric to be more robust: For Eg, for MSE, change it to MAE or Huber loss.
* Remove Outliers: Only do this if you're certain that the outliers are true anomalies not worth incorporating into the model. This should be the last consideration, since dropping data means losing information on the variability in the data.