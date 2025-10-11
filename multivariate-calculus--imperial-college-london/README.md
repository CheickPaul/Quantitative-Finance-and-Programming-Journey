# Mathematics for Machine Learning: Multivariate Calculus

**Institution**: Imperial College London  
**Instructors**: Prof. David Dye, Dr. Sam Cooper, Dr. Marc Deisenroth  
**Platform**: Coursera  
**Status**: In Progress 🟦  

[📄 View Certificate on Coursera](https://www.coursera.org/learn/multivariate-calculus-machine-learning)

· Book used as reference: *Calculus Vol. 1 & 2* — Tom M. Apostol  
· Projects (independent from the certificate)

---

## Purpose
This folder centralizes my notes, exercises, and Python projects for the *Multivariate Calculus* course.  
It focuses on derivatives, gradients, Taylor expansion, and optimization — key tools for machine-learning and quantitative-finance models.

---

## Modules of the Certificate
- [Module 1 – What is Calculus?](modules/module_1/README.md)  
  Review of single-variable calculus, functions, derivatives, chain/product rules.

- [Module 2 – Multivariate Calculus](modules/module_2/README.md)  
  Partial derivatives, gradient vectors, Jacobians, Hessians, geometric intuition.

- [Module 3 – Multivariate Chain Rule and Applications](modules/module_3/README.md)  
  Chain rule for vector functions, computational graphs, and backpropagation.

- [Module 4 – Taylor Series and Linearisation](modules/module_4/README.md)  
  Power and Taylor series in several variables, linear and quadratic approximations.

- [Module 5 – Introduction to Optimisation](modules/module_5/README.md)  
  Gradient descent, Newton–Raphson, convexity, constrained optimisation (Lagrange).

- [Module 6 – Regression](modules/module_6/README.md)  
  Linear and nonlinear least-squares regression, model fitting, curvature analysis.

---

## Exercises & Notes from *Calculus* — Tom Apostol
**Resolved exercises and notes**

### Chapters to revise first (certificate-critical)
- **Vol. 1 — Ch. 1–4** : limits, continuity, derivatives, integrals → module 1.  
  → [Notes](./book_apostol/vol1_ch01_04/README.md) · [Exercises](./book_apostol/vol1_ch01_04/exercises.md)

- **Vol. 2 — Ch. 8–9** : differential calculus of scalar & vector fields, Jacobian, Hessian, Lagrange → modules 2–5.  
  → [Notes](./book_apostol/vol2_ch08_09/README.md) · [Exercises](./book_apostol/vol2_ch08_09/exercises.md)

### Chapters for deeper quant-finance applications
- **Vol. 2 — Ch. 10–11** : line & multiple integrals → risk surfaces, continuous payoffs.  
- **Vol. 2 — Ch. 15** : numerical approximation → gradient descent, Taylor error.  
  → [Notes](./book_apostol/vol2_ch10_15/README.md)

---
## Exercise sets to solve (tracked as “resolved” in this repo)

- **Vol. 1 — Ch. 1–4** — functions, limits, continuity, derivatives, basic integrals *(refresh for M1)*  
  → [Exercises Vol.1 Ch.1–4](./book_apostol/vol1_ch01_04/exercises.md)

- **Vol. 2 — Ch. 8** — partial derivatives, gradient, directional derivative, Jacobian *(M2)*  
  → [Exercises Vol.2 Ch.8](./book_apostol/vol2_ch08_09/exercises.md#chapter-8)

- **Vol. 2 — Ch. 9** — Hessian, Taylor expansion in ℝⁿ, convexity, stationary points *(M3–M4–M5)*  
  → [Exercises Vol.2 Ch.9](./book_apostol/vol2_ch08_09/exercises.md#chapter-9)

- **Vol. 2 — Ch. 10–11 (sélection)** — multiple & line integrals, change of variables *(M4/M5 support)*  
  → [Exercises Vol.2 Ch.10–11](./book_apostol/vol2_ch10_15/README.md#exercises-ch10-11)

- **Vol. 2 — Lagrange multipliers (dans Ch.9)** — contraintes d’égalité, interprétation géométrique *(M5)*  
  → [Lagrange multipliers set](./book_apostol/vol2_ch08_09/exercises.md#lagrange-multipliers)

- **Least-squares / Regression (dérivé de Ch.9 & compléments)** — normal equations, sur-déterminé *(M6)*  
  → [Least-squares set](./book_apostol/vol2_ch10_15/README.md#least-squares)


---

## Projects
| Notebook | Description |
|-----------|-------------|
| [`gradient_descent_visualizer.ipynb`](projects/gradient_descent_visualizer.ipynb) | Visualizes gradient-descent and Newton steps on 3D loss surfaces. |
| [`jacobian_portfolio_sensitivities.ipynb`](projects/jacobian_portfolio_sensitivities.ipynb) | Uses Jacobians / Hessians to analyze portfolio sensitivity and convexity. |
| [`regression_least_squares.ipynb`](projects/regression_least_squares.ipynb) | Implements linear & nonlinear regression with gradient-based optimization. |
| [`taylor_series_risk_surface.ipynb`](projects/taylor_series_risk_surface.ipynb) | Applies Taylor expansion to approximate option or yield-curve changes. |

---

**Course Link**: [Coursera – Mathematics for Machine Learning: Multivariate Calculus](https://www.coursera.org/learn/multivariate-calculus-machine-learning)

