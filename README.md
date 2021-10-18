# Gulraiz00-Classification_with_Logistic_Regression

**
The Dataset¶**

The dataset contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions. It contains only numerical input variables which are the result of a PCA transformation. Unfortu- nately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, ... V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are ‘Time’ and ‘Amount’. [You will learn about PCA in a later Lesson.] Feature ‘Time’ contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature ‘Amount’ is the transac- tion Amount. Feature ‘Class’ is the response variable and it takes value 1 in case of fraud and 0 otherwise.


<br>
**Part 1:**

Read in the creditcard.csv dataset and display the first 5 rows


**Part 2:**


Then split the data into train and test for the outcome/response and the predictor variables. Hold out 50% of observations as the test set. Pass random_state=0 to train_test_split to ensure you get the same train and tests sets as the solution.


**Part 3:**


Read the documentation for sklearn’s LogisticRegression. In no more than 2 sentences per bullet point, answer the following in your own words.
<br>
• Does LogisticRegression use a penalty by default? If yes, what penalty?

YOUR ANSWER HERE:
<br>
• If we apply a penalty during learning, what difference do you expect to see in the resulting coeﬀicients, relative to not applying a penalty during learning?
<br>
YOUR ANSWER HERE:
<br>
• If using the default settings of LogisticRegression in sklearn, should you include a column of 1s in your feature/design matrix? Briefly explain why or why not.
<br>
YOUR ANSWER HERE: 

**Part 4:**

Create a instance of sklearn’s LogisticRegression object for unpenalized logistic regression. Note: If you get a warning about convergence of coef_, try increasing the max_iter parameter. I used max_iter=10000 which seems to supress the warning.
Using this object, run a logisitic regression analysis of Class (y-variable) against Amount (x-variable) using your training data.
Then make a plot with three main components based on the analysis: 1. Scatter-plot of Amount and Outcome on your test data 2. A curve showing the prediction (0 or 1, using predict - this curve will jump between 0 and 1) as a function of Amount 3. A curve showing the predicted probability of a positive outcome (using predict_proba) as a function of Amount. Note that predict_proba will return both p(Outcome=0) and p(Outcome=1) in an array.


**Part 5:**

Compute the label-based criteria we discussed in the Lesson for your amount-only classifier using the test data. Use a threshold of 0.5. Answer the questions in this text box below.
<br>
• How many of the test instances are labeled positive by your classifier?
<br>
YOUR ANSWER HERE: 
<br>
• Choose one of the positively-labeled test instances, and explain why the classifier labeled it positive.
<br>
YOUR ANSWER HERE:
<br>
• Is this classifier useful for finding fraudulent transactions? Explain in one or two sentences.
<br>
YOUR ANSWER HERE: 

**Part 6:**

Now fit a logistic regression model to the training data and include all the variables in the data frame (except for Class) in the cell below. You will want to make a new object like you did for the simpler model.
<br>
Answer the following question.
<br>
• According to this more complex model, are larger or smaller Amounts more strongly associ- ated with fraud, if all other variables are held equal?
<br>
YOUR ANSWER HERE:

**Part 7:**

In the cell below, Compute the label-based criteria we discussed in the Lesson for new classifier using the test data. (You don’t have to copy the function down into this cell; just call it again here.) Use a threshold of 0.5. Answer the questions in this text box below.
<br>
• How many of the test instances are labeled positive by your classifier?
<br>
YOUR ANSWER:
<br>
• Is this classifier better or worse than the amount-only classifier for finding fraudulent transactions? Explain in one or two sentences.
<br>
YOUR ANSWER:
 
 **Part 8**

Plot ROC curves for both of your classifiers using the cells below, then answer the following ques- tions, computing whatever quantities you need to answer them.
• Which classifier has a higher estimated probability of correctly distinguishing between a positive and a negative instance? How do you know?
<br>
YOUR ANSWER:
<br>
• How could you explain a result where a logistic regression classifier produces an AUROC that is “worse than random”, i.e. less than 0.5, even on its training set?
<br>
YOUR ANSWER:

**Part 9:**

Plot precision-recall curves for both of your classifiers using the cell below. Be sure to label your axes.
<br>
• Which classifier is preferable if we want to recover at least 60% of fraudulent transactions?
<br>
YOUR ANSWER:

