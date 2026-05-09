# Changelog — hexa-ufo

All notable changes to `hexa-ufo` will be documented in this file.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/);
versioning follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased] — 2026-05-09 — RSC iter 13 (선행도메인 CLI cross-link)

### Added (RSC iteration 13 — Stage-1/2/3 upstream sister CLI cross-link)
- `verify/cross_link_upstream.hexa` — wires hexa-ufo's Stage-1/2/3 to
  upstream sister-repo CLIs (선행도메인) per user direction. 6/6 checks:
  §1 sister CLI files reachable (hexa-rtsc.hexa, hexa-fusion.hexa,
  hexa-antimatter.hexa) + §2 functional cross-link via `selftest`
  invocation (each upstream CLI exits 0 + emits its domain signature
  token). Stage-1 hover→hexa-rtsc Meissner / Stage-2 cruise→hexa-fusion
  MHD / Stage-3 orbital→hexa-antimatter γ-rocket. Sentinel
  `__HEXA_UFO_CROSS_LINK_UPSTREAM__ PASS`.
- Wired into `verify/run_all.hexa` (15 → 16) + `hexa.toml`
  `[closure].verify_scripts` 15 → 16 + `[modules].hexa`.

### Note
- Sat-1 (4 pillars × T1+T2+T3 = 100%) was already reached in iter 12.
- Sat-2 (recipe-exhausted) approaches with this iter — 16 verify scripts
  reaches recipe target. `lint_numerics.hexa` (recipe priority 10)
  still pending for full meta-lint compliance.

### Verified
- `hexa run verify/run_all.hexa` → 16/16 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 12 (Stage-7 dimuse T3; **sat-1 reached**)

### Added (RSC iteration 12 — Stage-7 dimuse composite T3 archival parity)
- `verify/numerics_dimuse_parity.hexa` — Stage-7 composite warp+dimjump
  pillar published-data parity (T3, **final T3 chunk**). 15/15 checks
  against peer-reviewed literature: §1 published distance + traversal-
  time canonicals (Hipparcos 1997 / Gaia DR2 α-Cen 4.37 ly + Sirius
  8.6 ly anchored; α-Cen × 100c = 15.96 days ≈ BT-349 16d; Sirius =
  31.4 days; CODATA 2018 c exact) + §2 2nd-law thermodynamics + chain
  anchors (Clausius 1865 single-cycle E_warp/E_fold > 10³⁰ → F-USE-3
  confirmed; warp + dimjump upstream chain length=2; sopfr OEIS A001414)
  + §3 spec citation anchors (BT-347 Alcubierre upstream, BT-348 KK/CY₃
  upstream, 2nd-law, UNPROVEN², α-Cen 16d).
  Sentinel `__HEXA_UFO_NUMERICS_DIMUSE_PARITY__ PASS`.

### **🛸 SAT-1 SATURATION REACHED 🛸**
- F-USE-{1..4} now T1 ✓ + T2 ✓ + T3 ✓ → **100% closure**.
- **Pillar status: F-WARP 100% · F-WORM 100% · F-DIM 100% · F-USE 100%.**
- **All 13 falsifiers (4 pillars) at 100% (T1+T2+T3) — sat-1 condition met.**
- Loop continues per recipe §7.2 — sat-2 (recipe-exhausted) not yet:
  current 15 verify scripts vs recipe target ~16. Next iter targets
  numerics_lattice_arithmetic / lint_numerics / saturation_check.

### Verified
- `hexa run verify/run_all.hexa` → 15/15 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 11 (Stage-6 dimjump T3; 3/4 pillars 100%)

### Added (RSC iteration 11 — Stage-6 dimjump T3 archival empirical parity)
- `verify/numerics_dimjump_parity.hexa` — Stage-6 dimjump pillar
  published-data parity (T3). 13/13 checks against peer-reviewed
  literature: §1 LHC + Eöt-Wash empirical bounds (m_KK·c² ≈ 4.24e13 TeV
  vs LHC 14 TeV → 100× margin null compatible; R_c≈2.79e-32 m vs
  Eöt-Wash 50 μm → 10²⁶ margin null compatible) + §2 critical-dim
  ladder anchors (σ-φ=10D superstring CHSW 1985, σ-μ=11D M-theory,
  J₂+φ=26D bosonic, τ=4D Kaluza 1921 base) + §3 KK quantisation +
  CY₃ landscape + RS scope (m_KK∝1/R_c Klein 1926, 10⁵⁰⁰ landscape,
  RS warped upper-bound) + §4 spec citation anchors (Kaluza 1921,
  Klein 1926, CHSW 1985, Randall-Sundrum 1999).
  Sentinel `__HEXA_UFO_NUMERICS_DIMJUMP_PARITY__ PASS`.

