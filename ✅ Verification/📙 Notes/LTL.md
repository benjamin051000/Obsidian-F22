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

