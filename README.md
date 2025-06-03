

# 🔥 Forest Fires Dataset: Hypothesis Testing in Excel

## 📌 Overview

This project explores hypothesis testing using the **Forest Fires dataset** to determine if specific fire characteristics require intervention by national authorities or park services. You'll perform hypothesis tests in a spreadsheet (e.g., Excel or Google Sheets) using **real data** and **statistical tools**, such as z-scores, p-values, and the `Z.TEST` function.

---

## 🎯 Objectives

* Determine whether the **mean burned area** is greater than 10 hectares.
* Assess whether the **mean Initial Spread Index (ISI)** is **below 10**.
* Use statistical evidence to support resource allocation decisions.

---

## 📈 Hypothesis Test #1: Burned Area

**Research Question:**
Is the **average burned area** significantly greater than 10 hectares?

**Hypotheses:**

* **Null (H₀):** μ = 10
* **Alternative (H₁):** μ > 10

**Significance Level:**

* α = 0.05

**Test Type:**

* Right-tailed z-test

**Steps:**

1. Calculate the sample mean (`x̄`), standard deviation (`s`), and size (`n`).
2. Compute the test statistic:

   $$
   z = \frac{\bar{x} - 10}{s/\sqrt{n}} \approx 1
   $$
3. Calculate the p-value:

   $$
   p = 1 - \text{NORM.S.DIST}(z) \approx 0.155
   $$
4. Conclusion:
   Since p > 0.05, **fail to reject** the null hypothesis. There is **not enough evidence** to conclude that average burned area exceeds 10 hectares.

---

## 🌿 Hypothesis Test #2: Initial Spread Index (ISI)

**Research Question:**
Is the **mean ISI** significantly **less than** 10?

**Hypotheses:**

* **Null (H₀):** μ = 10
* **Alternative (H₁):** μ < 10

**Significance Level:**

* α = 0.01

**Test Type:**

* Left-tailed z-test

**Steps:**

1. Calculate the test statistic (e.g., z ≈ -5).
2. Compute the p-value:

   $$
   p = \text{NORM.S.DIST}(z) \approx \text{very small}
   $$
3. Conclusion:
   Since p < 0.01, **reject** the null hypothesis. There is **strong evidence** that the mean ISI is **less than 10**.

---

## 🛠 Excel Tips

* Use `=Z.TEST(data_range, 10)` for right-tailed tests.
* For **left-tailed tests**, use:

  $$
  \text{p-value} = 1 - \text{Z.TEST(data_range, 10)}
  $$
* Always double-check that you're using the right direction (left-tailed or right-tailed) for your test.

---

## 📚 Learning Outcomes

* Understand the relationship between confidence intervals and hypothesis testing.
* Use Excel's statistical functions to perform z-tests.
* Draw data-driven conclusions for real-world decision-making.

---

