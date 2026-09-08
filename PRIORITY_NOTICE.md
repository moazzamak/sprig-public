# Priority notice

Dated: 2026-09-08

This repository anchors priority for the CG-MoE project's claims.
The claims are stated below in final-system language. They are
bound to sealed evidence by the hash manifest in
`EVIDENCE_MANIFEST.sha256` (manifest hash:
`52ffa7a8de3fb656946f0c06c8886a7b0904008aaf23cb0ac42f7218918d039d`),
which lists the sha256 of the whitepaper
(`PAPER_ADDITIVE.tex`) and of each sealed evidence file. The
evidence files themselves remain private until the project's own
publication schedule; the hashes bind any later disclosure to
this date.

Amendments are recorded as subsequent commits of this
repository; each commit's SHA is an anchor for the revision it
contains. Revisions: r1 `0b2f2860` (initial claims); r2
`c8ad70b` (audit shadow and serve-refit measured); r3
`6ea5dc4` (the training-side leg measured at small scale - all
three prediction parts carry measurements); r4 (this commit:
abstract states the port-back to unconverted networks;
span-level r2 and intervention evidence sealed).

## Claims

1. A pretrained transformer's pointwise feed-forward layers can
   be converted, layer by layer, into closed-form frozen-key
   stages - the layer's own gate and up directions as keys, one
   ridge solve as the readout - that reproduce the layer's
   function on held-out rows (R^2 1.0 at full keys), with the
   residual structure, norms, positions, and head kept verbatim.
2. The conversion carries a measured property set: exact
   per-stage attribution, deterministic replay, growth by frozen
   addition, and gated composition - properties a
   gradient-trained network does not have.
3. Mid-model softmax attention can be converted to a
   training-free retrieval carrier (sink, local band, routed
   clusters exact; diffuse mass summarized as a monopole),
   admitted only through exactness, census, perplexity, and
   decode gates, and measured as a chain whose error does not
   compound.
4. The epistemic layer is separable from the conversion: the
   per-patch instruments (fit error, coverage, novelty) attach
   to any conventionally trained network without converting it.
   Measured by the audit shadow on a never-converted teacher,
   with per-layer readings matching across devices exactly.
5. The prediction, stated with its instruments named: the
   serve-refit law detaches from the conversion (a per-layer
   closed-form refit on a network's own served stream is a
   maintenance step for any network), and local least-squares
   targets can be inserted into training itself.

## Anchoring

This notice is anchored by the git commit that contains it,
posted publicly as of that commit's timestamp. External anchors
reference this repository and commit.
