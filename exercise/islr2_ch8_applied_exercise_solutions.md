solutioins to the applied exercises in islr2 ch8
================
Wenwen Kong
9/3/2022

### Problem 7

In the lab, we applied random forests to the `Boston` data using
`mtry = 6` and using `ntree = 25` and `ntree = 500`. Create a plot
displaying the test error resulting from random forests on this data set
for a more comprehensive range of values for `mtry` and `ntree`. You can
model your plot after Figure 8.10. Describe the results obtained.

### Problem 8

In the lab, a classification tree was applied to the `Carseats` data set
after converting `Sales` into a qualitative response variable. Now we
will seek to predict `Sales` using regression trees and related
approaches, treating the response as a quantitative variable.

1)  Split the data set into a training set and a test set.

2)  Fit a regression tree to the training set. Plot the tree, and
    interpret the results. What test
    ![MSE](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;MSE "MSE")
    do you obtain?

3)  Use cross-validation in order to determine the optimal level of tree
    complexity. Does pruning the tree improve the test
    ![MSE](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;MSE "MSE")?

4)  Use the bagging approach in order to analyze this data. What test
    ![MSE](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;MSE "MSE")
    do you obtain? Use the `importance()` function to determine which
    variables are most important.

5)  Use random forests to analyze this data. What test
    ![MSE](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;MSE "MSE")
    do you obtain? Use the `importance()` function to determine which
    variables are most important. Describe the effect of
    ![m](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;m "m"),
    the number of variables considered at each split, on the error rate
    obtained.

6)  Now analyze the data using
    ![BART](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;BART "BART"),
    and report your results.

### Problem 9

This problem involves the `OJ` data set which is part of the `ISLR2`
package.

1)  Create a training set containing a random sample of 800
    observations, and a test set containing the remaining observations.

2)  Fit a tree to the training data, with `Purchase` as the response and
    the other variables as perdictors. Use the `summary()` function to
    produce summary statistics about the tree, and describe the results
    obtained. What is the training error rate? How many terminal nodes
    does the tree have?

3)  Type in the name of the tree object in order to get a detailed text
    output. Pick one of the terminal nodes, and interpret the
    information displayed.

4)  Create a plot of the tree, and interpret the results.

5)  Predict the response on the test data, and produce a confusion
    matrix comparing the test labels to the predicted test labels. What
    is the test error rate?

6)  Apply the `cv.tree()` function to the training set in order to
    determine the optimal tree size.

7)  Produce a plot with tree size on the
    ![x](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;x "x")-axis
    and cross-validated classification error rate on the
    ![y](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;y "y")-axis.

8)  Which tree size corresponds to the lowest cross-validated
    classification error rate?

9)  Produce a pruned tree corresponding to the optimal tree size
    obtained using cross-validation. If cross-validation does not lead
    to selection of a pruned tree, then create a pruned tree with five
    terminal nodes.

10) Compare the training error rates between the pruned and unpruned
    trees. Which is higher?

11) Compare the test error rates between the pruned and unpruned trees.
    Which is higher?

### Problem 10

We now use boosting to predict `Salary` in the `Hitters` data set.

1)  Remove the observations for whom the salary information is unknown,
    and then log-transform the salaries.

2)  Create a training set consisting of the first 200 observations, and
    a test set consisting of the remaining observations.

3)  Perform boosting on the training set with 1,000 trees for a range of
    values of the shrinkage parameter
    ![\lambda](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;%5Clambda "\lambda").
    Produce a plot with different shrinkage values on the
    ![x](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;x "x")-axis
    and the corresponding traning set
    ![MSE](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;MSE "MSE")
    on the
    ![y](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;y "y")-axis.

4)  Produce a plot with different shrinkage values on the
    ![x](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;x "x")-axis
    and the corresponding test set
    ![MSE](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;MSE "MSE")
    on the
    ![y](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;y "y")-axis.

5)  Compare the test
    ![MSE](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;MSE "MSE")
    of boosting to the test
    ![MSE](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;MSE "MSE")
    that results from applying two of the regression approaches seen in
    Chapters 3 and 6.

6)  Which variables appear to be the most important predictors in the
    boosted model?

7)  Now apply bagging to the training set. What is the test set
    ![MSE](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;MSE "MSE")
    for this approach?

### Problem 11

This question uses the `Caravan` data set.

1)  Create a training set consisting of the first 1,000 observations,
    and a test set consisting of the remaining observations.

2)  Fit a boosting model to the training set with `Purchase` as the
    response and the other variables as predictors. Use 1,000 trees, and
    a shrinkage value of 0.01. Which predictors appear to be the most
    important?

3)  Use the boosting model to predict the response on the test data.
    Predict that a person will make a purchase if the estimated
    probability of purchase is greater than
    ![20\\%](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;20%5C%25 "20\%").
    Form a confusion matrix. What fraction of the people predicted to
    make a purchase do in fact make one? How does this compare with the
    results obtained from applying
    ![KNN](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;KNN "KNN")
    or logistic regression to this data set?

### Problem 12

Apply boosting, bagging, random forests, and
![BART](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;BART "BART")
to a data set of your choice. Be sure to fit the models on a training
set and to evaluate their performance on a test set. How accurate are
the results compared to simple methods like linear or logistic
regression? Which of these approaches yields the best performance?
