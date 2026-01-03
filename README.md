# SU(2) Lattice Gauge Theory on a Finite 2D Lattice (Closed Boundary Conditions)

This repository contains a **from-scratch exact diagonalization (ED) implementation** of **(2+1)-dimensional SU(2) lattice gauge theory** formulated in the **loop / prepotential (electric flux) basis**, with **Gauss law constraints enforced exactly** at every lattice site.

The code explicitly constructs the **physical gauge-invariant Hilbert space**, builds the **full Hamiltonian (electric + magnetic plaquette terms)**, diagonalizes it, and analyzes **energy spectra and degeneracies** for small lattice sizes.

This project is intended for **theoretical, numerical, and pedagogical studies** of non-Abelian lattice gauge theories.

---

## Physical Model

- **Gauge group:** SU(2)
- **Spatial dimension:** 2D lattice (Hamiltonian formulation)
- **Boundary condition:** Closed / open boundary (no periodic wrapping)
- **Hilbert space:** Gauge-invariant loop basis
- **Gauss law:** Enforced exactly at every vertex
- **Electric flux cutoff:** Finite truncation (`cut`)
- **Hamiltonian:**
  
  \[
  H = \frac{g^2}{4} \sum_{\text{links}} E^2 
  + \frac{1}{g^2} \sum_{\square} \left( 2\,\mathrm{Tr}\,U_{\square} \right)
  \]

---

## Features

- Exact construction of the **gauge-invariant Hilbert space**
- Explicit implementation of **Abelian Gauss Law (AGL) constraints**
- Strand-by-strand lattice construction
- Full **diagonal (electric)** and **off-diagonal (magnetic)** Hamiltonian
- Exact diagonalization using dense linear algebra
- Automatic detection of **degenerate energy levels**
- Identification of physical basis states contributing to degeneracies
- Visualization of the complete energy spectrum

---

## Code Overview

### 1. Local Gauge-Invariant Vertex Space

```python
discrete_local_h_space(cut)
