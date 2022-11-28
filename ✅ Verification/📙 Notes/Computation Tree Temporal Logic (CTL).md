---
powerpoint: ctl.pdf
---
![[Pasted image 20221127214409.png]]
- Most real-world sw/hw systems are reactive rather than transformative
	- Transformative: Receives input, generates output
	- Reactive: Responds to events from environment, usually never terminates
- Reactive systems need:
	- Ordering of events
	- Properties of events and responses

CTL is an alternative to [[LTL]]
- Lots of similarities

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
- Primary difference with LTL is the addition of quantifiers

# Semantics
![[Pasted image 20221127173805.png]]

- A computation tree rooted at a state *s* satisfies *p* means $s \models p$
- In the example above, $a \lor b$ is satisfied, but $c \land d$ is not, because the computation tree rooted at $s_0$ represents that state.

What about $AXp$ and $EXp$?
- $AXp$: All computation trees rooted at the successors of $s$ satisfy $p$.
- $EXp$: Some comp trees rooted at a successor of $s$ satisfy $p$.


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
- Transition relation: $R \equiv t_1 \lor t_2 \lor ... \lor t_7$ 

## Symbolic Manipulation of Transition Systems
To solve the model checking problem symbolically, we need to define symbolic equivalents of:
- Checking if a state is a member of a set of states
- Finding predecessors of a state
- Finding successors of a state
- Iterating over transition relation

### Checking membership
- Same logic is used to represent single state as well as set of states
- Logical implication operator $\rightarrow$ is used

- In simple example above, is $s_1$ an initial state?
	- Can be answered by checking if $s_1 \rightarrow s_0$.

### Finding predecessors
- Given a transition relation $R$ and a state $s$, $Pre[R](s)$ finds predecessors of $s$ in $R$.
	- Let $V(V')$ denote *current (next)* state variables used to define $R$.
	- $Pre[R](s) \equiv \exists V'.R \land s'$

### Finding successors
- $Post[R](s) \equiv (\exists V.R \land s)[V/V']$
- Where $\phi[X/Y]$ replaces all $Y$s with $X$s in $\phi$.

### Iterating over T
- With exception of *X*, all temporal operators require iteration to find set of states that satisfy the formula
- Use fixpoints


## Using Fixpoints in Symbolic model checking
- EX uses Pre operator
- EU uses least fixpoint algorithm
- EG uses greatest fixpoint algorithm

