Q. How is Set->Ani defined ? Intuitively this will send S to the constant simp set S, however this is not enough to give a functor.
There is an adjunction between Set and sSet

pi_0 ^ disc ^ (-)_0

remains true when the image is restricted to Kan.

This induces adjunctions between Cat and sCat.

There is an adjunction Cat and Cat_inf h ^ N

There is an adjunction Cat_inf and sCat C ^ N_h.

Check N_h*disc=N.

now suppose we are given an ordinary functor C->Kan.

Kan is (-)_0 of Kan enriched in Kan. so we have disc(C)->Kan (as a functor in sCat)

Now we can apply N_h and get N(C)-> Ani.

So there is a map Hom(C,Kan) to Hom(N(C),Ani) not sure if surjective.

Anyway, thisway disc : Set -> Kan promotes to a functor between inf cats disc : N(set)->Ani

similarly, there is a map Hom(ho,C) to Hom(Ani,N(C)). where ho is pi_0(Kan), the homotopy category of spaces.

The functor pi_0 : Kan -> Set inverts equivalences so it factors through ho and defines the desired functor.

We can also construct N(Gpds) -> Ani using the nerve functor, and Ani->N(Gpds) using h. 

My view on Ani.

objects = kan complexes or CW complex

morphisms = mapping spaces 

and I imagine each oject in Ani, (i.e. kan complex) as "Set with equality replaced with paths". Or "homotopy type of a space"

N(CW)[W^-1], N(Kan)[W^-1]

Useful observations.

pick a vertex of an anima X, x.

we can define pi^n(X,x) the hopotopy groups of a given anima.

This carries quite a lot of information as in topology. Specifically,

By whitehead thr a map of ani is an equiv <-> homotopy equiv <-> weak equiv.

We say X is n-truncated if pi^k=0 for k>n.

0-truncated <-> X->discpi_0X is a weak equiv. i.e. X is a "set"

h,N defines adjuntion between Groupoid and Ani.

1-truncated <-> X->NhX is a weak equiv. i.e. X is a "groupoid"

When G is a groupoid, one can defined pi_0 and pi_1. the formal to be isoclass, the latter is the automorphism.

N and h preserves pi_1. pi_1(N(C),x))=Aut_C(x), pi_1(X,x)=Aut_hX(x)

example : Let G be a groupoid with a single object, automorphism G. Then N(G)=BG classifying space in Ani. pi_1 = G and 0 otherwise.
