

First recall etale topology -> etale morphism as local isomorphisms.
However the category of schemes are not alligned with the view point above.
For example,
One can not glue along local isomorphisms:
The category of (X, scheme/X) is not a stack for the etale topology. (it is in zariski top by def, and if we restric to affine morphisms this is a stack for the fppf topology)
One can not quotient out by etale equiv relation:
An example of this case is when a finite group G acts freely on X, and "etale" propery discontinous X/G may not be a scheme contrary to our intuition for topological spaces.

This is the motivation for algebraic spaces and diamonds.


Interlude on equiv relations.
equiv relation familiar in Sets can be defined in any category with finite limits.
For f: X->Y kernel pair (pr1,pr2) X xY X -> X  is always an equiv relation. When f is a coequalizer of this diagram we say f is effective epimorphsim.
Similarly equiv relation if effective if coequalizer exist and the equivalence relation is the kernel pair of the coequalizer.

To summarize, epi and equiv relation being "effective" illustrates that quotient is well behaved.

In general when we pass a site C (with subcanonical top) to its sheaf J= sh(C). J is a topos having nice properties like sets. 
One instance is that all epi and equiv relations are effective just as in Sets.

Algebraic spaces and diamonds lie in between (not a topos). Instead of allowing arbitrary quotients and gluing, only allow then along local isomorphisms.
In that way the category sort of stays geometric.

About the diamond functor:
analytic adic space -> diamonds.
X->X^
Some view points :

*Forget structure morphism to Z_p and preserve topology.
Points of X^ only look at perfectoids over X not X->spaZp.
tilting equivalence identifies analytic, etale, finite etale sites.

*Extend the tilting functor.

*Moduli of untilts



About Torsors
in a Topos J A finite group G can be regarded as a group object as well. union of terminal object 1.
Let G act on F' then we have action map G x F' -> F' satisting some property.
f : F'->F  is a G torsor if the action of G fix commutes with f and locally G x F =F' G-equivariant iso.
about the last condition. I got a bit confused why there is such map.
A better way to think about this : first f should be epimorphism. G x F= F' if f admits a section s.
G x F -> G x F' -> F' is iso.
and in the case of f epimorphsim (which is necessary) G is a torsor iff G x F' = F' x_F F'. f itself is a cover. there are G possible sections.


X->Y G-torsor in Diamonds.

Y(R)= R'->R G-torsor and R'->X G-equivariant map
X(R) -> Y(R) map is
sending R->X to trivial G x R. 











