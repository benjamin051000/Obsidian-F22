---
date: 2022-08-26
tags: "ver/lecture"
---
Precision is important! Underspecifying something can lead to trouble!

Logic operators: $\land \lor \lnot \implies \rightarrow \leftrightarrow$

More logic symbols found [here](https://en.wikipedia.org/wiki/List_of_logic_symbols)

# Some logical operators
## Implication operator
$$ x \rightarrow y \equiv \lnot x \lor y $$
Truth table:
| x | y | $x \rightarrow y$ |
| - | - | - |
|0 | 0 |0 |
| 0 | 1 | 1 |
| 1 | 1 | 1 |
If x holds, y *must* hold.
If x doesn't hold, we don't know what y will be (could be either).

When you see "if", use implication.

## Bidirectional implication operator
$$ x \leftrightarrow y \equiv (x \land y) \lor (\lnot x \land \lnot y) $$

# Inferencing example
- If x is a prime number greater than 2, then x is odd.
- It is not the case that x is not a prime number greater than 2.
- x is not odd.
- What is x?

Make some propositional logic

p = x is a prime number >2.
q = x is odd


# Formal Reasoning Approaches
- Proof-theoretic
	- Use a deductive mechanism of reasoning, based on axioms and inference rules
	- For the above example:
	1. $p \rightarrow q$
		1. $\lnot\lnot p$
		$\implies p$
		$\therefore q$
	3. $\lnot q$

	We are left with: $q$ and $\lnot q$. This is a **contradiction**.

- Model-theoretic
	- Enumerate possible solutions from a finite number of candidates
	- basically make a big truth table

For n variables, your state space will be $2^n$.


## Inference System
An inference rule relates **antecedents** to their **consequences**.
Lots of rules: see the slides

# First-order logic
AKA predicate logic

Includes **quantifiers** and non-logical symbols

Some quantifiers:
- For all: $\forall$
- Exists: $\exists$
- Non-logical symbols: Functions and predicates
	- Also includes: math operators (equality and inequality, +-\*/), array indexing, pointers, bitwise operators, etc.

# Assignment
Sort of like variable assignment

- Full assignment: All variables have been assigned
- Partial assignment: Otherwise

$$\models$$
## Satisfiability
A formula is **satisfiable** if there exists an assignment of its variables under which the formula evaluates to TRUE.

Otherwise, it's a **contradiction.**

A formula is **valid** (aka *tautology*) if it evaluates to TRUE under all assignments.
- Denoted by: " $\models \phi$"

Satisfiability checking -> *SAT Checking*

Sometimes we want satisfiability, sometimes we want validity.

# The Decision Problem
Decision problem for a formula is to determine whether it is valid

Properties:
- Soundness: When decision procedure returns "valid", it is valid
- Completeness: Always terminates and it returns "valid" when it is valid

A theory is decidable if there is a decision procedure for it.

Further reading: Decision Procedures, An Algorithmic View by Daniel Kroening and Ofer Strichman, Springer, 2010



