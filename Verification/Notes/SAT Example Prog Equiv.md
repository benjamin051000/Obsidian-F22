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
	f();
```


First one:
$$((\lnot a \land \lnot b) \land \lnot f \land \lnot g \land h) \lor (((a \lor b)\land \lnot a) \land \lnot f \land g \land \lnot h) \lor (((a \lor b)\land a)\land f \land \lnot g \land \lnot h)$$
Second one:
$$()$$