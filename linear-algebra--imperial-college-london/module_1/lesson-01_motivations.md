Voici tes notes avec **tous les titres soulignés** (format préféré `<ins>**...**</ins>`). Tu peux coller tel quel :

## <ins>**[MOTIVATION FOR LINEAR ALGEBRA]**</ins>

### <ins>**1. Why Linear Algebra ?**</ins>

2 problem families motivate the course :

* (1) **Solving simultaneous equations**
* (2) **Fiting a model to data** (e.g. finding parameters that best match a histogram).

<div style="border:1px solid #ddd;padding:12px;border-radius:8px;margin:8px 0;">
  <strong>Key idea:</strong> Both tasks are expressed cleanly with vectors and matrices, then solved efficiently by algorithms.
</div>

---

### <ins>**2. Exemple of Solving simultaneous equations ?**</ins>

#### <ins>**2.1.with Vector**</ins>

<img width="3086" height="2182" alt="image" src="https://github.com/user-attachments/assets/f9fab266-1eff-4c0d-8ed3-f8704235dec5" />

#### <ins>**2.2 With Matrice (Cramer)**</ins>

<img width="3086" height="2182" alt="image" src="https://github.com/user-attachments/assets/7f3f4787-de77-4303-9653-d455065ac0c6" />

---

### <ins>**3. Exemple of Fiting a model to data ?**</ins>

#### <ins>**3.1 Fit a straight line to data**</ins>

<img width="3086" height="2182" alt="image" src="https://github.com/user-attachments/assets/ebcbab3c-313a-470b-bd9d-c443935238cc" />

* Assume a linear model:
  ŷ = α + β x

* Choose α, β to fit the data: minimize the sum of squared residuals
  SSE = ∑ᵢ (yᵢ − ŷᵢ)²

* Residual for point i:
  rᵢ = yᵢ − ŷᵢ

<img width="966" height="616" alt="image" src="https://github.com/user-attachments/assets/02d407d3-0976-454e-aac1-a0b3dfd38354" />

Interpretation: smaller residuals ⇒ better fit
(tip: α moves the line up/down; β changes the slope)

#### <ins>**3.2 Fit a Distribution to data**</ins>

A model is only useful if it matches the measured data. Then we need to fit the parameters and metrics to quantify the goodness of the fit.

One way is to compute the differents residuals ( the difference between the observed data and the model prediction bin by bin on the histogram)

rk=Hdata(k)−Hmodel(k)

<img width="1108" height="1192" alt="image" src="https://github.com/user-attachments/assets/d4330fc5-caa6-400d-9705-e382ed8ec57b" />

To improve the model above, we need to shift its center to the right and keep its width the same. In other word, we need to increase the mean μ to align both the peak of the model and the center of the observed data. The standard deviation of the model will approximately remain the same because the model spread already matches the data. Here we have a problem of **Location** not **Dispersion**
