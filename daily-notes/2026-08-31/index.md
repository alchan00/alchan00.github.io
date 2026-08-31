1. Dold kan correspondence

Facts : 
Equiv of categories, and also quillen equivalences. homotopy category is D>=0(Z).
simplicial abelian groups are all kan complexes. in particular weak equivalences are homotopy equivalences.
the equivalences respect homotopy and homotopy groups in sAb <-> homology groups in chZ>=0.


pi_n(ZsingX)=reduced homology
pi_n(SingX)=homotopy groups

2. homotopy group

Remark.
There is a functor Pointed Set <-> Ab
(S,s)->Z[S]/Zs and
(A,0)<-A.
compatible with the usual free forget adjuntion between Sets and Ab.

homotopy groups and homology are in similar relation. 


pi_n vs H_n?

both independent algebraic invariants of Top space invariant under homotopy/continous deformation, covariant.
H_n : measures holes in a space. "base point free (zero)" freely cut, add or subtract cycles. Due to prev, more computable, more algebraic methods.
pi_n : measures obstuctions for contracting spheres. homotopy group of spheres are not all known.

implication : homotopy equiv -> weak equiv -> quasi iso.
However vanishing of one do not imply the other.
ex) pi_3(S_2)=Z (hopf fibration) but H^3(S_2)=0
ex) pi_3(RP^inf)=0 (RP^inf is K(Z/2Z,1) with contractible Z/2Z cover S^inf) but H_3(RP^inf)=Z/2Z

Main results.

Hurewiez map pi_n(X,x_0) -> H_n(X,x_0)

Hurewiez thr :
(pi_1)ab=H_1,
if X is simply connected, and pi_k(X)=0 for all k<n. then n'th map is an iso. (so the first nonzero group agree)

n=0 : pointed set. path components.
n>=1 : group, abelian when n>=2

computational method : serre fibration or fiber bundle
F->E->B.
induces LES in homotopy groups.

Remark : this is a fiber seq. Given any map of pointed spaces A->B one can fiber product with PB (the path object, contractible) and obtain
a serre fibration. serre fibration is just a special case where one do not need such fibrant replacement.
Similarly the cofiber seq is the mapping cone. The case where one do not need replacement is when A->B is injection of CW and in that case A->B->B/A.
In this way CW has a "half" triangulated structure. one inducing LES in homotopy groups and one inducing homology groups.
suspension is similar to [1] and loop is to [-1] but they are not inverses in any sense. The motivation of Spectra Sp is to fix this and construct a stable inf category.

pi_n(LX)=pi_n+1(X)








