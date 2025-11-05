## [GETTING A HANDLE ON VECTOR]

### 1. Parameter Space & Vector

- We work in a **parameter space**: each pair **(μ, σ)** is a **point**.  
  **Contour lines** = same values of the cost (error).

- A **vector** is just a **small move** in this space:  
  **(Δμ, Δσ)** moves us on the contour map.

<img width="1512" height="464" alt="image" src="https://github.com/user-attachments/assets/a4a1347a-107d-47e0-93fb-5dde34f6fb67" />


Figure — Left: changing μ shifts the curve; changing σ widens/narrows it (area = 1). 
Right: each (μ, σ) is a model; contours are cost levels J. The gradient ∇J points uphill; we follow −∇J in small steps to reach (μ*, σ*). 

---

### 2. Optimization in Parameter Space - Why Vectors Matter for Optimization

- **Goal**: reach the **minimum** of the cost (best fit).

- **Optimization idea**: follow the **steepest downhill direction**  
  (gradient descent intuition).

- **General view of a vector**: not only a geometric arrow; it’s an **ordered list of components** along axes (here, the parameters).  
  Useful to **describe a direction** and **how much we move**.


---

### 3. Compact Formulae: dθ and f(x)

- **Minimal formula (memo)**:  
  **θ = (μ, σ)**, displacement **dθ = (Δμ, Δσ)**,  
  update: **θ_next = θ − η ∇J(θ)**.

- **Gaussian reference (optional)**:  
  **f(x) = 1/(σ√(2π)) · exp(−(x−μ)² / (2σ²))**

---

### 5. <ins>**Reflection — Gradient, Optimization & Quant/Trading **</ins>

**Core idea**
- We have **knobs to tune** (model parameters, portfolio weights, strategy thresholds).
- We want to **improve a score** (↓ error, ↑ Sharpe, ↓ costs).
- The **gradient** is the little arrow that says: “if you move here, your score improves the fastest.”

**How we use it (image)**
- **Hill + fog**: you can’t see far and you want to go downhill.  
  Take a **small step** in the **steepest downhill direction**, then **re-measure**. Repeat.

#### <ins>**Concrete applications — with gradient (∇) intuition**</ins>

| Case | Objective (score) | Parameters | Cost / Score (example) | Intuition of the **∇** arrow | Update rule + mini-example |
|---|---|---|---|---|---|
| **Beta regression** | Reduce error between **stock** and **index** | θ = (α, β) | **SSE(θ)** = Σ (R_stock − α − β·R_mkt)² | **∇SSE** points where the **error increases** the most → move **along −∇** to **decrease** it. | **θ ← θ − η ∇SSE(θ)**. *Example:* if β is too low, residuals are positive when the index rises ⇒ ∇ “pushes” β **up** step by step. |
| **Portfolio allocation** | Better **risk/return** trade-off | w = (w₁,…,wₙ) | **J(w)** = λ·wᵀΣw − μᵀw | **∇J(w) = 2λΣw − μ**. Per-asset read: if \[∇J(w)\]ᵢ **> 0** ⇒ **too much risk** vs return ⇒ **decrease** wᵢ; if **< 0** ⇒ **good return/low risk** ⇒ **increase** wᵢ. | **w ← w − η ∇J(w)** then **project** (Σw=1, w≥0). *Example:* a low-correlated, high-return asset often has \[∇J\]ᵢ < 0 ⇒ its weight goes up. |
| **Trading strategy** | ↑ **Net Sharpe** (after costs) | φ = (windows, thresholds, weights…) | **J(φ)** = −Sharpe_CV(φ) + penalties (fees, turnover, complexity) | **∇J(φ)** points toward settings that **hurt** net Sharpe (e.g., too-low entry threshold ⇒ **over-trading** ⇒ fees ↑). Move **along −∇** to **fix** it. | **φ ← φ − η ∇J(φ)**. *Example:* if the window is too short ⇒ noisy signals ⇒ ∇ pushes to **lengthen** the window / **raise** the threshold. |
| **Order execution** | ↓ **Impact + risk** of execution | q = (q₁,…,q_T) (slices) | **Cost(q)** = Impact(q) + Variance(PnL(q)) | \[**∇Cost(q)**\]ₜ = **marginal cost** of trading more in **slice t**. Large **positive** ⇒ that slice is **too expensive** (low liquidity, high vol) ⇒ move **along −∇** to **reduce** qₜ. | **q ← q − η ∇Cost(q)**. *Example:* open slice too heavy ⇒ large ∇ on q₁ ⇒ **decrease q₁** and **redistribute** to other slices. |

##### Notes
- **η (step size):** small = stable; large = fast but may overshoot the optimum.  
- **Normalize** features/returns to stabilize **∇**.  
- **Always include** fees, slippage, impact in the score.  
- **Market noise:** evaluate on multiple periods / use cross-validation.
  
> Optimization = **turn the right knobs little by little**, each time moving in the direction where the **score improves the most**, until you get a robust real-market setting.


