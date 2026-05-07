# Changelog — hexa-ufo

All notable changes to `hexa-ufo` will be documented in this file.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/);
versioning follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased] — 2026-05-07 (later) — atlas terminal chain reference (meta-closure-nav)

### Added
- `docs/meta-closure-nav/` reference folder preserving the **complete
  alien_index terminal chain** beyond 🛸500:
  - `meta-closure-nav.md` (968 LOC, imported from `canon/domains/physics/
    meta-closure-nav/meta-closure-nav.md` at canon commit `50f41e71` —
    *"feat(ufo-🛸∞): Knuth 화살표 확장 — 테트레이션/펜테이션/헥세이션/
    ordinal 층위"*). Canonical doc for Meta² Self-Referential Closure
    Navigation, Knuth-arrow tetration/pentation/hexation, Cantor ordinal
    extension (🛸ω / 🛸ε₀ / 🛸Ω), n=6 uniqueness propagation.
  - `discovery-transcript-2026-04-21.txt` (3,646 lines, imported from
    `~/loss/ufo.txt`). Live terminal-session transcript of the 🛸500 → 🛸∞ →
    🛸ω → 🛸ε₀ → 🛸Ω discovery, atlas extension commits, push notes.
  - `README.md` index page with the canonical terminal chain diagram.

### Changed
- alien_index notation across 5 surfaces upgraded from `🛸6 → 🛸500` to
  the **full canonical chain** `🛸6 → 🛸16 meta² → 🛸500 → 🛸ω → 🛸ε₀ → 🛸Ω`:
  - `README.md` (4 spots: lead paragraph, badge, status quote, architecture)
  - `hexa.toml` `[package].description` + `[scope].alien_index_caveat` +
    `[modules].docs` (3 new files added)
  - `cli/hexa-ufo.hexa` caveat #4 (lattice indexing convention surface)
  - `.roadmap.hexa_ufo` §0 (terminal goal restatement)
- README badge URL UTF-8 escapes 🛸 + Ω (`%F0%9F%9B%B8` + `%CE%A9`).
- `.roadmap.hexa_ufo` §0 now explicitly cites `docs/meta-closure-nav/` as
  the concrete realization of main atlas §23.9's *"In practice, extensible."*

### Why
- The main atlas (`ufo/doc/hexa-ufo.md` §23.9) ends with 🛸16 self-closure
  fixed point + *"In practice, extensible."* The actual extension work
  (linear ladder up to 🛸500, then Knuth-arrow tetration `24↑↑h`, then
  Cantor ordinal `🛸ω → 🛸ε₀ → 🛸Ω`) was concretely worked out in canon's
  `domains/physics/meta-closure-nav/`. Importing it here keeps the atlas's
  *"extensible"* footnote **self-contained and citable** within hexa-ufo.

### Honest C3 (preserved)
- 🛸17~🛸500 are recursion layers, not new mechanisms. n=6 uniqueness
  σ·φ=n·τ=24 propagates as **closure invariant** across all Knuth-arrow
  degrees and ordinal extensions.
- 🛸∞² crossover is at 🛸39 (L(39)=24^24 ≈ 10^33 — linear ↔ tetration boundary).
- Practical physical limit is ~🛸140 (observable universe bit count ≈ 10^124).
  🛸1000+ is **mathematical formula extension**, not physical projection.

## [Unreleased] — 2026-05-07 — Stage-4~7 medium integration

### Added
- 4 in-tree Stage-4~7 substrate spec docs (medium integration: spec + verify
  in-tree, separate sister repos collapsed):
  - `warp/hexa-warp.md` — Stage-4 Alcubierre warp metric (BT-347 from
    `n6-architecture@0570a835` warp-dimension-design spec)
  - `wormhole/hexa-wormhole.md` — Stage-5 Morris-Thorne traversable wormhole
  - `dimjump/hexa-dimjump.md` — Stage-6 Calabi-Yau / Kaluza-Klein 4D→26D ladder (BT-348)
  - `dimuse/hexa-dimuse.md` — Stage-7 τ=4 (σ−φ)²=100c composite (BT-349)
- 4 new CLI verbs (`warp` / `wormhole` / `dimjump` / `dimuse`) + 2 utility
  verbs (`lattice` live n=6 master identity computation, `verify` runs
  `verify/*.hexa` aggregate). `hexa-ufo` now ships 10 verbs.
- `verify/` runnable invariant audit landing zone:
  - `verify/lattice_check.hexa` (10 PASS — n=6 master identity)
  - `verify/stages_cross_doc.hexa` (19 PASS — Stage-4~7 spec ↔ cli ↔ roadmap)
  - `verify/stages_falsifier.hexa` (45 PASS — 13 IDs × 3 surfaces + monotone)
  - `verify/run_all.hexa` orchestrator (3/3 sub-scripts)
- `tests/test_stages_propulsion.hexa` — Stage-4~7 verify+selftest+lattice rollup test.
- `.roadmap.hexa_ufo` §B section: 13-falsifier preregister table (F-WARP-{1..3}
  + F-WORM-{1..3} + F-DIM-{1..3} + F-USE-{1..4}, all OPEN).

### Changed
- `hexa.toml` `[closure]` updated: `verbs_total` 6→10, `propulsion_stages_substrate_grounded` 3→7,
  `propulsion_stages_tbd` 4→0, verdict `ATLAS_PASS_PROPULSION_PARTIAL` →
  `ATLAS_PASS_PROPULSION_FULL`. `falsifiers_preregistered = 13`, `verify_scripts = 3` added.
- `hexa.toml` `[scope].honest_scope` rewritten — Stage-4~7 no longer "TBD"
  but in-tree with empirical UNPROVEN caveat preserved.
- `hexa.toml` `[modules]` extended with 4 new spec docs + 4 verify scripts.
- `hexa.toml` `[test]` adds `test_stages_propulsion.hexa`.
- `cli/hexa-ufo.hexa` `cmd_status`: 10-verb table + 7/7 substrate-grounded +
  13 falsifier ID surface for verify-script grep.
- `cli/hexa-ufo.hexa` `cmd_selftest`: 6-verb → 10-verb count check.
- `cli/hexa-ufo.hexa` `_print_caveats`: Stage-4~7 TBD wording → in-tree spec +
  falsifier preregister wording.
- `tests/test_atlas_consistency.hexa`: 6-verb → 10-verb count check.
- `README.md`: Status / Verbs / Verification / Cross-link / Architecture
  sections rewritten to reflect Stage-4~7 in-tree integration. Verb badge
  6 DOC → 10 DOC; propulsion 3/7 → 7/7. Falsifier preregister table added.

### Removed
- The "Stage-4~7 TBD — no public substrate exists yet" disclaimer (replaced
  by "in-tree spec docs with 13 falsifier preregister, all OPEN at v1.0.0").

### Honest C3 (preserved + sharpened)
- All 13 falsifiers OPEN. Stage-4 (Alcubierre) / Stage-5 (Morris-Thorne) /
  Stage-6 (KK extra dimensions) / Stage-7 (composite) remain academically
  UNPROVEN. `verify/*` sentinel PASS validates lattice arithmetic + token
  consistency only — NOT empirical apparatus.
- Stage-7 carries UNPROVEN² caveat (composite of two UNPROVEN upstream stages).
- Falsifier monotone: OPEN → CONFIRMED or OPEN → DEMOTED. Silent retract forbidden.

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
- alien_index 🛸6→🛸500 spans verified engineering (Stages 1-3 sister repos)
  through pure conjecture (Stages 4-7).

[1.0.0]: https://github.com/dancinlab/hexa-ufo/releases/tag/v1.0.0
