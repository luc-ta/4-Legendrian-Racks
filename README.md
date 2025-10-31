# 4-Legendrian-Racks
Program for classifying 4-Legendrian racks up to isomorphism. Data for those up to order 6.

Based on the [online rack library](https://www.cs.du.edu/~petr/libraries_of_algebraic_structures.html) of Petr Vojtěchovský and Seung Yeop Yang.

This repo accompanies the papet ["Distinguishing power of 4-Legendrian permutation racks"](https://arxiv.org/abs/2510.26619) (arXiv:2510.26619), which is joint work with Peyton Phinehas Wood.

# Usage
`4-legendrian-finder.txt` exhaustively searches for 4-Legendrian structures on all racks of a given order _n_ in Vojtěchovský and Yang's library, searches for isomorphisms between them, and outputs a list of all 4-Legendrian racks of order _n_ up to isomorphism.

For example, to run the search for all _n_ between 1 and 3, load Vojtěchovský and Yang's library and then run the following. The following assumes that you've saved `4-legendrian-finder.txt` in the same folder as the rack library; if not, then replace "LRQ.path" below and in `4-legendrian-finder.txt` with the path to wherever you've saved `4-legendrian-finder.txt`.
```
for n in [1..3] do
	ReadAsFunction(Concatenation(LRQ.path, "4-legendrian_finder.txt"))()(n);
od;
```
## Note
In the program and data, 4-Legendrian racks are stored as lists of the form (R, uL, uR, dR, dL), where R is the underlying rack. This ordering is distinct from the usual ordering.
