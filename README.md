## Start here 
- Executive summary + identity + reproduction target: `./AUDIT.md`
- Reproduce the check (source bundle): `python run_b1_path2.py` → `fig_gamma_geo_ci.pdf`
- Canonical record (DOI): https://doi.org/10.5281/zenodo.18414030

# Relative-Entropy Endpoint–Path Gaps as a Diagnostic of RG Coarse-Graining Failure

This repository preserves a single idea:

**Endpoint agreement is not the same as process-level validity.**
A reduced description can match selected endpoints and still be structurally incapable of representing the underlying flow.
This work gives a concrete diagnostic for that mismatch.

## What is the problem?

Across statistical physics, RG, effective theories, and modern machine learning, we repeatedly compress reality:
we map a high-dimensional system to a lower-dimensional representation and then try to predict.

Most validations implicitly rely on a comforting assumption:
if the reduced model matches the endpoints we care about, then it is “good enough”.

This assumption is often false.

## What this work contributes

I introduce an explicit quantity—an **endpoint–path gap**—built from **relative entropy**.

It is designed to separate two notions that are routinely conflated:

- **Endpoint agreement**: selected marginals / observables match.
- **Process-level consistency**: the reduced description genuinely preserves the information needed to represent the underlying evolution/flow.

The endpoint–path gap measures the irreducible information loss incurred when a process is compressed into a coarse description.
A key criterion is derived and linked to **statistical sufficiency**:

- When the chosen coarse variables are sufficient for the relevant family, the gap collapses.
- Otherwise, a nonzero gap persists, meaning endpoint matching can hide an unavoidable process-level failure.

In short: this provides a **prior diagnostic** for when coarse-graining/RG-style reduction is structurally capable of supporting precise prediction—and when it is not.

## Why this matters (in plain terms)

If you care about prediction under reduction, you should care about *how* information is lost, not only *what* endpoints are preserved.

This diagnostic can be used to:
- test whether a proposed coarse-graining can, in principle, preserve the information needed across a chosen interface;
- explain why some reduced models succeed only in limited regimes even when endpoint fits look perfect;
- make the boundary of validity explicit rather than relying on continuity/endpoint faith.

The thesis is not rhetorical:
**a failure mode can be diagnosed, quantified, and bounded.**


## Reading map

If you only have ~15–20 pages:
1. Definition and motivation of the endpoint–path gap.
2. Main vanishing / non-vanishing criterion and its connection to sufficiency.
3. Implications: what endpoint matching can certify, and what it cannot.
Appendices contain derivations and reproducibility-oriented details.

## Reproducibility
No datasets were generated or analysed.
A minimal reproduction check is provided in the source bundle: run `run_b1_path2.py` to generate `fig_gamma_geo_ci.pdf` (1-loop vs 2-loop comparison).

## Repository contents

- LaTeX sources for the manuscript
- Compiled PDF (when included in a release)
- LICENSE
