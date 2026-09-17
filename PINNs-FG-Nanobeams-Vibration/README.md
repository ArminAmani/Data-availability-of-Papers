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

Because the adopted NSGT eigenproblem is sixth order in the normalized coordinate $X$, six independent scalar boundary conditions are prescribed for each support configuration. The boundary conditions used in this study are:

| Configuration | Conditions at $X=0$ | Conditions at $X=1$ | Enforcement in the PINN formulation |
|---|---|---|---|
| **Clamped–Clamped (C–C)** | $\Phi(0)=0$, $\Phi'(0)=0$, $\Phi''(0)=0$ | $\Phi(1)=0$, $\Phi'(1)=0$, $\Phi''(1)=0$ | All six boundary conditions are imposed exactly through the admissible trial function; no active boundary-condition penalty is required. |
| **Simply Supported (S–S)** | $\Phi(0)=0$, $\Phi''(0)=0$, $\bar{M}(0)=0$ | $\Phi(1)=0$, $\Phi''(1)=0$, $\bar{M}(1)=0$ | Displacement and curvature conditions are imposed exactly, while the two dimensionless moment conditions are retained as soft constraints. |
| **Clamped–Free (C–F)** | $\Phi(0)=0$, $\Phi'(0)=0$, $\Phi''(0)=0$ | $\Phi''(1)=0$, $\bar{M}(1)=0$, $\bar{M}'(1)=0$ | The three clamped-end conditions are imposed exactly, while the three free-end conditions are enforced through the boundary loss. |

Here, $\Phi$ denotes the dimensionless mode shape and $\bar{M}$ denotes the dimensionless bending moment defined in the manuscript. In the adopted NSGT formulation, the zero-curvature and zero-moment conditions are independent and should not be interpreted as equivalent.

The complete derivation and mathematical definition of these higher-order boundary conditions are provided in the associated manuscript.

---

## Data and Code Availability

Selected computational artifacts associated with the C–C, S–S, and C–F cases are provided in this repository. These materials include selected configuration, optimization, and numerical verification records from the computations reported in the submitted manuscript.

During the peer-review process, the complete computational implementation, including the case-specific PINN source codes, independent BVP verification routines, checkpoints, detailed optimization histories, and supporting numerical outputs, is maintained as a controlled version to ensure consistency with the submitted work.

The complete computational package can be provided confidentially to the handling Editor and reviewers upon reasonable request during peer review.

Upon acceptance of the manuscript for publication, the source code and supporting computational materials corresponding to the final accepted version of the study will be released publicly in this repository.

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
