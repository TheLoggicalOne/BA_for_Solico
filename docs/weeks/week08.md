# Prepare for Week 8
## Beyond the Numbers: Probabilistic Reasoning for Business Analytics
- Understanding P-values, Conditional Probability, and Why Common Sense is Your Best Tool

## Our Approach so far
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

#### In other words:


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
        - $15100 - 15000 = 8100 - 8000 = 1100 - 1000$
        - $2 * 10000 = 20000$
        - in a way that  
    - Suffer from flaw of averages if, your real objective is non-linear function of this objective
    - It is not enough to have a objective function that is rank-consistent with your preferences

## To Reality:
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
- We can observe examples of (inputs, outputs) and we want to discover the system itself, or at least  parts of it
- From our domain knowledge an studiyng the system itself, we might e able to make some reasonable  
assumption:
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
- If we observe, each dollar increase in marketing, results in $1.5$ dollar increase in sale...
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

## From Reductio ad absurdum to Reductio ad unlikely
- How can we prove a theory?
- When we increase our beleife in a theory?
- If our observation are consistent with the theory?
- If negation of theory results in 

To confirm a theory, is it enough that our observation is consistent with that theory?
### Reductio ad absurdum
1. Suppose the hypothesis H is true. 
2. It follows from H that a certain fact F cannot be  the case. 
3. But F is the case.  
4. Therefore, H is false.


### Reductio ad unlikely

1. Suppose the null hypothesis H is true.  
2. It follows from H that a certain outcome O is  very improbable (say, less than Fisher’s 0.05  threshold).
3. But O was actually observed.  
4. Therefore, H is very improbable.
