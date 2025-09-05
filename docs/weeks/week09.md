# Prepare for Week 9
## Main Concepts of Data Operations in Relational Database

### Slide 1 — Data as Rows and Columns

- **Table as universal structure**:
    
    - **Rows** = individuals, data units, or samples.
        
    - **Columns** = attributes, variables, or measurements.
        
- **Rows** represent individual **records** or **observations**. Think of a row as a single "case  
"such as a customer, a product, or a specific transaction. Every row is a distinct entity
    
- **Columns** represent different **attributes** or **fields** for each record. For example,  
in a table of customers, you might have columns for `Customer_ID`, `Age`, `City`, and  
 `Total_Purchases` 
 
 **Idea** It is useful to think as Each column as a vector, which shows one variable across many  
 observations.
    

💡 _Think “rows = cases, columns = features.”_

---

### Slide 2: Understanding Data and Variable Types

Data is not just numbers; it comes in various types, and each type dictates what operations you can perform.

- **Numerical:**
    
    - **Discrete:** Whole numbers (e.g., number of items purchased).
        
    - **Continuous:** Any number within a range (e.g., temperature, height).

💡 Not all numeric variables should be treated as mathematical numbers in mathematical operations

- **Text (String):**
    
    - Unstructured text (e.g., a product description).
        
- **Boolean:**
    
    - Values are either `TRUE` or `FALSE` (e.g., `is_customer`).
        
    - In calculations, `TRUE` is often treated as `1` and `FALSE` as `0`, allowing for powerful filtering and counting.
        
- **Categorical:**
    
    - Values are a fixed set of categories (e.g., 'Male'/'Female', 'North'/'South'/'East'/'West').
        
    - Can be represented as text or numbers (e.g., `0` for 'Male', `1` for 'Female'), but the numbers have no mathematical meaning themselves.
        
- **Date Time**

Understanding these types is crucial for preparing data for analysis and choosing the right functions.

---

    

💡 _Knowing the type matters: it defines what(and how) operations make sense._

---

### Slide 3: The Two Pillars of Data Manipulation

Data manipulation primarily involves two core types of operations:

1. **Querying (Filtering) Data:** This operation selects a subset of **rows** (individuals, samples) from a table based on conditions applied to one or more **columns** (attributes).
    
    - **Concept:** You're not changing the data itself, but rather isolating the records of interest.
        
    - **Example:** `SELECT * FROM Sales WHERE Region = 'North' AND Total_Sales > 1000`. This returns all columns for a select group of rows that meet the criteria.
        
2. **Transforming Data:** This operation applies a function to one or more columns to create a new output. The output can be of the same shape as the input or a different shape.

💡 Transformation = new variable from old ones

💡 Transformations and queries are done using functions and operations    

💡 Operations could be seen as functions too

---

### Slide 4: A Data Manipulation Overview in SQL

**SQL** (Structured Query Language) is the standard language for managing and querying relational databases. It brings together all the concepts we've discussed into a single, powerful syntax.

### Key SQL Operations:

- **`SELECT`**: The command for **querying**. You specify which columns you want to retrieve.
    
- **`FROM`**: Indicates the table you are querying.
    
- **`WHERE`**: Filters the rows based on logical conditions. This is the **filtering** or **querying** step.
    
- **`GROUP BY`**: A command used for **aggregation**. It groups rows that have the same values in specified columns (e.g., `GROUP BY Region`).
    
- **`ORDER BY`**: Sorts the results.
    

This structured approach allows us to think abstractly about the operations we perform in tools like Excel, Power BI, or Python, understanding that they are all built on these same fundamental principles.

---




### Slide 5: The Function as a Transformation: Input → Output

Every operation we perform on data, from a simple calculation to a complex model, can be thought of  
as a **function** with a defined input and a defined output.

### Key Idea:

Understanding the **type** and **dimension** of the input and output is critical for thinking about  
data operations abstractly.

- **Scalar:** A single value (e.g., the number 5, the word 'apple').
    
- **Vector (Array):** A one-dimensional list of values of **single variable** (e.g., a single  
column of data).
    - the condition of **single variable** is not strictly necessary, it is just for better  
    conceptual understanding
    
- **Table (Matrix):** A two-dimensional collection of rows and columns (e.g., an entire dataset).
    
- **Arrays or tensors with higher dimensions:**  n-dimensional array of data 


This framework helps you anticipate what a function will do and how its output will interact with  
other data.

---

### Slide 6 — Functions as Input → Output

