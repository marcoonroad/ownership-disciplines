# Owners-as-Collectors

In this ownership discipline, owners hold strong references for their owned
objects. Any incoming (that is, from outside) pointer will be, thus, a weak
reference. It can be seen as a sort of owners-as-revokers, but the revocation
is for all subjects pointing for some object, once that object is not
referenced anymore by its respective owner. This brings some sort of purity on
GC-level, 'cause external pointers are weak and the lifetime of the owned is
subsumed on the lifetime of the owner. Here, in the same way of dominators, 
owner domains become regions where the GC can run deterministically. Some
overhead will exist anyways, 'cause the VM and the programmer must check
null-pointers (that is, against collected references) before dereferencing 
them.

Nevertheless, Owners-as-Collectors can enable us reasoning over how much time
objects live on memory, and possibly avoiding memory leaks. Some constraints
can be imposed, for example, accessing the given object only through its 
respective owner (a.k.a, Owners-as-Accessors), this avoids null-checks on owned
part (deferring such checks for the owner side), if the object's owner is
consumed, so is the object itself and such reference becomes therefore
_unusable_.

In a dynamic language such as Lua and JavaScript, we can implement that
discipline with no-op proxies and weak maps/tables. Owners have their target
objects while clients acquire proxies for such target owned objects. Be aware 
that such thing relies on proper isolation of code, that is, pointers for such
owned objects are _unforgeable_ outside the owner's scope, clients must request
a proxy through some sort of factory API.

END
