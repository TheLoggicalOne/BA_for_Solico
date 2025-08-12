# Prepare for Week 6
## Problems
### Problem 1: What do you think about [Flaw of Averages](../concepts/flaw_of_averages.md)? What is wrong with it?
- Find examples of Flaw of Averages,in personal and business decision making
### Prolem 2: Estimate chance of success of Bernouli random variable from data
- $ X $ is a Bernouli random variable with probability of success equal to $ p $, p is unknown to us.  
in other words, $ P(X=1) = p $
- We know the result of one trial, which was success ( $ X=1 $)
- What can we say about $p$? How can we predict result of future trials of $X$?
- What if we know the result of more than one trials?
- Solve problem 6 of [week 5](week05.md)

### Problem 3: Estimating production volume from single data
- Your competitor has started to produce a very special product. You want to know how many they have  
produced so far.
- Fortunately for you, they have numbered their productions: 1, 2, 3, ...You buy one, which  
is numbered 120
    - What can you say about their production volume?   
- You buy some more product, their numbers are: 33, 170, 220, 160...
    - What can you say about their production volume?  

- Solve problem 5 of [week 5](week05.md)

### Problem 4: Conider NCAA T-shirt problem, Should we do some research and survey?
- Consider the version where we know nothing about demand, is it a good idea to do some research?  
- How much should we spend on them?

### Problem 5: you are playing a simple dice game:
- You throw a dice, if the result is $ x $, you will win $ x $ dollar. How much are you willing to pay  
for each round of this game? What is the maximum value? You could play as many rounds as you want

- What if the dice is not fair, let say has following chances
    - $ P(D\le 1) = 0.025 $
    - $ P(D\le 2) = 0.1 $
    - $ P(D\le 3) = 0.25$
    - $ P(D\le 4) = 0.475 $
    - $ P(D\le 5) = 0.725 $
    - $ P(D\le 6) = 1$
### Problem 6: Consider problem 5 of [week 5](week05.md), how valuable is information or data here?
- How much are you willing to pay, to know the value of $ m $
- How much are you willing to pay for each single sample of data?

### Problem 7: Quality control: How many of them will be defective?
- You are a quality manager in a chocolate factory producing 10,000 chocolate bars per day.
- Each bar has a probability $ p $ of being defective (air bubble, wrong weight, broken).

- Defective or not → This is a Bernoulli trial (success = defective, failure = good).
- The number of defectives in a batch follows a Binomial distribution:

- $ X \sim \mathrm{Binomial}(n,p) $
- where: 
- $ n  = \text{number of inspected items}$
- $ p = \text{probability of defect} $
#### Probability perspective (known p, predict outcome)

- Suppose $ p = 0.06 $ (6% defect rate)

    
- If we have  $ n = 100 $ inspected bars.
    
    - What’s the probability of **exactly** 6 defectives?
        
    - What’s the probability of **at most** 6 defectives?
        
    - What’s the most likely number of defectives?

    - What’s the probability of **at most** 12 defectives?


- We have a speciall customer that needs 100 good chocolate , how many choclate should we send her?
    - If we want to be sure that there is 90 percent chance that she will have at least 100 good choclate? what about 90 percent? what about 99%?


#### Statistics perspective (unknown p, estimate from sample)
- We don't the what percent of choclates are defective
- Is the percentage of defective choclate same as chance of being defective?
- How can we find these values? what can we say about them?
- Let say we can take samples from choclates, and inspect the
- To start, we inspect some choclates to find the first defective one
- After checking 78 choclates, the 79'th is defective
    - What can we say about chance of bieng defective
- Let say we inspect more choclates, 500 of them in total and find out that $ x $ numbers of them  
are defective, what can we say about $ p $

### Problem 8: Work on Example 5.9 from the book: IS THIS MUTUAL FUND REALLY A WINNER?
- An investment broker at the Michaels & Dodson Company claims that he has found a real winner. He has tracked a mutual fund that has beaten a standard market index in 37 of the past 52 weeks. Could this be due to chance, or has he really found a winner?
- Objective  To determine the probability of a mutual fund outperforming a standard market index at least 37 out of 52 weeks

### Problem 9: Work on Example 5.11 from the book: OVERBOOKING BY AIRLINES
- This example presents a simplified version of calculations used by airlines when they overbook flights. They realize that a certain percentage of ticketed passengers will cancel at the last minute. Therefore, to avoid empty seats, they sell more tickets than there are seats, hoping that just about the right number of passengers show up.
- We assume that the no-show rate is 10%. In binomial terms, we assume that each ticketed passenger, independently of the others, shows up with probability 0.90 and cancels with probability 0.10.

- For a flight with 200 seats, the airline wants to see how sensitive various probabilities are to the number of tickets it issues. In particular, it wants to calculate 
    - (a) the probability that more than 205 passengers show up
    - (b) the probability that more than 200 passengers show up
    - (c) the probability that at least 195 seats are filled, and 
    - (d) the probability that at least 190 seats are filled. 

- The first two of these are “bad” events from the airline’s perspective; they mean that some customers will be bumped from the flight. The last two events are “good” in the sense that the airline wants most of the seats to be occupied.                                       