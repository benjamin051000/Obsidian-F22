1. SVMs
1.   
    1.  E_n is the slack variable, which controls the amount of softening the SVM tolerates, or the degree to which data points are allowed to lie within the margin.
    2.  w is the weight coefficient vector which creates a hyperplane that linearly separates the classes.
    3.  The first constraint listed states that the classification (t*y(x)) will lie on the correct side of the hyperplane (1-E_n). In soft-margin SVMs, the 1-E allows for points to be correctly classified but within the margin.
    4.  The second constraint ensures the slack variable for each data point is positive. If it was 0 or negative, points would not be able to be correctly classified and within the margin.

| Trend    | SVM Decision Surface | Performance | Num. support vectors |
| -------- | -------------------- | ----------- | -------------------- |
| C -> inf | Tighter margin       | Better      | Less                 |
| C -> 0   | Wider margin         | Worse       | More                     |

2. SVM vs Logit
1. 
	1. The SVM finds a decision surface by finding a hyperplane which linearly separates the two classes. It may use a kernel trick to work in a higher-dimensional space if the data is not apparently linear. It attempts to maximize the distance of each data point to the line, which is called the margin. Some points will touch the margin, which are then called support vectors.
	2. The logistic regression utilizes a function that classifies based off whether the output is above or below a particular threshold, called the sigmoid function.
2.  SVMs are better when there are a small number of features and a large number of data points. Logit is better when there are many features but not as much data.
   
3. chart
A. Random Forest: Shows vertical/horizontal cuts

B. Decision Tree: vertical/horizontal cuts but with overfitting

C. RBF SVM: Groups the data points properly in all cases, indicating use of a non-linear kernel in the solution.

D. Linear SVM: It always draws linear solutions, but the non-linear data (2nd row) gets a terrible solution because of this.

E. Adaboost: Process of elimination

F. Logistic regression: Always draws linear solutions, but does better in 2nd row than SVM.

4. Curse of dimensionality stuff
	1. The volume of the crust converges to infinity.
	2.  The curse of dimensionality
	3.  This is an important isssue in ML because as dimensions of our data set increases, it becomes more and more difficult to obtain samples near the mean of the data.
	4. #todo What strategies can we apply when features are uncorrelated and when features are strongly correlated.
5. 
	Feature selection is a good choice for dimensionality reduction when there are several features that contribute a lot of variance to the result. Using a process such as RFE allows a model to remove features that don't contribute much to the result. Feature extraction, on the other hand, is useful when there are many features that are not directly or easily comparable, like images. PCA is a useful tool to take data and extract new "features" to improve its variance.

6. During lecture we discussed the Recursive Feature Elimination (RFE) algorithm for feature selection. Suppose that instead of eliminating features from a pre-defined set of available features, you want to incrementally select one feature at a time to identify the subset that optimizes some performance measure. This algorithm is known as Forward Feature Selection.
	Provide the pseudo-code (list of steps) to implement the Forward Feature Selection algorithm.
	
> procedure getBestFeature()
> 
>     for feature in all unused features:  
>         train model with this feature only
> 
>         score trained model
> 
>     return  feature with highest score  
> 
> for feature in max(N, number of features):  
>     used features += getBestFeature()
	

7. Suppose you would like to use PCA to reduce dimensionality of your data prior to classification. Is PCA always an effective dimensionality reduction technique to be used in conjunction with classification? Why or why not?

/backup

8. MDS/ISOMAP/LLE
