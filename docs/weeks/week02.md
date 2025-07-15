- From Real World to a Mathematical Model

 - how can we convert it to a problem that makes sense and apply mathematicals tools to solve them
---

That's a strong starting point! Let's turn your raw ideas into  
**engaging, thought-provoking problems** that challenge learners to think about:

1. **Real-life decision-making**
2. **Quantifying preferences and values**
3. **The necessity and limitation of mathematical models**

Below are **three well-structured, motivating problem scenarios** with framing questions and  
follow-up ideas. You can use them for group discussion, modeling exercises, or simulation  
assignments later in the course.

---

## 🚗 Problem 1: **Buying a Car – What’s the Right Car for You?**

### **Scenario**

- Assume that you are decision scientist and decision making expert, helping people to make best   
"car buying decisions".
       - You are your first customer
- How should you make this decision? 
- Can you convert this problem to quantitative one?

**Do you need a car at all?**
If yes, which one should you buy?

---

### **Discussion Starters**

* What **criteria** matter most to you? (e.g., cost, comfort, fuel efficiency, resale value, social  
status, safety, maintenance cost, long-term flexibility)
* Can you **rank or assign weights** to your preferences?
* Can you **measure** these things objectively? If not, how would you estimate them?
* What **trade-offs** are involved? (e.g., new car = peace of mind vs. used car = cheaper now)
* How would you **model this decision**?

---

### **Challenge**

> Build a simple multi-criteria decision model for your top 3 car options. Assign weights to your  
values and score each option.

---

### **Key Learning Themes**

* Decision modeling
* Quantifying qualitative preferences
* Multi-criteria decision making
* Subjectivity and uncertainty in modeling
* Sensitivity analysis: what happens if weights change?

---

## 🧮 Problem 2: **Which Loan Offer Should You Take?**

### **Scenario**
- Assume that you are decision scientist and decision making expert, helping people to make best   
"financial decisions".
       - You are your first customer
You need a loan of 1 billion toman.
You have **two offers**:

* Bank A offers: 1B toman, repaid in 24 monthly installments of 60M each
* Bank B offers: 1B toman, repaid in 36 monthly installments of 45M each

You plug these into an IRR calculator(This is by far easiest part of the job in 2025)

> Bank A: **Effective interest rate = 20% per year**
> Bank B: **Effective interest rate = 25% per year**

So: “Bank A is better. Lower interest.”

But is that the full story?

---

### **Discussion Starters**

* What is **IRR**, and what does it mean in this context?
* Is interest rate the only factor that matters?
* What about your **cash flow** flexibility?
* What if inflation is high or uncertain?
* 

---

### **Challenge**

> Build a small cash flow model for both loans. Explore scenarios where a higher interest loan  
might be better (e.g., more flexibility, lower early payments).

---

### **Key Learning Themes**

* Time value of money (TVM), cash flow modeling
* Present value vs. internal rate of return
* Importance of context in interpreting model results
* Model limitations (e.g., assumes fixed future, ignores risk)

---

## 📈 Problem 3: **How Should You Allocate Your Marketing Budget?**

### **Scenario**

You are the marketing lead for a product with a 100 million toman budget. You have 3 possible channels:

* **Instagram influencers**
* **Search ads (Google)**
* **TV ads**

Your previous data shows:

| Channel   | Cost per 1K reach | Expected conversion rate |
| --------- | ----------------- | ------------------------ |
| Instagram | 50K toman         | 4%                       |
| Google    | 100K toman        | 8%                       |
| TV        | 300K toman        | 2%                       |

But these numbers are averages. Conversion varies by season, target segment, and message.

---

### **Discussion Starters**

* How would you **allocate** your budget?
* What’s your **objective**? Maximize conversions? Awareness? Long-term value?
* What assumptions are you making?
* What if your past data is **biased** or outdated?
* What about **uncertainty** or **competitor response**?

---

### **Challenge**

> Build a simple budget allocation model based on expected ROI per channel. Then run a **simulation** where conversion rates vary randomly.

---

### **Key Learning Themes**

* Data-driven decision making
* Assumptions and their risks
* Sensitivity to data quality
* Optimization under uncertainty
* When to trust the model and when to be skeptical

---

## 🧭 Optional Follow-up Questions (All Problems)

* What would you ask from a **data analyst** to help improve your decision?
* Can **AI help** you here? If so, what part of the decision? If not, why?
* What part of the decision needs **human judgment**?

