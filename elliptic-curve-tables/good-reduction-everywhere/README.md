# Elliptic curves with everywhere good reduction

### Contents

Each file `curves_deg_XXX_Dmax_YYY*` contains the set of all* elliptic curves with everywhere good reduction over all number fields K of degree `deg(K) = XXX` with `|disc(K)| <= YYY`.

### Completeness 

All number fields in the given range are considered, however if the filename contains an asterisk '*', then the completeness of the given sets of elliptic curves is conditional under GRH.
In particular, all fields K with `|disc(K)| <= 20000` are considered (of any degree).

### Notes

The data is simply extracted from the folder `good-reduction-away-from-2`.

In the files, only those fields are listed for which the computed list of elliptic curves is non-empty.
The complete list of fields in the given range can be obtained for example from the LMFDB.
