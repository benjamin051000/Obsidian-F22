# EDA
## 2-bit full adder
![[Pasted image 20220921105146.png]]

$$ sum = x \oplus y $$
$$ c_o = (c_i \land (x \oplus y)) \lor (x \land y )  $$
- Interpret circuit as a Directed Acyclic Graph (DAG)
- Traverse the graph to determine the boolean functions


## Create specification
Use a truth table to come up with a BDD
Use a truth table to determine the outputs (she used [[Minterm, Maxterm]] s)

Now, check if someone's circuit is correct.

