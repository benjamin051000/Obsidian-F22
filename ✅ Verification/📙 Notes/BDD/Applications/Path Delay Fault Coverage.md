- Many paths in circuits
- Ideally, cover as many unique paths as possible when validating a circuit
- Assume:
	- Each path is represented with a unique ID
	- We know max num. paths = N

# Using a [[BDD, ROBDD]] as a Set
Given a minterm, set membership can be checked by following the path from root -> leaf
- If leaf node = 1, minterm is a member
- If leaf node = 0, not a member

