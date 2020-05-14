# Two-division-field candidates

This folder contains files ``fields_K_XXX_S_YYY.sobj``.

Any such file contains all* field extensions L/K such that

- K is the number field given by [LMFDB label](https://www.lmfdb.org/NumberField/FieldLabels) XXX,
- L is the splitting field of some degree 3 polynomial over the number field K, and 
- L/K is unramified outside S, where S is the set of primes in K above YYY. 

An asterisk `*` in the filename signifies that the completeness is conditional on GRH. 

Equivalently, instead of storing L/K we could list all quadratic and cubic extensions F/K that are unramified outside the primes in K over S.
L is then simply the normal closure of F/K (or L is the trivial extension L = K).  

### Author

Benjamin Matschke.

### License

Creative Commons BY-NC 4.0.

### Acknowledgements

This project is being supported by the [Simons Collaboration on Arithmetic Geometry, Number Theory, and Computation](https://simonscollab.icerm.brown.edu/).

