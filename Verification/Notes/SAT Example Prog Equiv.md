# SAT Example: Program equivalence
Consider the two programs
```c
if (!a && !b)
	h();
else if (!a)
	g();
else
	f();
```

```c
if (a)
	f();
else if (b)
	g();
else
	h();
```


First one:
$$((\lnot a \land \lnot b) \land \lnot f \land \lnot g \land h) \lor (((a \lor b)\land \lnot a) \land \lnot f \land g \land \lnot h) \lor (((a \lor b)\land a)\land f \land \lnot g \land \lnot h)$$
Second one:
$$((a)\land f \land \lnot g \land\lnot h)\lor ((\lnot a \land b)\land\lnot f \land g \land\lnot h) \lor ((\lnot a \land \lnot b) \land \lnot f\land\lnot g \land h)$$

Use a solver to see if they are equivalent!

- If you use *or* to join stuff that is actually exclusive-or, it's okay so long as you "guard" each option with conditions.
- Here, we ensure that both variables are expressed in each guard, which makes these propositional statements work.
	- e.g., not a and b even though the code doesn't explicitly say that.

