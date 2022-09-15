One solution to avoid [[Overfitting]]

# Ridge Regularizer
TODO take notes about these

# Lasso Regularizer
- Drives coefficients towards 0 much quicker than ridge
- Drives coeffs to exactly 0
	- Creates a sparse vector
	- Therefore, will end up excluding features
	- This is a form of Feature Selection
![[Pasted image 20220913142927.png]]


# Elastic Net
Middle ground between Ridge and Lasso

Extra hyperparam $\beta$ to mix ridge and lasso