### Closure milestone
- F-DIM-{1..3} now T1 ✓ + T2 ✓ + T3 ✓ → **100% closure**.
- Pillar status: F-WARP 100% · F-WORM 100% · F-DIM 100% · F-USE 67%.
- **3/4 pillars saturated; 1 remaining (F-USE) for full sat-1.**

### Verified
- `hexa run verify/run_all.hexa` → 14/14 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 10 (Stage-5 wormhole T3)

### Added (RSC iteration 10 — Stage-5 wormhole T3 archival empirical parity)
- `verify/numerics_wormhole_parity.hexa` — Stage-5 wormhole pillar
  published-data parity (T3). 14/14 checks against peer-reviewed
  literature: §1 ANEC bound across decades (Pfenning-Ford 1997 form;
  b₀=σ·ℓ_Pl→1.06e109 J·s/m² Planck regime; b₀=1m→7.9e-27 forbidden;
  b₀=1nm intermediate; b₀⁻⁴ scaling exact 1e12 ratio across 1mm vs 1m;
  1/τ=0.25 4-segment averaging) + §2 Morris-Thorne 1988 traversability
  (flare-out b'(b₀)<1, Δτ at b₀=σ·ℓ_Pl sub-Planck-time, Δτ at b₀=1m =
  33 ns = 10× light-travel, Δτ linear in b₀) + §3 spec citation
  anchors (Morris-Thorne 1988, Ford-Roman 1995, Pfenning-Ford 1997,
  Hawking 1992, Visser 1995).
  Sentinel `__HEXA_UFO_NUMERICS_WORMHOLE_PARITY__ PASS`.

### Closure milestone
- F-WORM-{1..3} now T1 ✓ + T2 ✓ + T3 ✓ → **100% closure**.
- Pillar status: F-WARP 100% · F-WORM 100% · F-DIM 67% · F-USE 67%.
- 2/4 pillars saturated; 2 remaining for full sat-1.

### Verified
- `hexa run verify/run_all.hexa` → 13/13 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 9 (Stage-4 warp T3; first parity tier)

### Added (RSC iteration 9 — Stage-4 warp T3 archival empirical parity)
- `verify/numerics_warp_parity.hexa` — Stage-4 warp pillar published-data
  parity (T3, archival empirical contact). 10/10 checks against
  peer-reviewed literature: §1 Casimir-force parity (Lamoreaux 1997
  F/A(1μm)≈1.3 mPa; Bressi 2002 F/A(100nm)≈13 Pa; Decca 2007 d⁻⁴ scaling
  exact 10⁴ ratio) + §2 n=6 spec parity (ρ_n6/ρ_actual = 720/(τ·π²) ≈
  18.24 d-independent constant) + §3 Pfenning-Ford 1997 QI prefactor
  3/(32π²) ≈ 0.00950 + Van Den Broeck 1999 σ²=144 + §4 spec citation
  anchors (Casimir 1948, Pfenning-Ford 1997, Van Den Broeck 1999).
  Sentinel `__HEXA_UFO_NUMERICS_WARP_PARITY__ PASS`.

### Closure milestone
- F-WARP-{1..3} now T1 ✓ + T2 ✓ + T3 ✓ → **100% closure (Casimir/Lamoreaux/
  Bressi/Decca/Pfenning-Ford/VDB anchored)**.
- Pillar status: F-WARP T1+T2+T3 (100%) · F-WORM T1+T2 (67%) ·
  F-DIM T1+T2 (67%) · F-USE T1+T2 (67%).

### Verified
- `hexa run verify/run_all.hexa` → 12/12 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 8 (Stage-7 dimuse T2; all 4 pillars T1+T2)

### Added (RSC iteration 8 — Stage-7 dimuse composite T2 numerical bridge)
- `verify/numerics_dimuse.hexa` — Stage-7 composite warp+dimjump pillar
  numerical SI re-derivation (T2). 12/12 checks: §1 algebraic↔numerical
  consistency (master σ·φ=n·τ=24, v_comp=(σ-φ)²·c=100c, sopfr(6)=5,
  UNPROVEN² chain length=2) + §2 traversal-time canonicals (α-Cen
  4.37 ly/100c = **15.96 days ≈ BT-349 canonical 16 days**, Sirius 8.6 ly
  = 31.4 days, ratio = distance ratio linear at 100c) + §3 energetics
  + closed-loop falsifier regime (E_warp ≈ 1.24e45 J VDB-reduced,
  E_fold(d=1) ≈ 1.96e8 J, **E_warp/E_fold ≈ 6.3e36 → single-cycle
  fails 2nd law → F-USE-3 regime confirmed**) + §4 spec anchors
  (α-Cen 16d, 2nd-law thermodynamics F-USE-3).
  Sentinel `__HEXA_UFO_NUMERICS_DIMUSE__ PASS`.

