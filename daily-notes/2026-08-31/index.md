# Algebraic Topology: Dold–Kan Correspondence, Homotopy vs. Homology, and Homotopy Groups of Spheres

---

## 1. Dold–Kan Correspondence

### Core Properties
* **Equivalence of Categories:** Establishes an equivalence between the category of simplicial abelian groups $\mathbf{sAb}$ and the category of non-negatively graded chain complexes $\mathbf{Ch}_{\ge 0}(\mathbf{Ab})$.
* **Quillen Equivalence:** Induces a Quillen equivalence at the model category level. Its derived category yields the non-negative derived category of integers:

$$
D_{\ge 0}(\mathbb{Z})
$$

* **Fibrancy:** Every simplicial abelian group is a Kan complex. Consequently, weak equivalences in this setting correspond precisely to homotopy equivalences.
* **Compatibility:** The equivalence preserves both homotopy and homology groups:

$$
\pi_n(X_\bullet) \cong H_n(N(X_\bullet))
$$

---

## 2. Relations Between Topological Invariants

### Comparisons
* $\pi_n(\mathbb{Z}\mathrm{sing}(X)) \cong \widetilde{H}_n(X)$ (Reduced Singular Homology)
* $\pi_n(\mathrm{Sing}(X)) \cong \pi_n(X, x_0)$ (Homotopy Groups)

---

## 3. Homotopy Groups vs. Homology Groups

### Categorical Framework
There is a canonical adjunction between Pointed Sets ($\mathbf{Set}_*$) and Abelian Groups ($\mathbf{Ab}$):

$$
(S, s_0) \longmapsto\ \mathbb{Z}[S] / \mathbb{Z} s_0
\qquad \Longleftrightarrow \qquad
(A, 0) \longmapsto\ A
$$

This mirrors the relationship between homotopy groups and homology groups:

| Feature | Homotopy Groups ($\pi_n$) | Homology Groups ($H_n$) |
| :--- | :--- | :--- |
| **Concept** | Measures obstructions to contracting spheres ($S^n \to X$). | Measures "$n$-dimensional cycles mod boundaries" (holes). |
| **Computability** | Difficult to compute (e.g., higher homotopy groups of spheres). | Highly computable via algebraic and axiomatic methods. |
| **Structure** | Non-abelian for $n = 1$, abelian for $n \ge 2$. Basepoint-dependent. | Always abelian for $n \ge 1$. Basepoint-free (cycles can be added/subtracted). |

> **Note on Implication Chains:**  
> Homotopy Equivalence $\implies$ Weak Homotopy Equivalence $\implies$ Quasi-Isomorphism.  
> However, the vanishing of one invariant **does not** imply the vanishing of the other:
>
> * $\pi_3(S^2) \cong \mathbb{Z}$ (via the Hopf Fibration), whereas $H_3(S^2) = 0$.
> * $\pi_3(\mathbb{R}P^\infty) = 0$ (since $\mathbb{R}P^\infty \simeq K(\mathbb{Z}/2\mathbb{Z}, 1)$ with contractible universal cover $S^\infty$), whereas $H_3(\mathbb{R}P^\infty) \cong \mathbb{Z}/2\mathbb{Z}$.

---

## 4. Main Results: The Hurewicz Theorem

There exists a natural comparison map (the **Hurewicz homomorphism**):

$$
h_n \colon \pi_n(X, x_0) \longrightarrow H_n(X,x_0)
$$

### Hurewicz Theorem Statement
1. **Dimension $n = 1$:** For any path-connected space $X$, the Hurewicz map induces an isomorphism from the abelianization of the fundamental group:

$$
\pi_1(X)^{\mathrm{ab}} \;\cong\; H_1(X)
$$

2. **Dimensions $n \ge 2$:** If $X$ is $(n-1)$-connected (i.e., $X$ is simply connected and $\pi_k(X) = 0$ for all $1 \le k < n$), then the Hurewicz map

$$
h_n \colon \pi_n(X) \longrightarrow H_n(X)
$$

