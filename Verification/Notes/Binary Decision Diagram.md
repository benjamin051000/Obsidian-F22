# Binary Decision Diagram (BDD)
A BDD on a given set of propositional variables V is a rooted, directed acyclic graph, where
- 1-2 terminal nodes of out-degree 0 labeled 0 or 1,
- A set of variable nodes u of out-degree 2.
	- Two outgoing edges given by functions *low(u)* and *high(u)*.
		- In images, shown as dotted lines
	- A variable *var(u)* 

We are no longer bounded by the [[DPLL and CNF]] rules! (Specifically, CNF)

![[BDD_example.png]]

Feels intuitive, but bloated and brute-force

# Reduced Ordered BDD
Can we represent a BDD with no redundancy?

A canonical BDD:
- Two equivalent formulas have the same ROBDD even if they have different BDDs
	- e.g., two formulas that both simplify to the same thing

## Reduction Rules
1. Merge terminal nodes into two nodes "0" and "1".
	- This will make it look like a graph:
		- Each terminal node becomes a link to either 0 or 1, which are now the only two terminal nodes
	- Basically, combine redundant terminal nodes
1. Merge isomorphic subtrees.
	- Subtrees are isomorphic if their *low()* s and *high()* s are the same.
	- Dr. Yavuz said they are isomorphic if their root is at the same level
2. Remove redundant nodes
	- If a node low and high goes to the same node, remove it
		- It doesn't contribute in this path

