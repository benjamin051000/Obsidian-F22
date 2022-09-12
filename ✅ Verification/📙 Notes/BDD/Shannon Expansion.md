A propositional logic formula f can be rewritten by considering possible assignments to one of the variables, x, that appear in f:
$$ f = (x \land f_{x\leftarrow 1}) \lor (\lnot x \land f_{x\leftarrow 0}) $$
This maps directly to [[BDD, ROBDD]]!
- The two terms shown are the high/low functions!

# Construct ROBDDs with Shannon Expansion
![[shannon expansion bdd]]

This is recursive!

See [[Andersen-BDDs.pdf]] for an example
