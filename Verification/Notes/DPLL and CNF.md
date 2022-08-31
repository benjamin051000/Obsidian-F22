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

