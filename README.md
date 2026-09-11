# kotobase-federation

Kotobase-specific federation capability over immutable blocks and logical
checkpoints.

The initial extraction contains the replica availability challenge/response
kernel. It is deliberately distinct from the embedded-database meaning of
"peer": federation concerns replicas, signed heads, checkpoint convergence,
and injected transports. It does not own Datom or query semantics.

The availability proof is a replica-to-replica audit, not Filecoin PoRep/PoSt.
The verifier independently resolves the challenged bytes and compares the
salted response. Consensus/ref publication and real transports remain injected
capabilities rather than hidden storage assumptions.

```sh
kbb -M:test
kbb -M:lint
```
