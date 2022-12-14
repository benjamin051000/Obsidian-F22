[[Support Vector Machines]] transform data into infinite-dimensional spaces. That is difficult to compute.

- Kernel trick reduces an infinitely dimensional space into a similarity measure in a finite space.

- Basically, how similar are two points in infinite dimensions without actually having to go there?

- It will achieve this by taking inner products of vectors
$$\phi:\mathbb{R}^N \rightarrow \mathbb{R}^\infty$$

This only works if you pick the right $\phi$ function, not all $\phi$ functions work for this.


# Radial Basis Kernel
## aka RBF
Projects data into an infinite-dimensional space. In infinite dimensions, we are guaranteed to have a hyperplane that separates features.

$$K_{RBF}: \mathbb{R}^\infty \times \mathbb{R}^\infty \rightarrow \mathbb{R}, (x, y) |-> e^{-\gamma||x-y||^2} $$

As gamma increases, the more similar two points are viewed.

Scikit-learn uses this kernel by default

## Overfitting
If we are guaranteed to have a hyperplane that separates features, [[Overfitting]] becomes a big issue.

$$\phi_{RBF}: \mathbb{R}^D \rightarrow \mathbb{R}^\infty$$
She showed an example where the data was linearly separable, but the model fit a non-linear curve, which is a red flag that it is overfitting.

