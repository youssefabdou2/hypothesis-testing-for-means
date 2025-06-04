# 🔥 Forest Fires Dataset: Hypothesis Testing in Excel

## 📌 Overview

This project explores hypothesis testing using the **Forest Fires dataset** to determine if specific fire characteristics require intervention by national authorities or park services. You will perform **one-proportion and one-mean hypothesis tests** in Excel or Google Sheets using real data and statistical tools such as **z-scores**, **p-values**, and Excel’s built-in statistical functions.

---

## 🎯 Objectives

- Determine whether the **mean burned area** is greater than 10 hectares.
- Assess whether the **mean Initial Spread Index (ISI)** is below 10.
- Evaluate whether the **proportion of very small fires** (under 0.5 ha) now exceeds 50% after new containment measures.
- Use statistical evidence to support **resource allocation decisions** and validate park service efforts.

---

## 📈 Hypothesis Test #1: Burned Area

**Research Question:** Is the average burned area significantly greater than 10 hectares?

**Hypotheses:**

- **Null (H₀):** μ = 10  
- **Alternative (H₁):** μ > 10

**Significance Level:**  
α = 0.05

**Test Type:**  
Right-tailed z-test

**Steps:**
1. Calculate sample mean (x̄), standard deviation (s), and size (n).
2. Compute the test statistic:  
   \[
   z = \frac{\bar{x} - 10}{s / \sqrt{n}} \approx 1
   \]
3. Calculate p-value:  
   \[
   p = 1 - \text{NORM.S.DIST}(z) \approx 0.155
   \]

**Conclusion:**  
Since p > 0.05, **fail to reject the null hypothesis**. There is **not enough evidence** to conclude that the average burned area exceeds 10 hectares.

---

## 🌿 Hypothesis Test #2: Initial Spread Index (ISI)

**Research Question:** Is the mean ISI significantly less than 10?

**Hypotheses:**

- **Null (H₀):** μ = 10  
- **Alternative (H₁):** μ < 10

**Significance Level:**  
α = 0.01

**Test Type:**  
Left-tailed z-test

**Steps:**
1. Calculate the z-statistic (e.g., z ≈ -5).
2. Compute the p-value:  
   \[
   p = \text{NORM.S.DIST}(z) \approx \text{very small}
   \]

**Conclusion:**  
Since p < 0.01, **reject the null hypothesis**. There is **strong evidence** that the mean ISI is less than 10.

---

## 📊 Hypothesis Test #3: Proportion of Very Small Fires

**Research Question:** Has the proportion of very small fires (under 0.5 ha) increased to exceed 50% since implementing new containment methods?

**Column Used:** `is_small`  
- 1 = Fire under 0.5 hectares  
- 0 = Fire over 0.5 hectares

**Hypotheses:**

- **Null (H₀):** p = 0.5  
- **Alternative (H₁):** p > 0.5

**Significance Level:**  
α = 0.05

**Test Type:**  
Right-tailed **z-test for proportions**

**Steps:**
1. Compute:
   - Sample proportion (p̂) ≈ 0.478 using `=AVERAGE(is_small)`
   - Sample size (n) using `=COUNT(is_small)`
   - Standard error:  
     \[
     SE = \sqrt{\frac{0.5 \cdot (1 - 0.5)}{n}}
     \]
   - Test statistic:  
     \[
     z = \frac{\hat{p} - 0.5}{SE} \approx -1
     \]
2. Compute p-value using:
   \[
   p = 1 - \text{NORM.S.DIST}(z)
   \]

**Conclusion:**  
Since the p-value > 0.05, **fail to reject the null hypothesis**. There is **insufficient evidence** to conclude that over 50% of the fires are very small. More data is needed to confidently assess the effectiveness of the containment strategy.

---


---
