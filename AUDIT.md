# AUDIT — Relative-Entropy Endpoint–Path Gap Diagnostic (Executive Summary)

This repository provides a **certificate-style diagnostic** for finite-window RG / coarse-graining endpoint matching:
**endpoint agreement does not, by itself, license path/process agreement.**

---

## 1) The identity (what to verify)

Via relative-entropy chain decomposition, we isolate an endpoint–path decomposition of the form

\[
\Delta_{\mathrm{path}} = \Delta_{\mathrm{pair}} + \Gamma_{\mathrm{path}}, \qquad \Gamma_{\mathrm{path}} \ge 0 .
\]

- \(\Delta_{\mathrm{pair}}\): the observable endpoint discrepancy (what endpoint matching can see).
- \(\Gamma_{\mathrm{path}}\): the **irrecoverable path information loss** hidden by endpoint projection.

**Operational meaning:** \(\Delta_{\mathrm{pair}} \approx 0\) does *not* certify process agreement unless
\(\Gamma_{\mathrm{path}}\) is also negligible at the declared resolution.

A canonical sharp condition is:
\[
\Gamma_{\mathrm{path}} = 0 \iff \text{(endpoint is sufficient / no lost directions under the declared projection)} .
\]

---

## 2) QED-grade verification path (what you can reproduce here)

This repo includes a **single reproducible check** used in the paper:
a **1-loop vs 2-loop comparison plot** that exposes a non-negligible gap consistent with \(\Gamma_{\mathrm{path}} > 0\)
under endpoint matching.

**Reproduction target:** generate `fig_gamma_geo_ci.pdf` by running `run_b1_path2.py` (1-loop vs 2-loop comparison).

---

## 3) How to reproduce (minimal)

This repo ships a **single reproducible check** in the **source bundle**.

**Source bundle contents (relevant):**
- `run_b1_path2.py` — reproduction script (1-loop vs 2-loop comparison)
- `fig_gamma_geo_ci.pdf` — expected plot artifact (generated output / reference)

**Steps:**
1. Download the source bundle (release asset / source archive).
2. In the bundle root directory, run:

   ```bash
   python run_b1_path2.py

---

## 4) Relationship to the ψ–Δ framework

Conceptually, this diagnostic is a worked case study of the general theme:
**endpoint matching can mask non-negligible process/path gaps**.

It acts as a “magnifier”: the chain decomposition exposes a non-negative residual \(\Gamma_{\mathrm{path}}\) that
corresponds to the kind of cross-level gap the ψ–Δ reporting discipline forces you to account for.

(ψ–Δ framework repo: https://github.com/ybing2093-ops/psi-delta-structural-gaps)

---

