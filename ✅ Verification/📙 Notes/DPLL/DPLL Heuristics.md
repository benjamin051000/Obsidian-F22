## Jeroslow-Wang
- Give higher priority to literals that appear frequently in short clauses
- More likely that you will get a unit clause sooner!
- Therefore, fewer variables to decide
## Dynamic Largest Individual Sum
- Choose literal that satisfies the most unsat clauses
- Several clauses get closer to being satisfied
## Variable State Independent Decaying Sums
- For each literal, count number of clauses it appears in (sat or unsat) and periodically divide the score by 2
- Basically, keep a weight for each literal equal to the number of clauses the literal appears in
	- Count both sat and unsat
- 