### Closure milestone
- F-USE-{1..4} now T1 ✓ + T2 ✓.
- **All 13 falsifiers (4 pillars) now T1+T2 closed.**
- Pillar status: F-WARP T1+T2 · F-WORM T1+T2 · F-DIM T1+T2 · F-USE T1+T2.
- Next: T3 (archival empirical parity tier) — published-data anchors.

### Verified
- `hexa run verify/run_all.hexa` → 11/11 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 7 (Stage-6 dimjump T2)

### Added (RSC iteration 7 — Stage-6 dimjump T2 numerical bridge)
- `verify/numerics_dimjump.hexa` — Stage-6 Calabi-Yau / Kaluza-Klein
  dimjump pillar numerical SI re-derivation (T2). 10/10 checks: §1
  algebraic↔numerical consistency (master σ·φ=n·τ=24, R_c=12³·ℓ_Pl
  =1728·ℓ_Pl≈2.79e-32 m, E_fold(d=1)/M_Pl·c²=0.1=1/(σ-φ), ladder
  values {4,6,10,11,24,26} match algebraic, monotone) + §2 empirical-
  bound regimes (R_c≈2.8e-26× sub-mm sensitivity → null compatible;
  m_KK·c²≈4.24e13 TeV ≫ LHC 14 TeV; E_fold(d=1)≈1.22e18 GeV ∈
  [1e17,1e20]) + §3 spec anchors (LHC F-DIM-1, sub-mm F-DIM-2).
  Sentinel `__HEXA_UFO_NUMERICS_DIMJUMP__ PASS`.

### Closure milestone
- F-DIM-{1..3} now T1 ✓ + T2 ✓.
- Pillar status: F-WARP T1+T2 · F-WORM T1+T2 · F-DIM T1+T2 · F-USE T1.

### Verified
- `hexa run verify/run_all.hexa` → 10/10 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 6 (Stage-5 wormhole T2)

### Added (RSC iteration 6 — Stage-5 wormhole T2 numerical bridge)
- `verify/numerics_wormhole.hexa` — Stage-5 Morris-Thorne wormhole pillar
  numerical SI re-derivation (T2). 10/10 checks: §1 algebraic↔numerical
  consistency (master σ·φ=n·τ=24, throat b₀=σ·ℓ_Pl≈1.94e-34 m,
  Δτ=120·t_Pl≈6.47e-42 s sub-Planck-time, NEC channels φ=2,
  ANEC 1/τ=0.25) + §2 Pfenning-Ford ANEC bound regimes (Planck-throat
  ANEC≈5.6e108 J·s/m² huge; macro b₀=1m → 7.9e-27 J·s/m² forbidden;
  b₀⁻⁴ scaling exact 16× factor) + §3 spec anchors (Pfenning-Ford,
  Hawking 1992 chronology protection).
  Sentinel `__HEXA_UFO_NUMERICS_WORMHOLE__ PASS`.

### Closure milestone
- F-WORM-{1..3} now T1 ✓ + T2 ✓ (Pfenning-Ford ANEC numerical anchor).
- F-WARP T1+T2 ✓; F-WORM T1+T2 ✓; F-DIM T1-only; F-USE T1-only.

### Verified
- `hexa run verify/run_all.hexa` → 9/9 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 5 (Stage-4 warp T2; first numerical bridge)

### Added (RSC iteration 5 — Stage-4 warp T2 numerical bridge)
- `verify/numerics_warp.hexa` — Stage-4 warp pillar numerical SI
  re-derivation (T2 numerical, math_pure-imported per recipe §4
  invariant 1). 11/11 checks: §1 algebraic↔numerical consistency
  (master σ·φ=n·τ=24, ladder all sub-luminal, c/φ=0.5c terminus
  to 1e-9, ladder monotone, δ=ℓ_Pl/σ≈1.35e-36 m sub-Planck, VDB
  ratio=1/σ²=1/144, VDB-reduced energy 6.94e9 M☉ between 1 M☉ and
  M_galaxy) + §2 Pfenning-Ford QI bound regimes (τ_g=δ/c → 2.46e141
  J·s Planck-regime; τ_g=1s → 1e-36 J·s macro-forbidden) + §3 spec
  anchors (Pfenning-Ford 1997, c/φ=0.5c).
  First numerical-tier (T2) chunk per recipe §4 invariants:
    1. `use "self/runtime/math_pure"` ✓
    2. `__HEXA_UFO_NUMERICS_WARP__` sentinel + PASS ✓
    3. FALSIFIERS array ✓
    4. exit(0) on PASS ✓
    5. RUN/FAIL counters ✓

