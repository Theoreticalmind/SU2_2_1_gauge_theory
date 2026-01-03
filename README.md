# SU(2) Lattice Gauge Theory on a Finite 2D Lattice (Closed Boundary Conditions)
<img width="1316" height="652" alt="image" src="https://github.com/user-attachments/assets/1331af50-6142-4fb1-b906-80c6bca23de0" />
This is 
### Loop-State Representation on a Hexagonal Lattice (via Point Splitting)

We embed the square lattice into a **hexagonal lattice** using the **point-splitting construction**.  
Each local loop state is labeled by three integers
$\[
[l_{12},\, l_{13},\, l_{23}],
\]$
this is loop states for different configurations.

Below we list the explicit hexagonal-lattice representations of different loop states.  
Each loop state is mapped to a sequence of local vertex configurations.

---

#### Loop State: \( 123 \)

$\[
[l_{12}, l_{13}, l_{23}]
\]$

```text
[
 [0,0,0],[1,0,0],[0,1,0],[0,1,0],[0,1,0],[0,0,1],[0,0,1], [0,1,0],[0,1,0],[0,0,1],[0,1,0],[0,0,1],[0,0,0], [0,0,0],[0,0,1],[0,1,0],[1,0,0],[0,0,0]
]
```
#### Loop State: \( 234 \)
$\[
[l_{12}, l_{13}, l_{23}] 
\]$

```text
[
 [0,0,0],[0,0,0],[0,0,0],[1,0,0],[0,1,0],[0,0,1],[0,0,0],[1,0,0],[1,0,0],[0,0,0],[1,0,0],[0,0,1],[0,0,1],[0,1,0],[0,1,0],[0,1,0],[1,0,0],[0,0,0]
]
```
#### Loop State: \( 341 \)
$\[
[l_{12}, l_{13}, l_{23}] 
\]$

```text
[
 [0,0,0],[1,0,0],[0,1,0],[0,0,1],[0,0,0],[0,0,0],[0,0,1],[0,0,1],[0,0,1],[0,1,0],[0,1,0],[0,0,1],[0,0,1],[0,1,0],[0,1,0],[0,1,0],[1,0,0],[0,0,0]
]
```

This repository contains a **from-scratch exact diagonalization (ED) implementation** of **(2+1)-dimensional SU(2) lattice gauge theory** formulated in the **lsh basis**, with **Gauss law constraints enforced exactly** at every lattice site.

The code explicitly constructs the **physical gauge-invariant Hilbert space**, builds the **full Hamiltonian (electric + magnetic plaquette terms)**, diagonalizes it, and analyzes **energy spectra and degeneracies** for small lattice sizes.


---

## Physical Model

- **Gauge group:** SU(2)
- **Spatial dimension:** 2D lattice (Hamiltonian formulation)
- **Boundary condition:** Closed / open boundary (no periodic wrapping)
- **Hilbert space:** Gauge-invariant loop basis
- **Gauss law:** Enforced exactly at every vertex
- **Electric flux cutoff:** Finite truncation (`cut`)
- **Hamiltonian:**
  
  $\[
  H = \frac{g^2}{4} \sum_{\text{links}} E^2 + \frac{1}{g^2} \sum_{\square} \left( 2\,\mathrm{Tr}\,U_{\square} \right)
  \]$

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
## Author
**Md Osama Ali**

