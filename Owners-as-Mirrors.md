# Owners-as-Mirrors

This discipline restricts reflection over the owned object. Here, only the 
owner can perform introspection, self-modification and intercession on given
owned object. Instead of the common idea of owned mirrors (which can be
transferred or borrowed), this discipline embodies the mirror capabilities on 
the owner itself, thus, reducing the number of mirrors as it is usually known
in the mirrors-as-owned counterpart.

Every kind of reflection performed by other party must beforehand pass through
the owner, so some proper care must be used here. If the owner is
lured/confused by an attacker, this attacker gains full authority over all the
owned capabilities! In one hand, the owner is carrying too much authority, on
the other hand, reflection is exclusive meaning that only one party can reflect
over some object in one time (only if multiple ownership is not assumed here).
Through owners-as-collectors or owners-as-modifiers, reflection is not
exclusive per object when we instead take the mirrors-as-owned approach/policy.
