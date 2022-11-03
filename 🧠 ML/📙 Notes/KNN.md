# K-Nearest Neighbors
- Non-parametric classifier
- "Lazy" algorithm
	- Does not have a standard training stage
	- Like being on the dancefloor, you join but you don't have the moves
		- Copy your neighbors!
- K is a hyperparameter

## Tie breaking
Options:
- Pick label of closest neighbor
- Randomly choose
- Choice that minimizes risk
- Pick based on relative frequency of each class
	- In the case of imbalanced data, pick class that is least represented
