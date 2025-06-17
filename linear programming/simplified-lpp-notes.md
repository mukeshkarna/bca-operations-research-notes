# LINEAR PROGRAMMING: SIMPLIFIED NOTES

## What is Linear Programming?

Linear Programming (LP) is a method for finding the best outcome in a mathematical model with a linear objective function and linear constraints. In simple terms, it helps us make the best decisions when we have limited resources.

**Real-World Relevance:** Think of LP as a tool to answer questions like:
- How should a factory allocate its machines to maximize profit?
- What's the best diet to meet nutritional needs at minimum cost?
- How should an investor distribute money across different investments?

## The Basic Structure of Linear Programming Problems

### 1. Decision Variables
These are the quantities we need to determine. They represent our decisions.

**Example:** In a production problem, x₁ might be "how many Product A to make" and x₂ might be "how many Product B to make."

### 2. Objective Function
What we want to maximize (like profit) or minimize (like cost).

**Example:** Maximize Profit = $10x₁ + $15x₂

### 3. Constraints
Limitations on our resources or other requirements.

**Example:** 
- Labor hours: 2x₁ + 3x₂ ≤ 100 hours available
- Material: 1x₁ + 2x₂ ≤ 50 kg available

### 4. Non-negativity
Usually, we can't produce negative quantities of products.

**Example:** x₁ ≥ 0, x₂ ≥ 0

## Real-World Example 1: The Bakery Problem

**Scenario:** A bakery makes cakes and cookies. Each cake requires 2 hours of baking time and 4 cups of flour. Each cookie requires 0.1 hours of baking time and 0.2 cups of flour. The bakery has 20 hours of baking time and 40 cups of flour available daily. The profit is $30 per cake and $2 per cookie.

**Question:** How many of each should be made to maximize profit?

### Step 1: Define Variables
- Let x₁ = number of cakes to bake
- Let x₂ = number of cookies to bake

### Step 2: Write the Objective Function
- Maximize Profit = 30x₁ + 2x₂

### Step 3: Identify Constraints
- Baking time: 2x₁ + 0.1x₂ ≤ 20 hours
- Flour: 4x₁ + 0.2x₂ ≤ 40 cups
- Non-negativity: x₁, x₂ ≥ 0

### Step 4: Solve Graphically

To solve graphically, we:
1. Plot all constraints
2. Find the feasible region (the area where all constraints are satisfied)
3. Find the corner points
4. Calculate the objective function value at each corner point
5. Choose the highest value (for maximization)

Let's solve this step by step:

**Baking constraint:** 2x₁ + 0.1x₂ = 20
- If x₁ = 0: x₂ = 200
- If x₂ = 0: x₁ = 10

**Flour constraint:** 4x₁ + 0.2x₂ = 40
- If x₁ = 0: x₂ = 200
- If x₂ = 0: x₁ = 10

The corner points are:
- (0, 0) - Origin
- (0, 200) - Intersection of x₁ = 0 and both constraints (they intersect at the same point)
- (10, 0) - Intersection of x₂ = 0 and both constraints (they intersect at the same point)

Calculate profit at each point:
- Profit at (0, 0) = 30(0) + 2(0) = $0
- Profit at (0, 200) = 30(0) + 2(200) = $400
- Profit at (10, 0) = 30(10) + 2(0) = $300

Therefore, the optimal solution is to make 0 cakes and 200 cookies for a maximum profit of $400.

**Reality Check:** This solution suggests making only cookies and no cakes. This makes sense because cookies are more profitable per unit of resources used. However, in real business, other factors like product diversity and customer demand might need to be considered.

## Real-World Example 2: The Investment Portfolio

**Scenario:** An investor has $50,000 to invest in stocks and bonds. Stocks have an expected return of 10% but are risky. Bonds have an expected return of 6% and are safer. To manage risk, the investor wants at least 30% of the money in bonds. Also, the amount in stocks shouldn't exceed twice the amount in bonds.

