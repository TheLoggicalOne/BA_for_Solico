# Prepare for Week 8
## Beyond the Numbers: Probabilistic Reasoning for Business Analytics
- Understanding P-values, Conditional Probability, and Why Common Sense is Your Best Tool

## Our Approach so far: Forward problem
- So far we have discussed how to make deicison, assuming we know everything(at least up to distribution)
- Assuming we know mathematical model of system, and our preferences and distribution of variables,  
we have(hopefully) learned how to make decision
- But in real world, we dont know any of these
- Let first review the forward problem, and all the things we need for it
#### To solve business problem, and make optimal choices, we should:
- consider all possible choices: 
    - set of choices, represented by variables
    - This is a mathematical model of set choices!
- compute reslut of each possible choice: 
    - mathematical model that relates parameters, inputs, decision variables and outputs(results)
- evaluate and compare result of different choices(perfect-info judge)
    - This is a metric to compare and evaluate choices
    - Here we need a mathematical model of our preferences
    - we should be able to evaluate and weigh pros and cons of different resluts
    - we usually have multiple criteria
    - Objective function: a way of representing our preferences over set of all possible results
    - so we need a way of converting a multi criteria decision making problem to a single objective maximization problem

- evaluate and compare choices, without knowing the final outcome(imperfect-info judge)
    - Imperfect information choice evaluator/metric:
    - In presence of uncertainty, we don't see result of our choices, each choice will leads to distribution  of possible outcomes, so we should have decision rule, based on distribution of  
    outcome, not the outcome itslef

#### In other words we need:


- mathematical model of the system: variables and their relations: represent relation between variables(inputs, outputs)
    - In deterministic case, we model variables using numbers, so we talk about their values
    - In presence of uncertainty, we model variables using random variable, so we talk about  distribution of value   


- mathematical model of our preferences and descion making: 
    - algorithm to compare and evaluate choices:
    - perfect-info algorithm , which can rank and score different finall outcomes
    - imperfect info algorithm, which can compare choices, without even knowing the finall outcome, these algorithm should decide based on distribution of outcomes
actually, we could consider our objective as another variable, but since it depends on our subjective

- Deterministic vs stochastic
    - variales vs random variable
    - value of input vs distribution of values of input
    - value of output vs distribution of values of outputs
    - preferences over outcomes vs preferences over distribution of outcomes\
    - value of objective vs distribution of value of objective



#### From Perfect-Info Choice evaluator(Judge), to Imperfect-Info choice evaluator(judge)
- From prefernces over deterministic objective to preferences over distribution of objective
- Most common approach is considering expected value of objective
    - wokrs great if, your objective is your real objective! As represented bu numbers:
        - $ 15100 - 15000 = 8100 - 8000 = 1100 - 1000 $
        - $ 2 * 10000 = 20000 $
        - in a way that  
    - Suffer from flaw of averages if, your real objective is non-linear function of this objective
    - It is not enough to have a objective function that is rank-consistent with your preferences

## To Reality: Inverse Problem
- To solve a business problem, we need to know:
    - relations between variables
    - distribution of inputs
    - distribution of outputs
    - distribution of objectives
    - which distribution of outputs we prefer
    - Our preferences over outputs and distribution of outputs

