- Uses a learning rate to descend down an error surface

## Types
- Stochastic Gradient Descent (AKA Online Learning)
	- Uses a single (misclassified) sample to make corrections to $w$ and $w_0$.  
	- Typically much noisier
	
- Batch learning
	- Uses an "average gradient"
	- Solution converges much more slowly but is more accurate

## Update Equations
$$w^{(t+1)}\leftarrow w^t + y \cdot x_m \cdot t_m$$
$$w_0^{(t+1)} \leftarrow $$


# NN vs Logit
- NN only cares about misclassified samples
- Logit evalutes all probabilities
