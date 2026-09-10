# Sprig converted-network anchor (r18)

Dated: 2026-09-10

The delivered converted network for Qwen3-4B (the "Sprig"
conversion) is anchored here by hash, so the bytes of the artifact
are fixed as of this date.

## What the artifact is

The full conversion of Qwen3-4B: all 36 attention layers replaced
by the wormhole carrier (fixed state per layer - a sink row, a
256-row exact ring, a 64-row exact band, 64 farthest-point cluster
centers and the running per-cluster value sums; no key-value cache
anywhere in the forward pass) and all 36 feed-forward layers
replaced by int8-derived additive readout packs. The package also
ships the retained base-model tensors (token embedding with the
tied head, the norms and the attention projections, 2.50
GiB), so the artifact is self-contained: nothing else is
downloaded. A standalone CLI applies the conversion on load,
verifies every shipped file against `checksums.json` and
generates greedily.

Reference-machine serving (Radeon RX 9070 XT, ROCm): 16.0 tokens
per second single stream, 126.4 at batch 8 and 169.6 at batch 16,
about 10 GiB of reserved GPU memory including activations. The
quality battery for this form is sealed in the private repository
(`analysis/pc_fullcarrier_battery_2026-09-10.json`) and is not
restated here.

## The binding

- `checksums.json` sha256 (`9e9392dee9e892b69e7ac61589875670adc0d75fe433156049bab7950fb9c922`):
  this file lists the sha256 and byte size of each of the
  53 other shipped files (4.55 GiB total, of which
  2.05 GiB are the 36 packs and 2.50 GiB the
  retained base-model tensors).
- package digest
  (`44a886b903877a5bb94e00799b76b87477435c261ab3bd26ac7099522a8ec1b3`):
  sha256 over the concatenation, in name-sorted order, of the
  `{sha256} *{file}` lines of those 53 entries.
- `EVIDENCE_MANIFEST.sha256` lists the `checksums.json` hash, so
  the manifest hash embedded in `PRIORITY_NOTICE.md` binds every
  byte of the artifact transitively:
  manifest -> checksums.json -> each shipped file.
- Built from the main-repository commit `b2d5e55` (2026-09-10).

## Checking

    cd exports/sprig-qwen3-4b-wormhole-v1
    python serve_incremental.py --check

reports `checksums: 53 checked, 0 bad` when the artifact
is intact. The same sha256 values are what Hugging Face records
for the published copy of these files.
