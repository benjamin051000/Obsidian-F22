# Conjunctive Normal Form
CNF uses clauses:
$$ (l_i \lor l_j \lor ...) \land (l_m \lor l_k \lor ...) $$
Clauses are ANDed together

# DPLL
Solver that tries to find if each clause is true

If it detects a conflict, it backtracks to try something else

Process can be viewed as a binary tree
- Internal nodes are partial assignments
- leaves are full assignments

Each decision is associated with a decision level (starts at 1). Level 0 represents ground level at which decisions for clauses with a single literal are made.

- For example, if your clauses are:
$$ (x) \land (y) \land (z) \land (\lnot x \lor\lnot y) $$
- The first three clauses must be assigned at level 0 in order to move on (since we can't ignore them)

- **BCP**: Boolean Constraint Propagation
	- If we make decisions about variables, it opens the possibilities of other clauses to be decided upon

# Clause States
Given clause $c_1 = (\lnot x \lor\lnot y)$, 

A clause is...
- **Satisfied** if one or more of its literals is satisfied
	$\alpha = x=0 \rightarrow c_1$  satisfied
  
- **Conflicting** if all of its literals are assigned but not satisfied
	$\alpha = x=1, y=1 \rightarrow c_1$ is conflicting
- **Unit** if it is not satisfied and all but one of its literals are assigned
	$\alpha = x=1 \rightarrow c_1$ is unit
	- This is where we propagate our knowledge (BCP) to try to make it true
		- In this example, BCP needs to try to make $\lnot y$ true
- **Unresolved** otherwise
	$\alpha = no assignments \rightarrow c_1$  unresolved

If there are no unresolved clauses, then they are all satisfied.

***

Due to use of heuristics and optimization, these solvers are actually much faster than their naive implementations.

However, there are still problems that are very difficult to solve.

# Unit Clause Rule
- Extend unit clauses so that the unassigned literal is satisfied.
- For a given unit clause C with unassigned literal I, we say that I is implied by C and that C is the antecedent clause of I, denoted by *Antecedent(I)*.
- There may be multiple clauses implying a literal
	- The one used by the SAT solver will be the antecedent clause.

