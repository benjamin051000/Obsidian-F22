# Amdahl's Law
Favor frequent case over infrequent case!

- $Fraction_{enhanced}$ is the part of the system/program that can be enhanced: F = 25%, 60%, etc.
- $Speedup_{enhanced}$ is the amount you can speed that part up
- E.g., we can speed up 25% of the program by 5x


$$
Speedup_{overall} = \frac{Execution time_{old}}{Execution time_{new}}
$$
$$
= \frac{1}{(1-Fraction_{enhanced})+\frac{Fraction_{enhanced}}{Speedup_{enhanced}}}
$$

