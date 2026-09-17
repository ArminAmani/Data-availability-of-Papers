# PINNs-FG-Nanobeams-Vibration

## Overview

This repository accompanies the manuscript:

**“Unsupervised physics-informed neural networks for free-vibration eigenanalysis of two-dimensional functionally graded Euler–Bernoulli nanobeams under nonlocal strain gradient theory.”**

The study develops an unsupervised Physics-Informed Neural Network (PINN) framework for the fundamental free-vibration eigenanalysis of two-dimensional functionally graded (2D-FG) Euler–Bernoulli nanobeams governed by Nonlocal Strain Gradient Theory (NSGT).

The formulation leads to a sixth-order variable-coefficient eigenvalue problem and employs case-specific hard/hybrid trial functions, a trainable positive eigenvalue, and differentiable inertia-weighted modal normalization.

---

## Associated Manuscript

**Title:**  
Unsupervised physics-informed neural networks for free-vibration eigenanalysis of two-dimensional functionally graded Euler–Bernoulli nanobeams under nonlocal strain gradient theory

**Authors:**  
Armin Amani, Seyed Hamed Hoseini

**Corresponding Author:**  
Seyed Hamed Hoseini  
E-mail: h.hoseini@uok.ac.ir

**Journal:**  
*Thin-Walled Structures*

**Manuscript Status:**  
Submitted for peer review.

---

## Repository Structure

The repository is organized according to the three boundary-condition configurations investigated in the manuscript:

```text
PINNs-FG-Nanobeams-Vibration/
│
├── Clamped-Clamped/
├── Simply-Support/
├── Cantilever (C-F)/
└── README.md
```

Each case folder currently contains archived numerical outputs and Jupyter notebook material associated with the corresponding reported results.

---

## Boundary-Condition Cases

Three support configurations are considered.

| Configuration | Boundary treatment in the PINN formulation |
|---|---|
| **Clamped–Clamped (C–C)** | Deflection, slope, and curvature are enforced exactly at both endpoints through the trial function; no active boundary-condition penalty is required. |
| **Simply Supported (S–S)** | Deflection and curvature are enforced exactly at both endpoints, while the remaining natural moment conditions are retained as soft constraints. |
| **Clamped–Free (C–F)** | The clamped-end conditions are enforced exactly, while the three higher-order free-end conditions are imposed through the boundary loss. |

The complete mathematical definitions of the sixth-order NSGT boundary conditions are provided in the associated manuscript.

---

# Code and Data Availability

## Publicly Available Material

The numerical outputs supporting the results reported in the submitted manuscript are publicly available in this repository.

These materials document the principal numerical results for the C–C, S–S, and C–F configurations, including the quantities used in the reported eigenvalue, mode-shape, residual, and convergence analyses.

## Source-Code Availability During Peer Review

The complete executable source code is currently maintained in a controlled private archive during the peer-review process in order to preserve version consistency between the computational implementation and the submitted manuscript.

The complete source package includes:

- the case-specific PINN implementations;
- the training and optimization procedures;
- the independent boundary-value-problem (BVP) reference calculations; and
- the scripts required to reproduce the principal numerical results reported in the manuscript.

During peer review, the complete source code can be provided confidentially to the **handling Editor and/or reviewers upon reasonable request**.

## Public Release Upon Acceptance

Upon acceptance of the manuscript for publication, the complete source code corresponding to the final accepted version of the work will be publicly released in this repository.

---

## Numerical Verification

The PINN predictions are independently compared with separately implemented boundary-value-problem (BVP) reference solutions.

The BVP calculations are used exclusively for **a posteriori numerical verification** and do not enter the PINN training, optimization, stopping criteria, or model selection procedure.

The repository should therefore be interpreted together with the governing formulation, numerical settings, and verification procedure described in the manuscript.

---

## Reproducibility

The final public release will include the complete computational implementation required to reproduce the principal results of the study.

To ensure consistency, users should refer to the final accepted manuscript for:

- material and geometric parameters;
- nondimensionalization;
- neural-network architecture;
- optimizer settings;
- collocation and quadrature specifications;
- boundary-condition definitions; and
- numerical verification procedures.

---

## Citation

If you use the numerical results or, following public release, the source code associated with this project, please cite the corresponding article.

**Armin Amani and Seyed Hamed Hoseini**

*Unsupervised physics-informed neural networks for free-vibration eigenanalysis of two-dimensional functionally graded Euler–Bernoulli nanobeams under nonlocal strain gradient theory.*

Manuscript submitted to *Thin-Walled Structures*.

**The complete bibliographic citation and DOI will be added here upon publication.**

---

## Contact

For questions regarding the manuscript or access to the source code during peer review, please contact:

**Seyed Hamed Hoseini**  
Department of Mechanical Engineering  
University of Kurdistan  
E-mail: h.hoseini@uok.ac.ir
