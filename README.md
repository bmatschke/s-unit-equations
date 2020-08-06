# S-unit equations

A general solver for S-unit equations over number fields and applications (in progress).

### About S-unit equations

An [S-unit equation](https://en.wikipedia.org/wiki/S-unit#S-unit_equation) is a diophantine equation of the form `a*x + b*y = 1`, where `a` and `b` are given constants in a number field `K`, and the variables `x` and `y` are constrained to be [S-units](https://en.wikipedia.org/wiki/S-unit) for some given set of primes `S` in `K`.

### Contents

 - Solutions to certain examplary S-unit equations over number fields.
 - Tables of elliptic curves over number fields with good reduction outside S.
 - Soon: sage code of the S-unit equation solver.

### Status

This project is still in progress, and the S-unit equation solver still in development. 

### Completeness of the data

Up to possible bugs, each given data file is either provably complete, or its completeness is conditional on GRH.
If GRH is assumed, the filename is marked with an asterisk '*', and the json file also mentions it.

### About possible bugs

In principle the programs in this repository should be provably correct (modulo assumptions on GRH, which are always mentioned in that case).
However during this project, a [bug](https://pari.math.u-bordeaux.fr/cgi-bin/bugreport.cgi?bug=2207) in the S-unit group implementation of Pari/GP 2.11.2 was found, and it is still present in SageMath versions 9.0 and 9.1, which were used in all the computations in this repository up to now.
I assumed that I can detect this bug, and in that case rerun with higher precision using Pari or using Magma (versions V2.24-10 and V2.25-3) within Sage for the S-unit groups.
However I recently ran into instances where my bug detection for the S-unit group class fails.
Thus it is at present **not clear up to which point the tables in this repository are complete**.
The bug was fixed with Pari/GP 2.11.4.
Thus, to solve this issue for this repository, all computations for computing the tables in this repository should be run again, once Sage uses Pari 2.11.4 or higher. (Perhaps a more economical solution would be to first bound the set S-unit groups that are potentially affected by this bug.)

On a more philosophical note, Magma is closed-source and proprietary, which make proofs bases on Magma computations at least debatable -- and this repository uses Magma as a fallback option for S-unit groups and also for computing discriminants of relative field extensions.
Also the code in this repository has 20000 lines, and it relies on much larger computer algebra systems (Sage, Pari, Singular, Magma), such that more undetected bugs might occur.
 
### Related projects

- An S-unit equation solver over number fields by Alvarado, Koutsianas, Malmskog, Rasmussen, Vincent, West [[arxiv:1903.00977]](https://arxiv.org/abs/1903.00977), available in [sage](https://www.sagemath.org/).
- An S-unit equation solver over Q by von Känel and Matschke [[arxiv:1909.00480]](https://arxiv.org/abs/1909.00480), [[github]](https://github.com/bmatschke/solving-classical-diophantine-equations).

### Author

Benjamin Matschke.

### License

Creative Commons BY-NC 4.0.

### Acknowledgements

This project is being supported by the [Simons Collaboration on Arithmetic Geometry, Number Theory, and Computation](https://simonscollab.icerm.brown.edu/).