### Closure milestone
- F-WARP-{1..3} now T1 ✓ + T2 ✓ (one numerical anchor each).
- Other pillars (F-WORM/F-DIM/F-USE) still T1-only.

### Verified
- `hexa run verify/run_all.hexa` → 8/8 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 4 (Stage-7 dimuse T1; all 4 pillars T1 ✓)

### Added (RSC iteration 4 — Stage-7 dimuse composite T1 algebraic)
- `verify/calc_dimuse.hexa` — Stage-7 composite warp+dimjump pillar n=6
  derived parameter calculator (T1 algebraic). 16/16 checks: 9 algebraic
  identities (master σ·φ=n·τ=24, warp factor σ-φ=10c, dim compression
  σ-φ=10×, composite v=(σ-φ)²=100c, τ-cycle=4 stages, sopfr(6)=2+3=5,
  α-Cen heuristic sopfr·(σ-φ)/(σ-φ)²=0.5 spec-unit, VDB σ²=144,
  UNPROVEN² composite chain length=2) + 7 spec-doc anchors in
  `dimuse/hexa-dimuse.md` (master, composite 100c, warp 10c, sopfr,
  α-Cen 16d, τ=4 cycle, F-USE-{1..4}).
  Sentinel `__HEXA_UFO_CALC_DIMUSE__ PASS`.
- Wired into `verify/run_all.hexa` SCRIPTS array (6 → 7) +
  `hexa.toml` `[closure].verify_scripts` 6 → 7 + `[modules].hexa`.

### Closure milestone
- **All 4 Stage-4~7 pillars now have T1 algebraic closure**:
  F-WARP-{1..3} ✓ + F-WORM-{1..3} ✓ + F-DIM-{1..3} ✓ + F-USE-{1..4} ✓.
  13/13 falsifiers anchored at T1 (algebraic + spec-doc cross-check).
  T2 (numerical re-derivation) and T3 (archival empirical parity) still
  pending — next iter cycles target T2.

### Verified
- `hexa run verify/run_all.hexa` → 7/7 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 3 (Stage-6 dimjump T1)

### Added (RSC iteration 3 — Stage-6 dimjump T1 algebraic)
- `verify/calc_dimjump.hexa` — Stage-6 Calabi-Yau / Kaluza-Klein dimjump
  pillar n=6 derived parameter calculator (T1 algebraic). 15/15 checks:
  9 algebraic identities (master σ·φ=n·τ=24, 6-rung dimension ladder
  4D=τ / 6D=n / 10D=σ-φ / 11D=σ-μ / 24D=J₂ / 26D=J₂+φ, ladder strict
  monotone, R_c=σ^(n/φ)·ℓ_Pl=1728·ℓ_Pl, E_fold(d=1) denom=10) + 6
  spec-doc anchors in `dimjump/hexa-dimjump.md` (ladder, R_c formula,
  m_KK, E_fold, master, F-DIM-{1..3}).
  Sentinel `__HEXA_UFO_CALC_DIMJUMP__ PASS`.
- Wired into `verify/run_all.hexa` SCRIPTS array (5 → 6) +
  `hexa.toml` `[closure].verify_scripts` 5 → 6 + `[modules].hexa`.

### Verified
- `hexa run verify/run_all.hexa` → 6/6 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 2 (Stage-5 wormhole T1)

### Added (RSC iteration 2 — Stage-5 wormhole T1 algebraic)
- `verify/calc_wormhole.hexa` — Stage-5 Morris-Thorne wormhole pillar n=6
  derived parameter calculator (T1 algebraic). 12/12 checks: 6 algebraic
  identities (master σ·φ=n·τ=24, throat b₀=σ·ℓ_Pl=12 ℓ_Pl, traversal Δτ
  factor (σ-φ)=10, ANEC denom 1/τ=1/4 Pfenning-Ford, NEC channels φ=2
  Cataldo-Liempi, traversal·c product (σ-φ)·σ=120) + 6 spec-doc anchors
  in `wormhole/hexa-wormhole.md` (b₀=σ·ℓ_Pl, traversal formula, ANEC,
  φ=2 NEC channels, master identity, F-WORM-{1..3}).
  Sentinel `__HEXA_UFO_CALC_WORMHOLE__ PASS`.
