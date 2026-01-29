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

## How to engage with it (verification / falsification)

I do not ask for authority-based acceptance.
If the framework is wrong, it should be rejected by:
- a counterexample to the main criterion,
- a proof-level objection,
- or a precise identification of which assumption is invalid.

If it is right, it should be usable as a diagnostic tool independent of venue.

## Reading map

If you only have ~15–20 pages:
1. Definition and motivation of the endpoint–path gap.
2. Main vanishing / non-vanishing criterion and its connection to sufficiency.
3. Implications: what endpoint matching can certify, and what it cannot.
Appendices contain derivations and reproducibility-oriented details.

## Data / reproducibility

No datasets were generated or analysed.
All derivations and reproducibility-oriented details are contained in the manuscript and its appendices.

## Repository contents

- LaTeX sources for the manuscript
- Compiled PDF (when included in a release)
- LICENSE
