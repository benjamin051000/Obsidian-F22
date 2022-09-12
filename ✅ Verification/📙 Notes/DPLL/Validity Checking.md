Validity checking: Check if it is satisfiable under ALL assignments

- Don't loop over every input, that would take too long
- Instead, use what we know about SAT solvers!

![[validity-checker.excalidraw]]

If we give SAT solver $\lnot\phi$, then the SAT solver will actually return whether it found an unsatisfiable condition for $\phi$.


