# EDA
## 2-bit full adder
![[Pasted image 20220921105146.png]]

$$ sum = x \oplus y $$
$$ c_o = (c_i \land (x \oplus y)) \lor (x \land y )  $$
- Interpret circuit as a Directed Acyclic Graph (DAG)
- Traverse the graph to determine the boolean functions


## Create specification
Use a truth table to come up with a [[BDD, ROBDD]] 
Use a truth table to determine the outputs (she used [[Minterm, Maxterm]] s)

Now, check if someone's circuit is correct.

## Verify a new circuit
Check if two BDDs have the same root node
- Assuming they have been constructed using the same variable ordering
- This is due to canonicity!
