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

Each given data file is either provably complete, or its completeness is conditional on GRH.
If GRH is assumed, the filename is marked with an asterisk '*', and the json file also mentions it.

### Related projects

- An S-unit equation solver over number fields by Alvarado, Koutsianas, Malmskog, Rasmussen, Vincent, West [[arxiv:1903.00977]](https://arxiv.org/abs/1903.00977), available in [sage](https://www.sagemath.org/).
- An S-unit equation solver over Q by von K"anel and Matschke [[arxiv:1909.00480]](https://arxiv.org/abs/1909.00480), [[github]](https://github.com/bmatschke/solving-classical-diophantine-equations).

### Author

Benjamin Matschke.

### License

Creative Commons BY-NC 4.0.

