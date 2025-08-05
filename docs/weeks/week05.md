# Prepare for Week 5
## Problems
#### **Problem 1:** Solve version 4 of NCAA T-shirt problem
- Here is [version 4](weeks/week03/#version-4-unifrom-random)
- You could do exactly what we did for version 3, only instead of 3 possible scenario for demand,  
consider 2000 possible scenario for demand!
- Remember,  if you could do it for more than one case, you could do it for 2000 or 2 million or cases!
    - This is one of super powers of spreadsheet or mathematical modeling using computer, 
- If you could do it one time, you could do it one billion time!
#### **Problem 2:** Go Beyond EMV in version 4 of NCAA T-shirt problem
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
> Bank B: **Effective interest rate = 23% per year**

Which one is better? 
Try to solve this problem without any financial function or calculator, directly,  
from first princilples!

#### Problem 4: Solve version 6 of NCAA T-shirt problem!
##### Version 6: We have 3000 potential customer
- Each of them has a 50% chance of buying a T-shirt
- what is the optimal order in this version?

- Is our assumption realistic? how can we make it more realistic?

#### Problem 5: Solve combination of version 4 and 6 of NCAA T-shirt problem!
##### version 46: 
- In this version, we know (for a fact!) that demand is a number between 500 to 2500, and it could  
be any of these numbers, all with same chance 


- also,we know ishistory of our previus three years demand at the same event:


|Year|Demand|
|---|---|
|2024 |1400|
|2023 |2000|
|2022 |1600|
|2021 |1700|

- what is the optimal order in this version? 
- How real are our assumptions? How can we make them better?
#### Problem 6: Solve combination of version 5 and 6 of NCAA T-shirt problem!
##### version 56: 
- we have 3000 potential customer, Each of them has a 50% chance of buying a T-shirt
- also,we know is history of our previus three years demand at the same event:

|Year|Demand|
|---|---|
|2024 |1400|
|2023 |2000|
|2022 |1600|
|2021 |1700|


#### Problem 7: Work on EXAMPLE 15.1 ORDERING CALENDARS AT WALTON BOOKSTORE page 736 of the book
- solve it Using excel file for NCAA T-shirt problem!
- could you generalize this frame work?


