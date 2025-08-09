Understanding how **linear models express assumptions about constant tradeoffs and relative importance** is *fundamental* to building intuition in business analytics.


---

## 🧠 Module: Modeling Objectives as Linear Combinations of Inputs

### 🎯 Learning Goals:

* Understand what it means to model an objective as a linear function of variables.
* Interpret coefficients in terms of **marginal effects** or **weights**.
* Explore **hidden assumptions** of linearity (e.g., constant tradeoffs, independence).
* Identify **when linear models are reasonable**, and when they fail.

---

## 🧮 What is a Linear Model?

We model a target or objective (e.g. profit, cost, score, satisfaction) as:

$$ \text{Objective} = w_1 x_1 + w_2 x_2 + \dots + w_n x_n + b $$

Where:

* $x_i$: input variables (e.g., features of a product, price, time spent)
* $w_i$: weights or coefficients (value or cost per unit of each variable)
* $b$: baseline (intercept)

---

## 🧩 Business Interpretation

Each coefficient $w_i$ answers:

> “How much does the objective change if we increase $x_i$ by 1 unit, holding others constant?”

This implies:

* **Constant marginal value**: Each unit of $x_i$ contributes exactly $w_i$ more (or less) to the objective.
* **Additivity**: The effect of each variable is independent and adds up linearly.
* **No interactions** unless explicitly modeled.

---

## ⚠️ Hidden Assumptions and Implications of Linearity

| Assumption              | Implication                      | Real-World Concern                                          |
| ----------------------- | -------------------------------- | ----------------------------------------------------------- |
| Constant marginal value | The tradeoff doesn’t change      | Often unrealistic (e.g. diminishing returns)                |
| Additivity              | No interaction between variables | But often variables **interact** (e.g. price and marketing) |
| Linearity               | Simple decision surfaces         | But real-world systems often non-linear                     |
| Perfect measurement     | No error, full observability     | Rarely true in practice                                     |

---

## ✅ Example 1: Advertising Budget Allocation

### Problem:

You want to model the **sales** as a function of spending in two channels: TV and Social Media.

Assume:

$$
\text{Sales} = 20 \cdot \text{TV} + 10 \cdot \text{Social} + 500
$$

### Interpretations:

* Each \$1 spent on TV increases sales by \$20.
* Each \$1 spent on Social increases sales by \$10.
* The model assumes **TV and Social have independent, constant effects.**

### Questions:

* What if spending more on Social changes how effective TV is?
* What if the effect of TV tapers off after some amount?

---

## ✅ Example 2: Product Feature Value

A company makes custom laptops and assigns utility scores to features:

$$
\text{Utility Score} = 50 \cdot \text{RAM(GB)} + 300 \cdot \text{SSD(GB)} + 100 \cdot \text{Battery(Hours)}
$$

### Assumptions:

* The value of 1GB RAM is always \$50 — no matter how much RAM you already have.
* 1 extra hour of battery is always worth \$100 — even going from 1 → 2 hours, or 9 → 10.

### But…

* Users may **value battery life more when it’s low**, and less when it's already high.
* Customers may only need “enough” SSD and value flattens after that.

---

## ✅ Example 3: Linear Scoring in HR

A hiring team uses:

$$
\text{Score} = 2 \cdot \text{Experience (Years)} + 3 \cdot \text{Education Level} + 1 \cdot \text{Skill Test Score}
$$

Assumptions:

* 1 year of experience is worth +2 points, always.
* 1 more point in test score is worth +1 point in hiring score, regardless of baseline.

### Ask Students:

* Are these assumptions fair?
* Should the value of 5 years vs 6 years of experience be same as 1 vs 2?

---

## 📈 Visualization Idea

Use graphs to **visualize the implication** of linearity:

* **Linear line**: constant slope → constant rate of change
* **Nonlinear**: slope changes → diminishing/increasing returns

---

### 📊 Exercise: Identify Linear vs Nonlinear Behavior

Provide students with different objective formulas and ask:

* Is the relation linear?
* What does the coefficient mean?
* What’s the assumption behind this coefficient?

Example:

1. $\text{Profit} = 100 \cdot \text{Units Sold} - 50 \cdot \text{Advertising Cost}$
2. $\text{Satisfaction} = 50 \cdot \log(\text{Speed}) + 100 \cdot \text{Design Quality}$

Ask:

* Which one is linear?
* Where might it break?

---

## 🧠 Summary Takeaways

| Insight                             | Description                                         |
| ----------------------------------- | --------------------------------------------------- |
| Coefficients reflect value/tradeoff | Interpret weights as marginal effects               |
| Linearity simplifies modeling       | But may hide real-world complexity                  |
| Constant value = constant tradeoff  | Useful approximation, but verify                    |
| Visualize to test reasonableness    | Plot input vs output to see relationships           |
| Nonlinearity is everywhere          | Linear models are starting points, not final truths |

---

## 📦 Optional: Python Notebook Idea

Use `matplotlib` and `numpy` to simulate and visualize:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 10, 100)
linear = 50 * x  # e.g., value of RAM in GB
nonlinear = 300 * (1 - np.exp(-0.4 * x))  # diminishing returns

plt.plot(x, linear, label="Linear (constant value)")
plt.plot(x, nonlinear, label="Nonlinear (diminishing returns)")
plt.xlabel("Input (e.g. RAM GB)")
plt.ylabel("Utility / Value")
plt.title("Linear vs Nonlinear Relationship")
plt.legend()
plt.grid(True)
plt.show()
```

---

