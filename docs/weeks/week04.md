# Prepare for Week 4
# 🧠 Week 4 – Decision Making Under Uncertainty: From Playing the Averages & to Playing the distributions

## 🧩 Part 1 – What Do You Do When You Face Uncertainty? Start Thiking

- Many of our decisions, depend on variables that are not deterministic, or even if they are, we  
don't know their value, so we are uncertain aout their value

> Think of a time when you had to make a decision but didn’t know all the facts. What did you do?

### 👀 Real-World Examples of Decisions with Uncertainty

| Decision                      | Uncertain Variable                   |
| ----------------------------- | ------------------------------------ |
| Budgeting for next year       | Future income                        |
| Hiring staff for a new branch | Customer demand                      |
| Advertising spend             | Conversion rate                      |
| Stocking a new product        | Future sales volume                  |
| Expanding a factory           | Future energy prices / market growth |



---


 
#### Consider following scenario
- You want to decide how much money you should spend on apartment, car and other costs for next year for next year, but it all depends on your next year income
    - But you don't know how much you will make next year
    - There are many uncertain factors that affect the income
- find some more examples here, related to business
- what do you do this situation? what should you do?
- Ask an expert, what will the expert do in this situation?

- We will make an educated guess for your income, and then solve a deterministic decision making  
problem, or a deterministic optimization problem
- If you want to be more scientific, using data analysis and scientific method, you will find  
best estimate for your future income, which is usually average value of possible future incomes  
(where the average is taken over all possible future incomes, with wights equal to probability of  
each of them)
- There are many situations similar to this one, when your best choice deopends on values of some  
uncertain quantity. Find some of these situations in your job and your life. How do you handle  
those annoying uncertain values?
- When facing uncertainty, many people, even experts, try to find the best estimate(best guess) for uncertain quantity, which is usually the average value of that quantity, or its expected value, this strategy,  
is a famous one:
    - Playing the averages

#### Consider version 2 of ORDERING NCAA T-SHIRTS
- As we saw in version 2 of ORDERING NCAA T-SHIRTS in week 3 (review it [here](weeks/week03/#version-2-three-way-fair-dice)) demand is uncertain, and data analyst is suggesting to replace  
demand with our best estimate for demand, play the averages for demand, and then proceed and make the best choice assuming that demand is just our best guess(here, our best guess is a result of sound data analysis method)
    - Does this method find the optimal choice?
    - Explain!

??? warning
    be carefull when you say "best estimate" or "best guess", whenever you say best, you should ask  best in what? Best with respect to what? actually, any "best" relates to an objective, when talking about best estimate or best predecition, or best guess for a value, we are talking about best in terms of error, or accuracy...when we are saying best estimate for demand, we do not care about which demand is good or bad, we are just searching for a number, which has minimum error
    But when we say "best choice" , we mean the choice that maximize our decicion making objective!
    Yes, these are two different objective, for two different problems: For estimation of demand, our objective is minimizing error of our estimation(which is different form our main decision making objective)

### Formulate version 2 of ORDERING NCAA T-SHIRTS as an optimization problem
- Can we formulate this problem as an optimization problem?

- If yes, what is the exact objective we are trying to maximize?
- What assumptions are we making?
- How well this objective represent the reality?
- Is the final optimization problem deterministic or stochastic?
- Can we generalize method of solving this to other decision making under uncertainty problems? 

### Work on EXAMPLE  15.1 ORDERING CALENDARS AT WALTON BOOKSTORE page 736 of the book
In August, Walton Bookstore must decide how many of next year’s nature calendars to order. Each calendar costs the bookstore $7.50 and sells for $10. After January 1, all unsold calendars will be returned to the publisher for a refund of $2.50 per calendar. Walton believes that the number of calendars it can sell by January 1 follows some probability distribution with mean 200. Walton believes that ordering to the average demand, that is, ordering 200 calendars, is a good decision. Is it?


### Think about "Playing The Averages" 
- Can you find examples that you or others use this?
- How common is this used?
- How good is this strategy?
- When does this strategy work?
- Think about reasons and situations that this strategy fails 


##  What Do You Do When You Face Uncertainty? Do not fall for flaw of averages
## Summary
- as explained by de Neufville in MIT Decision Analysis ans Risk Management course
### what is it?
- a fundamental problem in the design and evaluation of projects
- The patern of designing, evaluating projects based on the average, "most likely" future forecast
- Derives from misunderstanding of probability and systems behavior
### The name
- A pun by Sam Savage(See the book "Flaw of Averages, 2009")
- A mistake -> Flaw
- The concept of the "Law of averages that things balance out on averages

### What is the Flaw?
The error consist of assuming analyses based on "average" or "most likely" conditions give correct answer

### Mathematics of Flaw:
- $E[f(x)] \neq f(E(X))$
- See also Jensen Inequality
- where $E(x)$ is expected value of $x$

### Flaw of averages in words
- Average of all possible outcomes associated with uncertain parameters, generally does not equall  
the value obtained from using the average value of the parameters

## What Do You Do When You Face Uncertainty? Use expected value of your deterministic objective
- In version 2 of NCCA Tshirt problem, instead of profit, we considered expected profit as our   
ojective, and we find the order that maximizes this objective profit
- The expected monetary value, or EMV, for any decision is a weighted average of the possible  
payoffs/costs for this decision, weighted by the probabilities of the outcomes. Using the EMV  
criterion, you choose the decision with the largest EMV. This is sometimes called “playing the averages.”
- If your objective is utility, use expected utility! more generally use "expected value of  
objective

## Are you ok with using Expected manoetary average as your objective?
- consider version 2 of NCCA Tshirt problem
### The prolem is beyond risk
#### Your real objective is utility, not money
- Even if you are risk neutral with respect to utility, just because of  
"law of diminishing rate of return" or convexity(non-linearity) of utility with respect to money  
(profit in NCCA Tshirt problem), you will still suffer from flaw of averages if you treat EMV is  
your ultimate objective, while your real objective is utility
- we are using money(profit) to represent our real objective which is actually utility. What really  
causes the problem is that utility has non-linear relation with money(more specifically convex)
- We should always be aware of convexity of utility(and many other objectives) with respect to  
different values. This is related to law of diminishing rate of retruns
- If you are thinking, for businesses, we don't have this problem, think again! 
#### Your real objective is not single period-short term
- We are using static profit, a single period short-term profit
- What is our real objective?
- It is profit and value of our business not just this period, but for long run
- Again, the real problem is: Relation between long-term profit(our real objective) and short term profit(objective that we used) is non-linear and complex...so we are fooled y flaw of averages again....
### Expected value is only for your final ultimate real objective



## What Do You Do When You Face Uncertainty? Think in terms of random variables and distribution
- This is the right approach
- Consider NCCA Tshirt problem, we need to answer following questions:
- How likely is that:
    - Demand is lower than 1000
    - Demand is lower than 500
    - Demand is higher than 2000
    - Profit is lower that 0
    - Profit is lower than 5000
    - Profit is higher than 10000
- To make optimal decisions, and answer all the questions that we have, we need proability distribution
of any variable of interest

## Embrace the uncertainty

## What Do You Do When You Face Uncertainty? Create a magical expriment generator device
- yes simulation is the cheat code to exprience, and is more easier than ever thaks to probability  
and computer!




