# Summary of Scholze (2012): Perfectoid Spaces

## Main Ideas

### 1. Almost Mathematics & Philosophy of Perfectoid $K$-Algebras

* **Core Philosophy:** Information and results on the generic fiber can be "spread out" almost integrally.
* **Mechanism:** This is possible because the base field $K$ contains a pseudo-uniformizer $\varpi$ admitting all $p^n$-th roots ($\varpi^{1/p^r}$). Consequently, $\varpi^N$-torsion modules extend to $\varpi^{N/p^r}$-torsion via the Frobenius endomorphism.
* **Almost Mathematics Framework:** This philosophy is made precise using *Almost Mathematics* (developed by Faltings, Almost Ring Theory by Gabber-Ramero), which systematically ignores modules annihilated by the maximal ideal $\mathfrak{m}_K$ (e.g., $\mathfrak{m}_K \approx \mathfrak{m}_K \otimes \mathfrak{m}_K$).

There are two primary ways to establish the tilting equivalence:
1. Via the Fontaine $\Theta$ map.
2. Via Almost Mathematics.

While both constructions agree, the latter is more powerful for proving structural results—namely, that rational subsets of perfectoid spaces are perfectoid, and the analytic site is equivalent to the étale site.

* **Another Example of the Philosophy:** $\mathcal{O}_X^+$ is almost acyclic (higher sheaf cohomology is annihilated by $\mathfrak{m}_K$).

#### Theorem 5.2 (Tilting for Perfectoid Algebras)
The categories of perfectoid $K$-algebras and perfectoid $K^\flat$-algebras are equivalent. In fact, we have the following sequence of equivalences of categories:

$$K\text{-Perf} \cong K^{\circ a}\text{-Perf} \cong (K^{\circ a}/\varpi)\text{-Perf} = (K^{\flat \circ a}/\varpi^\flat)\text{-Perf} \cong K^{\flat \circ a}\text{-Perf} \cong K^\flat\text{-Perf}$$

---

### 2. Tilting Equivalence & Almost Purity

While almost mathematics and the approximation lemma are the primary technical tools, the following theorems represent the main structural takeaways:

* **Tilting Functor ($\text{Char } 0 \rightsquigarrow \text{Char } p$):** Allows the distillation of characteristic $p$ results into characteristic $0$.
* **Properties Preserved:** Basic properties of perfectoid spaces—such as open rational subsets and finite étale extensions remaining perfectoid—are established first in characteristic $p$.
* **Key Feature:** The tilting functor forgets the structure morphism while preserving topological and étale information.

#### Theorem 6.3 (Structure of Perfectoid Spectra)
Let $(R, R^+)$ be a perfectoid affinoid $K$-algebra, and let $X = \mathrm{Spa}(R, R^+)$ with associated presheaves $\mathcal{O}_X, \mathcal{O}_X^+$. Let $(R^\flat, R^{\flat +})$ be its tilt with $X^\flat = \mathrm{Spa}(R^\flat, R^{\flat +})$.

1. **Homeomorphism:** There is a natural homeomorphism $X \cong X^\flat$ given by mapping $x \in X$ to $x^\flat \in X^\flat$, defined by $|f(x^\flat)| = |f^\sharp(x)|$. This homeomorphism identifies rational subsets.
2. **Rational Subsets:** For any rational subset $U \subset X$ with tilt $U^\flat \subset X^\flat$, the completed affinoid $K$-algebra $(\mathcal{O}_X(U), \mathcal{O}_X^+(U))$ is perfectoid, with tilt $(\mathcal{O}_{X^\flat}(U^\flat), \mathcal{O}_{X^\flat}^+(U^\flat))$.
3. **Sheafiness:** The presheaves $\mathcal{O}_X$ and $\mathcal{O}_{X^\flat}$ are sheaves.
4. **Almost Acyclicity:** The cohomology group $H^i(X, \mathcal{O}_X^+)$ is $\mathfrak{m}_K$-torsion for all $i > 0$.

#### Theorem 7.9 (Almost Purity Theorem)
Let $(R, R^+)$ be a perfectoid affinoid $K$-algebra, and $X = \mathrm{Spa}(R, R^+)$.

* For any finite étale cover $S/R$, $S$ is perfectoid, and $S^{\circ a}$ is finite étale over $R^{\circ a}$.
* Moreover, $S^{\circ a}$ is a uniformly almost finitely generated $R^{\circ a}$-module.

#### Theorem 1.11 (Equivalence of Étale Sites)
Let $X$ be a perfectoid space over $K$ with tilt $X^\flat$ over $K^\flat$. Then tilting induces an equivalence of étale sites:

$$X_{\text{ét}} \cong X^\flat_{\text{ét}}$$

---

### 3. Applications to the Weight-Monodromy Conjecture

* **Overview:** The conjecture can be viewed as an analogue of the Riemann Hypothesis for local fields.
* **Proof Strategy:**
  1. The result is already known in characteristic $p$ (Deligne).
  2. One passes from finite-type rigid analytic varieties to characteristic $0$ perfectoid spaces via successive étale extensions and perfection techniques.
  3. Using the tilting equivalence of étale sites ($X_{\text{ét}} \cong X^\flat_{\text{ét}}$) together with pro-étale descent, one transports results from characteristic $p$ back to characteristic $0$.
* **Limitation:** This technique does not apply universally to all algebraic varieties because the tilting operation is non-algebraic (it inherently relies on analytic/rigid geometry constructions).

#### Conjecture 1.13 (Weight-Monodromy Conjecture / Deligne)
Let $X$ be a proper smooth variety over $k$, and let $V = H^i(X_{\bar{k}}, \mathbb{Q}_\ell)$. Then for all $j \in \mathbb{Z}$ and any geometric Frobenius $\Phi \in G_k$, all eigenvalues of $\Phi$ on $\mathrm{gr}_j^N V$ are Weil numbers of weight $i + j$; i.e., algebraic numbers $\alpha$ such that:

$$|\alpha| = q^{(i+j)/2}$$

for all complex embeddings.
