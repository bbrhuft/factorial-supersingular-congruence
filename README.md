# A factorial supersingular congruence and signed discriminant ratios

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24120141.svg)](https://doi.org/10.5281/zenodo.24120141)

**David Jordan** · Maynooth University Social Sciences Institute (MUSSI), Maynooth University · Manuscript v2.0, 9 November 2026

> This paper was split from the combined manuscript *A factorial supersingular congruence and signed discriminant ratios* (v1.13), whose Fricke-Hauptmodul application now forms a separate companion paper, *Supersingular poles and signed residues of prime-level Fricke Hauptmoduln*, in [bbrhuft/fricke-signed-residues](https://github.com/bbrhuft/fricke-signed-residues). The combined versions remain archived on Zenodo: v1.11 ([10.5281/zenodo.24024359](https://doi.org/10.5281/zenodo.24024359)) and v1.13 ([10.5281/zenodo.24084789](https://doi.org/10.5281/zenodo.24084789)).

## About the paper

Let $`p \ge 5`$ be prime, $`h = (p-1)/2`$ and $`k = (p^2-1)/24`$. Baker's supersingular congruence determines the *square* of a ratio formed from $`E_{p+1}`$ and $`\Delta`$. The paper evaluates the ratio itself: on the supersingular locus it equals a factorial times a Legendre symbol, the same for every supersingular elliptic curve. Combined with Robert's isogeny identity, this fixes the half-exponent sign of the discriminant ratio along every prime-to-$`p`$ isogeny. Neither result needs a genus-zero hypothesis.

### Main results

**Theorem 1.1 (supersingular factorial evaluation).** For every prime $`p \ge 5`$,

```math
E_{p+1}^{(p-1)/2} \equiv \left(\frac{6}{p}\right)\left(\frac{p-1}{2}\right)!\,\Delta^{(p^2-1)/24} \pmod{(p, E_{p-1})}.
```

The proof applies an iterated theta operator to $`\eta^{p+1}`$, and Euler's pentagonal identity determines the sign.

**Corollary 1.2 (constancy and Baker's congruence).** The ratio $`c(E) = E_{p+1}(E)^h / \Delta(E)^k`$ takes the single value $`c_p = \left(\frac{6}{p}\right) h!`$ at every supersingular $`E`$. Squaring gives $`c_p^2 = -\left(\frac{-1}{p}\right)`$, which recovers Baker's congruence.

**Theorem 1.3 (signed discriminant ratio).** For every prime $`\ell \ne p`$, at every supersingular point of $`X_0(\ell)`$,

```math
\left(\frac{\Delta(\tau)}{\Delta(\ell\tau)}\right)^{(p^2-1)/24} = \left(\frac{\ell}{p}\right).
```

This determines the half-exponent sign in Ono's supersingular discriminant-ratio identity. Corollary 3.2 extends it to arbitrary prime-to-$`p`$ isogenies.

**Computational evidence.** Exact-arithmetic checks of Theorem 1.1 at all supersingular $`j`$-values for $`5 \le p \le 997`$, and Vélu-quotient checks of Theorem 1.3 for all primes $`\ell \le 47`$ and $`5 \le p \le 199`$. The code and records are in `supplementary/`.

> **Status:** Preprint, not yet peer reviewed. The work was AI-assisted (OpenAI GPT-6.1 Sol and Claude Opus 5.5) in developing arguments, checking calculations and preparing the manuscript.

**Keywords:** supersingular congruences; Eisenstein series; discriminant ratios; isogenies; theta operator.

## How to cite

Jordan, D. (2026). *A factorial supersingular congruence and signed discriminant ratios: Manuscript, code and data* (Version v2.0) [Computer software]. Zenodo. https://doi.org/10.5281/zenodo.24120141

## Repository layout

| Path | Contents |
|---|---|
| `paper/` | Manuscript source (`.tex`) and compiled PDF, version 2.0 |
| `supplementary/Factorial_Conjecture_Result_v1_0/` | Code and recorded results for Theorem 1.1 under `new_work/`; reproduce with `new_work/run_all.sh` |
| `supplementary/Eta_Frobenius_Lemma_Audit_v1_0/` | Eta-multiplier and Vélu-quotient checks of Theorem 1.3: code, results, audit report |
| `supplementary/Theorem_1_3_Benchmark_v1_0/` | Timings for exact evaluation of $`E_{p+1}^h`$ by Theorem 1.1 (numbered Theorem 1.3 in an earlier draft): timing code, exact inputs and outputs, raw timings, verification records |

The package names follow the theorem numbering of earlier manuscript versions and are kept unchanged so that the archived manifests stay valid. Each package has its own README with reproduction instructions and a SHA-256 manifest. The packages are included exactly as archived, with one exception: three copyrighted third-party papers were removed from `Factorial_Conjecture_Result_v1_0/sources/`. See the `REMOVED_FROM_PUBLIC_REPO.md` file in that folder.

## Software environment

All computations use exact arithmetic. Tested with Python 3.13 on Linux x86_64.

- `python-flint` 0.9.0
- `mpmath` 1.3.0
- `cypari2` 2.2.4, bundling PARI/GP 2.17.2 (factorial package)
- A C compiler for the optional native kernel in the benchmark package

Pinned versions are in each package's `requirements.txt`.

## Verifying file integrity

From inside a package directory:

```sh
sha256sum -c SHA256SUMS.txt
```

## Licence

- **Code** (all `*.py`, `*.c`, `*.gp`, `*.sh` files): MIT Licence; see `LICENSE`.
- **Manuscript and notes** (`paper/` and the `.tex`/`.pdf` notes inside the packages): © 2026 David Jordan, all rights reserved, pending journal publication.
- **Data** (JSON, CSV and log outputs): free to reuse with attribution.

## Contact

David Jordan, Maynooth University Social Sciences Institute (MUSSI), Maynooth University, Maynooth, Co. Kildare, Ireland. David.Jordan@mu.ie
