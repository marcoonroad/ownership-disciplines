# Owners-as-Prototypes

In this discipline, cloning is a private operation and the only one way to
create objects. All object creation, so, pass through the self-send
`self.clone { … }` operation, where `{ … }` are the additional/extension 
slots for the child/owned object. Without any kind of ownership
releasing/transference beforehand, the owner will only own objects resembling
himself. Cloning is assumed to be concatenative, if it were "delegative",
owned/child objects would be able to observe effects implicitly from the
owner/prototype, a really undesirable thing for sure.

It can be achieved by making  cloning the only one possible operation to 
allocate memory in the system (besides making cloning a private operation, that
is, an operation available only for the object itself). Cloning indirectly is
also possible, the owner just need to expose a method performing cloning
internally for its own owner (i.e, owner's owner).