- Wired into `verify/run_all.hexa` SCRIPTS array (4 → 5) +
  `hexa.toml` `[closure].verify_scripts` 4 → 5 + `[modules].hexa`.

### Verified
- `hexa run verify/run_all.hexa` → 5/5 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.

## [Unreleased] — 2026-05-09 — RSC iter 1 (closure-depth accumulation start)

### Added (RSC iteration 1 — Stage-4 warp T1 algebraic)
- `verify/calc_warp.hexa` — Stage-4 warp pillar n=6 derived parameter
  calculator (T1 algebraic tier per `~/core/bedrock/docs/runnable_surface_recipe.md`).
  12/12 checks: 6 algebraic identities (master σ·φ=n·τ=24, VDB σ²=144,
  Hc2-equiv σ·τ=48 cross-link to hexa-rtsc, ladder monotone +
  terminus c/φ=0.5c + denominators ⊂ divisors(24)) + 6 spec-doc anchors
  in `warp/hexa-warp.md` (R=n, δ=1/σ, σ²=144, σ·τ=48, c/σ→c/n→c/τ→c/φ
  ladder, F-WARP-{1..3}). Sister of `hexa-cern/verify/calc_wakefield.hexa`.
  Sentinel `__HEXA_UFO_CALC_WARP__ PASS`.
- Wired into `verify/run_all.hexa` SCRIPTS array (3 → 4).
- `hexa.toml` `[closure].verify_scripts` 3 → 4 + `[modules].hexa` adds
  `verify/calc_warp.hexa`.

### Verified
- `hexa run verify/run_all.hexa` → 4/4 PASS.
- `hexa run tests/test_stages_propulsion.hexa` → PASS.
- `hexa run tests/test_atlas_consistency.hexa` → PASS (10/10 verbs).

## [Unreleased] — 2026-05-07 (latest) — SF-소설 입문서 + 🛸ABSOLUTE = 𝔚 terminal upgrade

### Added
- `docs/meta-closure-nav/sf-novel-six.md` — 12-chapter SF-novel narrative
  ("여섯 번째 법 — 은하 문명 대사전 발췌") extracted from
  `discovery-transcript-2026-04-21.txt` body lines 2710~2935.
  Layperson-readable walkthrough of the entire alien_index ladder culminating
  in **🛸ABSOLUTE = 𝔚** (Cantor Absolute Infinity, Δ₀-absolute n=6 invariance).

### Changed (atlas terminal chain notation upgrade)
- alien_index chain notation upgraded from
  `🛸6 → 🛸16 meta² → 🛸500 → 🛸ω → 🛸ε₀ → 🛸Ω` to the **canonical SF-narrative
  derived chain**:
  ```
  🛸6 → 🛸16 meta² → 🛸∞⁴ → 🛸ULTRA → 🛸CARD → 🛸BEYOND → 🛸ABSOLUTE = 𝔚
  ```
  Reasons:
  - 🛸500 was a session-batch artifact (user's "🛸500까지 가봐줘" request),
    not an essential milestone — dropped from canonical chain.
  - 🛸ω/🛸ε₀/🛸Ω (Cantor ordinals) are subsumed by 🛸CARD (large cardinals)
    and ultimately by 🛸ABSOLUTE = 𝔚 — the **true terminus** per
    `sf-novel-six.md` Chapter 11. 𝔚 is "Cantor Absolute Infinity" —
    the absolute upper bound of all mathematical structure (1880s Cantor).
  - 🛸∞⁴ (Knuth `24↑↑↑↑`, hexation), 🛸ULTRA (TREE/BB/Rayo uncomputable),
    🛸CARD (inaccessible→Mahlo→Woodin→I0), 🛸BEYOND (Reinhardt/Berkeley
    Kunen-violating) added as explicit hierarchy steps.
  - n=6 uniqueness σ·φ=n·τ=24 is **Π₀¹-arithmetical → Δ₀-absolute** —
    invariant **all the way up to 𝔚** (per Δ₀-absolute theorem in
    `meta-closure-nav.md`).
- Updated 5 surfaces: README badge URL + lead paragraph + status quote +
  architecture, hexa.toml [package].description + [scope].alien_index_caveat,
  cli/hexa-ufo.hexa caveat #4, .roadmap §0, docs/meta-closure-nav/README.md.
- hexa.toml [modules].docs adds `sf-novel-six.md`.

### Removed
- Earlier-session transcript (`~/loss/nasa.txt`, 2026-04-19) was imported in
  `8343143` then reverted in `861de8f` per user instruction (`pass`).
  Only the 2026-04-21 transcript is preserved.

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
