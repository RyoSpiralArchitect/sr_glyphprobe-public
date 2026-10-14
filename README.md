# Beyond Short Names

**Emoji Keyword Retrieval across Models and Bounded Causal Tests**

Ryo Higa · GlyphProbe

[日本語](README.ja.md) · [Paper PDF](releases/v1.0.0/paper/preprint.pdf) ·
[Experiment guide](releases/v1.0.0/paper/EXPERIMENT_GUIDE.md) ·
[Current claim boundaries](releases/v1.0.0/paper/CURRENT_CLAIMS_20261015.md)

## What the study shows

The study separates information readable from hidden states from the causal
conclusions supported by specific interventions. Emoji provide a controlled,
text-only case; CLDR keywords are lexical targets, not human meaning labels.

- **Keyword retrieval (T19-L):** across nine prespecified model–tokenizer
  configurations, raw emoji retrieve word-disjoint CLDR keywords better than
  literal codepoint spellings under the specified unrestricted and exact
  four-view token-count-matched analyses. The primary partial-conjunction p-value is
  0.0027.
- **Fixed and optimized subspace interventions (T19-C/T20-C):** the tested
  rank-8 accounts do not meet their joint causal criteria; the optimized test
  is uncalibratable at both primary sites. This does not rule out every
  low-rank account.
- **Attention-path intervention after readout reset (T21-C):** on 195 items,
  glyph-position messages contribute to keyword cosine margins under the
  specified reset. All five simultaneous lower bounds are positive; absolute
  disruption and restoration have zero mean top-1 effects.
- **Text-only readout qualification:** 32 authored facts yield 88/96 correct
  reserved direct/minimal answers and 104/192 correct A/B answers. Both
  prespecified requirements fail. Question and answer encoding remain material
  measurement limitations before contextual emoji interpretation is claimed.

These results establish neither rendered-glyph perception, independent human
semantic validity, nor a mechanism for ordinary generated responses.

## Paper and release status

This is a revised preprint incorporating reviewer feedback from the NeurIPS
2026 workshop **Interpretability as a Science (InterpScience)**. It is not an
accepted workshop or proceedings paper. Zenodo DOI **`10.5281/zenodo.23376699`
is reserved; registration and public deposit are not yet asserted here**.
The new curated repository `sr_glyphprobe-public` is prepared for publication;
this status paragraph will be updated after external publication is verified.
The package manifests record pre-publication preparation and remain distinct
from subsequently verified live publication metadata.

## Evidence and replay

The versioned payload is in [`releases/v1.0.0/`](releases/v1.0.0/). Read the
[release and replay guide](releases/v1.0.0/paper/PUBLIC_RELEASE_20261015.md)
for exact included files, exclusions, dependencies, and historical replay scope.
To verify the payload hashes and replay the new qualification's saved scores:

```bash
cd releases/v1.0.0
python3 -S -B paper/scripts/build_public_release_20261015.py verify .
```

This check uses Python's standard library, runs no model, and compares two
arithmetic implementations on the recorded scores. It does not reacquire GPU
logits. Fixed/optimized-subspace results have summary-only coverage, not complete
item-level inference replay. Private author responses and model/tokenizer
weights are excluded.

This is an independent, allowlisted release repository, not a mirror of the
original private repository or its full source history. The original history
is not published here. Keep the versioned payload unchanged when verifying it.

## Licenses

The current paper, original paper-specific figures, and newly released public
data are CC BY 4.0 for the author's rights. Code and ordinary project
documentation retain Apache 2.0. Third-party and historical notices remain
controlling; see the [scope-specific license guide](releases/v1.0.0/paper/PUBLIC_LICENSES_20261015.md).

