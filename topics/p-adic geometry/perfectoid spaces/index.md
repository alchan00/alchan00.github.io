Summary of Scholze 2012, perfectoid spaces.

Main ideas

1. Almost mathematics,

The philosophy behind perfectoid K -algebras = info/results on generic fiber can be spread out almost integrally.
The reason this is possible is because K has pseudouniformizer admitting all p'th roots so that and w^N torsion extend to w^N/p^r torsion via Frobenious.
This is made explicit via almost math, which systematically ignores m_K torsion modules. ex) m_K ~ K^0

There are two ways for establishing tilting equivalence. One is via Fontaine theta map and one via almost math.
Two constructions agree, but the later is more useful in proving furthure important results.
Namely, that rational subsets of perfectoids are perfectoids, and equivalence of analytic and etale site.

Another example of the philosophy : O^+_X is almost acylic. 

Theorem 5.2. The categories of perfectoid K-algebras and perfectoid K[
-algebras are
equivalent. In fact, we have the following series of equivalences of categories.
K −Perf ∼= K◦a−Perf ∼= (K◦a
/$)−Perf = (K[◦a
/$[
)−Perf ∼= K[◦a−Perf ∼= K[−Perf


2. Tilting equivalence, almost purity

While almost math and approximation lemma are the main tool for proving things, I would say these are the main results and takeaways.
There is a tilting functor from char 0 to char p that allows distillation of results in char p to char 0.
For example basic properties of perfectoids that their rational open subsets and finite etale extensions are perfectoids are
first proven in char p.
The tilting functor is usefull in the sense that it forgets structure morphism and preserves topological information.

Theorem 6.3. Let (R, R+) be a perfectoid affinoid K-algebra, and let X = Spa(R, R+)
with associated presheaves OX, O
X+
. Also, let (R[
, R[+) be the tilt given by Lemma 6.2,
and let X[ = Spa(R[
, R[+) etc. .
(i) We have a homeomorphism X ∼= X[
, given by mapping x ∈ X to the valuation
x
[ ∈ X[ defined by |f(x
[
)| = |f
]
(x)|. This homeomorphism identifies rational subsets.
(ii) For any rational subset U ⊂ X with tilt U
[ ⊂ X[
, the complete affinoid K-algebra
(OX(U), O
X+
(U)) is perfectoid, with tilt (OX[ (U
[
), O
X+
[
(U
[
)).
(iii) The presheaves OX, OX[ are sheaves.
(iv) The cohomology group Hi
(X, O
X+
) is m-torsion for i >


Theorem 7.9. Let (R, R+) be a perfectoid affinoid K-algebra, and let X = Spa(R, R+)

(iii) For any finite ´etale cover S/R, S is perfectoid and S
◦a
is finite ´etale over R◦a
.
Moreover, S
◦a
is a uniformly almost finitely generated R◦a
-module


Which implies

Theorem 1.11. Let X be a perfectoid space over K with tilt X[ over K[
. Then tilting
induces an equivalence of sites X´et ∼= X´et[
.



3. Applications to weight monodromy conjecture.

I could only understand the statement and ideas of the proof.
The statement is basically the Riemann hypothesis for local fields.
The point is that the results are known for char p, and one can reach 
from finite type rigid analytic varieties to char 0 perfetoid via successive etale extensions.
Using the tilting equivalence of etale sites, and proetale descent one can prove results in char 0.
However the reason this do not apply for all cases is that the tilt map is not algebraic.


Conjecture 1.13 (Deligne, [9]). Let X be a proper smooth variety over k, and let
V = Hi
(Xk¯, Q¯
`). Then for all j ∈ Z and for any geometric Frobenius Φ ∈ Gk, all
eigenvalues of Φ on grj N
V are Weil numbers of weight i + j, i.e. algebraic numbers α
such that |α| = q
(i+j)/2
for all complex absolute values.



