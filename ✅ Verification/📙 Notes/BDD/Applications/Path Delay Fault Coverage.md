- Many paths in circuits
- Ideally, cover as many unique paths as possible when validating a circuit
- Assume:
	- Each path is represented with a unique ID
	- We know max num. paths = N

## Using a [[BDD, ROBDD]] as a Set
Given a minterm, set membership can be checked by following the path from root -> leaf
- If leaf node = 1, minterm is a member
- If leaf node = 0, not a member

Construct an ROBDD for covered paths, initialize it to an empty set
- Use `ceil(log(N))` variables
- While testing has not ended
	- Generate test for circuit
	- Find path ID for test
	- Convert path ID to corresponding minterm
	- Check if path is in set of covered paths
	- If not a member, add it to set of covered paths
- Compute size of set of covered paths

