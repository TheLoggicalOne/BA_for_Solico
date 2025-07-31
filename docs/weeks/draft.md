Here is a well-structured **Week 4 course content** draft based on your outline, expanded with added examples, explanations, and teaching strategies. It aims to:

* Connect intuition to modeling
* Emphasize the dangers of naïve estimation
* Introduce expected value and optimization under uncertainty
* Deepen student understanding of how and why simulation and probability distributions matter

---

# 🧠 Week 4 – Decision Making Under Uncertainty: Playing the Averages & Its Limits

## 🧩 Part 1 – What Do You Do When You Face Uncertainty?

**Discussion prompt:**

> Think of a time when you had to make a decision but didn’t know all the facts. What did you do?

### 👀 Real-World Examples of Decisions with Uncertainty

| Decision                      | Uncertain Variable                   |
| ----------------------------- | ------------------------------------ |
| Budgeting for next year       | Future income                        |
| Hiring staff for a new branch | Customer demand                      |
| Advertising spend             | Conversion rate                      |
| Stocking a new product        | Future sales volume                  |
| Expanding a factory           | Future energy prices / market growth |

📌 **Class Activity**: Ask students to give business examples from their own work experience where they had to guess or estimate an uncertain quantity.

---

## 🧪 Part 2 – What Should You Do?

You have two choices:

1. Ignore uncertainty (and hope for the best)
2. Be scientific — use **data and models** to make better decisions

💬 **Narrative**:

> Even the best experts cannot “know” the future. But we can make **educated guesses**. If we gather data and understand the forces behind uncertainty, we can **summarize uncertainty using probability distributions**.

---

## 🧮 Part 3 – Playing the Averages

### Example: Future Income

You don’t know your income next year. Based on past years and trends, you estimate:

| Scenario                 | Probability | Income            |
| ------------------------ | ----------- | ----------------- |
| Low Market               | 0.2         | 120 million toman |
| Normal                   | 0.5         | 180 million toman |
| Promotion or Project Win | 0.3         | 250 million toman |

🎯 **Expected Value**:
$\text{EV} = 0.2 \times 120 + 0.5 \times 180 + 0.3 \times 250 = 186$

So you use 186 million toman as your **"best guess"** and make all your financial plans based on it.

---

## 🤔 Part 4 – But Wait… "Best Guess" for What?

### 🧠 Important Concept:

> "Best guess" for an uncertain value is often just the number with **least average error**, not the one that gives you the **best decision outcome**.

### 📢 Critical Distinction:

* Estimation Objective: Minimize **error in guessing** uncertain value
* Decision Objective: Maximize **business outcome** (e.g., profit)

---

## 📈 Part 5 – Revisit NCAA T-Shirt Problem (Version 2)

Demand is uncertain. In Version 2, we had:

* Three possible demand levels
* Probabilities associated with each
* We optimized **based on expected demand**

🎯 Does this lead to the best decision?

⚠️ **Flaw of Averages**:

> Using expected demand hides risk. You may choose a quantity that leads to large losses if demand is low or high.

---

## 🧩 Part 6 – The Walton Bookstore Calendar Problem

(From book, Page 736)

* Cost: \$7.50
* Selling price: \$10
* Unsold refund: \$2.50
* Demand is uncertain, average 200

**Q1**: Should we order 200 calendars (the expected demand)?

Use a **probability distribution** of demand and simulate or calculate expected profit for each possible order quantity.

📊 **Jupyter Notebook Suggestion**:
Let students simulate profits for order quantities of 150 to 250, under a triangular or normal distribution of demand centered at 200.

---

## 🧪 Part 7 – When Does Playing the Averages Work?

✅ When:

* Your objective is linear in the uncertain quantity (e.g., profit = price × demand)
* You have no downside or upside risk (e.g., over/understocking doesn’t hurt much)
* The distribution is symmetric and narrow

❌ When:

* You face **nonlinear costs or revenues**
* Large downside risk (like overstocking calendars)
* Highly **skewed** or **uncertain** distributions
* Your objective involves probabilities, not just averages (e.g., minimizing chance of stockout)

---

## 🔮 Part 8 – Summary

* Decision making under uncertainty requires a **distribution**, not just a guess
* **Expected value** is useful, but not always optimal
* Many people (even pros) make decisions by **"playing the averages"**
* This works **sometimes**, but **fails spectacularly** in others
* Simulation is a powerful tool to understand the **range of possible outcomes**

---

## 💻 Hands-On Assignment (Jupyter Notebook or Excel)

1. Simulate the Walton Bookstore problem.
2. Try three order quantities (e.g., 180, 200, 220).
3. Use a normal or triangular distribution centered at 200.
4. Estimate average profit from 1000 simulations for each.
5. Which one has the best performance **on average**?
6. What is the downside risk for each?

---

## 🧠 Class Discussion

* Can you find examples where you or your company use the "play the average" strategy?
* Have you seen it backfire?
* How could you introduce **probabilistic thinking** into your daily or organizational decision-making?

---

Would you like a ready-to-use Jupyter Notebook or Excel template to accompany this session?
