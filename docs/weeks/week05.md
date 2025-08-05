# Prepare for Week 5
## Problems
#### P1. Solve version 4 of NCAA T-shirt problem
- Here is [version 4](weeks/week03/#version-4-unifrom-random)
- You could do exactly what we did for version 3, only instead of 3 possible scenario for demand,  
consider 2000 possible scenario for demand!
- Remember,  if you could do it for more than one case, you could do it for 2000 or 2 million or cases!
    - This is one of super powers of spreadsheet or mathematical modeling using computer, 
- If you could do it one time, you could do it one billion time!
#### P2. Go Beyond EMV in version 4 of NCAA T-shirt problem
- Review how well EMV(expected monetary profit) represent our real world preferences and objectives
- in each of following cases, find the optimal order!
##### version 4.1: Fix cost for low profit
- If our profit falls below 8000, it will cost us another 1000$
##### version 4.2: True objective is function of profit
- Our economist, did an extensive research, asking many questions from owners about how valuable is  
money in different situations, he finally claimed that:
- Profit is not our real objective, our real objective is utility, which itself can be seen as a  
function of profit
- He also came up with the formula: $ U(m) = \sqrt{m} $ , where $ U $ is our utility and $ U(m) $ is money  
or profit

- We accept his claim! Now find optimal order!

- You should Replace Profit or monetary value, with Utility which leads to replacing EMV with  
Expected Utility (EU)


- So basically, instead of: $$ \text{Choose } x \text{ to maximize } \mathbb{E}[\text{profit}(x)] $$



- You should: $$ \text{Choose } x \text{ to maximize } \mathbb{E}[U(\text{profit}(x))] $$


- You can simulate uncertain outcomes, compute utility of each, and then average them → just like with monetary profit, but now with utility instead of money.

#### 🧠 **Problem 3:** 🧮 **Which Loan Offer Should You Take?**

#### **Scenario**
- Assume that you are decision scientist and decision making expert, helping people to make best   
"financial decisions".
       - You are your first customer
You need a loan of 1 billion toman.
You have **two offers**:

- Bank A offers: 1B toman, repaid in 24 monthly installments of 50M each

- Bank B offers: 1B toman, repaid in 48 monthly installments of 31M each

You plug these into an IRR calculator(This is by far easiest part of the job in 2025)

> Bank A: **Effective interest rate = 20% per year**
> Bank B: **Effective interest rate = 25% per year**