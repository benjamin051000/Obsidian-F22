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

## Bidirectional implication operator
$$ x \leftrightarrow y \equiv (x \land y) \lor (\lnot x \land \lnot y) $$

