- Most real-world sw/hw systems are reactive rather than transformative
	- Transformative: Receives input, generates output
	- Reactive: Responds to events from environment, usually never terminates
- Reactive systems need:
	- Ordering of events
	- Properties of events and responses

# Examples
- The services of a secure website cannot be used until a user logs in successfully.
- A user process preempted by another process eventually gets rescheduled by an OS.
- Any change on a document gets saved by word processing app.
- From any state, it is possible to get to the restart state.

# Syntax
CTL formula: $\phi$ 
- Defined in terms of **atoms** (atomic properties)
	- Temporal operators that are preceded by quantifiers
		- A for $\forall$ 
		- E for $\exists$ 
	- boolean connectives
![[Pasted image 20221127171344.png]]
- Just like in [[LTL]], 
	- X: next
	- G: always
	- F: eventually
	- U: until

# Semantics
- A computation tree rooted at a state *s* satisfies *p* means $s \models p$

# Dualities
![[Pasted image 20221127171703.png]]

# CTL [[Model Checking]]
- Given a transition system $T=(S,S_0,R,L)$ and a CTL formula $\phi$, decide whether all initial states satisfy $\phi$.
	- i.e., $\forall s_0 \in S_0.s_0 \models \phi$.
- To Check whether a state satisfies a CTL formula, we need to check whether the computation tree rooted at that state satisfies the CTL formula.

## Explicit State CTL Model Checking
- May employ algorithm for finding strongly connected components (SCCs) in a graph, where
	- nodes = states of transition system
	- edges = transitions
- Tarjan'a algorithm for finnding SCCs runs in O(V+E)
	- V = number of nodes
	- E = number of edges

## Symbolic CTL Model Checking
- Explicit approach represents each individual state of $T$ separately  
- Symbolic approach encodes $T$ using logical formula
- Potentially achieves a more compact representation
	- All states including initial are encoded using logical formula
	- Compact representations for logical formula,e.g., BDDs, can further improve symbolic approaches
- Simple example of encoding:
![[Pasted image 20221127173805.png]]
- $R \equiv t_1 \lor t_2 \lor ... \lor t_7$ 

## Symbolic Manipulation of Transition Systems
To solve the model checking problem symbolically, we need to define symbolic equivalents of:
- Checking if a state is a member of a set of states
- Finding predecessors of a state
- Finding successors of a state
- Iterating over transition relation
