# Priority notice

Dated: 2026-09-10

This repository anchors priority for the CG-MoE project's claims.
The claims are stated below in final-system language. They are
bound to sealed evidence by the hash manifest in
`EVIDENCE_MANIFEST.sha256` (manifest hash:
`848bf27aeb9da39a200d765c913d7bdb27567a8eb7c0b292ba83123cb9cedb07`),
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
Face; claims unchanged).

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
   compound. Composed with the int8-pack stages, the full converted
   network holds the binding battery at 0.5547 against the
   teacher's 0.5938 with perplexity 17.24 against 15.80,
   and its incremental-carrier form serves at constant
   memory with a flat speed ladder.
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
