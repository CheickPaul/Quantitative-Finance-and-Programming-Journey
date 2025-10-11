# Probability & Statistics: To p or not to p? (University of London)

**Institution**: University of London  
**Instructors**: Dr. James Abdey & Dr. Robert Blackburn  
**Platform**: Coursera  
**Status**: In Progress 🟦  

[📄 View Course on Coursera](https://www.coursera.org/learn/to-p-or-not-to-p)

· Reference book: *Introduction to Probability* — Joseph K. Blitzstein & Jessica Hwang  
· Projects (independent from the certificate)

---

## Purpose
This folder centralizes my notes, exercises, and Python projects for the **To p or not to p?** course.  
It focuses on probability intuition, randomness, sampling, inference, and hypothesis testing — foundations of statistical reasoning in quantitative finance and data-driven decision-making.

---

## Modules of the Certificate
- [Module 1 – Dealing with Uncertainty and Complexity in a Chaotic World](modules/module_1_uncertainty_complexity/README.md)  
  Real-world randomness, complexity, and the need for probability models.

- [Module 2 – Quantifying Uncertainty With Probability](modules/module_2_probability_principles/README.md)  
  Core principles of probability, conditional probability, Bayes’ theorem.

- [Module 3 – Describing the World the Statistical Way](modules/module_3_descriptive_statistics/README.md)  
  Data visualization, central tendency, dispersion, and correlation.

- [Module 4 – On Your Marks, Get Set, Infer!](modules/module_4_sampling_inference/README.md)  
  Sampling distributions, estimation, confidence intervals.

- [Module 5 – To p Or Not To p?](modules/module_5_pvalues_hypothesis/README.md)  
  Hypothesis testing, Type I/II errors, p-values, power, and interpretation.

- [Module 6 – Applications](modules/module_6_applications/README.md)  
  Real-world statistical applications and decision-making under uncertainty.

---

## Exercises & Notes from *Introduction to Probability* — Blitzstein & Hwang  
**Resolved exercises and notes**

###  Part A  Certificate Focus (Coursera)
| Book Chapters | Main Concepts | Links |
|----------------|----------------|--------|
| **Ch. 1–3** | Combinatorics, conditional probability, Bayes' theorem | [Notes](book_blitzstein/ch01_03/README.md) · [Exercises](book_blitzstein/ch01_03/exercises.md) |
| **Ch. 4–6** | Discrete & continuous random variables, expectation, variance | [Notes](book_blitzstein/ch04_06/README.md) · [Exercises](book_blitzstein/ch04_06/exercises.md) |
| **Ch. 7–10** | Joint distributions, covariance, correlation, CLT | [Notes](book_blitzstein/ch07_10/README.md) · [Exercises](book_blitzstein/ch07_10/exercises.md) |
| **Ch. 11–14** | Estimation, confidence intervals, hypothesis testing | [Notes](book_blitzstein/ch11_14/README.md) · [Exercises](book_blitzstein/ch11_14/exercises.md) |

---

###  Part B  Quant & Finance Extensions
| Focus | Relevant Topics / Applications | Reference Chapters |
|--------|--------------------------------|--------------------|
| **Risk & Expectation** | Expected value as risk-neutral pricing | Ch. 4–5 |
| **Dependence & Covariance** | Portfolio risk, correlation matrices | Ch. 8–9 |
| **Central Limit Theorem (CLT)** | Monte Carlo convergence, volatility clustering | Ch. 10 |
| **Estimation & Confidence Intervals** | VaR/ES estimation & sampling error | Ch. 12–13 |
| **Hypothesis Testing** | Trading signal validation, p-values misuse | Ch. 14 |
| **Bayesian Updating** | Dynamic probability of market regimes | Ch. 3 (Bayes), Ch. 11 (posterior inference) |

---

## Exercise Sets to Solve (tracked as “resolved” in this repo)

- **Ch. 1–3** — counting, conditional probability, Bayes  
  → [Exercises Ch.1–3](./book_blitzstein/ch01_03/exercises.md)

- **Ch. 4–6** — random variables, expectation/variance  
  → [Exercises Ch.4–6](./book_blitzstein/ch04_06/exercises.md)

- **Ch. 7–10** — joint distributions, covariance, LLN & CLT  
  → [Exercises Ch.7–10](./book_blitzstein/ch07_10/exercises.md)

- **Ch. 11–14** — estimation, confidence intervals, hypothesis tests  
  → [Exercises Ch.11–14](./book_blitzstein/ch11_14/exercises.md)

> 💡 *Tip:* Solve 1–6 first for solid intuition, then 7–10 for convergence logic, and finish with 11–14 for inference & p-values.

---

## Projects
| Notebook | Description |
|-----------|-------------|
| [`returns_distribution_analysis.ipynb`](projects/returns_distribution_analysis.ipynb) | Fit & compare distributions on asset returns (fat tails, QQ plots). |
| [`bayesian_update_coin.ipynb`](projects/bayesian_update_coin.ipynb) | Bayesian updating (Beta–Binomial) & predictive checks. |
| [`clt_simulation.ipynb`](projects/clt_simulation.ipynb) | Simulate LLN/CLT and visualize sampling distributions. |
| [`hypothesis_testing_ab.ipynb`](projects/hypothesis_testing_ab.ipynb) | p-values, power, effect size — A/B testing framework. |
| [`monte_carlo_risk.ipynb`](projects/monte_carlo_risk.ipynb) | Monte Carlo simulation of VaR/ES and portfolio drawdowns. |
| [`decision_tree_credit.ipynb`](projects/decision_tree_credit.ipynb) | Simple credit-risk decision tree (application module). |

---

**Course Link**: [Coursera – Probability & Statistics: To p or not to p?](https://www.coursera.org/learn/to-p-or-not-to-p)

