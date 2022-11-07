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
   

4. Curse of dimensionality stuff
	1. The volume of the crust converges to infinity.
	2.  The curse of dimensionality
	3.  This is an important isssue in ML because as dimensions of our data set increases, it becomes more and more difficult to obtain samples near the mean of the data.
	4. #todo What strategies can we apply when features are uncorrelated and when features are strongly correlated.
5. Write a paragraph (at least 200 words) discussing in what circumstances you would prefer to use feature selection over feature extraction. Explain your reasoning and provide examples.

	