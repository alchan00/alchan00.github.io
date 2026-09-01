# Monodromy and Local Systems

## 1. Topological Spaces

Let $(X, x_0)$ be a pointed, connected, and "good" topological space.

### Fundamental Theorem of Covering Spaces
There is an equivalence of categories:
$$\mathbf{Cov}/X \;\simeq\; \pi_1(X, x_0)\text{-}\mathbf{Sets}$$

Let $\Lambda$ be a discrete ring. A **$\Lambda$-local system** on $X$ corresponds to a representation:
$$\mathbf{Loc}_{\Lambda}(X) \;\simeq\; \pi_1(X, x_0)\text{-}\mathbf{Mod}_{\Lambda}^{\text{f.g.}}$$

> **Geometric Interpretation via Étale Space ($E \to X$):**
> * A sheaf $\mathcal{F}$ on $X$ and its *espace étalé* $E(\mathcal{F}) \to X$ can be identified interchangeably.
> * Under this identification, a local system is a covering map $p: E \to X$ such that each fiber $E_x$ possesses a $\Lambda$-module structure that varies locally constantly over $X$.
> * **Difference from Vector Bundles:** Unlike smooth/complex vector bundles (where fibers are isomorphic to $\mathbb{R}^n$ or $\mathbb{C}^n$ with continuous topologies), the fibers here are **discrete spaces**.
> * **Monodromy Action:** Each fiber $Y_x$ of a covering map $Y \to X$ is a discrete set naturally endowed with a $\pi_1(X, x)$ action, defined by uniquely lifting loops in $X$ to paths in $Y$.

---

### Examples

1. **Trivial $\mathbb{Z}/2\mathbb{Z}$ Rank 1 Local System on $S^1$:**
   $$E = S^1 \sqcup S^1 \longrightarrow S^1$$
   The monodromy representation $\pi_1(S^1) \to \operatorname{Aut}_{\mathbb{Z}/2\mathbb{Z}}(\mathbb{Z}/2\mathbb{Z}) \cong \{1\}$ is trivial.

2. **Non-trivial $\mathbb{Z}/3\mathbb{Z}$ Local System on $S^1$:**
   $$E = S^1 \sqcup S^1 \longrightarrow S^1 \quad (\text{1-fold cover } \sqcup \text{ 2-fold cover})$$
   Corresponding to the non-trivial representation:
   $$\rho: \pi_1(S^1) \cong \mathbb{Z} \longrightarrow (\mathbb{Z}/3\mathbb{Z})^\times \cong \{\pm 1\} \subset \operatorname{Aut}_{\mathbb{Z}/3\mathbb{Z}}(\mathbb{Z}/3\mathbb{Z})$$
   Here, the zero element forms a trivial 1-fold cover $S^1$, while $\{1, 2\}$ form a connected 2-fold cover $z \mapsto z^2$.

---

### Local Systems from Topology (Fibrations)

**Theorem:** Let $f: X \to Y$ be a fiber bundle with fiber $F$ (e.g., a smooth proper map of manifold/complex varieties). If $F$ has finitely generated cohomology $H^i(F, \Lambda)$, then the higher direct image sheaf $R^i f_* \Lambda$ is a **$\Lambda$-local system on $Y$**.

* **Intuition:** The fibers vary smoothly over $Y$, so their cohomology groups $H^i(f^{-1}(y), \Lambda)$ form a locally constant family.

---

## 2. Schemes and Étale Topology

Let $X$ be a connected normal scheme and let $\bar{x}_0: \operatorname{Spec} \Omega \to X$ be a geometric point.

### Étale Fundamental Group $\pi_1^{\text{et}}(X, \bar{x}_0)$
The étale fundamental group is defined as the group of automorphisms of the fiber functor $F_{\bar{x}_0}$:

$$F_{\bar{x}_0}: \mathbf{FEt}/X \longrightarrow \mathbf{FinSet}, \quad (Y \to X) \longmapsto Y_{\bar{x}_0} = Y \times_X \operatorname{Spec} \Omega$$

