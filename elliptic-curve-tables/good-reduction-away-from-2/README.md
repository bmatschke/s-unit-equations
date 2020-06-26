# Elliptic curves with good reduction away from 2

Let `M(2,K)` denote the set of all elliptic curves over K with good reduction outside the primes above 2.

### Contents

Each folder `K_deg_XXX_S_2` contains sets `M(2,K)` for certain number fields of degree XXX, including all with `|disc(K)| <= 20000`.

### Completeness 

As in all tables of this repository, the completeness of the computed sets `M(2,K)` may be conditional on GRH, in which case this is signified by an asterisk `*` in the filename. 
 
All fields K with `|disc(K)| <= 20000` are considered.
Moreover, in certain degrees n, all fields K of degree n up to `|disc(K)| <= B(n)` are considered, where n and `B(n)` are given in the following table:
    
     n        B(n)
    ---------------
     2       20000
     3       20000
     4       20000
     5       50000
     6      100000
     7     1000000

In degrees `n >= 8`, it is known that `|disc(K)| >= 1000000`, and we only computed `M(2,K)` for a few examples.

For information, see the README.md in the folder above.
