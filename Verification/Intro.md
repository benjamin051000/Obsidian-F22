# Why do we do Formal Verification?
Systems are complex these days

Safety-critical systems (e.g., airplanes)
IoT devices everywhere

How can we *trust* technology?

# Famous Technology Failures
## Intel Pentium FDIV Bug
**Symptom: Processor returns incorrect decimal values at or beyond 4 digits**
- Cause: Missing entries in LUT in FP division circuitry
- Discovered in 1994 by a professor doing numerical methods research
- Replacing flawed processors cost $475M
- Caused Intel to begin using Formal Ver.

## Therac 25
I wrote a paper about this back in the day!

Radiation therapy machine
Six accidents occurred where patients received doses in excess of 1000x greater than normal
- Cause: Concurrency error
- AECL never tested the Therac-25 with the combination of HW and SW until it was assembled at the hospital

## Northeast blackout of 2003
2003 in New England area looks like

- Alarm/logging system failed due to a data race
- 50 Million people lost power
- Report: Bug didn't come up even after 300 million online operational hours.

> I'm not sure that more testing would have revealed it
> - Report

## Mars Pathfinder
Rover!
- Symptom: Total system reset of spacecraft
- Cause: Priority inversion error
- Data loss occurs
- Failure scenario:
	- Low priority thread grabs mutex
	- High priority blocks on mutex
	- Medium priority preempts low priority thread
	- Low priority cannot release mutex. Deadlock! 
	- Watchdog (probably) resets system

# What is formal reasoning?
**Encoding a problem in suitable logic and inferring validity of claims expressed in that logic.**

Logics with varying expressiveness
- Propositional logic
- Linear arithmetic
- Equality logic with uninterpreted functions
- Temporal logic
	- Linear-time temporal logic (LTL)
	- Computation-tree temporal logic (CTL)

# Automated formal reasoning
- Representation of logical formulas
	- Conjunctive Normal Form (CNF)
		- (x OR y) AND (NOT x OR z)
	- Binary decision diagrams
- Decision procedures
	- Given a logic formula f under a theory T, decides satisfiability or validity of f
	- satisfiable: One set of inputs yields outputs
- SAT solvers for propositional logic
	- SAT -> Satisfiability
- Satisfiability Modulo Theories (SMT) solvers for various theories
	- Theory of linear arithmetic
	- Theory of arrays

# Z3
Microsoft SMT solver
Open-source!
Various language APIs
Will be used in assignments


# What is Model Checking?
A bit later in the semester
- Need a formal representation of the System Under Analysis (SUA)
	- Model
	- Graph where nodes are possible states of the SUA and edges are transitions between states
- Systematic exploration of state space of a system
	- Start from nodes that represent initial states
	- Traverse all possible paths
	- See if bad states or sequences of bad states are encountered
	- Or, start at bad states and traverse backwards... to initial states (hopefully not)


# Temporal Logic
- Atomic properties
	- e.g., thread1 = waiting
- Temporal operators
	- always, next, eventually
- Safety properties
- Liveness properties

# Model Checking Problem
Will learn about later

# Testing vs Model Checking
## Testing
- Safety properties
	- Assertions, pre/post condition checks
- May fail to exercise inputs that lead to bad states
- Coverage is limited
- Does not provide explanation as to why errors occur
- Analyzes actual code
## Model checking
- More expressive correctness specification
	- Liveness
- Possible to talk about bad states
- Potentially all possible scheduling scenarios can be analyzed
- Provides detailed explanation of how the error occurred
- Does not scale to complex software code!

# How to deal with State-space explosion
Will discuss later