---

Would you like me to turn these into:

* A printable handout or slide set?
* Excel / Python / Jupyter examples for one or more of them?
* A group activity format (discussion + model + presentation)?

Let me know how you'd like to run this session.




## 🎯 **Session Goals**

* Show the **big picture of decision making**
* Emphasize the role of **mathematical models** in supporting decisions
* Discuss the **limits and assumptions** of models
* Position **probability, statistics, and simulation** in this process
* Reflect on what matters **most in the AI age**
* Engage participants with **motivating problems** that provoke thought

---

## 🧠 1. Conceptual Anchor: Decision = Model + Judgment



> "All models are wrong, but some are useful." – George Box

Use this to frame **why we model reality**, even if imperfectly.

---

## ⚙️ 2. Big Picture of Decision Making (Framework)

Draw or show this simplified flow:

```
[Real-World Problem]
       ↓
[Understanding / Assumptions]
       ↓
[Modeling] → [Computation / Optimization / Simulation]
       ↓
[Interpretation / Insights]
       ↓
[Real-World Action / Decision]
       ↓
[Feedback & Revision]
```

Now let's support this with real-world thinking challenges 👇

---

## 🔍 3. Motivating Thinking Problems (Real-World Inspired)

Each of these shows the **importance of modeling**, **limitations of models**, and **need for judgment**.

---

### **Problem 1: The Ice Cream Vendor at the Beach**

**Scenario**: You’re selling ice cream at a beach. You can bring 20, 40, or 60 ice creams in a cooler. If you bring too few, you lose customers. Too many, and they melt.

* How should you decide how many to bring?
* What variables matter?
* How would you model it?
* What information would you need?
* Can a mathematical model give you a perfect answer?

**Themes**: Uncertainty, demand modeling, trade-offs, simulation, model limits.

---

### **Problem 2: Hiring a New Team Member**

You must decide between two candidates:

* Candidate A has experience, high performance, but poor team fit
* Candidate B is a great team fit, eager to learn, but less experienced

You try to model future team productivity under each scenario.

* What are the variables?
* What can you quantify?
* What remains qualitative?
* Can a spreadsheet or formula help?

**Themes**: Judgment vs. modeling, soft factors, limited info.

---

### **Problem 3: The Bakery Optimization Problem**

You own a bakery and want to maximize profit:

* You make cakes and cookies
* Each uses flour, labor, and oven time
* There are constraints (supply, hours)

**Mathematical model possible**: Linear programming

Now:

* What if customer demand is uncertain?
* What if sugar price changes tomorrow?
* What if a big buyer suddenly walks in?

**Extension**: How would AI help you? What can it not do?

**Themes**: Optimization, assumptions, volatility, AI limitations

---

### **Problem 4: Marketing Budget Allocation**

You want to allocate a fixed budget between:

* TV ads
* Instagram influencers
* Search engine ads

You model conversions per dollar spent based on past data.

Now:

* What if your past data is outdated?
* What if influencer popularity suddenly changes?
* What if a competitor enters the market?

**Themes**: Statistics, assumptions, overfitting, causal inference, robustness

---

### **Problem 5: Pandemic Policy Planning**

Governments modeled lockdown policies using:

* Infection rates
* Mobility data
* ICU capacity

But:

* Data was uncertain and delayed
* Behavioral reactions were unpredictable
* Ethical concerns arose (freedom vs. safety)

Ask: Can any model capture all of this? What should the role of the model be?

**Themes**: Systems thinking, simulation, complexity, uncertainty, judgment

---

## 💡 4. Interactive Prompt

Ask participants:

> Think of a decision **you or your team recently made**.
>
> * Did you use a model (even an informal one)?
> * What was known vs. uncertain?
> * How would a mathematical model help?
> * What could it miss?

This encourages **personal reflection** and sets the stage for modeling concepts.

---

## 🧠 5. Bonus: AI-Age Emphasis

Close with discussion:

* AI and data help build better models
* But **understanding** the **fit between model and real world** becomes even **more important**
* Humans are still needed for:

  * Framing the problem
  * Choosing the right model type
  * Judging when the model’s outputs don’t apply
  * Ethical considerations

---

## 🧰 Would You Like Slides or Handouts?

I can generate:

* A slide deck outline
* Markdown or PDF handout summarizing the big picture
* Jupyter Notebook or Excel-based modeling demos (for the bakery or budget problem)

Let me know what you’d like next.
