# Prepare for Week 3


## Problems
#### Revisit example EXAMPLE  1.1 ORDERING NCAA T-SHIRTS of the book(page 9)
- This is the example that we worked in week 2 class, it is from the book, but we are generalizing it(as we did in class)
- Here is the question if you forgot:
??? note 
    It is March, and the annual NCAA Basketball Tournament is down to the final four teams. Randy  
    Kitchell is a T-shirt vendor who plans to order T-shirts with the names of the final four teams  
    from a manufacturer and then sell them to the fans.The fixed cost of any order is $750, the  
    variable cost per T-shirt to Randy is $8, and Randy’s selling price is $18. However, this price  
    will be charged only until a week after the tournament. After that time, Randy figures that  
    interest in the T-shirts will be low, so he plans to sell all remaining T-shirts, if any, at $6  
    each.His best guess is that demand for the T-shirts during the full-price period will be 1500.He  
    is thinking about ordering 1450 T-shirts, but he wants to build a spreadsheet model that will  
    let him experiment with the uncertain demand and his order quantity. How should he proceed?

- we will consider three different version of this problem, in each of following versions explain:
    - what are inputs? 
    - what are decision variables?
    - what is our exact objective? 
- You will need to use Excel, or Google Sheet, or LibreOffice or Python or...

#### Deterministic Version

- In first version, we are sure about future demand! we know for a fact that future demand  
will be 15000
- using a excel file that relates all variables together(this is spreadsheet model or mathematical  
model!) change value of different inputs and decision variable and see how objective changess
- find optimal choice for decision variable(the value for order that maximizes objective)
- How does changing fixed cost affect our choice?
    - How about sell price?
    - How about variable cost?
    - How about discount price?
- Do you think relation between profit and variable cost is linear?
    - what about profit and fixed cost?
    - what about profit and order?
    - what about profit and demand?

#### Three way fair dice Version
- In this version, we know for a fact that Demand will have only three possiblity, all of them  
equally likely

|Scenario|Demand|Probability|
|---|---|---|
|Low Interest |1,000|33.33%|
|Medium Interest |1,500|33.33%|
|High Interest|2,000|33.33%|

- The data analyst, says that when we face a random variable, our best guess is its average value  
so we should assume demand is 1500, and we know when demand is 1500, best order is 1500

- some one else suggest that best order is 1800
- How can you decide ( in a logical and pricncipled way) which choice is better? 1500 or 1800?
- What is our objective in this problem? Can you express all of our criteria and preferences in a  
single objective function?
- One crazy guy says that the best choice is to order 2000, can you convince him that he is wrong?


#### Three way unfair diceVersion
- In this version, we know for a fact that Demand will have only three possiblity, with following  
probailities

|Scenario|Demand|Probability|
|---|---|---|
|Low Interest |1,000|40%|
|Medium Interest |1,500|35%|
|High Interest|2,000|25%|

#### Unifrom Random Version
- In this version, we know (for a fact!) that demand is a number between 500 to 2500, and it could  
be any of these numbers, all with same chance
- again, The data analyst, says that when we face a random variable, our best guess is its average  
value so we should assume demand is 1500, and then find optimal order for this demand
    - is he right?
- what is the best choice for order?
- If we decrease the value of sell price , how does it affect optimal choice for order?
- for what value of sell price, our data analyst 


#### In reality,Future demand is uncertain, what is the best thing we could hope to know about demand?

#### What if we have data?
- in this version, we don't know anything magical about demand, the only thing that we know is  
history of our previus three years demand at the same event:


|Year|Demand|
|---|---|
|2024 |1400|
|2023 |2000|
|2022 |1600|
|2021 |1700|


#### PROJECTING THE COSTS OF BOOKSHELVES AT WOODWORKS  
- This is Example 1.2 from the book, its excel file name is `Bookshelf Costs Finished.xlsx` in  
chapter2 folder
- The Woodworks Company produces a variety of custom-designed wood furniture for its  
customers. One favorite item is a bookshelf, made from either cherry or oak. The company knows tha  
wood prices and labor costs are likely to increase in the future. Table 1.1 shows the number o  
board-feet and labor hours required for a bookshelf, the current costs per board-foot and labor  
hour, and the anticipated annual increases in these costs. (The top row indicates that either type  
of bookshelf requires 30 board-feet of wood and 16 hours of labor.) Build a spreadsheet model that  
enables the company to experiment with the growth rates in wood and labor costs so that a manage  
can see, both numerically and graphically, how the costs of the bookshelves increase in the next  
few years. 
 
 |resource |Cherry| Oak| Labor|
 |---|---|---|---|
 |Required per bookshelf| 30| 30| 16|
   Current unit cost| $5.0| $4.30| $18.50| 
  |Anticipated annual cost increase|  2.4%| 1.7%| 1.5%


- What is the relation between total cost(projected cost) and year? How does increasing year affect total cost?

