# Mathematics for Machine Learning: Linear Algebra
**Institution**: Imperial College London  
**Instructors**: Prof. David Dye, Dr. Sam Cooper, Dr. Marc Deisenroth  
**Platform**: Coursera  
**Status**: In Progress 🟦  
[📄 View Certificate on Coursera](https://www.coursera.org/learn/linear-algebra-machine-learning)



· Book used as reference to go further *Linear Algebra Done Right (4th ed.)* — Sheldon Axler 

· Projects (independent from the certificate)

---

## Purpose
This folder centralizes all my notes, exercises, and projects for the Linear Algebra course.
Feel free to explore it.

---

## Modules of the certificate
- [Module 1: Introduction to Linear Algebra and to Mathematics for Machine Learning](modules/module_1/README.md)  
  Motivation, course logistics, geometric intuition, first vector operations.

- [Module 2: Vectors are Objects that Move Around Space](modules/module_2/README.md)  
  Vector operations, parameter space, geometry in ℝⁿ.

- [Module 3: Matrices in Linear Algebra – Objects that Operate on Vectors](modules/module_3/README.md)  
  Matrices as operators, systems of equations, matrix multiplication, rank.

- [Module 4: Matrices Make Linear Mappings](modules/module_4/README.md)  
  Linear transformations, composition, change of basis.

- [Module 5: Eigenvalues and Eigenvectors – Application to Data Problems](modules/module_5/README.md)  
  Eigen decomposition, diagonalization, link to PCA and covariance.

---

## Exercises & Notes from the book *Linear Algebra Done Right* (Axler)
**Resolved exercises and notes**

### Chapters to revise first (certificate-critical)
- **Ch. 1 – Vector Spaces** (1A–1C): definitions, subspaces, direct sums  
  → [Notes](./book_axler/ch01_vector_spaces/README.md) · [Exercises 1A–1C (resolved)](./book_axler/ch01_vector_spaces/exercises_1A_1C.md)

- **Ch. 2 – Finite-Dimensional Vector Spaces** (2A–2C): span, basis, dimension  
  → [Notes](./book_axler/ch02_finite_dimensional/README.md) · [Exercises 2A–2C (resolved)](./book_axler/ch02_finite_dimensional/exercises_2A_2C.md)

- **Ch. 3 – Linear Maps** (3A–3D): null space, range, matrix of a map, invertibility, change of basis  
  → [Notes](./book_axler/ch03_linear_maps/README.md) · [Exercises 3A–3D (resolved)](./book_axler/ch03_linear_maps/exercises_3A_3D.md)

- **Ch. 5 – Eigenvalues & Eigenvectors** (5A–5D): minimal polynomial, upper-triangular form, diagonalizability  
  → [Notes](./book_axler/ch05_eigenvalues/README.md) · [Exercises 5A–5D (resolved)](./book_axler/ch05_eigenvalues/exercises_5A_5D.md)

### Chapters to add for career (quant-oriented depth)
- **Ch. 6 – Inner Product Spaces** (6A–6C): norms, Gram–Schmidt, orthogonal projections, pseudoinverse → least-squares / regression  
  → [Notes](./book_axler/ch06_inner_product/README.md) · [Exercises 6A–6C (resolved)](./book_axler/ch06_inner_product/exercises_6A_6C.md)

- **Ch. 7 – Operators on Inner Product Spaces** (7A–7B, 7E–7F): spectral theorem, SVD, QR/polar → PCA, risk factors, dimensionality reduction  
  → [Notes](./book_axler/ch07_operators/README.md) · [Exercises 7A–7F (resolved)](./book_axler/ch07_operators/exercises_7A_7F.md)

### Exercise sets to solve (tracked as “resolved” in this repo)
- **1A–1C** — fields / vectors / subspaces (proof fluency)  
  → [Exercises 1A–1C](./book_axler/ch01_vector_spaces/exercises_1A_1C.md)

- **3B–3C** — null/range, rank, matrices of linear maps (bridge to code)  
  → [Exercises 3B–3C](./book_axler/ch03_linear_maps/exercises_3B_3C.md)

- **5A–5D** — eigenvalues, minimal polynomial, diagonalization (PCA foundation)  
  → [Exercises 5A–5D](./book_axler/ch05_eigenvalues/exercises_5A_5D.md)

- **6A–6C** — inner products, Gram–Schmidt, projections / pseudoinverse (least-squares)  
  → [Exercises 6A–6C](./book_axler/ch06_inner_product/exercises_6A_6C.md)

- **7B, 7E** — Spectral Theorem & SVD (risk factors / compression)  
  → [Exercises 7B & 7E](./book_axler/ch07_operators/exercises_7B_7E.md)

---

## Projects
| Notebook | Description |
|-----------|-------------|
| [`pca_covariance.ipynb`](projects/pca_covariance.ipynb) | Principal Component Analysis applied to market returns and risk decomposition. |
| [`linear_transformations.ipynb`](projects/linear_transformations.ipynb) | Visualization of eigenvectors, eigenvalues, and transformations in a financial context. |

---

**Course Link**: [Coursera – Mathematics for Machine Learning: Linear Algebra](https://www.coursera.org/learn/linear-algebra-machine-learning)