is an **isomorphism** (and $H_k(X) = 0$ for $1 \le k < n$). That is, the first non-zero homotopy and homology groups coincide.

---

## 5. Computational Tools & Duality Frameworks

### Long Exact Sequences & Fibrations vs. Cofibrations

* **Fibrations (Serre Fibrations):**  
  Given a fiber sequence $F \to E \to B$, there is an induced long exact sequence (LES) in homotopy groups:

  $$
  \dots \to \pi_n(F) \to \pi_n(E) \to \pi_n(B) \to \pi_{n-1}(F) \to \dots
  $$

  * *Path-Loop Replacement:* For any continuous map of pointed spaces $A \to B$, one can replace $B$ with an equivalent fibration via the path space $PB$ (which is contractible) to obtain a Serre fibration.

* **Cofibrations & Mapping Cones:**  
  Dual to fibrations, a inclusion of CW complexes $A \hookrightarrow B$ gives a cofiber sequence $A \to B \to B/A$, which induces a long exact sequence in reduced homology groups.

### Duality Summary Table

| Concept | Homotopy Structure | Homology Structure |
| :--- | :--- | :--- |
| **Sequence Type** | Fiber Sequence ($F \to E \to B$) | Cofiber Sequence ($A \to B \to B/A$) |
| **Exact Sequence** | Long Exact Sequence in $\pi_n$ | Long Exact Sequence in $H_n$ |
| **Adjoint Operators** | Loop Space functor $\Omega X$ ($\text{right adjoint}$) | Reduced Suspension functor $\Sigma X$ ($\text{left adjoint}$) |
| **Shift Relation** | $\pi_n(\Omega X) \cong \pi_{n+1}(X)$ | $\widetilde{H}_{n+1}(\Sigma X) \cong \widetilde{H}_n(X)$ |

> **Motivation for Spectra ($\mathbf{Sp}$):**  
> Suspension ($\Sigma$) and Loop ($\Omega$) functors are adjoints ($\Sigma \dashv \Omega$), but they are not inverses of each other in the unstable homotopy category. Constructing the stable homotopy category of **Spectra ($\mathbf{Sp}$)** inverts $\Sigma$, formalizing a true stable $\infty$-category.

---

## 6. Homotopy Groups of Spheres $\pi_k(S^n)$

### Fundamental Results
1. **Low Dimensions & Spheres:**
   * By the Cellular Approximation Theorem and the Hurewicz Theorem:

     $$
     \pi_k(S^n) = 0 \quad \text{for } k < n, \qquad \text{and} \qquad \pi_n(S^n) \cong \mathbb{Z}
     $$

   * Since $S^1$ is an Eilenberg–MacLane space $K(\mathbb{Z}, 1)$:

     $$
     \pi_n(S^1) \cong 
     \begin{cases} 
     \mathbb{Z} & n = 1 \\ 
     0 & n \neq 1 
     \end{cases}
     $$

2. **Serre's Finiteness Theorem:**  
   The homotopy groups $\pi_k(S^n)$ are **finite abelian groups** for all $k > n$, except when $k = n$ or $k = 2n - 1$ 

3. **Freudenthal Suspension Theorem & Stable Homotopy Groups:**  
   The natural suspension map $\pi_k(X, x_0) \to \pi_{k+1}(\Sigma X, x_0)$ implies that $\pi_{n+k}(S^n)$ stabilizes when $n > k + 1$.  
   The **stable $k$-stem** is defined as:

   $$
   \pi_k^s \mathrel{:=} \varinjlim_{n \to \infty} \pi_{n+k}(S^n)
   $$

   * $k < 0 : 0$
   * $k = 0 : \mathbb{Z}$
   * $k = 1 : \mathbb{Z}/2\mathbb{Z}$
   * $k = 2 : \mathbb{Z}/2\mathbb{Z}$
   * $k = 3 : \mathbb{Z}/24\mathbb{Z}$
   * $k = 4, 5 : 0$
