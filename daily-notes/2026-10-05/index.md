colimit and limit are "functors", left and right adjoint to constant diagram functor. Existence of colim/lim = existence of map witnessing ~ as a left/right adjoint object.

Existence depend on the shape of the diagram I. some facts:

Sets have all (small) lim and colim.

if (co)lim exist for I=discrete cat (disc(set)) and

$$
*\rightrightarrows *
$$

diagram with two maps, all co(lim) exists.

colim and lim are reverse when switched to

$$
I^{\mathrm{op}}\to C^{\mathrm{op}}
$$

if I had initial object

$$
C^I\to C
$$

limit is just evaluation at the initial object.

if I is filtered exists

$$
J\to I
$$

cofinal where J is a directed set.

Part 2.  
Set_* and Top_*

the cat of pointed top space seem to be more useful in stable homotopy theory.

Recall that forget functor U from Top to Set had left adjoint D and right adjoint I. D stands for discrete, I for indiscrete.

Due to this it is very easy to compute (co)lim in Tops : do it in Sets where (co)lim has explicit discription and give (final)initial topology.

Top_* and Set_* has same adjunctions. Also

$$
\mathrm{Top}_*\to \mathrm{Top}
$$

has left adjoint

$$
(-)_+
$$

which simply adds a basepoint.

Using above facts we get

1. limits are just same as in Tops, the new basepoint is just compatible basepoints.

2. colimit is more interesting. When I is connected (pushout, coequalizer ... ) basically the same. However if I is not connected we need to identify basepoints. ex) coproduct is "wedge sum"

in particular

$$
(*,*)
$$

is initial and final object (zero object)

Recall that Top (say reasonable sub cat like CGWH) is closed cartesian.

Top_* is closed symmetric monoidal.

internal hom is

$$
\operatorname{Map}_*(X,Y)
$$

maps of pointed spaces where the basepoint is

$$
c_{y_0}
$$

constant map.

there is "smash product" denoted

$$
X\wedge Y
=
\frac{X\times Y}{X\vee Y}
$$

quotient of the map induced by

$$
X\to X\times Y,
\qquad
x\mapsto (x,y_0)
$$

$$
Y\to X\times Y,
\qquad
y\mapsto (x_0,y)
$$

This is the space by contracting all

$$
(x,y_0),\qquad (x_0,y)
$$

to the basepoint

$$
(x_0,y_0).
$$

ex)

$$
S^n\wedge S^m\cong S^{n+m}
$$

ex) "loop space"

$$
\Omega X=\operatorname{Map}_*(S^1,X).
$$

"suspension"

$$
\Sigma X=S^1\wedge X.
$$

by special case f adjunction,

$$
\Sigma\dashv\Omega.
$$

ex)

$$
H:I_+\wedge X\to Y
$$

is a homotopy between

$$
H_0
$$

and

$$
H_1.
$$

$$
\pi_n(X,x)
:=
[(S^n,*),(X,x)]_*
=
\pi_0\!\left(\operatorname{Map}_*(S^n,X)\right)
$$

is defined for every object in this category. defines a class of functors

$$
\mathrm{Top}_*
\to
\begin{cases}
\mathrm{Set}_*, & n=0,\\
\mathrm{Grp}, & n=1,\\
\mathrm{Ab}, & n\ge 2.
\end{cases}
$$

Now fiber cofiber seq.

for map

$$
f:(X,x_0)\to (Y,y_0)
$$

of top spaces, we can take "homotopy" kernel and cokernel.

recall that

$$
*
$$

is the zero object.

there is a unique map to Y. By some model category argument, we can compute homotopy fiber product of this diagram after we factor

$$
*\to Y
$$

to

$$
*\to PY\to Y.
$$

$$
*\to PY
$$

is a trivial cofibration, and

$$
PY\to Y
$$

is now a fibration, so that naive pullback is the same. i.e. take ordinary fiber product * replaced to PY.

Denote this limit as

$$
\operatorname{hofib}(f).
$$

we call

$$
\operatorname{hofib}(f)\to X\to Y
$$

"fiber seq"

same way by replacing

$$
X\to *
$$

to

$$
X\to CX\to *
$$

and take naive pushout we get

$$
\operatorname{hocofib}(f)
$$

and

$$
X\to Y\to \operatorname{hocofib}(f)
$$

"cofiber seq"

ex)

$$
\operatorname{hofib}(*\to Y)\simeq\Omega Y,
$$

$$
\operatorname{hocofib}(X\to *)\simeq\Sigma X.
$$

when one extends

$$
\operatorname{hofib}(f)\to X\to Y
$$

to the left by succesively taking fibers one gets:

$$
\Omega Y\to \operatorname{hofib}(f)\to X\to Y
$$

when one extends

$$
X\to Y\to\operatorname{hocofib}(f)
$$

to the right by succesively taking cofibers one gets:

$$
X\to Y\to\operatorname{hocofib}(f)\to\Sigma X
$$

Note : being a fiber seq is not equiv to being a cofiber seq. in otherwords, Top_* fails to be stable, suspension and loop functors are not inverses.

$$
\widetilde{H}_n
$$

sends cofib seq to exact seq.

$$
\pi_n
$$

sends fib seq to exact seq.

combining this fact with

$$
\pi_n(\Omega Y)\cong\pi_{n+1}(Y),
$$

$$
\widetilde{H}_{n+1}(\Sigma X)\cong \widetilde{H}_n(X)
$$

we get LES of homotopygroups/homologygroups.

ex) if f was a serre fibration, then

$$
\operatorname{hofib}(f)
$$

is just the fiber

$$
F=f^{-1}(y_0).
$$

we get the usual LES.

e) if f was inclusion of

$$
A\hookrightarrow X
$$

cell complex,

$$
\operatorname{hocofib}(f)
$$

is just

$$
X/A.
$$

we get the usual LES on reduced homology.
