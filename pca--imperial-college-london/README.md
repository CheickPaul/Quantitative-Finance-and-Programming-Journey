# Mathematics for Machine Learning: Principal Component Analysis (PCA)

**Institution**: Imperial College London  
**Instructors**: Prof. David Dye, Dr. Sam Cooper, Dr. Marc Deisenroth  
**Platform**: Coursera  
**Status**: In Progress  
[View Certificate on Coursera](https://www.coursera.org/learn/pca-math-machine-learning)

· Book used as reference to go further *Principal Component Analysis (2nd ed.)* — I.T. Jolliffe, Springer Series in Statistics  
· Projects (independent from the certificate)

---

## Purpose
This folder centralizes all my notes, exercises, and projects for the PCA course.  
It documents how Principal Component Analysis builds on linear algebra and statistics to extract key features, reduce dimensionality, and interpret variance in financial or data-driven contexts.

---

## Modules of the certificate
- [Module 1: Statistics of Datasets](modules/module_1_statistics/README.md)  
  Mean, variance, covariance matrices, and the impact of linear transformations.

- [Module 2: Inner Products](modules/module_2_inner_products/README.md)  
  Dot product, orthogonality, distances, and vector lengths.

- [Module 3: Orthogonal Projections](modules/module_3_orthogonal_projections/README.md)  
  Projections onto subspaces and geometric intuition for least squares.

- [Module 4: Principal Component Analysis](modules/module_4_pca/README.md)  
  PCA derivation, optimization objective, eigenvectors, and explained variance.

---

## Exercises & Notes from the book *Principal Component Analysis* (Jolliffe)

**Resolved exercises and notes**

### Chapters to revise first (certificate-critical)
- **Ch. 1 – Introduction**: history, motivation, geometric interpretation  
  → [Notes](book_jolliffe/ch01_intro/README.md) · [Exercises 1 (resolved)](book_jolliffe/ch01_intro/exercises.md)

- **Ch. 2 – Covariance and Correlation Matrices**: covariance structure, eigen decomposition  
  → [Notes](book_jolliffe/ch02_covariance/README.md) · [Exercises 2 (resolved)](book_jolliffe/ch02_covariance/exercises.md)

- **Ch. 3 – The Mathematical Foundations of PCA**: eigenvalues, eigenvectors, orthogonal transformations  
  → [Notes](book_jolliffe/ch03_math_foundations/README.md) · [Exercises 3 (resolved)](book_jolliffe/ch03_math_foundations/exercises.md)

- **Ch. 4 – Choosing the Number of Components**: explained variance, scree plot, cumulative variance  
  → [Notes](book_jolliffe/ch04_num_components/README.md) · [Exercises 4 (resolved)](book_jolliffe/ch04_num_components/exercises.md)

---

### Chapters to add for career (quant-oriented depth)
- **Ch. 5 – PCA in Practice**: preprocessing, scaling, outliers, missing data  
  → [Notes](book_jolliffe/ch05_pca_in_practice/README.md) · [Exercises 5 (resolved)](book_jolliffe/ch05_pca_in_practice/exercises.md)

- **Ch. 6 – PCA and Multivariate Techniques**: regression, factor analysis, clustering  
  → [Notes](book_jolliffe/ch06_multivariate/README.md) · [Exercises 6 (resolved)](book_jolliffe/ch06_multivariate/exercises.md)

- **Ch. 7 – Nonlinear & Kernel PCA**: kernel trick, nonlinear transformations  
  → [Notes](book_jolliffe/ch07_kernel_pca/README.md) · [Exercises 7 (resolved)](book_jolliffe/ch07_kernel_pca/exercises.md)

- **Ch. 8 – Applications in Finance and Data Science**: dimensionality reduction, portfolio risk decomposition  
  → [Notes](book_jolliffe/ch08_applications/README.md) · [Exercises 8 (resolved)](book_jolliffe/ch08_applications/exercises.md)

---

### Exercise sets to solve (tracked as “resolved” in this repo)
- **1–2** — covariance matrices, eigen decomposition, correlation interpretation  
  → [Exercises 1–2](book_jolliffe/ch02_covariance/exercises.md)

- **3–4** — eigenvalues, orthogonal transformations, explained variance  
  → [Exercises 3–4](book_jolliffe/ch03_math_foundations/exercises.md)

- **5–6** — scaling, centering, and multivariate projection methods  
  → [Exercises 5–6](book_jolliffe/ch05_pca_in_practice/exercises.md)

- **7–8** — kernel PCA, nonlinear manifolds, portfolio PCA application  
  → [Exercises 7–8](book_jolliffe/ch07_kernel_pca/exercises.md)

---

## Projects
| Notebook | Description |
|-----------|-------------|
| [`pca_market_risk.ipynb`](projects/pca_market_risk.ipynb) | PCA applied to market returns — explained variance and factor loadings. |
| [`covariance_matrix_visualizer.ipynb`](projects/covariance_matrix_visualizer.ipynb) | Covariance and correlation visualization (heatmaps, eigenvalues). |
| [`dimensionality_reduction_demo.ipynb`](projects/dimensionality_reduction_demo.ipynb) | PCA applied to synthetic and financial datasets. |
| [`robust_pca_noise.ipynb`](projects/robust_pca_noise.ipynb) | Detecting outliers and noise in portfolio returns using robust PCA. |

---

**Course Link**: [Coursera – Mathematics for Machine Learning: PCA](https://www.coursera.org/learn/pca-math-machine-learning)
