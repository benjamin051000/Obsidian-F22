# Decision Trees
- Solve classification and regression tasks
- Non-parametric
See xournal doc `decision_tree.xopp` for an example.

- Splitting nodes can be done with both *categorical* and *continuous* features
- `sklearn` will use a binary split in order to minimize search space
- Feature used to split a node:
	- One that *maximizes* information gain
- In classification, a **pure node** means the output results in a single class prediction
	- Does not exist in Regression tasks, since regression doesn't predict classes
		- For those, you pick a different objective function

# Information Gain
$$IG(D_p, f) = $$