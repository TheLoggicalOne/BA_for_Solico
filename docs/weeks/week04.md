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


## 🧩 Part 1 – What Do You Do When You Face Uncertainty?
### Do not fall for flaw of averages
- see [Flaw of Averages](concepts/flaw_of_averages.md)