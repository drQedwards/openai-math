# External note, not an OpenAI manuscript

**Author:** Dr. Q (`drQedwards`)

**Date:** 6 October 2026

This directory is not a product of the OpenAI math-release model, and it is not one of the 372 families in `CONTENTS.md`. It is an outside note, offered as a pull request the maintainers can close if community files are out of scope. It does not edit the catalogue, the overview, or any existing preprint.

## What is decided

| Width | Decision | Bound |
| --- | --- | --- |
| 2-SAT | Decided by implication-graph components | Linear in variables plus clauses (Aspvall, Plass, Tarjan, 1979) |
| 3-SAT and wider | Decided by DPLL with unit propagation | Exact on every finite instance. No polynomial bound is claimed |

Checked copies of both procedures are in `src/`. `tests/` compares them with exhaustive search for n ≤ 10.

```bash
python community/drQedwards/tests/test_two_sat.py
python community/drQedwards/tests/test_three_sat.py
```

The same text is family 001 and family 002 of [drQedwards/math](https://github.com/drQedwards/math).

## What is not decided

P versus NP is open. A linear algorithm for 2-SAT does not decide 3-SAT: a clause of three literals is not a pair of implications.

The Hodge conjecture is also open. The word "linear" in that conjecture means a rational linear combination of algebraic-cycle classes. It is not a runtime. Assuming the conjecture does not put n-SAT in linear time. The Boolean ideal membership certificate from the Nullstellensatz can have exponential degree, and Hodge does not bound that degree.

Nothing here should be cited as `OAI:...`.
