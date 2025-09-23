# Prepare for Week 12
## Problems
### Problem 1: Coninue problem that we were working in Week 11 Class:
- We have coin, which is built to be fair, but, Because of its production process, we know it could  
be have some small bias
- Our phisycist, who is expert on production process of coin, belives the coin has at most 4 percent  
bias(could be in favor or agains head) and true chance of head is in $ [0.46, 0.54] $ uniformly
- What is Prior distribution of $ p $, probability of head?
    - Be carefull, It is really easy to get confused, we are talking about distribution of parameter  
    of distribution!
- We do some expriment(or gather some data, or use our existing data): In 10 flips, we have 8  
success(head)
- What can we say about true parameter(chance of success) of this coin? 
    - Before seeing data, our beleif was: true parameter of this coin could be:
     any of $ 46, 47, 48, 49, 50, 51, 52, 53, 54 $ all equally likely

- Do you still beleive 46 and 54 are equally likely?
#### Evaluating Single possiblity of Reality(true chance of success)
- How liklely is 46?
    - what is answer of this question in terms of conditional probabilities?
- If our coin was really of type 46(true chance of success was 46), How likely would it be to  
generate 8 success out of 10 flips?
    - This is "Likelihood": Chance of generation of current data, in a world(hypothetical) that  
    reality is 46
    - what is answer of this question in terms of conditional probabilities?

- answer above questions for 54

#### Comparing to candidate reality
- How likely is that our coin type was 46? how likely is that our coin type was 54?
- How much more likely is 54 than 46?

#### Comparing all possible candidates for reality
- For any possible value of $ p $(true chance of head, which we do not know):
    - Assuming the true chance of success is $ p $ , How likely would it be to  
        generate 8 success out of 10 flips?
    - This is called likelihood: 
- How liklely is $ p $?

#### More Observation
- We gather 10 more sample(results of flips) which 5 of them are head
- What is distribution of $p$ after seeing these new samples?

#### what can you say about next coin flip?


### Problem 2: Revisit Joe Medical test, page 262 and 263 of the book(section 6.6)
#### Original Problem( to review):
- During a routine physical exam, a middle-aged man named Joe tests positive for a certain disease.  
There were previously no indications that Joe had this disease, but the positive test sends him into  
a panic. He “knows” now that he has the disease. Or does he?
- Suppose that only 1% of all undiagnosed middle-aged men have this disease
- Also, suppose the test Joe took is not entirely accurate. 
    - For middle-aged men who don’t have the disease, there is a 10% chance they will test positive  
    (the false positive rate). 
    - For middle-aged men who have the disease, there is a 5% chance they will test negative  
    (the false negative rate).

- So with a positive test result, what is the probability that Joe has the disease?

#### What to do after the test
- If Joe retakes the physical exam and his result is positive again, what is the probability that  
Joe  
has the disease?

#### Taking another test? 
- There is another test, with totaly different method, for this disease
- Joe is considering taking this test too
- Accuracy of this test: 
    - False positive rate for this test is $ 5\% $ 
    - False Negative rate for this test is $ 8 \% $

- If Joe  takes the new test and his result is positive again, what is the probability that  
Joe has the disease?
- If Joe  takes the new test and his result is negative , what is the probability that  
Joe has the disease?

### Solve [Problem 2 of week 6](weeks/week06/#prolem-2-estimate-chance-of-success-of-bernouli-random-variable-from-data)