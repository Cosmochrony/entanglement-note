This repository contains the source of the **Entanglement Presentation Note** Cosmochrony paper  
*Residual-Rank Entanglement of Conjugate Weil Pairs in the Spectral Admissibility Cascade*.

This note computes the entanglement entropy of a closed conjugate Weil pair
$\{c,q-c\}$ along the spectral admissibility cascade of the Cosmochrony
programme. Entanglement is treated as the infra-projectable invariant of a
non-decomposable joint fibre of the non-injective projection $\Pi$, not as an
added postulate.

## Central Question

Given the conjugate Weil structure that organises the spectral admissibility
cascade on $\mathrm{Heis}_3(\mathbb{Z}/q\mathbb{Z})$:

> How much entanglement does a closed conjugate pair $\{c,q-c\}$ carry, and how
> does it evolve as the cascade resolves?

## Core Result

The bipartite state lives on the residual fibre-level support of the
Gram--Schmidt span of Weil fingerprints on the Heisenberg Cayley graph. With
the diagonal Schmidt pairing $e_j\leftrightarrow\overline{e_j}$ selected by the
Born--Infeld parity involution $V_{q-c}\simeq\overline{V_c}$:

- the normalized admissibility residual of each newly admitted independent
  direction is exactly $w_j=1$ in the tested finite-$q$ runs;
- admitted Weil fingerprint directions are therefore mutually orthogonal, so
  the reduced Schmidt spectrum on the residual support is flat;
- the reduced entropy is
  $$\Sent(n)=\log r_{\mathrm{pair}}(n),$$
  with no surviving spectral weighting (the admissibility-weight deficit
  $\varepsilon_{\mathrm{adm}}(n)$ is identically zero).

Here $r_{\mathrm{pair}}(n)=R_\infty-R(n)$ is the residual fibre-level
Gram--Schmidt rank: the number of independent admissible directions not yet
activated at BFS depth $n$.

## Monotonicity

Because the cascade only adjoins independent directions, $R(n)$ is
non-decreasing, hence $r_{\mathrm{pair}}(n)$ is non-increasing. The
entanglement profile is therefore monotone non-increasing in $n$, **maximal at
the earliest admissible stage** and decreasing as independent fingerprint
directions are stabilized into the projected span. This monotonicity is
structural — it follows from the Gram--Schmidt construction alone, with no
numerical input.

The decrease is not a loss of correlation to an environment: it is the
conversion of residual correlated capacity into projected stable structure.

## Status of Claims

| Claim | Status |
|---|---|
| Closure of the conjugate pair: bipartite composition and purity | Supplied composition structure (K4 crossing), not derived |
| Closure of the conjugate pair: diagonal pairing, given purity | Structural (Born--Infeld parity) |
| Orthogonality of admitted Weil fingerprints ($w_j=1$) | Numerical, verified for $q\in\{29,61,101,151\}$; proved analytically (companion paper E1) |
| $\Sent(n)=\log r_{\mathrm{pair}}(n)$ | Derived (conditional on orthogonality) |
| Monotone non-increase of $\Sent(n)$ | Proved (Gram--Schmidt structural) |
| Capacity-level one-way activation $\Delta I(n)\ge 0$ | Conjecture (PTO); supported numerically only within tolerance, $\Delta I(n) \ge -10^{-6} I_{\max}$ after burn-in; analytic proof open |

## Numerical Deliverable

For $q\in\{61,151,211,307\}$ the residual rank trajectory
$r_{\mathrm{pair}}(n)$ is reconstructed from the cumulative capacity profiles
of the systematic pair campaign, via
$$r_{\mathrm{pair}}(n)=R_\infty-\sum_{m\le n}\sigma_c(m)\,|S_m|,$$
and $\Delta I(n)=\sigma^{\mathrm{can}}_{\mathrm{pair}}(n)-\sigma^{\mathrm{can}}_{\mathrm{pair}}(n+1)$
follows directly from the stored pair-capacity profile.

The task is to measure the **contraction law** of $r_{\mathrm{pair}}(n)$, its
scaling exponent, and its relation to the pair-capacity exponent
$\delta_{\mathrm{pair}}$:

- if the contraction exponent agrees with $\delta_{\mathrm{pair}}$ within the
  expected finite-$q$ window, the entanglement trajectory and the capacity law
  share the same spectral engine;
- if it differs, the gap marks a genuine separation between residual rank
  contraction and shell-wise capacity decay.

## Position in the Programme

- The non-injective projection $\Pi$ is the primitive shared with the
  white-paper and foundation paper.
- The Bell-correlation derivation of the bell-paper is the canonical empirical
  anchor for the same fibre mechanism; locality at the projected level is
  preserved here in the same way the Tsirelson bound is reached without
  superluminal signalling.
- The conjugate Weil pair, Born--Infeld parity, and the pair-capacity
  observable $\sigma^{\mathrm{can}}_{\mathrm{pair}}$ are imported from the
  O-series spectral admissibility sub-programme.
- The projected mass hierarchy is the downstream trace of the cascade
  stabilization recorded by $\delta_{\mathrm{pair}}$, not an independent input.

## Build

```bash
bash compile.sh
```

This runs `pdflatex → bibtex → pdflatex → pdflatex` on
`tex/EntanglementNote.tex` and produces `out/EntanglementNote.pdf`.

## Citation

> J. Beau, *Residual-Rank Entanglement of Conjugate Weil Pairs in the Spectral Admissibility
> Cascade*, Zenodo, 2026. DOI: [10.5281/zenodo.20498835](https://doi.org/10.5281/zenodo.20498835).