Think about **type and shape** of input and output.

1. **Scalar → Scalar**
    
    - `f(x) = x^2`, `log(x)`.
        
    - Apply to single numbers.
        
2. **Multi-scalar → Scalar**
    
    - `f(x,y) = x+y`, `max(x,y)`,  `profit(order, demand)`
        
3. **Vector → Vector (same shape)**
    
    - Apply elementwise: `7*A1:A8`, `log(Salary)` , `Age+5` where `Salary` and `Age` are columns
        
4. **Vector → Scalar (aggregate)**
    
    - `SUM(A1:A8)`, `mean(Age)`, `sum(Sales)`
    - `SUBTOTAL(1, A1:A8)`
        
5. **Multi-vector → Vector**
    
    - Row-wise computation: `A1:A8*B1:B8`, `Profit = Revenue – Cost`.

- This elementwise computation logic is generalized into multi dimensional arrays and tensors        

💡 _Understanding input/output types clarifies how functions behave on data._

---

### Slide 7 — Main Operations on Data

1. **Query rows**:
    
    - Select individuals with conditions on attributes.
        
    - Examples:
        
        - `Age > 30`
            
        - `Department = "Sales"`
            
    - SQL: `SELECT * FROM Employees WHERE Age > 30;`
        
2. **Transform columns (vectors)**:
    
    - Apply functions to variables.
        
    - Examples: scaling salaries, taking logarithms, computing new ratios.
        
3. **Aggregate**:
    
    - Collapse many values into a summary (scalar).
        
    - Examples: `SUM(Salary)`, `AVG(Age)`, `COUNT(Department)`.
        

---

### Slide 8: Querying and Filtering Data

One of the most fundamental operations is **querying**, which involves selecting a subset of data based on specific conditions. This is how you narrow down your focus to the records that matter.

#### The Power of Logical Conditions

- You define conditions using logical operators: `WHERE`, `AND`, `OR`, `NOT`.
    
- These conditions evaluate to `TRUE` or `FALSE` for each row.
    
- The query then **filters** the table, keeping only the rows where the condition is `TRUE`.
    

**Example:** `SELECT * FROM Orders WHERE Region = 'North' AND Total_Sales > 1000`. This query returns only the rows for orders in the 'North' region with sales greater than $1,000.

---


### Slide 9 — Querying examples

- Filtering is based on **Boolean conditions**.
    
- Example dataset:
    

|Name|Age|Salary|Dept|
|---|---|---|---|
|Ali|25|4000|Sales|
|Sara|38|6500|HR|
|Reza|42|7200|Sales|

- Query: `Age > 30 AND Dept = 'Sales'`.
    
- Result: only rows that satisfy both conditions.
    

Excel: filters, IF functions.  
SQL: `WHERE` clause.  
Pandas: `df[df.Age > 30 & (df.Dept=="Sales")]`.

---


### Slide 10 — Transforming Columns

- Apply a function to a **whole column (vector)**:
    

Examples:

- `Salary * 1.1` (raise by 10%).
    
- `log(Sales)`.
    
- `HoursWorked / Sales` (new variable).
    

Excel: formula drag.  
SQL: `SELECT Salary*1.1 AS NewSalary`.  
Pandas: `df["Salary"] * 1.1`.

💡 _Transformation = new variable from old ones._

---
### Slide 11: Aggregation: Summarizing Data

**Aggregation** is the process of applying a function to a group of values to produce a **single summary value**. This is how we get a high-level view of our data.

- **Common Aggregation Functions:**
    
    - **`SUM`**: Adds up all values.
        
    - **`AVERAGE` (`AVG`)**: Calculates the mean.
        
    - **`COUNT`**: Tallies the number of records.
        
    - **`MAX`** and **`MIN`**: Finds the highest and lowest values.
        

These operations are often performed on groups of data, for example, finding the average sales for each region or the total number of customers for each product category.

---

### Slide 12 — Aggregate Operations examples

- Collapse a vector into a **single summary scalar**:
    
    - `SUM`, `AVG`, `COUNT`, `MIN`, `MAX`, `MEDIAN`, `MODE`.
        
- SQL:
    
    ```sql
    SELECT AVG(Salary) FROM Employees;
    ```
    
- Excel: `=AVERAGE(SalaryRange)`.
    
- Pandas: `df["Salary"].mean()`.
    

💡 _Aggregation reduces dimensionality: many values → one._

---


### Slide 13: The Logic of `TRUE` and `FALSE`

