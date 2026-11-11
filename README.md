# Prime Survival in Affine Collatz Dynamics

**Paper X — v20**

A study of prime survival under the general affine map φ_{a,b,c}(p) = (ap+b)/c, of which the Collatz map φ(p) = (3p+1)/2 is the special case a=3, b=1, c=2.

> This repository does not claim a proof of the Collatz conjecture.

---

## Erratum (2026-11-12)

- **"c-B exits in at most 2 steps" (Section 2, Lemma 1) is false.** Example: 95 -> 143 -> 215 -> 323 -> 485 stays composite and in pattern c for three steps. The correct statement is simpler and covers every case: since (3n+1)/2 + 1 = 3(n+1)/2, any n = 3 (mod 4) leaves pattern c after exactly v2(n+1) - 1 steps.
- **An infinite chain under p -> (3p+1)/2 does not exist**, for the same reason. The item "infinitude of the chain (Bateman-Horn level)" in the list of open problems should read: existence of arbitrarily long finite prime chains, which for each fixed length would follow from Dickson's conjecture.
- Unaffected: monotone growth, admissibility, the rho(q) classification, the general admissibility theorem, and the numerical sections.

The PDF in `paper/` is the original, uncorrected version.

---

## Overview

This paper develops a rigorous local obstruction theory for prime survival under affine Collatz-type maps, together with sieve heuristics and numerical verification.

The central results are:

- **Complete ρ(q) classification** for general φ_{a,b,c}: the local sieve density depends entirely on divisibility conditions among a, b, c, q
- **General admissibility theorem**: local obstruction is absent whenever q ∤ a
- **Numerical experiments** (v20, N ≤ 50,000): the sieve-passage count for the Collatz map matches the predicted asymptotic 2.527N/(ln N)² at ratio ≈ 0.98
- **Seven map families** tested: qualitative trends confirmed, with limitations of the density constant formula identified for c=1 maps

---

## Main Results

### Proved (Rigorous)

| Result | Method | Status |
|--------|--------|--------|
| c-A / c-B finite escape (Collatz) | Congruence | corrected: exit after exactly v2(n+1) − 1 steps, see Erratum |
| Admissibility (Collatz) | Congruence | ✓ proved |
| Monotone growth of φ-chains | Direct computation | ✓ proved |
| ρ(q) = 1 (Collatz, q ≥ 5) | Congruence | ✓ proved |
| ρ(q) complete classification (general) | Divisibility conditions | ✓ proved |
| General admissibility theorem | q ∤ a → no local obstruction | ✓ proved |

### Numerical (v20)

| Result | Evidence |
|--------|----------|
| Collatz: sieve-passage / predicted ≈ 0.98 | N = 50,000 |
| General maps: C_{a,b,c} formula captures qualitative trends | 7 map families |
| (5p+1)/2 and (7p+1)/2: ratio ≈ 1.0 | High precision match |
| c=1 maps (twin prime, Sophie Germain): ratio ≈ 1.5–2.6 | Formula underestimates |

### Conjectural

```
#{p ≤ N : φ(p) ∈ P2} ~ 2.527 · N / (ln N)²
```

Numerically supported. Not proved. Requires independence assumptions.

---

## Structure

```
§2   c-classification (Collatz)              ✓
§4   Monotone growth                         ✓
§6–7 Admissibility + ρ(q)=1 (Collatz)       ✓
§8   ρ(q) complete classification (general)  ✓
§9   General admissibility theorem           ✓
§10  Density constant C_{a,b,c}, W(z)        heuristic
§11  Numerical experiment I (Collatz)        ★ v20
§12  Numerical experiment II (general maps)  ★ v20
§13  Connection to Collatz conjecture        open
```

---

## Open Problems

- Error term control (requires Bombieri–Vinogradov type estimates)
- Infinite existence of P2 primes
- Refinement of C_{a,b,c} formula for c=1 maps
- Connection to the full Collatz conjecture (§13)

---

## Repository Structure

```
collatz-prime-survival/
├── README.md
├── paper/
│   └── prime_survival_affine_collatz_v20.pdf   — full paper
└── LICENSE
```

---

## Related Work

This paper is part of a series on Collatz dynamics:

- [collatz-renewal-structure](https://github.com/KAMANOI/collatz-renewal-structure) — Paper A: exact renewal structure and operator theory
- [collatz-finite-mixing-geometry](https://github.com/KAMANOI/collatz-finite-mixing-geometry) — Paper B: finite-level mixing geometry
- [collatz-spectral-amplification](https://github.com/KAMANOI/collatz-spectral-amplification) — Paper C: spectral amplification
- [collatz-scale-coherence](https://github.com/KAMANOI/collatz-scale-coherence) — Paper D: scale-coherence rigidity

---

## Author

Hiroki Kamanoi  
hirokikamanoi@gmail.com  
2026

---
Related research and services by HDR (Human Driven Reality): https://hdr-ai.com/#research
