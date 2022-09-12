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

# Canonicality
What is the ROBDD that represents all valid formulas?
- A: The 1 node!
- From [[Intro to Formal Reasoning]]: Formula is **valid** if it evaluates to TRUE under all assignments.
What is the ROBDD that represents all false formulas?
- A: The 0 node!
-  How can we check satisfiability?
	- If a 0 node does not exist, then it *must* be satisfiable!
	- Technically existence of a 1 node may or may not mean it's satisfiable... not sure. Look into this #todo 

## Time Complexity
No known polynomial algorithm

- In general, SAT checking is NP-hard!
- ROBDD construction is exponential time
- Determining whether ROBDD is satisfiable is constant time!

