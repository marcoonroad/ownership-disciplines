# Owners-as-Accessors

This kind of discipline lies between owners-as-dominators and
owners-as-modifiers, somehow. While the dominator approach doesn't leak the
owned object, the modifier has a greater privilege over such owned object
(incoming pointers will only be able to describe a potentially restricted
object). Owners as accessors have full and unique rights over their owned
objects, but these objects can be leaked with no access rights (that is, the 
client is not able to read neither write them). Such objects with "empty
rights" carry yet an identity capability, and so, can be
discriminated/compared against. It is in some sense a kind of Abstract Data
Type, the owner performs the role of the module while the owned plays the role
of the Data Type instance.


### References

* [1] _On Owners-as-Accessors_ — by James Noble and Alex Potanin
