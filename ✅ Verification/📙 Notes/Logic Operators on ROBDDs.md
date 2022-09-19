# Binary operators
(Two operands)
- Take BDD from operand 1
- Take BDD from operand 2
- Use apply algorithm to apply an operator to the two BDDs

# Unary operators
Works with Unary operators too
$${!f} \equiv (x \land !f_{x\leftarrow 1}) \lor (\lnot x \land !f_{x\leftarrow 0}) $$
