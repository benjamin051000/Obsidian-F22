# Regularization
Helps solve [[Overfitting]]

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

# Tradeoffs
- Ridge
	- Forces param values to be small but not 0
	- Highly affected by outliers
- Lasso
	- Promotes sparsisty
	- Not as affected by outliers
- Elastic net
	- Requires fine tuning of an extra hyperparameter

# Which to use?
- Ridge is a good default
- If you suspect only a few features are actually useful, use Lasso/Elastic Net
- In general, Elastic Net is preferred over Lasso since Lasso may behave erratically when the number of features is greater than the number of training instances or when several features are strongly correlated.

