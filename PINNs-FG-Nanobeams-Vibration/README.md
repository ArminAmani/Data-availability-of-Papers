# PINNs-FG-Nanobeams-Vibration

This project applies unsupervised Physics-Informed Neural Networks (PINNs) to the free-vibration eigenanalysis of two-dimensional functionally graded (2D-FG) Euler–Bernoulli nanobeams, incorporating size-dependent effects through the Nonlocal Strain Gradient Theory (NSGT).

---

## Paper Title

Unsupervised physics-informed neural networks for free-vibration eigenanalysis of two-dimensional functionally graded Euler–Bernoulli nanobeams under nonlocal strain gradient theory

## Authors

Armin Amani, Seyed Hamed Hoseini

## Corresponding author

E-mail address: h.hoseini@uok.ac.ir (S.H. Hoseini)

## journal
Thin-Walled Structures

## Boundary Conditions
Three structural support configurations are considered, representing the most common cases in nanobeam applications.

| Support Configuration | Conditions at X = 0 (Left End) | Conditions at X = 1 (Right End) |
|---|---|---|
| Clamped–Clamped (C–C) | Zero deflection, zero slope, zero curvature | Zero deflection, zero slope, zero curvature |
| Clamped–Free (C–F) | Zero deflection, zero slope, zero curvature | Zero curvature, zero nonlocal moment, zero derivative of nonlocal moment |
| Simply Supported (S–S) | Zero deflection, zero curvature, zero nonlocal moment | Zero deflection, zero curvature, zero nonlocal moment |

Notes:

- Zero deflection enforces no transverse displacement at the support.
- Zero slope enforces no rotation (clamped condition).
- Zero curvature enforces no classical bending moment.
- Zero nonlocal moment and its derivative enforce the additional higher-order boundary conditions required by Nonlocal Strain Gradient Theory (NSGT).

## Each folder includes a Jupyter notebook (`.ipynb`) with output Main Results.

## Citation 
If you use this code, please cite:

Armin Amani, Seyed Hamed Hoseini.

Unsupervised physics-informed neural networks for free-vibration eigenanalysis of two-dimensional functionally graded Euler–Bernoulli nanobeams under nonlocal strain gradient theory.

Thin-Walled Structures, Elsevier.
