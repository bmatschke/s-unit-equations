# Data for certain S-unit equations

Files containing solutions to certain S-unit equations.

### Format

- K: A number field K is given by a monic polynomial f in Q[x], such that K is isomorphic to Q[x]/(f).
  - Elements of K will then be uniquely represented by polynomials in Q[x] of degree less than deg(f).
  - In filenames, K will be given by its [LMFDB label](https://www.lmfdb.org/NumberField/FieldLabels) 
    (although that the last entry may not yet be assigned by the LMFDB, in which case we choose one).  
    The label is composed of the degree of K, its number of real places, the absolute value of its discriminant, and index (usually 1).
    For example, the label of Q is 1.1.1.1.
- S: Primes of K are prime ideals of OK, which are given as lists of their generators.
  - In filenames, we list primes in Q, such that S is then the set of all primes in K above these.

The `.sobj` files are loadable within [sage](https://www.sagemath.org/).  
The `.txt` files are humanly readable and in json format.  

### Author

Benjamin Matschke.

### License

Creative Commons BY-NC 4.0.

