# Changelog — hexa-ufo

All notable changes to `hexa-ufo` will be documented in this file.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/);
versioning follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] — 2026-05-06

### Added
- Initial extraction from `n6-architecture/domains/sf-ufo/` at SHA `c0f1f570`.
- 6-verb DOC-grade atlas: `ufo` (1890 LOC main atlas) + `grav` / `hover` /
  `cloak` / `teleport` / `sim` propulsion sub-axis docs.
- 7-stage propulsion stack table (Stage-1 Meissner → Stage-7 Calabi-Yau).
- `cli/hexa-ufo.hexa` standalone CLI router (verbs + status + selftest).
- `tests/test_atlas_consistency.hexa` — verb count + `L(k)=24^(k-15)`
  lattice arithmetic sanity.
- `examples/propulsion_stack.md` — 7-stage evolution table.
- Cross-link table to 4 sister substrate repos (`hexa-rtsc`, `hexa-fusion`,
  `hexa-antimatter`, `hexa-cern`).
- `install.hexa` hx hook (pre/post selftest).
- Auxiliary docs: `cross-domain-mega/`, `hypotheses/`, `experiments/`,
  `rtsc-12-products-evolution/`.

### Honest C3 caveats
- 6 verbs ship as DOC-grade (markdown atlases); no empirical sandbox.
- Propulsion Stages 4-7 (warp / wormhole / dim-jump / dim-use) are TBD —
  no public substrate exists yet.
- The 484-tier `L(k)=24^(k-15)` lattice is an arithmetic indexing convention,
  not an empirical claim.
- alien_index 6→500 spans verified engineering (Stages 1-3 sister repos)
  through pure conjecture (Stages 4-7).

[1.0.0]: https://github.com/need-singularity/hexa-ufo/releases/tag/v1.0.0
