- Count the number of minterms that lead to leaf node 1
- Or, compute number of paths that lead to leaf node 1 for each node

Simple case: A node's number of paths is equal to the sum of its childrens' paths

Complex: What if a child node skips a level/variable?
- Multiply child size * $2^{j-i-1}$ where j is the ID of the child node, i is the ID of this node

