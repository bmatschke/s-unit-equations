# Elliptic curve tables "rad2N"

This folder contains tables of elliptic curves over number fields K with bounded radical of twice the conductor norm.

### Contents

- Folder `K_1.1.1.1`: All elliptic curves over Q with `rad(2*N) <= 2000`, given by (c4,c6).
- Folder `K_1.1.1.1*`: All* elliptic curves over Q with `rad(2*N) <= 420000`, given by j. 
- Folder `K_2.0.3.1*`: All* elliptic curves over Q(sqrt(-3)) with `rad(2*Norm(N)) <= 2000`, given by j.
- Folder `K_2.0.4.1*`: All* elliptic curves over Q(i) with `rad(2*Norm(N)) <= 2000`, given by j.
- Folder `K_2.2.5.1*`: All* elliptic curves over Q(sqrt(5)) with `rad(2*Norm(N)) <= 1000`, given by j.
- Folder `K_2.2.8.1*`: All* elliptic curves over Q(sqrt(2)) with `rad(2*Norm(N)) <= 1000`, given by j.

Here, * signifies that a table is conditional on [GRH](https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis), N denotes the [conductor](https://en.wikipedia.org/wiki/Conductor_of_an_abelian_variety) of an elliptic curve, Norm is the [absolute norm](https://en.wikipedia.org/wiki/Ideal_norm#Absolute_norm), and rad is the [radical](https://en.wikipedia.org/wiki/Radical_of_an_integer) of a rational integer.

Note that `rad(2*Norm(N)) <= X` is equivalent to `2*prod_{p in S'} p <= X` if S' is the set of odd rational primes over which there is a prime in K at which the curve has bad reduction. 
The files in this table are indexed by `S = S' \cup {2}`.

Moreover, all folders except for `K_1.1.1.1*` contain further data for additional S, outside the above mentioned range.

### Format

The format is the same as in the parent directory, except that in `K_1.1.1.1*` the files are zipped: 
Each zip file contains the j-invariants of all* rational elliptic curves with good reduction outside S, for all S containing 2 with `10000*i <= prod_{p in S} p <= 10000*(i+1)` for some i.

### Redundancy

Note that the files have a certain overlap, as any single file represents some M(S,K), and M(S,K) is contained in M(T,K) for any superset T of S.
This redundancy is intended to make the data more searchable and uniform, at the price of a larger table.

### Author

Benjamin Matschke.

### License

Creative Commons BY-NC 4.0.

### Acknowledgements

This project is being supported by the [Simons Collaboration on Arithmetic Geometry, Number Theory, and Computation](https://simonscollab.icerm.brown.edu/).