**Question:** How should the money be invested to maximize return?

### Step 1: Define Variables
- Let x₁ = amount invested in stocks ($)
- Let x₂ = amount invested in bonds ($)

### Step 2: Write the Objective Function
- Maximize Return = 0.10x₁ + 0.06x₂

### Step 3: Identify Constraints
- Total investment: x₁ + x₂ ≤ 50,000
- Minimum bond requirement: x₂ ≥ 0.3(x₁ + x₂)
- Stock limitation: x₁ ≤ 2x₂
- Non-negativity: x₁, x₂ ≥ 0

### Step 4: Simplify Constraints
- The bond requirement: x₂ ≥ 0.3(x₁ + x₂)
  - x₂ ≥ 0.3x₁ + 0.3x₂
  - 0.7x₂ ≥ 0.3x₁
  - x₂ ≥ (0.3/0.7)x₁ = (3/7)x₁

### Step 5: Solve the Problem

Let's simplify the constraints:
- x₁ + x₂ ≤ 50,000
- x₂ ≥ (3/7)x₁
- x₁ ≤ 2x₂

From x₁ ≤ 2x₂, we get x₁/2 ≤ x₂, or x₂ ≥ x₁/2
Comparing with x₂ ≥ (3/7)x₁:
- x₁/2 > (3/7)x₁ when x₁ > 0
- So the stronger constraint is x₂ ≥ x₁/2

The active constraints are:
- x₁ + x₂ = 50,000 (budget constraint)
- x₂ = x₁/2 (stock limitation)

Solving these:
- x₁ + x₁/2 = 50,000
- (3/2)x₁ = 50,000
- x₁ = 33,333.33

And:
- x₂ = x₁/2 = 16,666.67

Let's verify the bond requirement:
- x₂ = 16,666.67
- 0.3(x₁ + x₂) = 0.3(50,000) = 15,000
- Since 16,666.67 > 15,000, the bond requirement is satisfied.

Therefore, the optimal investment is $33,333.33 in stocks and $16,666.67 in bonds, for a maximum expected return of:
- Return = 0.10(33,333.33) + 0.06(16,666.67) = $3,333.33 + $1,000 = $4,333.33

## Solving Linear Programming Problems: Step-by-Step Guide

### Method 1: Graphical Method (for problems with 2 variables)

**Example: Furniture Manufacturing**

**Scenario:** A furniture maker produces tables and chairs. Each table requires 4 hours of carpentry and 2 hours of finishing. Each chair requires 3 hours of carpentry and 1 hour of finishing. There are 240 hours of carpentry time and 100 hours of finishing time available. The profit is $70 per table and $50 per chair.

**Step 1: Set up the problem**
- Let x₁ = number of tables
- Let x₂ = number of chairs
- Maximize: Z = 70x₁ + 50x₂
- Subject to:
  - 4x₁ + 3x₂ ≤ 240 (carpentry)
  - 2x₁ + x₂ ≤ 100 (finishing)
  - x₁, x₂ ≥ 0

**Step 2: Graph the constraints**

First, we convert the constraints to equations to find their boundaries:
- 4x₁ + 3x₂ = 240
- 2x₁ + x₂ = 100

For 4x₁ + 3x₂ = 240:
- If x₁ = 0: x₂ = 80
- If x₂ = 0: x₁ = 60

For 2x₁ + x₂ = 100:
- If x₁ = 0: x₂ = 100
- If x₂ = 0: x₁ = 50