Logical operations are at the heart of filtering and conditioning. In many programming languages and data systems, `TRUE` and `FALSE` have a numerical representation.

#### Numerical Representation

- **`TRUE`** is represented by the number **1**.
    
- **`FALSE`** is represented by the number **0**.
    

#### Practical Implications

- This allows you to perform mathematical operations on logical results. For example, `SUM(C2:C100)` on a column of `TRUE`/`FALSE` values would count the number of `TRUE`s.
    
- Conversely, in some systems, `0` is treated as `FALSE`, and **any other number** (positive or negative) is treated as `TRUE`.
    

Be careful! While you can `SUM` logical values, functions like `SUMPRODUCT` in Excel may not work as expected on `TRUE` and `FALSE` directly and often require a conversion, such as `(--)` or `N()`, to convert them into `1`s and `0`s. This highlights the importance of understanding how different tools handle data types.

---

### Slide 14: Excel's Secret to Vectorized Thinking

Excel's user interface, while seeming simple, is a masterclass in performing **vectorized operations** without the jargon.

- **The Drag-and-Fill Handle:** When you write a formula in a single cell (e.g., `=A2*B2`) and drag the fill handle down, you are essentially telling Excel to apply that same operation to every subsequent row.
    
- **Vectorized Computation:** Excel isn't just copying the formula; it's efficiently applying the logic to the entire range of cells, effectively operating on the `A` and `B` columns as vectors to produce a new `C` column vector.
    

This intuitive process prepares your mind for the vectorized thinking that is fundamental to languages like Python (with libraries like Pandas and NumPy) and R.

---

### Slide 15: The Evolution of Excel's Computation Engine

Excel's "drag-and-fill" method, while intuitive, was a row-by-row, cell-based approach. The new **dynamic array engine** represents a paradigm shift to truly vectorized computation.

* **The Old Way:** In the past, you'd write a formula in one cell and drag it down a column. Excel would then copy that formula, essentially treating each cell as a separate calculation. This was inefficient for large datasets.
* **The New Way (Dynamic Arrays):** With dynamic arrays, a single formula entered in one cell can **spill** its results into multiple adjacent cells. This means you are writing a single vectorized formula that operates on an entire range of data at once.

This is a fundamental change from a scalar-oriented mindset (one cell, one value) to a **vector-oriented** mindset (one formula, multiple values). This makes complex calculations simpler, more readable, and significantly more efficient.

### New Functions and Formulas

The dynamic array engine introduces new functions designed for this vectorized approach:

* **`FILTER`**: Returns a filtered range of data based on criteria you define. Instead of a complex `INDEX`/`MATCH` formula, you can write `FILTER(data_range, criteria_range)`.
* **`SORT`**: Sorts a range of data based on a specified column. It's much simpler than the old method of sorting a range.
* **`UNIQUE`**: Returns a list of unique values from a range. This saves you from having to use `PivotTables` or manual data cleaning.
* **`XLOOKUP`**: A more powerful and flexible replacement for `VLOOKUP` and `HLOOKUP`.

These functions operate on entire arrays, making your spreadsheets more robust and easier to manage, truly preparing you for vectorized thinking in more advanced data analysis tools.


I can create a new set of slides that explains how `GROUP BY` is handled in both Excel and Pandas, and connects the concepts to the core `split-apply-combine` methodology.

***

## Slide 16: Grouping Data: Summarizing by Category

Often, you don't want to analyze every individual record. Instead, you want to get a high-level view by summarizing data based on a category. This operation is known as **grouping**. 

### The Core Idea

The goal is to take a detailed table and condense it into a new, smaller table that shows an aggregated value for each unique group. This is the essence of data reporting and analysis.

* **Example:** How many orders did each customer place? What was the total revenue for each product category?

Both Excel and more advanced data tools like Pandas have powerful ways to perform this operation.

***

## Slide 17: The Excel `GROUP BY` - The Power of the PivotTable

In Excel, the most famous tool for grouping data is the **PivotTable**. It provides a user-friendly, drag-and-drop interface for what is, under the hood, a complex data operation.

1.  **Split**: You drag a field (like `Region`) into the "Rows" or "Columns" area. Excel automatically identifies every unique value and creates a new row or column for each one. This is the **splitting** step.
2.  **Apply (Aggregate)**: You then drag a numerical field (like `Sales`) into the "Values" area. Excel applies an aggregate function to each group. By default, it's `SUM`, but you can change it to `COUNT`, `AVERAGE`, `MAX`, or `MIN`.
3.  **Combine**: The PivotTable then presents the final, summarized table, which is the result of applying the aggregate function to each group.

