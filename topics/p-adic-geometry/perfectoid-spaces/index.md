# Summary of Scholze 2012, Perfectoid Spaces

## Main Ideas

### 1. Almost Mathematics

The philosophy behind perfectoid $K$-algebras = info/results on generic fiber can be spread out almost integrally.

The reason this is possible is because $K$ has pseudouniformizer admitting all $p$'th roots so that $\varpi^N$ torsion extend to $\varpi^{N/p^r}$ torsion via Frobenius.

This is made explicit via almost math, which systematically ignores $\mathfrak{m}_K$ torsion modules. ex) $\mathfrak{m}_K \sim K^\circ$

There are two ways for establishing tilting equivalence. One is via Fontaine theta map and one via almost math. Two constructions agree, but the latter is more useful in proving further important results. Namely, that rational subsets of perfectoids are perfectoids, and equivalence of analytic and étale site.
.

#### Theorem 5.2
The categories of perfectoid $K$-algebras and perfectoid $K^\flat$-algebras are equivalent. In fact, we have the following series of equivalences of categories:

$$K\text{-Perf} \cong K^{\circ a}\text{-Perf} \cong (K^{\circ a}/\varpi)\text{-Perf} = (K^{\flat \circ a}/\varpi^\flat)\text{-Perf} \cong K^{\flat \circ a}\text{-Perf} \cong K^\flat\text{-Perf}$$

---

### 2. Tilting Equivalence, Almost Purity

While almost math and approximation lemma are the main tool for proving things, I would say these are the main results and takeaways.

There is a tilting functor from char 0 to char $p$ that allows distillation of results in char $p$ to char 0. For example basic properties of perfectoids that their rational open subsets and finite étale extensions are perfectoids are first proven in char $p$.

The tilting functor is useful in the sense that it forgets structure morphism and preserves topological information.

#### Theorem 6.3
Let $(R, R^+)$ be a perfectoid affinoid $K$-algebra, and let $X = \mathrm{Spa}(R, R^+)$ with associated presheaves $\mathcal{O}_X, \mathcal{O}_X^+$. Also, let $(R^\flat, R^{\flat +})$ be the tilt given by Lemma 6.2, and let $X^\flat = \mathrm{Spa}(R^\flat, R^{\flat +})$ etc.

* **(i)** We have a homeomorphism $X \cong X^\flat$, given by mapping $x \in X$ to the valuation $x^\flat \in X^\flat$ defined by $|f(x^\flat)| = |f^\sharp(x)|$. This homeomorphism identifies rational subsets.
* **(ii)** For any rational subset $U \subset X$ with tilt $U^\flat \subset X^\flat$, the complete affinoid $K$-algebra $(\mathcal{O}_X(U), \mathcal{O}_X^+(U))$ is perfectoid, with tilt $(\mathcal{O}_{X^\flat}(U^\flat), \mathcal{O}_{X^\flat}^+(U^\flat))$.
* **(iii)** The presheaves $\mathcal{O}_X, \mathcal{O}_{X^\flat}$ are sheaves.
* **(iv)** The cohomology group $H^i(X, \mathcal{O}_X^+)$ is $\mathfrak{m}$-torsion for $i > 0$.
.

#### Theorem 7.9
Let $(R, R^+)$ be a perfectoid affinoid $K$-algebra, and let $X = \mathrm{Spa}(R, R^+)$.

* **(iii)** For any finite étale cover $S/R$, $S$ is perfectoid and $S^{\circ a}$ is finite étale over $R^{\circ a}$. Moreover, $S^{\circ a}$ is a uniformly almost finitely generated $R^{\circ a}$-module.

Which implies:

#### Theorem 1.11
Let $X$ be a perfectoid space over $K$ with tilt $X^\flat$ over $K^\flat$. Then tilting induces an equivalence of sites:

$$X_{\text{ét}} \cong X^\flat_{\text{ét}}$$

---

### 3. Applications to Weight Monodromy Conjecture

I could only understand the statement and ideas of the proof.

The statement is basically the Riemann hypothesis for local fields.

The point is that the results are known for char $p$, and one can reach from finite type rigid analytic varieties to char 0 perfectoid via successive étale extensions. Using the tilting equivalence of étale sites, and proétale descent one can prove results in char 0.

However the reason this does not apply for all cases is that the tilt map is not algebraic.

#### Conjecture 1.13 (Deligne, [9])
Let $X$ be a proper smooth variety over $k$, and let $V = H^i(X_{\bar{k}}, \bar{\mathbb{Q}}_\ell)$. Then for all $j \in \mathbb{Z}$ and for any geometric Frobenius $\Phi \in G_k$, all eigenvalues of $\Phi$ on $\mathrm{gr}_j^N V$ are Weil numbers of weight $i + j$, i.e. algebraic numbers $\alpha$ such that:

$$|\alpha| = q^{(i+j)/2}$$

for all complex absolute values.