$$\pi_1^{\text{et}}(X, \bar{x}_0) \coloneqq \operatorname{Aut}(F_{\bar{x}_0})$$

By construction, $\pi_1^{\text{et}}(X, \bar{x}_0)$ acts naturally and continuously on the fiber $Y_{\bar{x}_0} = F_{\bar{x}_0}(Y)$.

---

### Relation Between Different Base Points $\bar{x}_0$ and $\bar{x}_1$

If $\bar{x}_0$ and $\bar{x}_1$ are two geometric points of a connected scheme $X$:

1. **Non-canonical Isomorphism:** The fiber functors $F_{\bar{x}_0}$ and $F_{\bar{x}_1}$ are **isomorphic (étale path connected)**, which induces an inner automorphism:
   $$\pi_1^{\text{et}}(X, \bar{x}_0) \;\cong\; \pi_1^{\text{et}}(X, \bar{x}_1)$$
   This isomorphism is unique up to inner automorphisms (conjugacy by an element of $\pi_1^{\text{et}}$), analogous to changing the base point in classical topology.

2. **Galois Action Context:** If $X = \operatorname{Spec} K$ and $\bar{x}_0, \bar{x}_1$ correspond to two algebraic closures $\bar{K}_0, \bar{K}_1$, choosing an isomorphism $\bar{K}_0 \cong \bar{K}_1$ specifies an isomorphism between $\operatorname{Gal}(\bar{K}_0/K)$ and $\operatorname{Gal}(\bar{K}_1/K)$.

---

### Fundamental Equivalences in Étale Topology

Let $X$ be a connected scheme. The following categories are equivalent:

$$\mathbf{FEt}/X \;\simeq\; \text{Finite Discrete } \pi_1^{\text{et}}(X, \bar{x}_0)\text{-}\mathbf{Sets} \;\simeq\; \mathbf{LCC}(X)$$

Where $\mathbf{LCC}(X)$ denotes the category of **Locally Constant Constructible Sheaves** of sets on $X$.

Furthermore, for a finite ring $\Lambda$ (where $n\Lambda = 0$ for some $n \in \mathcal{O}_X^\times$):
$$\mathbf{Loc}_{\Lambda}(X) \;\simeq\; \pi_1^{\text{et}}(X, \bar{x}_0)\text{-}\mathbf{Mod}_{\Lambda}^{\text{f.g., cont}}$$

---

### Relation to Torsors and Cohomology Groups

For a rank $n$ local system $\mathcal{L}$ of $\Lambda$-modules:

$$\begin{aligned}
\text{Rank } n \text{ }\Lambda\text{-local systems} &\;\Longleftrightarrow\; \mathrm{GL}_n(\Lambda)\text{-torsors} \\
&\;\Longleftrightarrow\; H^1_{\text{et}}(X, \mathrm{GL}_n(\Lambda)) \\
&\;\Longleftrightarrow\; \operatorname{Hom}_{\text{cont}}(\pi_1^{\text{et}}(X, \bar{x}_0), \mathrm{GL}_n(\Lambda))
\end{aligned}$$

---

### Smooth Proper Base Change Theorem

Let $\Lambda = \mathbb{Z}/n\mathbb{Z}$ where $n$ is invertible on $Y$

**Theorem:** If $f: X \to Y$ is a **smooth and proper morphism** of schemes, then the higher direct image sheaf $R^i f_* \Lambda$ is a **$\Lambda$-local system on $Y$** for all $i \ge 0$.

** For any geometric point $\bar{y} \to Y$, there is a canonical isomorphism:
  $$(R^i f_* \Lambda)_{\bar{y}} \;\cong\; H^i_{\text{et}}(X_{\bar{y}}, \Lambda)$$
  Since $X \to Y$ is smooth and proper, the geometric fibers $X_{\bar{y}}$ vary smoothly, making their étale cohomology groups $H^i_{\text{et}}(X_{\bar{y}}, \Lambda)$ form a locally constant family on $Y$.
