# Elliptic curve tables

This folder contains tables of elliptic curves over number fields K with good reduction outside a given set of primes S.

### Contents

- Folder `good-reduction-away-from-first-primes`: smaller fields K, S the primes in K above the first n primes.
- Folder `good-reduction-away-from-2`: many fields K, S the primes in K above 2.
- Folder `good-reduction-everywhere`: many fields K, S the empty set.
- Folder `bounded-rad2N`: smaller fields K, all elliptic curves with a bound on the radical of twice the conductor norm.
- Folder `fields`: tables of number fields, which were computed along the way.

### Computation method

Let M(S,K) denote the set of K-ismorphism classes of elliptic curves over K with good reduction outside S.  
To compute M(S,K), we first use Koutsianas' (Elkies, Cremona) reduction to finitely many S-unit equations over certain extension fields L, which we then solve using the solver in this repository.

### Format

- K: A number field K is given by a monic polynomial f in Q[x], such that K is isomorphic to Q[x]/(f).
  - Elements of K will then be uniquely represented by polynomials in Q[x] of degree less than deg(f).
  - In filenames, K will be given by its [LMFDB label](https://www.lmfdb.org/NumberField/FieldLabels) 
    (although the last entry may not yet be assigned by the LMFDB, in which case we choose one).  
    The label is composed of the degree of K, its number of real places, the absolute value of its discriminant, and index (usually 1).
    For example, the label of Q is 1.1.1.1.
- S: Primes of K are prime ideals of OK, which are given as lists of their generators.
  - In filenames, we list primes in Q, such that S is then the set of all primes in K above these.
- E: An elliptic curve E over K has a Weierstrass model `y^2 = x^3 - 27 c4 x - 54 c6`.
  - The K-isomorphism class of E is determined by a tuple (c4,c6), where c4 and c6 are unique up the usual common scalar factors u^4 and u^6 for some u in K^*. 
    (If K has provably class number 1, then we will choose c4 and c6 as the classical invariants of a global minimal Weierstrass model of E.)
  - The Qbar-isomorphism class of E is uniquely determined by the j-invariant.

- Files that start with "js" contain j-invariants, i.e. Qbar-isomorphism classes, of elliptic curves over some number field K with good reduction outside some set of primes S.
- Files that start with "curves" contain (c4,c6)-tuples, i.e. K-isomorphism classes, of elliptic curves over K with good reduction outside S. 

In general, the K isomorphism classes can be quickly computed from the Qbar-isomorphism classes.
For example over Q, these come from quadratic twists for j not in {0,1728}, and in the other two cases from quartic and sextic twists.
In general, the only difficulty can be the required class group computation of K. 
Thus we sometimes store only the j-invariants to save space.

Note on the running time: The running times in the *.txt-files do usually include the time for the class group computations (if GRH is not assumed), except if K=Q and S=S(n).

### Status

This project is still in progress, and the S-unit equation solver still in development. 
The shared files are provably correct, up to possibly assuming GRH, which is signified by '*', and up to possible bugs in the quite delicate software.
This being said, great effort has already been undertaken to assure that every detail should be correct.

### Completeness of the data

Each given data file is either provably complete, or its completeness is conditional on GRH.
If GRH is assumed, the filename is marked with an asterisk '*', and the json file also mentions it. 
See README.md of top folder about possible bugs.

### Number of elliptic curves for some small fields

    K = Q = "1.1.1.1":
    ==================
    
    S               Isomorphism classes over Q        over Qbar
    ------------------------------------------------------------
    {}                                       0                0
    {2}                                     24                5
    {2,3}                                  752               83
    {2,3,5}                               7600              442
    {2,3,5,7}                            71520             2140
    {2,3,5,7,11}                        592192             8980
    {2,3,5,7,11,13}                    4576128            34960
    {2,3,5,7,11,13,17}                32367872           124124
    {2,3,5,7,11,13,17,19}            217923072           418816
    {2,3,5,7,11,13,17,19,23}      > 1390818304        > 1338028 (bug detected, needs to be recomputed)

    K = Q(sqrt(-3)) = "2.0.3.1":
    ============================

    Primes over     Isomorphism classes over K        over Qbar
    ------------------------------------------------------------
    {}                                       0                0
    {2}                                     44               10
    {2,3}                                 1776              193
    {2,3,5}                              12944              722
    {2,3,5,7}                           754112*           11024*
    {2,3,5,7,11}                       4044672*           29350*

    K = Q(i) = "2.0.4.1":
    =====================

    Primes over     Isomorphism classes over K        over Qbar
    ------------------------------------------------------------
    {}                                       0                0
    {2}                                     64               13
    {2,3}                                 1280              145
    {2,3,5}                             107296*            3242*
    {2,3,5,7}                           617024*            9336*
    {2,3,5,7,11}                       3368576*           25462*
    
    * - conditional on GRH.

### Related data:

- M({2,3,23},Q) was computed by Koutsianas via S-unit equations [[arxiv:1511.05108]](https://arxiv.org/abs/1511.05108), [[github]](https://github.com/akoutsianas/ERGOS).
- M({2,3,5,7,11},Q) was computed by von Känel and Matschke via a reduction to Mordell equations [[arxiv:1909.00480]](https://arxiv.org/abs/1909.00480), [[github]](https://github.com/bmatschke/solving-classical-diophantine-equations), and recomputed by Bennett, Gherga and Rechnitzer via a reduction to Thue--Mahler equations [[pdf]](https://www.math.ubc.ca/~andrewr/pubs/BeGhRe.pdf), [[www.nt.math.ubc.ca/BeGhRe/]](https://www.nt.math.ubc.ca/BeGhRe/).
- M({2,3,5,7,11,13},Q) was heuristically computed and analysed by Best and Matschke via Mordell equations, [[github]](https://github.com/elliptic-curve-data/ec-data-S6). 

### Author

Benjamin Matschke.

### License

Creative Commons BY-NC 4.0.

### Acknowledgements

This project is being supported by the [Simons Collaboration on Arithmetic Geometry, Number Theory, and Computation](https://simonscollab.icerm.brown.edu/).

