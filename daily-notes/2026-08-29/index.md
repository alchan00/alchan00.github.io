sheaf and stacks

Locally ringed space or category V, is defined with a "sheaf" of rings. 
This seems super natural when we regard O_X as the ring of functions defined on a space.
The main reason of this def is (rather than just a presheaf) is to make sense of gluing by automatically defining sections via its section on subspaces.
This property was a key for defining schemes and adic spaces.

Stacks share the similar philosophy with sheaves in the sense that local data controls global data.
Fact that can help understanding the stack condition.
TFAE:
1. Given any fppf cover U->X pullback induces an equiv of categories from Qcoh(X) to Qcoh(U/X), where the later is the category of descent data.
2. pi : Qcoh -> sch_fppf is a stack.
In general when a statement says ~ is a sheaf/ ~ is a stack. One should understand this statement as ~ can be glued uniquely from local data. (The word local here depends heavily on the topology of the site.)

The difference between sheaf and stack.

sheaves glue Sets and the compatibility is given by stricy equality ex) f_i|U_ij=f_j|U_ji
stacks glue Groupoids and the compatibility is given by isomorphisms. ex) phi_ij : M_i|U_ij -> M_j|U_ji 
In order to glue Groupiods one needs to also check that the isomorphisms data agree on overlap as well.
The essence is that Sets is 1 category and Groupoids is 2 category, and the sheaf condition for infinity categories requires infinite data of coherence.
