# Goal of today: Grothendieck monodromy theorem

Fix notation: $F = \text{Frob}$ (arithmetic frobenius).

---

## 1. Class Field Theory & Ramification Groups

Recall:
$$G_K \supset I_K \supset P_K \supset G_K^1 \supset G_K^2 \supset \cdots$$

* $I_K$: Inertia group
* $P_K$: Wild inertia group
* Tame inertia quotient: $I_K / P_K \cong \prod_{\ell \neq p} \mathbb{Z}_\ell(1)$

### Interpretations of Higher Ramification Groups $G_{L/K, i}$
1. $\sigma \in G_{L/K, i} \iff \sigma$ acts trivially on $\mathcal{O}_L / \mathfrak{m}_L^{i+1}$
2. $\sigma \in G_{L/K, i} \iff |\sigma(x) - x| < q^{-1-i} \quad \forall x \in \mathcal{O}_L$
3. Same for uniformizer $\pi_L \in \mathcal{O}_L$

*(Herbrand theorem gives upper numbering $G_K^v$.)*

---

## 2. Tate Twist $\mathbb{Z}_\ell(1)$

Here $p$ can be replaced by $q = p^f$. ($\ell \neq p$)

Most convenient definition: $T_\ell\mathbb{G}_{m,\mathbb{F}_p}$.  
Notation: $\mathbb{Z}_\ell(1)$, where $\text{Frob}$ acts as $p$.

To construct an isomorphism with $\mathbb{Z}_\ell$, we have to choose a compatible sequence of primitive roots of unity $\{\zeta_{\ell^n}\}_{n \ge 1}$.


* The choice of different roots amounts to an automorphism of $\mathbb{Z}_\ell$ by multiplying a unit.
* Map: $\phi_n : \mathbb{Z}/\ell^n\mathbb{Z}(1) \to \mu_{\ell^n}$ sending $a \mapsto \zeta_{\ell^n}^a$
* Transition maps:
  * $\mathbb{Z}/\ell^n\mathbb{Z} \to \mathbb{Z}/\ell^{n-1}\mathbb{Z} \quad (a \mapsto a \bmod \ell^{n-1}\mathbb{Z})$
  * $\mu_{\ell^n} \to \mu_{\ell^{n-1}} \quad (x \mapsto x^\ell \text{ power map})$
* $\phi_n$ is a compatible, $G_{\mathbb{F}_p}$-equivariant $\mathbb{Z}/\ell^n\mathbb{Z}$-module isomorphism and induces $\mathbb{Z}_\ell(1) \xrightarrow{\sim} T_\ell \mathbb{G}_{m, \mathbb{F}_p} \cong \mathbb{Z}_\ell$.

### $\ell$-adic Cyclotomic Character
$\chi_\ell : G_{\mathbb{F}_p} \to \mathbb{Z}_\ell^\times$ is the $\ell$-adic cyclotomic character corresponding to $\mathbb{Z}_\ell(1)$, completely determined by $\text{Frob} \mapsto p$ (unramified).

### Transition Maps for Discrete Groups
We can also take transition maps:
* $\mathbb{Z}/\ell^{n-1}\mathbb{Z} \to \mathbb{Z}/\ell^n\mathbb{Z}$ (multiplication by $\ell$)
* $\mu_{\ell^{n-1}} \to \mu_{\ell^n}$ (inclusion)

In this case we get $\mathbb{Q}_\ell/\mathbb{Z}_\ell(1) \to \mu_{\ell^\infty}$ (Pontryagin dual, discrete groups).

---

## 3. Kummer Theory

$$I_K / P_K = G(K^{\text{tame}} / K^{\text{ur}}) \cong \prod_{\ell \neq p} \mathbb{Z}_\ell(1)$$

Take inverse limit of:
$$G(K^{\text{ur}}(\pi^{1/n}) / K^{\text{ur}}) \to \mu_n \quad \text{sending } \sigma \mapsto \frac{\sigma(\pi^{1/n})}{\pi^{1/n}}$$
for all $p \nmid n$.

Kummer theory says these are tamely ramified extensions.  
One can look at the map and check:
$$F \sigma F^{-1} = \sigma^p$$

Thus we have a full description of $G_K / P_K = \left( \prod_{\ell \neq p} \mathbb{Z}_\ell(1) \right) \rtimes \hat{\mathbb{Z}}$ when $K$ is a finite extension of $\mathbb{Q}_p$.

---

## 4. $\ell$-adic Representations

Since $G_K$ is compact, image contained in some $\text{GL}_n(\mathbb{Z}_\ell) \iff$ exists an invariant lattice $T$.

Principal congruence subgroups are pro-$\ell$ groups while $P_K$ is pro-$p$. This results in the image of $P_K$ to be finite, and $1$ for a finite extension $L/K$.

### Definitions / Terminologies
* $V/\rho$ is **unramified** (good reduction) if $\rho(I) = 1$.
* **Semistable** if $\rho(\sigma)$ is unipotent for all $\sigma \in I$.
* **Potentially ~** when it is ~ after a finite Galois extension.

---

## 5. Statement of Monodromy Theorem ($K/\mathbb{Q}_p$)

1. Every representation is potentially semistable.
2. In the semistable case, for all $\sigma \in I_K$:
   $$\rho(\sigma) = \exp(t_\ell(\sigma) N)$$
   for some $N : V \to V(-1)$ $G$-equivariant nilpotent operator.

$t_\ell : I_K \to \mathbb{Z}_\ell(1)$ is the character from the Kummer map.

The point is that only $t_\ell$ part survives due to topological issues. Choose any lift $y$ of $1$ in $\mathbb{Z}_\ell$.  
$N := \log(\rho(t_\ell(y)))$, then $N$ is nilpotent, and (2) is easy.

---

## Moral
Complex representation can be reduced to semistable representation after field extension, and then it is equivalent to some linear algebra data:

* $V = \mathbb{Q}_\ell$-vector space
* $F$: automorphism
* $N$: nilpotent operator such that $F N F^{-1} = N^p$