![Graphical Solution Visualization](https://i.imgur.com/example.png)

**Step 3: Identify the feasible region**

The feasible region is the area bounded by all constraints and the axes.

**Step 4: Find corner points**

The corner points of our feasible region are:
- (0, 0): Origin
- (0, 80): Where carpentry constraint meets the y-axis
- (30, 40): Intersection of both constraints
- (50, 0): Where finishing constraint meets the x-axis

Let's verify the intersection point (30, 40):
- Carpentry: 4(30) + 3(40) = 120 + 120 = 240 ✓
- Finishing: 2(30) + 40 = 60 + 40 = 100 ✓

**Step 5: Evaluate the objective function at each corner point**
- Z(0, 0) = 70(0) + 50(0) = 0
- Z(0, 80) = 70(0) + 50(80) = 4,000
- Z(30, 40) = 70(30) + 50(40) = 2,100 + 2,000 = 4,100
- Z(50, 0) = 70(50) + 50(0) = 3,500

**Step 6: Select the optimal solution**

The maximum Z value is 4,100 at the point (30, 40).
Therefore, the company should produce 30 tables and 40 chairs to maximize profit to $4,100.

### Method 2: Simplex Method (for problems with any number of variables)

The Simplex Method is a systematic way to solve linear programming problems by moving from one "corner point" to another, improving the solution at each step.

Let's solve the furniture example using the Simplex Method:

**Step 1: Convert to standard form**

Add slack variables to convert inequalities to equations:
- 4x₁ + 3x₂ + s₁ = 240 (s₁ = unused carpentry hours)
- 2x₁ + x₂ + s₂ = 100 (s₂ = unused finishing hours)

**Step 2: Set up the initial simplex tableau**

| Basic | x₁ | x₂ | s₁ | s₂ | RHS |
|-------|----|----|----|----|-----|
| s₁    | 4  | 3  | 1  | 0  | 240 |
| s₂    | 2  | 1  | 0  | 1  | 100 |
| Z     | -70| -50| 0  | 0  | 0   |

**Step 3: Select the entering variable**

The most negative coefficient in the objective row is -70, so x₁ will enter the basis.

**Step 4: Select the leaving variable**

The minimum ratio test:
- s₁ row: 240/4 = 60
- s₂ row: 100/2 = 50

The minimum ratio is 50, so s₂ will leave the basis.

**Step 5: Perform the pivot operation**

First, make the pivot element equal to 1 by dividing Row 2 by 2:

| Basic | x₁ | x₂ | s₁ | s₂ | RHS |
|-------|----|----|----|----|-----|
| s₁    | 4  | 3  | 1  | 0  | 240 |
| x₁    | 1  | 1/2| 0  | 1/2| 50  |
| Z     | -70| -50| 0  | 0  | 0   |

Now, make all other elements in the x₁ column zero:
- Row 1: Row 1 - 4(Row 2)
- Row 3: Row 3 + 70(Row 2)

| Basic | x₁ | x₂      | s₁ | s₂      | RHS       |
|-------|----|---------|----|---------|-----------|
| s₁    | 0  | 3-4(1/2)=1 | 1  | -2      | 240-4(50)=40 |
| x₁    | 1  | 1/2     | 0  | 1/2     | 50        |
| Z     | 0  | -50+70(1/2)=-15 | 0  | 35      | 0+70(50)=3500 |

**Step 6: Continue the process**

The coefficient -15 in the Z row is still negative, so we continue with x₂ entering the basis.

The ratios are:
- s₁ row: 40/1 = 40
- x₁ row: 50/(1/2) = 100

The minimum is 40, so s₁ leaves the basis.

Pivot on the element in position (s₁, x₂):

| Basic | x₁ | x₂ | s₁ | s₂  | RHS |
|-------|----|----|----|----|-----|
| x₂    | 0  | 1  | 1  | -2  | 40  |
| x₁    | 1  | 0  | -1/2| 3/2| 30  |
| Z     | 0  | 0  | 15 | 5  | 4100|

**Step 7: Check for optimality**

All coefficients in the Z row are non-negative, so we have reached the optimal solution:
- x₁ = 30 (tables)
- x₂ = 40 (chairs)
- Maximum profit = $4,100

## Special Cases in Linear Programming

### 1. Multiple Optimal Solutions

Sometimes, there can be more than one solution that gives the same optimal value.

**Example:**
Maximize Z = 3x₁ + 3x₂
Subject to:
- x₁ + x₂ ≤ 10
- x₁, x₂ ≥ 0

Since both variables have the same coefficient in the objective function (3), any combination of x₁ and x₂ that satisfies x₁ + x₂ = 10 will give the same maximum Z = 30. For example, (10, 0), (5, 5), and (0, 10) are all optimal solutions.

### 2. Unbounded Solution

An unbounded solution occurs when the objective function can increase (or decrease) infinitely within the feasible region.

**Example:**
Maximize Z = 2x₁ + x₂
Subject to:
- x₁ - x₂ ≤ 10
- x₁, x₂ ≥ 0

In this case, x₂ can increase indefinitely without violating any constraint, and since its coefficient in the objective function is positive, Z can grow without bound.

### 3. Infeasible Solution

Sometimes, the constraints can be contradictory, leading to no feasible solution.

**Example:**
Maximize Z = 5x₁ + 3x₂
Subject to:
- x₁ + x₂ ≤ 10
- x₁ + x₂ ≥ 15
- x₁, x₂ ≥ 0

These constraints are contradictory because the sum x₁ + x₂ cannot be both ≤ 10 and ≥ 15 simultaneously.

## Practical Applications of Linear Programming

### 1. Production Planning

**Example: Car Manufacturing**

A car factory produces sedans and SUVs. Each sedan requires 40 hours of assembly and 10 hours of painting. Each SUV requires 60 hours of assembly and 15 hours of painting. The factory has 2,400 hours of assembly time and 750 hours of painting time available. The profit is $3,000 per sedan and $4,000 per SUV.

Using LP, we can find that the optimal production is 30 sedans and 30 SUVs, yielding a profit of $210,000.

### 2. Diet Planning

**Example: Nutritional Planning**

A dietitian needs to create a meal plan using two food types. Food A costs $2 per serving and provides 10g of protein and 15g of carbohydrates. Food B costs $3 per serving and provides 20g of protein and 5g of carbohydrates. The meal plan needs at least 60g of protein and 45g of carbohydrates.

Using LP to minimize cost, the solution is 3 servings of Food A and 1.5 servings of Food B, costing $10.50.

### 3. Transportation Problems

**Example: Distribution Center**

A company has warehouses in three locations and needs to ship products to four retail stores. The cost of shipping from each warehouse to each store varies. The supply at each warehouse and demand at each store are known.

LP can determine the optimal shipping plan to minimize total transportation costs.

### 4. Portfolio Optimization

As we saw in our investment example, LP can help determine the optimal allocation of investments to maximize returns while managing risk.

## Tips for Solving Linear Programming Problems

1. **Clearly define your variables:** Make sure you understand what each variable represents in the real-world context.

2. **Identify the objective clearly:** Are you maximizing profit or minimizing cost?

3. **List all constraints:** Think about all limitations on resources, requirements, and specifications.

4. **Check your units:** Make sure all terms in each constraint use the same units of measurement.

5. **Use the right method:** For 2 variables, graphical method is easiest. For more variables, use the Simplex Method.

6. **Interpret your solution:** Always relate the mathematical solution back to the real-world problem.

7. **Reality check:** Does your answer make sense in the real world? Sometimes mathematical solutions need practical adjustments.

## Conclusion

Linear Programming is a powerful tool for optimization problems in business, economics, engineering, and many other fields. By representing real-world problems as mathematical models with linear relationships, we can find optimal solutions that would be difficult to identify through trial and error.

Remember, the key steps are:
1. Define variables
2. Formulate the objective function
3. Identify constraints
4. Solve using appropriate methods
5. Interpret the solution in context

With practice, you'll become more comfortable with this process and be able to apply it to increasingly complex real-world situations.
