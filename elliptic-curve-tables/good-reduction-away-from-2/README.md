# Elliptic curves with good reduction away from 2

Let `M(2,K)` denote the set of all elliptic curves over K with good reduction outside the primes above 2.

### Contents

Each folder `K_deg_[n]_S_2` contains sets `M(2,K)` for certain number fields of degree `n`, including all with `|disc(K)| <= 20000`.

### Completeness 

As in all tables of this repository, the completeness of the computed sets `M(2,K)` may be conditional on GRH, in which case this is signified by an asterisk `*` in the filename. 
 
All fields K with `|disc(K)| <= 20000` are considered, of any degree.
Moreover, in certain degrees `n`, all fields K of degree `n` up to `|disc(K)| <= B(n)` are considered, where `n` and `B(n)` are given in the following table:
    
     n          B(n)           L(n)
    --------------------------------
     2        20,000
     3        20,000
     4        20,000
     5        50,000
     6       100,000
     7     1,000,000
     8     1,656,109      2,400,000
     9    27,316,369    100,000,000

Furthermore, in degrees `n = 8` and `n = 9` we consider all fields in the LMFDB up to `|disc(K)| <= L(n)`, however these lists of fields are only known to be complete up to `|disc(K)| <= B(n)`.

In degrees `n >= 10`, it is known that `|disc(K)| > 100,000,000`, and we computed `M(2,K)` for a few examples.

For further information, see the README.md in the folder above.
