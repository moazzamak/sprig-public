# Sprig converted-network anchor (r19)

Dated: 2026-09-10

The delivered converted network for Qwen3-4B (the "Sprig"
conversion) is anchored here by hash, so the bytes of the artifact
are fixed as of this date.

## What the artifact is

The full conversion of Qwen3-4B: all 36 attention layers replaced
by the wormhole carrier (fixed state per layer - a sink row, a
512-row exact ring, a 512-row exact band, 64 farthest-point cluster
centers and the running per-cluster value sums; no key-value cache
anywhere in the forward pass) and all 36 feed-forward layers
replaced by int8-derived additive readout packs. The package also
ships the retained base-model tensors (token embedding with the
tied head, the norms and the attention projections, 2.50
GiB), so the artifact is self-contained: nothing else is
downloaded. A standalone CLI applies the conversion on load,
verifies every shipped file against `checksums.json` and
generates greedily.

Reference-machine serving (Radeon RX 9070 XT, ROCm): about 16
tokens per second single stream at 4k-8k context (12.3 / 16.1 /
15.6 / 11.9 at 1k / 4k / 8k / 16k), 93.4 at batch 8 and 70.2 at
batch 16, about 9.9 GiB of reserved GPU memory including
activations. The quality battery for this form is sealed in the
private repository
(`analysis/pc_fullcarrier_battery_band512r512_2026-09-10.json`)
and is not restated here.

## The binding

- `checksums.json` sha256 (`6a0cd361cadeb435a3df2dd03334553b0cad61904c29344b891968ec2a252acc`):
  this file lists the sha256 and byte size of each of the
  54 other shipped files (4.55 GiB total, of which
  2.05 GiB are the 36 packs and 2.50 GiB the
  retained base-model tensors).
- package digest
  (`fa78d2bb748bff02f869b9f67e627c39a4ca0280c18ff381f7968c58a3e0c816`):
  sha256 over the concatenation, in name-sorted order, of the
  `{sha256} *{file}` lines of those 54 entries.
- `EVIDENCE_MANIFEST.sha256` lists the `checksums.json` hash, so
  the manifest hash embedded in `PRIORITY_NOTICE.md` binds every
  byte of the artifact transitively:
  manifest -> checksums.json -> each shipped file.
- Built from the main-repository commit `92d34e8` (2026-09-10).

## Checking

    cd exports/sprig-qwen3-4b-wormhole-v1
    python serve_incremental.py --check

reports `checksums: 54 checked, 0 bad` when the artifact
is intact. The same sha256 values are what Hugging Face records
for the published copy of these files.
