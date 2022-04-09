# Owners-as-Traders

Ownership transference (either upgrade or downgrade) and borrowing are often 
unidirectional. In this discipline, we propose a bidirectional approach, that
is, to release ownership, you must acquire another ownership in exchange. This
exchange involves two parties (that is, owners), one propose the trade and the
other can agree or refuse the trading. Note that who is making the request will
accept any ownership in exchange, we are not concerned with any details of the
exchange, and who is proposing the trade should know exactly what the other
partner is offering in exchange. There are two kinds of ownership releasing,
either permanent (that is transference) and temporary (in the case, borrowing).
We can also sketch such temporary counterpart of trading, the parties can just 
trade again the previously exchanged ownership titles to "dismiss" the previous
trade. Transference can be encoded with a fresh useless/empty object being
exchanged, after that transaction, this useless object will be discarded and
collected anyways.

Owners-as-traders can be really interesting in the context of distributed
computing, MMORPGs and economic simulations. The mutually exclusive ownership
concept catches very well the idea of resource allocation with a given net of
players, surely it is useful in Game Theory. The implementation of such
ownership policy can use two channels of communication, such channels will
synchronize actors/threads until the exchange is performed or either cancelled.
