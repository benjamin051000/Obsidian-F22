In very high-dimensional space, all the samples are pushed to the corners of your input space.

- The ratio of "Crust" to "pizza as a whole" approaches just crust as dimensions get higher. (She showed an algebraic proof of this)
- She also demonstrated the Unit Porcupine, which is a unit hypersphere inside of a unit hypercube
- As Dimensions increase, the ratio of sphere to cube - sphere approaches 0
- Same thing with Gaussian distributions:
	- As D increases, you are more and more likely to sample from the tails rather than the mean.

- It's called a curse because we need features in order to make models

This class just became a meme... She just played Thriller laugh

# What can we do about this?
- Choose random features
- Choose only highly correlated features
- Lasso selects non-zero features
	- Doesn't work for Discriminative classifiers like [[Decision Trees]] or Random Forests

More formally:
- Feature selection
	- Wrappers
		- Use a specific algorithm to make decisions
			- e.g., [[Logistic Regression]]
		- e.g., Recursive feature elimination
	- Filters
		- Pearson Correlation Coefficient
		- Embedded
			- Results may vary by model
			- Lasso [[Regularization]]
- Feature extraction
	- [[Principal Component Analysis]] (PCA)
	- [[Manifold Learning]]
