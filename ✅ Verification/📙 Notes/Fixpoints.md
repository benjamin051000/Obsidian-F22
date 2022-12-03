# Lattice
- Basically a graph of the Power set of a transition system
- Universal set at top, empty set at bottom
- In order of complexity, connect elements of power set together, in a lattice-like structure


- Greatest Lower Bound: Intersection
- Least upper bound: Union

# Fixpoint
Z is a fixpoint to a function F iff $F(Z) = Z$.

- May not do this for every argument, so it's not exactly like an identity function

- To find the greatest fixpoint, start at the top and apply F on various things and head down. 
- To find the least fixpoint, start at the bottom and head up.
- In a finite lattice and with a monotonic F, you are guaranteed to find either/both.
