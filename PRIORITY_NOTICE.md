# Priority notice

Dated: 2026-09-11

This repository anchors priority for the CG-MoE project's claims.
The claims are stated below in final-system language. They are
bound to sealed evidence by the hash manifest in
`EVIDENCE_MANIFEST.sha256` (manifest hash:
`8a5a2c3c895cd5bd15910bae8234b9809045d5b9b3bb35058509c4f8eebbd190`),
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
three prediction parts carry measurements); r4 `9b84fcd`
(abstract states the port-back to unconverted networks;
span-level r2 and intervention evidence sealed); r5 `d6ad73c`
(the data-starvation sentence measured - starved vs hard
patches separated on the audited network); r6 `bc627ba`
(pre-wormhole measurement marking pass; claims unchanged); r7
`b2c1dbc` (the fifteen-layer wormhole chain's decode battery
and zero-shot gate are measured and pass - the pending marker
becomes a result; RS-5 evidence sealed); r8 `258aa6e` (the
conversion instruments measured on a second modality - a
trained ViT's MLP blocks reproduce at R2 1.0 and substituting
all six leaves CIFAR-10 accuracy exactly the network's own;
GC-V1/GC-V2 evidence sealed); r9 `bf4bb1c` (the vision
key-attribution ladder measured - 0.7722 / 0.7695 / 0.7519 /
0.7235 at 3/4, 1/2, 1/4, 1/8 keys against 0.7732; GC-V3
evidence sealed); r10 (this commit: the closed-form field
classifier bounded - 36.1 percent against the convnet's 56.4
at matched parameters across all four registered levers;
known-limit 12 states the bound; V-E1 series evidence
sealed); r11 (this commit: readability and prior-art delta
pass - integration-back passages restated as measured deltas
over the linear-probe, deep-supervision, dataset-cartography,
and self-distillation lines, twelve citations added; internal
cell codes replaced by descriptive names; claims unchanged);
r12 (this commit: the transfer-back prediction framed as a
registered composition claim over its cited ingredients; the
serve-refit and training-target dose curves stated (2,300 vs
36,500 stream tokens; the target-weight sweep); claims
unchanged). r13 (this commit: the composed conversion
measured - int8-pack stages with the four-layer wormhole chain hold
the battery at 0.5547 against the teacher 0.5938 with perplexity 17.24
against 15.80; the mixed-cache and incremental-carrier serving ladders
measured, flat at 15 tokens per second from 1k to 8k context;
pc_wormhole_pack_battery, pc_speed_mixedcache, and pc_incremental_carrier
evidence sealed; the manifest re-binds lm_d4_gates to its appended
d4_mc_kmap arm, prior content unchanged). r14 (this commit: the cache metric restated in the published
convention of cache bytes per token held - the final form writes
128 KiB of key-value cache per token against the teacher 144, the
four carrier layers instead holding a fixed 0.14 MiB, or 13 MiB
incremental, that summarizes the whole prefix and drops nothing;
the abstract constant-memory wording corrected to scope the carrier
layers; the mixed-cache chain input stream disclosed at 5 KiB per
token; known-limit 8 states the deployment mitigation of routing
mathematics to external primitives, framed as a new formulation
with nothing claimed; claims otherwise unchanged). r15 (this commit: the prior-art pass for the wormhole
carrier and the incremental cache - the compressed-memory family
cited (Compressive Transformers, Infini-attention, Landmark
Attention, LM-Infinite, Dynamic Memory Compression, Mamba, RWKV),
the displacement stated as summarized-not-windowed with nothing
dropped; claims unchanged). r16 (this commit: the wormhole-vs-linear-attention relation
stated - the far field is a linear-attention recurrence with a
frozen hard-assignment kernel, while the retained set stays exact
softmax under one shared normalization (Katharopoulos and random
feature attention cited); claims unchanged). r17 (this commit: the delivered converted network is anchored -
the full Sprig conversion of Qwen3-4B (all thirty-six attention
layers on the wormhole carrier, all thirty-six feed-forwards as
int8-derived additive readouts) is bound by hash through
`SPRIG_ARTIFACT_ANCHOR.md` and through its shipped checksum file,
now listed in the manifest; the current whitepaper marks the
four-chain serving passages pending the full-carrier
re-measurement, presentation only; claims unchanged). r18 (this commit: the converted network made self-contained -
the retained base-model tensors (the token embedding with the
tied head, the norms and the attention projections, 2.5 GiB) now
ship inside the package, so the download is 4.6 GiB with nothing
else fetched and no base-model dependency at runtime; the
parts-loaded and base-loaded serving paths are gated bit-exact
against each other; the artifact digests are re-anchored (package
digest 44a886b9 over 53 files, checksums.json 9e9392de); the
model card gains a start-here section for users new to Hugging
Face; claims unchanged). r19 (this commit: the delivered
conversion restated on the adopted exact-window configuration -
band 512 with the ring grown to match: perplexity 18.56 against
the teacher's 15.80 on the forty-thousand-token slice, inside
the registered +5 flag (the sealed band-64 form read 31.37),
MMLU 0.5391 with boolq improved from 0.500 to 0.625; the exact
recent-window width is measured as the quality dial (64 / 128 /
192 / 256 / 512 rows read 31.37 / 25.29 / 23.17 / 21.12 /
18.56) at a cost of 72 MiB of fixed state, single-stream speed
unchanged at about 16 tokens per second, batched throughput
93.4 (batch 8) and 70.2 (batch 16) tokens per second; a
center-tracking variant measured inert (0.006); the continuation
repetition gate remains the measured limit at 0.04-0.85 against
the 0.21 bar; both papers' bibliographies were verified against
live records and repaired where wrong; artifact re-anchored
(package digest fa78d2bb over 54 files, checksums.json
6a0cd361); the model card and paper restate the numbers above). r20 (this commit: the cross-network map positioned against the nearest
lines - model stitching certified by use, relative representations, and
function-preserving transforms cited, with the instruments that read the
map itself stated against them (a per-layer correspondence census scored
against a shuffled-control floor, a closed-form lens fitted from paired
activations and scored on a held-out grid, an output-preserving
reconditioning under a warp-spectrum monitor with an identity control);
the superposition complexity line cited for the capacity side;  six
references added; claims unchanged). r21 (this commit: the transfer track is measured and stated in the paper - one closed-form read across paired networks: the validation (a real arm of +0.179 nats of the 0.597-nat gap with a rank-flat shuffled floor of +0.073 and +0.106 nats pairing-specific), the rank curve (+0.111 to +0.213 nats; captures 0.186 to 0.386), the coherence profile (no argmax-level steering; no induced repetition), donor economy (quality is not transferability; count is not the lever; a 0.10-nat donor screen), the differential artifact (40 to 77 MB against a 2,944 MB donor; +0.039/+0.045 nats on the coding domain), the mode gate (retention 1.00x; outside-domain change to zero), cluster-routed fits (+0.044 capture over the global fit, a shuffled-assignment control at +0.2345), and the seed special case specified as the production receiver; the abstract, introduction, conclusion and open-measurements list extend to four tracks; seventeen transfer-track evidence files sealed;  the claims list gains the transfer claim). r22 (this commit: the mode gate's mixed-stream measurement stated - gate accuracy 0.983 across eight coding/wiki block alternations; the domain gain retained and larger than on the pure stream (+0.064/+0.087 nats at ranks 128/256); the outside-domain change within 0.006 nats; the hard and soft gates identical under saturated discrimination; the transition band measured at sixteen positions; and the theme-concentration criterion restated at the composition level - a temporary cost at the concentration step is admissible if the seed-with-patches composition recovers it, measured as seed-plus-concentration-plus-patches against seed-plus-patches at a matched budget; claims otherwise unchanged).

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
   compound. Composed with the int8-pack stages over all
   thirty-six layers, the delivered converted network holds the
   binding battery at 0.5391 against the teacher's 0.5938 with
   perplexity 18.56 against 15.80 on the forty-thousand-token
   slice; the four-layer intermediate held 0.5547 and 17.24.
   The width of the exact recent window is the measured quality
   dial (31.37 at 64 rows to 18.56 at 512, at a fixed state size
   per row). The form serves with a fixed 0.19 GiB state at any
   context, and the continuation repetition gate remains its
   measured limit.
4. The epistemic layer is separable from the conversion: the
   per-patch instruments (fit error, coverage, novelty) attach
   to any conventionally trained network without converting it.
   Measured by the audit shadow on a never-converted teacher,
   with per-layer readings matching across devices exactly.
5. One trained network's behavior can be read into another, frozen,
   through one closed-form solve of paired states: the
   pairing-specific transfer is +0.106 nats of a 0.597-nat gap
   (rank-128 real arm +0.179 with a rank-flat shuffled floor of
   +0.073), the read is a distributional recalibration rather than
   an argmax-level steering, donor quality is not transferability
   and donor count is not the lever (a same-family pair overlaps
   about 70 percent), and the transfer ships as a domain
   differential tens of megabytes against a gigabytes-scale donor
   with a mode gate that holds outside-domain behavior fixed. The
   intended production receiver is the project's own from-scratch
   seed.

6. The prediction, stated with its instruments named: the
   serve-refit law detaches from the conversion (a per-layer
   closed-form refit on a network's own served stream is a
   maintenance step for any network), and local least-squares
   targets can be inserted into training itself.

## Anchoring

This notice is anchored by the git commit that contains it,
posted publicly as of that commit's timestamp. External anchors
reference this repository and commit.
