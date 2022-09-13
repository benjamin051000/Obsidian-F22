# Models
## Overfitting
1. Add more data
	1. Assuming you *have* more data.
2. Apply cross-validation


## Cross-Validation
Experimental design via cross-validation
Can do it once, or multiple times

Data:
- 80% Training
	- Train set
	- Validation set
- 20% Test

### K-fold
Divide training data into *k* folds.
(4 equally-sized chunks)

- Train with 3 of them, use the 4th as validation
- Then, rotate
	- For example, given sets a, b, c, d
	- Training 1: Train with {a, b, c}, validate with {d}
	- Training 2: Train with {b, c, d}, validate with {a}
	- etc.

#### Calculate error
Either:
- Take the average performance for validation
- Take maximum error (we are minimizing it via training)


# Linear Regression, Hyperparameters
$$y=\omega_0+\sum_{j=1}^{M}\omega_j f_j$$
Here, $M$ is a hyperparameter!
M = number of features
- user-defined

Will be n-polynomial:
- M=1 is a horizontal line
- M=2 is a line with nonzero slope
- M=3 is parabola,
- etc.

![[lin reg formulas.png]]

![[train vs val MSE.png]]

In the beginning, the model is simple and generalizing well, so the validation error decreases.
Later, it starts overfitting so validation error increases.

- Underfitting: $0 < M^*$
- Overfitting: $M^* < \infty$
- Ideal: $M^*$


# Overfitting
Model attempts to do crazy stuff to minimize error.
- Example: 10-term polynomial

## Options for overfitting
- Add more data
- Cross-validation
- Ensemble learning
- [[Occam's Razor]]
