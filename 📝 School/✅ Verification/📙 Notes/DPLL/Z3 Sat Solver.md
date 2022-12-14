APIs in multiple languages (c/c++/py)

For assignments, you **must** encode your logic as *propositional* logic, not any other types of logic.

You can make expressions via Abstract Syntax Trees (ASTs):
- Create a symbol, e.g., $p$
- Assign it to an AST
- Create a negation AST: $\lnot p$
- Tell Z3 to combine different ASTs via an operator (e.g., or) 
	- This yields your formula, e.g., $\lnot p \lor q$


`Z3_solver_assert()` ANDs all the clauses together
- You can also do this on your own with ands

Z3 will tell you if it's satisfiable, which can be captured in a `switch/case`:
- `Z3_L_FALSE`: Unsatisfiable
	- You can see elements in the vector (not sure which vector she said it was)
	- You can see the [[Unsatisfiable Core]]
- `Z3_L_TRUE`: Satisfiable!
	- You can check assignments of variables in a given model
- `Z3_L_UNDEF`: Something went wrong.
	- This is an unexpected result, something wasn't configured properly

