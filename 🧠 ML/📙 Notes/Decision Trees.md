# Decision Trees
- Solve classification and regression tasks
- Non-parametric
See xournal doc `decision_tree.xopp` for an example.

- Splitting nodes can be done with both *categorical* and *continuous* features
- `sklearn` will use a binary split in order to minimize search space
- Feature used to split a node:
	- One that *maximizes* information gain
- In classification, a **pure node** means the output results in a single class prediction
	- In her 2-class example, the leaf node with only one class (20, 0) was pure
	- Does not exist in Regression tasks, since regression doesn't predict classes
		- For those, you pick a different objective function

# Information Gain
$$IG(D_p, f) = I(D_p) - \sum_{j=1}^m \frac{N_j}{N_p} *I(D_j)$$

Key:
![[Pasted image 20220922152849.png]]

## Binary splitting
Formula above is generalized to $m$ branches, but `sklearn` will use $m=2$ .

$$\therefore IG(D_p, f) = I(D_p) - \frac{N_{left}}{N_p} * I(D_{left}) - \frac{N_{right}}{N}*I(D_{right})$$

## Impurity measures:
### Entropy
$$I_H(t)=-\sum_{i=1}^c p(i | t) * log_2(p(i | t))*$$
t = node
c = num classes
p(i|t) = probability of class i under node t
	
### Gini Impurity
$$I_G(t) = 1 - \sum_{i=1}^c(p(i|t))^2$$
Gini is going to minimize probability of misclassification

### Classification Error
$$I_E(t) = 1 - max(p(i|t))$$
Not recommeneded because we can't grow the tree with it (what?)

*Useful when trying to prune the tree:*

- Branching out a ton leads to [[overfitting]]
- Use this to prune the tree which will constrain the model, prevent excessive branching

- Thus will return a simpler tree than the other impurity measures

Example:
![[2-class-example.png]]

She also hand-calculated Gini impurity
