작성해주신 노트를 바탕으로 GitHub Markdown LaTeX 수식($ / $$) 문법에 맞추어 깔끔하게 정돈했습니다. 미완성되거나 생략된 문장은 내용의 흐름을 해치지 않는 선에서 자연스럽게 마무리했습니다.
Study Note: Grothendieck Monodromy Theorem
Goal of Today: Understand Grothendieck Monodromy Theorem.
Notation: Let F = \text{Frob} be the arithmetic Frobenius.
1. Class Field Theory & Ramification Groups
Recall the sequence of inertia and higher ramification groups for a local field K:
 * Inertia group: I_K = \text{Gal}(\bar{K}/K^{\text{ur}})
 * Wild inertia group: P_K (the unique pro-p Sylow subgroup of I_K)
 * Tame inertia quotient: I_K / P_K \cong \prod_{\ell \neq p} \mathbb{Z}_\ell(1)
Interpretations of Higher Ramification Groups G_K^i (or G_{L/K, i})
For a finite Galois extension L/K with ring of integers \mathcal{O}_L and maximal ideal \mathfrak{m}_L:
 * Ring quotient view:
   
 * Metric view:
   
 * Uniformizer view:
   
(Note: Herbrand's theorem allows us to define upper numbering G_K^v, which is compatible with quotients.)
2. Tate Twist \mathbb{Z}_\ell(1) and Cyclotomic Character
Let p be the residue characteristic, and let q = p^f. We consider \ell \neq p.
The most convenient definition of the Tate module is T_\ell \mathbb{G}_{m, \mathbb{F}_p} \cong \mathbb{Z}_\ell(1), on which \text{Frob} acts as multiplication by p (or q).
Construction of Isomorphism \mathbb{Z}_\ell(1) \cong T_\ell \mathbb{G}_m
To construct an isomorphism with \mathbb{Z}_\ell, we choose a compatible sequence of primitive \ell^n-th roots of unity \{\zeta_{\ell^n}\}_{n \ge 1} (i.e., \zeta_{\ell^n}^\ell = \zeta_{\ell^{n-1}}).
 * The choice of a different primitive root sequence corresponds to an automorphism of \mathbb{Z}_\ell given by multiplication by a unit u \in \mathbb{Z}_\ell^\times.
 * Define the map:
   
 * Transition maps for projective system:
   
 * \phi_n is a compatible, G_{\mathbb{F}_p}-equivariant \mathbb{Z}/\ell^n\mathbb{Z}-module isomorphism, inducing:
   
\ell-adic Cyclotomic Character
The action of G_{\mathbb{F}_p} (and G_K) on \mathbb{Z}_\ell(1) defines the \ell-adic cyclotomic character:


which is unramified and completely determined by \chi_\ell(\text{Frob}) = p.
Inductive System (Discrete Group / Pontryagin Dual)
Taking transition maps as multiplication by \ell on \mathbb{Z}/\ell^n\mathbb{Z} and inclusion on \mu_{\ell^n}:


This gives the Pontryagin dual discrete group.
3. Kummer Theory and Structure of G_K
By Kummer theory applied to unramified extensions:

Taking the inverse limit over n with p \nmid n:

Kummer theory guarantees these generate all tamely ramified extensions of K^{\text{ur}}.
Checking the conjugation action of Frobenius F:

Thus, we obtain a complete description of G_K / P_K as a semi-direct product:

4. \ell-adic Representations
Let K/\mathbb{Q}_p be a local field, and let \rho : G_K \to \text{GL}(V) be a continuous \ell-adic representation (\ell \neq p) on a finite-dimensional \mathbb{Q}_\ell-vector space V.
Subgroup Image Properties
 * Since G_K is compact, \rho(G_K) is bounded, so there exists a G_K-invariant lattice T \subset V. Thus, \rho(G_K) \subseteq \text{GL}_n(\mathbb{Z}_\ell).
 * The principal congruence subgroups U_k = I + \ell^k M_n(\mathbb{Z}_\ell) are pro-\ell groups, whereas P_K is a pro-p group (\ell \neq p).
 * Therefore, \rho(P_K) must be finite. Passing to a finite Galois extension L/K, we can assume \rho(P_L) = 1.
Terminology
 * Unramified (Good reduction): \rho(I_K) = 1.
 * Semistable: \rho(\sigma) is unipotent for all \sigma \in I_K.
 * Potentially (Property): \rho satisfies the property after restricting to G_L for some finite Galois extension L/K.
5. Grothendieck Monodromy Theorem
Let K/\mathbb{Q}_p be a local field, \ell \neq p, and \rho : G_K \to \text{GL}(V) an \ell-adic representation.
Statement
 * Potential Semistability:
   Every \ell-adic representation \rho : G_K \to \text{GL}(V) is potentially semistable. (i.e., after a finite extension L/K, \rho(I_L) acts unipotently).
 * Monodromy Operator Structure:
   In the semistable case (or restricting to G_L), for all \sigma \in I_K, the action of inertia is given by:
   
   
   where:
   * t_\ell : I_K \to I_K / P_K \xrightarrow{\text{proj}} \mathbb{Z}_\ell(1) is the tame character from Kummer theory.
   * N : V \to V(-1) is a G_K-equivariant nilpotent endomorphism (the Monodromy operator).
Proof Idea
Due to topological constraints (pro-p vs pro-\ell), only the t_\ell factor survives in the quotient I_K/P_K.
Choosing a topological generator (or lift of 1 \in \mathbb{Z}_\ell) y \in I_K, we can define:


Since \rho(y) is unipotent, this sum is finite, making N nilpotent and rendering formula (2) straightforward.
Moral / Takeaway
The infinite-dimensional topological G_K-representation V can be reduced (after a finite field extension) to simple linear algebra data:
 * A finite-dimensional \mathbb{Q}_\ell-vector space V.
 * An unramified representation \rho : W_K \to \text{GL}(V) (or an automorphism F = \rho(\text{Frob})).
 * A nilpotent operator N \in \text{End}(V) satisfying:
   
