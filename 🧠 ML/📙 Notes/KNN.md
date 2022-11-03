# K-Nearest Neighbors
- Non-parametric classifier
- "Lazy" algorithm
	- Does not have a standard training stage
	- Like being on the dancefloor, you join but you don't have the moves
		- Copy your neighbors!
- K is a hyperparameter

# Tie breaking
Options:
- Pick label of closest neighbor
- Randomly choose
- Choice that minimizes risk
- Pick based on relative frequency of each class
	- In the case of imbalanced data, pick class that is least represented

## Weighted KNN
- Voting scheme weighted by distance
$$score=1/d_i$$
- Whichever class scores highest becomes the classification
- Sensitive to outliers
- More prone to [[overfitting]]

- Sometimes gets "islands" where outliers lie

# Tuning Issues
KNN is non-parametric
- no mapper function
- cannot use standard [[Regularization]] terms

# Other observations
- KNN is sensitive to the [[curse of dimensionality]]
	- Works in high dimensions *if* you keep your num neighbors small.
		- With small k values, manifold is approximately linear.
