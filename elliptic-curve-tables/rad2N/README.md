# Elliptic curve tables "rad2N"

This folder contains tables of elliptic curves over number fields K with bounded radical of twice the conductor norm.

### Contents:

- Folder `K_1.1.1.1`: All rational elliptic curves (given by c4,c6) with `rad(2*N) <= 1000`.
- Folder `K_1.1.1.1*`: All* rational elliptic curves (given by j) with `rad(2*N) <= 130000`. 
- Folder `K_2.0.4.1*`: All* elliptic curves over Q(i) (given by j) with `rad(2*Norm(N)) <= 2000`.

    * - conditional on [GRH](https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis).  
    N - the (conductor)[https://en.wikipedia.org/wiki/Conductor_of_an_abelian_variety] of an elliptic curve.  
    Norm - the [absolute norm](https://en.wikipedia.org/wiki/Ideal_norm#Absolute_norm).  
    rad - the [radical](https://en.wikipedia.org/wiki/Radical_of_an_integer) of a rational integer.  

Note that `rad(2*Norm(N)) <= X` is equivalent to `2*prod_{p in S'} p <= X` if S' is the set of odd rational primes over which there is a prime in K at which the curve has bad reduction. 
The files in this table are indexed by `S = S' \cup {2}`.

Moreover, all folders except for `K_1.1.1.1*` contain further data for additional S, outside the above mentioned range.

### Format:

The format is the same as in the parent directory, except that in `K_1.1.1.1*` the files are zipped: 
Each zip file contains the j-invariants of all* rational elliptic curves with good reduction outside S, for all S containing 2 with `10000*i <= prod_{p in S} p <= 10000*(i+1)` for some i.

### Redundancy:

Note that the files have a certain overlap, as any single file represents some M(K,S) and M(K,S) is contained in M(K,T) for any superset T of S.
This redundancy is intended to make the data more searchable, at the price of a larger table.