This simple workflow performs the full `split-apply-combine` process that is central to data analysis. 

***

## Slide 18: The Pandas `GROUP BY` - `split-apply-combine`

In the Python world, the **Pandas** library provides a more explicit and powerful way to perform grouping, formalized by the **`split-apply-combine`** methodology.

1.  **Split**: The `df.groupby('column_name')` method is the **splitting** step. It creates a special object that logically separates the `DataFrame` into sub-groups without creating copies.
    * Example: `df.groupby('Region')`
2.  **Apply**: You then chain an aggregate function to this object. This is the **applying** step, where the function is executed on each of the groups.
    * Example: `.sum()`, `.mean()`, `.count()`, or even a custom function.
3.  **Combine**: Pandas takes the results from each group and **combines** them back into a new `DataFrame` or `Series`. The final output is a clean, summarized table.

This explicit syntax makes it easy to read and understand exactly what is happening to your data, which is essential for reproducibility and automation. 

***

## Slide 19: Why Grouping is a Fundamental Concept

Understanding grouping is a major step toward thinking abstractly about data. It's the operation that lets you move from looking at individual records to identifying trends and patterns across your dataset.

* **Business Intelligence**: Grouping is the basis for all dashboards and reports, allowing you to quickly see total sales by month, customer counts by city, or average order value by product type.
* **Data Cleaning**: You can use `GROUP BY` to quickly check for duplicates or find unique values, which is a critical part of data preparation.
* **Data Science**: In machine learning, grouping is used for feature engineering, where you create new variables by aggregating data. For example, you might create a `total_purchases` variable for each customer from a transaction log.

By mastering this concept, you are no longer just looking at a spreadsheet; you are thinking about data at a higher, more strategic level.



Yes, you are absolutely right. Decision trees are fundamentally about finding the "best" way to group data for prediction. They do this by recursively partitioning the dataset into smaller, more homogeneous subsets based on the values of the input features.

Here are some slides that expand on this concept.

---

## Slide 20: Decision Trees and the Art of Grouping for Prediction

A **decision tree** is a predictive model that uses a series of simple, logical rules to predict an outcome. It works by repeatedly splitting the data into groups that are as **pure** as possible with respect to the target variable.

* **The Core Idea:** Imagine you want to predict if a customer will buy a product. A decision tree might first split customers into two groups: those with an income over $50,000 and those with an income below. It then repeats this process on each of those new groups, perhaps splitting again based on age.
* **Recursive Partitioning:** The tree continues this process of **recursive partitioning** until it reaches a point where each final group (a "leaf") contains records that are very similar to each other in terms of the outcome.

This method of repeatedly finding the best way to group the data is how a decision tree learns to make predictions. 

---

## Slide 21: The Logic of Splitting: How Trees Find the "Best" Groups

The "best" split is the one that results in the most **homogeneous** or "pure" child nodes. But how does the tree measure purity?

* **Purity Metrics:** Decision trees use mathematical functions to evaluate the quality of a split. Common metrics include:
    * **Gini Impurity**: Measures how often a randomly chosen element from the set would be incorrectly labeled if it were randomly labeled according to the distribution of labels in the subset. A Gini score of 0 means perfect purity (all elements belong to the same class).
    * **Entropy**: A concept from information theory that measures the disorder or randomness in a set of data. A split that reduces entropy the most is considered the best.
* **The Goal:** At each step, the algorithm evaluates every possible split on every feature and chooses the one that maximizes the reduction in impurity. It’s like finding the single question that gives you the most information about the outcome.

The result is a set of rules (the tree's path) that lead you from the initial data to a final prediction by narrowing down the data into highly pure groups.

---

## Slide 22: From Groups to Predictions

Once the decision tree is built, making a prediction for a new, unseen data point is a straightforward process of following the rules.

* **Classification:** For a **classification** task (predicting a category, like `yes/no` or `buy/don't buy`), you simply drop the new data point down the tree. At each node, you check the condition and follow the appropriate branch. When you reach a **leaf node**, the prediction is the most common class in that final group.
* **Regression:** For a **regression** task (predicting a numerical value, like price or sales), the process is the same. The prediction at the leaf node is typically the **average** of all the values in that final group.

This intuitive process makes decision trees easy to understand and interpret, as the "decision-making" process is transparent and based on simple groupings of your data.