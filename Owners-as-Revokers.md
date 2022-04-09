# Owners-as-Revokers

This discipline states that owners can control the access for their owned
objects. These objects can be leaked and accessed (and even changed) outside 
the associated owner domain, but once the owner revokes the access for some
specific subject, it must perform a new request for that owner to be able to
access again the owned object. If the owner refuses the request, the subject
will not be able anymore to access such owned object. Such revocation can be
made through a kind of black-list.