- If we know all of these things, we are facing a simple forward problem:
- froward Problem: we know the system, and what it does on its input. Given each set of inputs,   
we can compute output of the system
- But, we don't know any of these thing!  
- How can we find these? We are actually facing the inverse problem. 
- We can observe examples of (inputs, outputs) and we want to discover the system itself, or  
at least parts of it
- From our domain knowledge an studiyng the system itself, we might be able to make some  
reasonable assumption:
    - Number of defective product is a bionomial random variable( but we still don't know its parameter)  
    - There is a relation between daily demand and weekday
    - Relation between y and x is linear(but we don't know what are its coefficients)
- To make reasonable assumption about our problem, we shoould:
    - know and feel structure and properties of mathematical model
    - know and feel structure and properties of our real problem(domain knowledge)
- We also have some observations: Data! 
- We have observed the system for many cases of inputs, and recorded its output
- So we have hundreds(or more, or less) of (inputs, outputs) examples
- But, all we can do, is probabilistic arguments...
- Based on our observations, we can judge liklihood of different theories, but we never could make  
sure judgments
- If a fund, beats the market 37 weeks in a 52 week year, what can we say about his weekly chance of  
success?
- If we observe, each dollar increase in marketing, results in $ 1.5 $ dollar increase in sale...
- Here is our demand data, what is the distribution of demand? of course, we can not answer this with usuall certainty, we just can make some probabilistic reasoning

## probability to the rescue
- answer of all of these questions is in probability language, more specifically conditional probability  
and bayesian perspective
- You want to really understand results of A/B testing? hypothesis testing?
- Regression results?
- Is this distriution good fit to the data?
- Should I invest in this broker?
- Is this new change really working?
- Are we facing a different year? is the shift in demand just a fluctuation or something foundametal has changes?
- Is this new website design better, or was that sales bump just luck?
- Did our marketing campaign actually work?
- Did our marketing campaign actually work?
- Is this food casuing cancer? 
- Should I change my diet, because of all of these medical studies?
- DEAD FISH DON’T READ MINDS
e
## we need an overview of [scientific method](../concepts/scientific_method.md)

## From Reductio ad absurdum to Reductio ad unlikely
- How can we prove a theory?
- When we increase our beleife in a theory?
- If our observation are consistent with the theory?
- If negation of theory results in contradiction?

To confirm a theory, is it enough that our observation is consistent with that theory?
### Reductio ad absurdum
To prove a theory $ T $ is true, we consider its negation, call it $ H_0 $
1. Suppose the negation of target theory is true: $ H_0 $ is true. 
2. It follows from $ H_0 $ that a certain fact F cannot be  the case. 
3. But F is the case.  
4. Therefore, H is false.

- basically, we show(deductively) that negation of our target theory is inconsistent with observations(facts)

### Reductio ad unlikely

1. Suppose the null hypothesis H is true.  
2. It follows from H that a certain outcome O is  very improbable (say, less than Fisher’s 0.05  threshold).
3. But O was actually observed.  
4. Therefore, H is very improbable.



## **Beyond the Numbers: Probabilistic Reasoning for Business Analytics**

### Understanding P-values, Conditional Probability, and Why Common Sense is Your Best Tool

---

### Why Are We Here? The Analyst's Dilemma 🧐**

In business, we face constant uncertainty.
* Did our marketing campaign *actually* work?
* Is this new website design better, or was that sales bump just luck?
* Is this flagged transaction fraudulent or a false alarm?

Our goal is to use math as an **extension of common sense** to make better judgments under uncertainty. This means going beyond just calculating numbers and truly understanding what they mean.

---

###  A Classical Argument: "Reductio ad Unlikely"**

This is a powerful form of reasoning used to evaluate a hypothesis.

**The Logic:**
1.  **Assume a hypothesis (H) is true.** (e.g., "This star cluster is just a random coincidence.")
2.  **If H is true, a certain outcome (O) would be extremely improbable.** (e.g., "The chance of 6 stars being this close randomly is 1 in 500,000.")
3.  **But, we observed that improbable outcome O!** (e.g., "We see the Pleiades star cluster right there.")
4.  **Conclusion: The initial hypothesis (H) is probably false.**



[Image of the Pleiades star cluster]


This helps us infer that there's an underlying structure or cause, not just random chance.

---

###  When "Unlikely" Reasoning Fails ⚠️**

This logic has critical pitfalls if we're not careful. It's easy to misuse!

* **The Albino Paradox**: Imagine finding one albino in a random group of 50 people.
    * Hypothesis (H): "This is a group of human beings."
    * Observation (O): We found an albino. This is a very rare event (improbable).
    * **Flawed Conclusion**: "Therefore, the hypothesis that they are human is probably false."
    * **The Lesson**: **Improbable is not impossible.** A rare event doesn't automatically disprove a very plausible hypothesis.

* **The Bible Codes & Data Mining**: People "found" predictions in ancient texts by looking for equidistant letter sequences.
    * **The Trap**: With enough "wiggle room" (changing the skip interval, direction, etc.), you can find *any* pattern you look for.
    * **Business Lesson**: This is like "torturing the data until it confesses." If you run enough tests without a clear hypothesis, you're bound to find a statistically significant result by pure chance.

---

###  The P-value: A Formal Tool for "Unlikely"**

The p-value is a cornerstone of statistical testing, used everywhere from medicine to marketing.

* **Null Hypothesis ($ H_0 $)**: The "skeptic's" hypothesis. It assumes **no effect**.
    * "The new drug has no effect."
    * "The ad campaign did not increase sales."
    * "There is no difference between website A and website B."

* **P-value Definition**: The probability of seeing our observed data (or something even more extreme), **assuming the null hypothesis ($ H_0 $) is true.**
    * $ p = P(\text{Observed Data or more extreme} | H_0 \text{ is true}) $

* **P-value if a measure of surprise!** it basically shows how surpring given extremness of  
our observation is

* **The Magic Threshold**: Conventionally, if $ p < 0.05 $, we call the result  
**"statistically significant"** This suggests the outcome was too unlikely to have occurred by random chance alone, so we **reject the null hypothesis**.



### P-values in Business: A/B Testing**

P-values are crucial for making data-driven decisions.

**Scenario**: You're running an A/B test on your website.

* **Version A**: The original button.
* **Version B**: A new, bright green button.
* **Null Hypothesis ( $ H_0 $ )**: The button color has no effect on clicks.  
($ Conversion_A = Conversion_B $)

**Results**: Version B gets more clicks. You run a statistical test and get a **p-value of 0.03**.

**Interpretation**:

* Since $ 0.03 < 0.05 $ , the result is statistically significant.
* There is only a 3% chance you would see this difference in clicks (or a larger one) if the green button truly had no effect.
* **Decision**: You can be reasonably confident(how much) the effect is real. You reject $ H_0 $ and implement the green button.

**Question**: How confident are you that the effect is reall? How likely?  
What is the probability that effect is real?  

---
###  The Prosecutor's Fallacy & The Base Rate Fallacy

**Scenario**: A crime is committed. DNA evidence at the scene matches a suspect.
* The chance of a random person matching the DNA is 1 in 10,000. (This is like a p-value).

**The Prosecutor's Argument**: "The chance of a random match is 1 in 10,000. Therefore, there is  
only a 1 in 10,000 chance the suspect is innocent." **WRONG.**

---

###  The #1 Most Dangerous Mistake with P-values!**

This is the single most important concept to understand. It's all about **conditional probability**.

A p-value tells you:

* $ P(\text{Data} | H_0 \text{ is True}) $ -> *The probability of seeing the evidence, assuming the person is innocent.*

What you *want* to know is:

* $ P(H_0 \text{ is True} | \text{Data}) $ -> *The probability the person is innocent, given the evidence.*

**These are NOT the same thing!** Confusing them is called the **Prosecutor's Fallacy**.

---

###  The Prosecutor's Fallacy & The Base Rate Fallacy**

**Scenario**: A crime is committed. DNA evidence at the scene matches a suspect.
* The chance of a random person matching the DNA is 1 in 10,000. (This is like a p-value).

**The Prosecutor's Flawed Argument**: "The chance of a random match is 1 in 10,000. Therefore, there is only a 1 in 10,000 chance the suspect is innocent." **WRONG.**

**Why it's wrong: The Base Rate Fallacy**

* The prosecutor ignores the **base rate**: How many people *could* have been at the crime scene?
* If the crime was in a city of 1,000,000 people, you'd expect about 100 people to match the DNA by pure chance!
* The DNA evidence tells you the suspect is one of those 100 people, not that they are 99.99% guilty.


---

###  Statistical Significance ≠ Practical Importance 💰**

A "significant" result doesn't mean it's a *meaningful* result.

**The Birth Control Scare Example**:

* A study found a new birth control pill "doubled the risk" of a blood clot (thrombosis). This was a statistically significant finding ($ p < 0.05 $).
* Panic ensued, and many women stopped taking it.
* **The Missing Context**: The original risk was incredibly small (1 in 7,000). Doubling it made it 2 in 7,000. The risk of getting a blood clot from pregnancy was far higher! The "significant" result was not practically important.

**Business Lesson**: A marketing change might produce a statistically significant 0.01% lift in sales. But is that tiny lift worth the cost of the campaign? **Always ask about the size of the effect and the ROI.**

---

###  The Analyst's "Wiggle Room": P-Hacking & Bias**

Pressure to find "significant" results can lead to bad science.

* **P-hacking**: Trying different things (deleting outliers, adding variables, stopping the test at a convenient time) until you get a $ p < 0.05 $. This is cheating.
* **File Drawer Problem**: Studies with non-significant ("boring") results often don't get published or shared. We only see the successes, which makes effects look more robust than they really are.

This creates a distorted view of reality and leads to investing in ideas that only worked due to luck. **Be skeptical** of amazing, one-off results. Demand replication!

---

###  A More Intuitive Way: Bayesian Inference 🧠**

While p-values are common, Bayesian thinking is often closer to how we naturally reason.

* **P-values ask**: "How surprising is this data, assuming my hypothesis is wrong?"
* **Bayesian Inference asks**: "Given the data I just saw, how much should I update my belief in my hypothesis?"

It lets you formally combine:
* **Prior Belief**: What you thought before the experiment (e.g., "I'm 30% sure this new ad will work based on past campaigns.")
* **Evidence**: The data from your test.
* **Posterior Belief**: Your updated belief after seeing the data.

This directly answers the question managers care about: "How likely is it that this is working?"

---

###  Your Toolkit as a Smart Analyst 🛠️**

Your job is to provide wisdom, not just numbers.

1.  **Use P-values as a Detective, Not a Judge**: A low p-value is a clue that something interesting *might* be happening. It's a starting point for more investigation, not the final verdict.
2.  **Mind Your Conditionals**: Always be clear if you're talking about $ P(\text{Data} | \text{Hypothesis}) $ or $ P(\text{Hypothesis} | \text{Data}) $.
3.  **Context is King**: Never forget the base rate. A result is meaningless without context. How big is the effect? What's the ROI?
4.  **Stay Skeptical**: Be aware of p-hacking and the file drawer problem. One study is just one study. Is there corroborating evidence? Can it be replicated?

By mastering these principles, you move from being a data cruncher to a trusted strategic advisor.
