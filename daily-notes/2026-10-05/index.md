colimit and limit are "functors", left and right adjoint to constant diagram functor. Existence of colim/lim = existence of map witnessing ~ as a left/right adjoint object.

Existence depend on the shape of the diagram I. some facts:

Sets have all (small) lim and colim.

if (co)lim exist for I=discrete cat (disc(set)) and

$$
* \rightrightarrows *
$$

diagram with two maps, all co(lim) exists.

colim and lim are reverse when switched to

$$
I^{\mathrm{op}} \to C^{\mathrm{op}}
$$

if I had initial object

$$
C^{I} \to C
$$

limit is just evaluation at the initial object.

if I is filtered exists

$$
J \to I
$$

cofinal where J is a directed set.

Part 2.  
Set_* and Top_*

the cat of pointed top space seem to be more useful in stable homotopy theory.

Recall that forget functor U from Top to Set had left adjoint D and right adjoint I. D stands for discrete, I for indiscrete.

Due to this it is very easy to compute (co)lim in Tops : do it in Sets where (co)lim has explicit discription and give (final)initial topology.

Top_* and Set_* has same adjunctions. Also

$$
\mathrm{Top}_{*} \to \mathrm{Top}
$$

has left adjoint

$$
(-)_{+}
$$

which simply adds a basepoint.

Using above facts we get

1. limits are just same as in Tops, the new basepoint is just compatible basepoints.

2. colimit is more interesting. When I is connected (pushout, coequalizer ... ) basically the same. However if I is not connected we need to identify basepoints. ex) coproduct is "wedge sum"

in particular (*,*) is initial and final object (zero object)

Recall that Top (say reasonable sub cat like CGWH) is closed cartesian.

Top_* is closed symmetric monoidal.

internal hom is

$$
\mathrm{Map}_{*}(X,Y)
$$

maps of pointed spaces where the basepoint is

$$
c_{y_{0}}
$$

constant map.

there is "smash product" denoted

$$
X \wedge Y
=
\frac{X \times Y}{X \vee Y}
$$

quotient of the map induced by

$$
X \to X \times Y,
\qquad
x \mapsto (x,y_{0})
$$

$$
Y \to X \times Y,
\qquad
y \mapsto (x_{0},y)
$$

This is the space by contracting all

$$
(x,y_{0}),\qquad (x_{0},y)
$$

to the basepoint

$$
(x_{0},y_{0}).
$$

ex)

$$
S^{n} \wedge S^{m} \cong S^{n+m}
$$

ex) "loop space"

$$
\Omega X = \mathrm{Map}_{*}(S^{1},X).
$$

"suspension"

$$
\Sigma X = S^{1} \wedge X.
$$

by special case f adjunction,

$$
\Sigma \dashv \Omega.
$$

ex)

$$
H : I_{+} \wedge X \to Y
$$

is a homotopy between

$$
H_{0}
$$

and

$$
H_{1}.
$$

$$
\pi_{n}(X,x)
:=
[(S^{n},*),(X,x)]_{*}
=
\pi_{0}\left(\mathrm{Map}_{*}(S^{n},X)\right)
$$

is defined for every object in this category. defines a class of functors

$$
\mathrm{Top}_{*}
\to
\begin{cases}
\mathrm{Set}_{*}, & n=0,\\
\mathrm{Grp}, & n=1,\\
\mathrm{Ab}, & n\geq 2.
\end{cases}
$$

Now fiber cofiber seq.

for map

$$
f : (X,x_{0}) \to (Y,y_{0})
$$

of top spaces, we can take "homotopy" kernel and cokernel.

recall that

$$
*
$$

is the zero object.

there is a unique map to Y. By some model category argument, we can compute homotopy fiber product of this diagram after we factor

$$
* \to Y
$$

to

$$
* \to PY \to Y.
$$

$$
* \to PY
$$

is a trivial cofibration, and

$$
PY \to Y
$$

is now a fibration, so that naive pullback is the same. i.e. take ordinary fiber product * replaced to PY.

Denote this limit as

$$
\mathrm{hofib}(f).
$$

we call

$$
\mathrm{hofib}(f) \to X \to Y
$$

"fiber seq"

same way by replacing

$$
X \to *
$$

to

$$
X \to CX \to *
$$

and take naive pushout we get

$$
\mathrm{hocofib}(f)
$$

and

$$
X \to Y \to \mathrm{hocofib}(f)
$$

"cofiber seq"

ex)

$$
\mathrm{hofib}(* \to Y) \simeq \Omega Y,
$$

$$
\mathrm{hocofib}(X \to *) \simeq \Sigma X.
$$

when one extends

$$
\mathrm{hofib}(f) \to X \to Y
$$

to the left by succesively taking fibers one gets:

$$
\Omega Y \to \mathrm{hofib}(f) \to X \to Y
$$

when one extends

$$
X \to Y \to \mathrm{hocofib}(f)
$$

to the right by succesively taking cofibers one gets:

$$
X \to Y \to \mathrm{hocofib}(f) \to \Sigma X
$$

Note : being a fiber seq is not equiv to being a cofiber seq. in otherwords, Top_* fails to be stable, suspension and loop functors are not inverses.

$$
\widetilde{H}_{n}
$$

sends cofib seq to exact seq.

$$
\pi_{n}
$$

sends fib seq to exact seq.

combining this fact with

$$
\pi_{n}(\Omega Y) \cong \pi_{n+1}(Y),
$$

$$
\widetilde{H}_{n+1}(\Sigma X) \cong \widetilde{H}_{n}(X)
$$

we get LES of homotopygroups/homologygroups.

ex) if f was a serre fibration, then

$$
\mathrm{hofib}(f)
$$

is just the fiber

$$
F = f^{-1}(y_{0}).
$$

we get the usual LES.

e) if f was inclusion of

$$
A \hookrightarrow X
$$

cell complex,

$$
\mathrm{hocofib}(f)
$$

is just

$$
X/A.
$$

we get the usual LES on reduced homology.
