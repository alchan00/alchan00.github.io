Fun observation.

Tops->Sets forget functor is left and right Bousfield localisation (wrt a functor that endows a set with discrete, chaotic top)

This explains why underlying set of lim/colim of topological spaces are always same to those evaluated in Sets. 

(compare with Ab->Set. forget functor is only a right adjoint and coproduct = tensor product)

Sets=Tops[{bijections}^-1]]

Suppose i:Z->X closed immersion j:U->X open immersion. X\U=Z. Z->X<-U interesting things happen on the category of sheaves of some coeff ring. 

i* / i_* / i^!

j_! / j* / j_*

i*, i_*, j_!, j* are exact, and i^!, j_* are not 
In particicular i_*, j* preserves injectives.

j* is left and right Bousfield localisation
i* is left, i^! is right Bousfield localisation.
i_* is fully faithful inclusion to the sub cat of sh(X) supported on Z.

j*i_*=0 and induces sh(U)=sh(X)/sh(Z)
i^!j_*=0, i*j_!=0. sh(Z)=sh(X)/sh(U)

i_!i^! -> 1 -> j_*j^*

j_!j^!-> 1 ->i_*i^*

intuition of _!?

j_! extending a sheaf by zero in open immersions. generally pushforward/direct image with proper support. ex) if f : X->* final map, R^if_*Z=H^i(X,Z), "R^if_!Z=H^i_c(X,Z)" cohomology with compact support.

intuition of ^!?

i^! + j_* / i^* + j_! can be thought as complements to each other.

In the first SES above, for x in U unit map is iso. for x in Z counit map is iso.
In the second SES above, for x in U the counit map is iso. for x in Z the unit map is iso. 
 
i_*i^!F = largest subsheaf supported on Z. 


Remark.
Unlike others, f^! is not always defined as maps between sheaves but only exists in the derived level.
In special case when f is a closed immersion the right derived functor of i^! is this functor.
At least this is true for locally compact spaces and etale schemes.


+same picture appears in the def of almost zero modules.
