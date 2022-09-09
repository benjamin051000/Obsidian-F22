# Binary Decision Diagram (BDD)
A BDD on a given set of propositional variables V is a rooted, directed acyclic graph, where
- 1-2 terminal nodes of out-degree 0 labeled 0 or 1,
- A set of variable nodes u of out-degree 2.
	- Two outgoing edges given by functions *low(u)* and *high(u)*.
		- In images, shown as dotted lines
	- A variable *var(u)* 

We are no longer bounded by the [[DPLL and CNF]] rules! (Specifically, CNF)

![[BDD_example.png]]

Feels intuitive, but bloated (for lack of a better word)

# Reduced Ordered BDD
Can we represent a BDD with no redundancy?

A canonical BDD:
- Two equivalent formulas have the same ROBDD even if they have different BDDs
	- e.g., two formulas that both simplify to the same thing

## Reduction Rules
1. Merge terminal nodes into two nodes "0" and "1"
2. 