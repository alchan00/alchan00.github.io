
# From Abelian Groups to Condensed Algebra

Commutative algebra and algebraic geometry can be thought of as a study of the abelian category $\mathrm{Ab}$.

$\mathrm{Ab}$ is closed symmetric monoidal with the usual tensor product and internal Hom. Commutative algebra objects are commutative rings with unity $R$, and $\mathrm{Mod}_R(\mathrm{Ab})$ is the usual category of $R$-modules.

Homological algebra and derived algebraic geometry turn our attention to $D(\mathrm{Ab})$, which fixes exactness issues and retains homological information.

Now, given a small site $\mathcal C$, and

$$
\mathcal A=\mathrm{Sh}(\mathcal C,\mathrm{Ab}),
$$

we can repeat the same process.

The main example I keep in mind is when $\mathcal C$ is the category of light profinite sets, and $\mathcal A$ is the category of condensed abelian groups. Now this becomes a study of "topological algebra".

$\mathcal A$ is a Grothendieck abelian category which really behaves like $\mathrm{Ab}$. It inherits a tensor product and internal Hom from $\mathrm{Ab}$.

**Example.** $\mathrm{TopAb}$ is not an abelian category, but $\mathrm{CondAb}$ is a very nice abelian category which accommodates essentially all topological abelian groups of interest.

Furthermore, $\mathcal A$ has enough injectives and flat objects, so that $D(\mathcal A)$ becomes a presentable stable closed symmetric monoidal category.

Now $D(\mathcal A)$ is our new playground.

For any $E_\infty$-algebra $R$, I will denote

$$
D(R):=\mathrm{Mod}_R(D(\mathcal A)).
$$

## Useful facts and machinery

### 1. Tensor product and internal Hom

First, $D(R)$ is also a presentable stable closed symmetric monoidal category.

Let

$$
\mathrm{Bar}_n(M,R,N)
=
M\otimes R^{\otimes n}\otimes N,
$$

with face and degeneracy maps coming from the actions, multiplication, and unit maps.

The relative tensor product is defined as the geometric realization

$$
M\otimes_R N
:=
|\mathrm{Bar}_\bullet(M,R,N)|.
$$

Since tensoring preserves colimits, by the adjoint functor theorem it has a right adjoint, the internal Hom.

We can be more explicit. The underlying object of the internal Hom can be computed as

$$
U\underline{\mathrm{Hom}}_R(M,N)
\simeq
\mathrm{Tot}\left(
[n]\longmapsto
\underline{\mathrm{Hom}}_{\mathcal C}
(R^{\otimes n}\otimes M,N)
\right),
$$

where $\mathcal C=D(\mathcal A)$, and the cosimplicial structure comes from the $R$-module actions and multiplication.

### 2. Free–forgetful–cofree adjunctions

Second, $D(R)$ and $D(\mathcal A)$ have three canonical functors, with adjunctions

$$
R\otimes -
\;\dashv\;
U
\;\dashv\;
\underline{\mathrm{Hom}}_{\mathcal C}(R,-).
$$

Here:

- $R\otimes -$ is the free module functor.
- $U$ is the forgetful functor.
- $\underline{\mathrm{Hom}}_{\mathcal C}(R,-)$ is the cofree module functor.

The free module functor is symmetric monoidal, and the forgetful functor is lax symmetric monoidal.

The cofree functor does not, in general, have a canonical monoidal structure.

### Remark: Base change

We can play the same game with $D(\mathcal A)$ replaced by $D(R)$.

For every map of $E_\infty$-algebras

$$
R\longrightarrow S,
$$

we have the adjunctions

$$
S\otimes_R -
\;\dashv\;
U_{S/R}
\;\dashv\;
\underline{\mathrm{Hom}}_R(S,-).
$$

We also obtain a commuting triangle of forgetful functors with vertices

$$
D(\mathcal A),\qquad D(R),\qquad D(S).
$$

Equivalently, extension of scalars satisfies

$$
S\otimes_R(R\otimes X)
\simeq
S\otimes X.
$$

Here we also use the fact that forgetful functors are lax symmetric monoidal.
