

## **The Foundation of Knowing: The Scientific Method**

Before we can analyze data, we need a reliable way to ask questions about the world. Our brains are incredible pattern-matching machines, but they are also flawed. We suffer from **cognitive biases**, like confirmation bias (seeing what we want to see) and finding illusory patterns in random noise.

The **scientific method** isn't a magic formula; it's a rigorous process designed to protect us from fooling ourselves. It's a systematic way of asking questions and testing ideas to build reliable knowledge, whether in a physics lab or a business meeting. 🧪

**We should see scientific method as a principled way of using our exprience and observations  
it helps us generalize and predict, using our exprience and data**
---

### **The Core Loop of Discovery**

The scientific method is a cycle of disciplined thinking. You can think of it as a loop that constantly refines our understanding. 

1.  **Observation & Question:** It starts with noticing something interesting or puzzling.
    * *Science*: "Why do apples fall down but the moon stays up?"
    * *Business*: "Our customer churn rate increased by 5% last quarter. Why?"

2.  **Hypothesis:** You formulate a specific, testable explanation or prediction. A good hypothesis must be **falsifiable**—meaning, there has to be a way to prove it wrong.
    * *Science*: "A force called gravity pulls objects with mass toward each other."
    * *Business*: "The churn rate increase was caused by the recent price hike."

3.  **Experiment:** You design a fair test to see if the evidence supports or contradicts your hypothesis. **This is the most critical step.** The goal is to isolate the one factor you're interested in and see what effect it has.

4.  **Analysis & Conclusion:** You examine the results of your experiment.
    * Does the evidence support the hypothesis? If so, your confidence in it grows.
    * Does the evidence contradict the hypothesis? If so, you must either discard the hypothesis or revise it. This is not a failure! It's progress.

5.  **Iteration:** The conclusion of one experiment becomes the observation for the next. If the price hike wasn't the cause of churn, what is? A new cycle begins.

---

### **The Heart of the Method: The Controlled Experiment**

In most tests of economic theory, and certainly for evaluating business strategy, our goal is to infer that one variable (such as marketing spend) has a **causal effect** on another variable (such as sales). Simply finding an association between two variables might be suggestive, but unless causality can be established, it is rarely compelling.



The notion of **_ceteris paribus_**—which means **“all other relevant factors being equal”**—plays the most important role in causal analysis. For example, in analyzing consumer demand, we are interested in knowing the effect of changing the price of a good on its quantity demanded, while holding all other factors—such as income, prices of other goods, and individual tastes—fixed. If other factors are not held fixed, then we cannot know the true causal effect of a price change.

- note: even in sensitivity analysis, we assume a **cetris paribus** frame work

- **Cetris Paribus start from our question definition or our theory**: Most of our theory,  
and questions that we ask, are cetris paribus in by nature

How do you design a "fair test" that achieves *ceteris paribus*? The gold standard is the **controlled experiment**. To design one, we must define our variables:

* **Independent Variable**: The one and only thing you intentionally **change** or manipulate. This is the presumed *cause*.
* **Target(Dependent) Variable**: The outcome you **measure** to see if the independent variable had an effect. This is the presumed *effect*.
* **Controlled Variables**: Everything else that could possibly influence the dependent variable. You must keep these **constant** to isolate the true effect of the independent variable.

#### **Example: A Simple Deterministic Experiment**

Let's test a simple, non-random hypothesis where we can easily control the variables.
* **Question**: Does the time it takes to boil water depend on the amount of water?
* **Hypothesis**: More water will take longer to boil.
* **Independent Variable**: The volume of water (1 liter vs. 2 liters).
* **Dependent Variable**: The time it takes to reach 100°C.
* **Controlled Variables**: The starting temperature of the water, the stove's heat setting, the pot used, and the atmospheric pressure.

By keeping everything else the same (*ceteris paribus*), if the 2-liter pot takes longer to boil, you can be very confident it's because of the volume.

---

### **The Challenge of a Noisy World: The Probabilistic Experiment**

In business, biology, or marketing, we rarely have such clean, deterministic systems.  
The world is full of **noise**, which is the combination of many other unobserved and random factors.  
This noise is another variable we must control for. **But how can we control for millions of random, unobserved factors like a customer's mood or their unique need**s?

We can't control them individually. However, thanks to the **law of large numbers**, we can manage their aggregate effect.  
This is where probability enters the process. Because we can only account for the effect of this noise probabilistically, we can only make **probabilistic inferences** about the results.

#### **Example: A Probabilistic Experiment**

* **Question**: Does our new website design ("Version B") lead to more sales than the old design ("Version A")?
* **Hypothesis**: Version B will have a higher average conversion rate.
* **Independent Variable**: The website design shown to the user (Version A or Version B).
* **Dependent Variable**: Whether the user makes a purchase.
* **Uncontrolled Variables (Noise)**: The user's mood, budget, internet speed, whether they got distracted, etc.

To run a fair test, we use two key techniques:

1.  **Control Group vs. Treatment Group**: We split our subjects (website visitors) into two groups.
    * **Control Group**: Sees the old design, Version A. This gives us a **baseline** for comparison.
    * **Treatment Group**: Sees the new design, Version B.

2.  **Randomization**: We assign visitors to each group **randomly**. This is the magic ingredient! By randomizing, we don't eliminate the noise, but we ensure that it is, on average, evenly distributed between the two groups. Randomization turns all those uncontrollable factors into manageable random noise, allowing us to approximate a *ceteris paribus* condition.

Now, if we see a difference in the average conversion rate, we can be much more confident that it was caused by our **independent variable** (the website design) and not some other hidden factor.

---

### **What the Scientific Method Demands of Statistical Inference**

We can't just look at the results and say, "Version B got 5.2% conversions and Version A got 5.0%, so B is better." That difference could just be the random noise we talked about!

This is where the scientific method hands the baton to statistical inference. The principles of good experimental design inform how we must use our statistical tools:

1.  **The Need for Hypothesis Testing**: Because of randomness, we need a formal way to decide if the observed difference between our groups is a **real effect** or if it could have plausibly happened by **random chance alone**. This is the entire purpose of hypothesis testing.

2.  **The Logic of the Null Hypothesis**: The principle of **falsification** is built directly into statistics. We start by assuming the skeptical hypothesis—the **Null Hypothesis ($H_0$)**—is true ("The new design has no effect"). We then calculate how strange our observed result would be if that were the case.

3.  **The Meaning of the P-value**: The p-value is the tool that quantifies that "strangeness." It's the probability of seeing a difference as large as the one we observed, *assuming the null hypothesis is true*. A small p-value tells us that our result is very surprising if there's truly no effect, giving us a reason to reject the null hypothesis.

In short, **statistical inference is the mathematical toolkit for executing the scientific method in a world full of noise, randomness, and uncertainty.** It gives us the rules for weighing evidence and making principled conclusions without fooling ourselves.
