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
- 