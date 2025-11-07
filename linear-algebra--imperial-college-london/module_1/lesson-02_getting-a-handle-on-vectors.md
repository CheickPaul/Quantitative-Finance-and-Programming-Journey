## [GETTING A HANDLE ON VECTOR]

### <ins>1. Parameter Space & Vector</ins>

#### <ins>1.1 Parameter Space, Cost & Vector Moves</ins>
- We work in a **parameter space**: each pair **(μ, σ)** is a **point**, maps to a **bell curve**, which also maps to a single **Sum of Squared Residuals (SSR)**.  
 --> **Contour lines** = same SSR but different (μ, σ).

- A **vector** is just a **small move** in this space:  
  **(Δμ, Δσ)** moves us on the contour map.

<img width="1512" height="464" alt="image" src="https://github.com/user-attachments/assets/a4a1347a-107d-47e0-93fb-5dde34f6fb67" />


Figure — Left: changing μ shifts the curve; changing σ widens/narrows it (area = 1). 
Right: each (μ, σ) is a model; contours are cost levels J. The gradient ∇J points uphill; we follow −∇J in small steps to reach (μ*, σ*). 

#### <ins>1.2 Numerical SSR Maps: 3D Surface & Top-Down</ins>


- (1) Plotting SSR over the (μ,σ) planes gives a bowl shaped surface, the lowest point at the bottom of the bowl corresponds to the best fit :

<img width="592" height="588" alt="image" src="https://github.com/user-attachments/assets/95f01c19-bee9-469f-9374-7a26d56bba49" />

- (2) From a top-down view, the contour lines represent constant SSR levels. The closer we are to the central hotspot, the lower the SSR :
<img width="718" height="584" alt="image" src="https://github.com/user-attachments/assets/c0af51d7-a954-45e4-a895-3916df62c678" />


---

### <ins>2. Optimization in Parameter Space - Why Vectors Matter for Optimization</ins>

#### <ins>2.1 Optimization in (μ,σ): Goal, Idea & Step-by-Step</ins>

- **Goal**: Find the pair (μ,σ) which reachs the **minimum** of the cost (best fit).

- **Optimization idea**: follow the **steepest downhill direction**
  (gradient descent intuition).
  On a contour line, the SSR is constant. Moving along that line does not change the error.    Then, in order to reduce the SSR, we must leave that line perpendicularly in the direction   of −∇SSR (the steepest descent)

  
- **Mini procedure (step by step)** : Choose a starting point (μ₀, σ₀). / Compute the residuals (bin by bin or point by point) and the SSR./ Adjust μ if the bell curve is shifted; adjust σ if it is too wide or too narrow. / Repeat until the SSR stops decreasing (or until the desired threshold).

#### <ins>2.2 Vectors in Parameter Space: Direction & Step Size</ins>
**General view of a vector**: not only a geometric arrow; it’s an **ordered list of components** along axes (here, the parameters).  
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


