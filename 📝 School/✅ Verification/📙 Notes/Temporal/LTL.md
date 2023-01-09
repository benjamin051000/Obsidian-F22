# Linear Time Temporal Logic

- X: Next
- G: Always
- F: Eventually
- U: Until

# Dualities
$\lnot Gp \equiv F\lnot p$
$\lnot Fp \equiv G \lnot p$
$\lnot Xp \equiv X \lnot p$
$\lnot (pUq) \equiv \lnot q U (\lnot p \land \lnot q)$  (weak until, where q not required to hold eventually)
$\lnot (pUq) \equiv G \lnot q \lor \lnot q U(\lnot p \land\lnot q)$ (strong until, use this one by default)

- LTL has infinitely long traces to model the transitions of a system. TODO learn how this works
- This is in contrast to [[Computation Tree Temporal Logic (CTL)]], which has infinitely large trees to represent system transitions