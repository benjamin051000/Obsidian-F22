# Implication Graphs
- Illustrates steps of Boolean Constraint Propagation (see [[DPLL and CNF]])
-  Nodes: Assignments to literals
- Edges: Order of assignment decisions
- Conflict clauses are denoted with $\kappa$
	- If $\kappa$ exists, BCP returns "conflict"
- Conflict nodes help us learn the mistakes we made in the assignment process
	- Don't make the same mistake again!

## Block conflicts
- Apply Binary Resolution Rule to the antecedent labeling the edges on the path from $\kappa$ to the root
- Infer the *asserting clause*

### Binary Resolution Rule
$$\frac{(a_1\lor ... \lor a_n \lor \beta)(b_1 \lor ... \lor b_m \lor \lnot \beta)}{(a_1 \lor ... \lor a_n \lor b_1 \lor ... \lor b_m)}$$

Appears to remove the $\beta$ conflict!

# Unique Implication Point
Given a partial conflict graph corresponding to the decision level of the conflict, UIP is
- Any node
- Not conflict node
- Node which is on all paths from decision -> conflict

- Decision node itself is a UIP
- UIP closest to conflict node is the *first UIP*.

## When to stop applying the resolution rule?
Empirical studies show:
- Good strategy for stopping criterion is to return TRUE iff the clause contains:
- Negation of first UIP as its single literal at current decision level
- Negated literal becomes asserted immediately after backtracking
