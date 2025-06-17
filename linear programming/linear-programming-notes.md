# UNIT 2: LINEAR PROGRAMMING PROBLEM

## Introduction to Linear Programming

Linear Programming (LP) is a mathematical technique used for optimizing a linear objective function subject to linear constraints. It is one of the most widely used operations research techniques for solving resource allocation problems.

### Key Features of Linear Programming:
- **Objective Function**: A linear function that needs to be maximized or minimized
- **Constraints**: Linear inequalities or equations that restrict the solution
- **Decision Variables**: Variables whose values we need to determine
- **Linearity**: All relationships must be linear
- **Non-negativity**: Decision variables are typically non-negative

## Linear Programming Problem Formulation

### Standard Form of LP Problem:
- **Maximize or Minimize**: Z = c₁x₁ + c₂x₂ + ... + cₙxₙ
- **Subject to**: a₁₁x₁ + a₁₂x₂ + ... + a₁ₙxₙ (≤, =, or ≥) b₁
              a₂₁x₁ + a₂₂x₂ + ... + a₂ₙxₙ (≤, =, or ≥) b₂
              ...
              aₘ₁x₁ + aₘ₂x₂ + ... + aₘₙxₙ (≤, =, or ≥) bₘ
- **Non-negativity**: x₁, x₂, ..., xₙ ≥ 0

### Steps in Formulating an LP Problem:
1. Identify the decision variables
2. Formulate the objective function
3. Identify and formulate the constraints
4. Express non-negativity conditions

### Example 1: Product Mix Problem

**Problem Statement:**
A furniture company produces tables and chairs. Each table requires 4 hours of carpentry and 2 hours of finishing. Each chair requires 3 hours of carpentry and 1 hour of finishing. The company has 240 hours of carpentry time and 100 hours of finishing time available each week. The profit is $70 per table and $50 per chair. How many tables and chairs should the company produce each week to maximize profit?

**Formulation:**
Let x₁ = number of tables produced
Let x₂ = number of chairs produced

**Objective Function:** 
Maximize Z = 70x₁ + 50x₂ (profit)

**Constraints:**
- Carpentry time: 4x₁ + 3x₂ ≤ 240 (hours)
- Finishing time: 2x₁ + x₂ ≤ 100 (hours)
- Non-negativity: x₁, x₂ ≥ 0

## Formulation with Different Types of Constraints

### Types of Constraints:
1. **Less than or equal to (≤)**: Resource limitations
2. **Greater than or equal to (≥)**: Minimum requirements
3. **Equal to (=)**: Exact requirements

### Example 2: Diet Problem

**Problem Statement:**
A dietitian is planning a meal that includes two foods, A and B. Each unit of food A contains 2 units of protein, 3 units of carbohydrates, and 1 unit of fat. Each unit of food B contains 1 unit of protein, 1 unit of carbohydrates, and 2 units of fat. The meal must contain at least 10 units of protein, exactly 15 units of carbohydrates, and at most 12 units of fat. The cost is $3 per unit for food A and $2 per unit for food B. How many units of each food should be included to minimize the cost?

**Formulation:**
Let x₁ = units of food A
Let x₂ = units of food B

**Objective Function:**
Minimize Z = 3x₁ + 2x₂ (cost)

**Constraints:**
- Protein (≥): 2x₁ + x₂ ≥ 10
- Carbohydrates (=): 3x₁ + x₂ = 15
- Fat (≤): x₁ + 2x₂ ≤ 12
- Non-negativity: x₁, x₂ ≥ 0

## Graphical Analysis of Linear Programming

The graphical method is used to solve LP problems with two decision variables by:
1. Plotting the constraints on a graph
2. Identifying the feasible region
3. Finding the optimal solution at one of the corner points

### Key Concepts:
- **Feasible Region**: Area satisfying all constraints
- **Corner Points (Extreme Points)**: Points where constraint lines intersect
- **Objective Function Line**: Line representing different values of the objective function

## Graphical Linear Programming Solution

### Steps in Graphical Method:
1. Plot all constraints on a graph
2. Identify the feasible region
3. Find all corner points of the feasible region
4. Evaluate the objective function at each corner point
5. Select the corner point that gives the optimal value

### Example 3: Solving Example 1 Graphically

From Example 1:
- Maximize Z = 70x₁ + 50x₂
- Subject to:
  - 4x₁ + 3x₂ ≤ 240
  - 2x₁ + x₂ ≤ 100
  - x₁, x₂ ≥ 0

**Step 1:** Convert constraints into equations and plot them
- 4x₁ + 3x₂ = 240
- 2x₁ + x₂ = 100
- x₁ = 0, x₂ = 0

**Step 2:** Identify the feasible region
The feasible region is the area bounded by the constraint lines and the axes.

**Step 3:** Find the corner points
- (0,0): Origin
- (0,80): Intersection of x₁ = 0 and 3x₂ = 240
- (50,0): Intersection of x₂ = 0 and 2x₁ = 100
- (30,40): Intersection of 4x₁ + 3x₂ = 240 and 2x₁ + x₂ = 100

**Step 4:** Evaluate the objective function at each corner point
- Z(0,0) = 70(0) + 50(0) = 0
- Z(0,80) = 70(0) + 50(80) = 4000
- Z(50,0) = 70(50) + 50(0) = 3500
- Z(30,40) = 70(30) + 50(40) = 4100

**Step 5:** Select the optimal solution
The maximum value of Z is 4100 at the point (30,40).
Therefore, the company should produce 30 tables and 40 chairs for maximum profit.

## Multiple Optimal Solutions

In some cases, an LP problem may have multiple optimal solutions. This occurs when the objective function line is parallel to one of the constraint boundaries, resulting in multiple points that give the same optimal value.

### Example 4: Multiple Optimal Solutions

**Problem Statement:**
Maximize Z = 3x₁ + 2x₂
Subject to:
- x₁ + x₂ ≤ 40
- 3x₁ + x₂ ≤ 60
- x₁, x₂ ≥ 0

In this case, if we plot and solve, we find that the objective function line (3x₁ + 2x₂ = k) is parallel to the constraint line x₁ + x₂ = 40. This means that any point on the line segment between two corner points will give the same optimal value.

## Unbounded Solution

An LP problem has an unbounded solution when the objective function can be increased (for maximization) or decreased (for minimization) indefinitely without violating any constraints.

### Example 5: Unbounded Solution

**Problem Statement:**
Maximize Z = 2x₁ + x₂
Subject to:
- x₁ - x₂ ≤ 10
- x₁, x₂ ≥ 0

When we graph this problem, we find that the feasible region extends infinitely in the positive x₂ direction. Since the objective function increases as x₂ increases, there is no finite maximum value for Z.

## Infeasible Solution

An LP problem is infeasible when there is no solution that satisfies all constraints simultaneously, resulting in an empty feasible region.

### Example 6: Infeasible Solution

**Problem Statement:**
Maximize Z = 5x₁ + 3x₂
Subject to:
- x₁ + x₂ ≥ 10
- x₁ + x₂ ≤ 5
- x₁, x₂ ≥ 0

These constraints are contradictory because we cannot have x₁ + x₂ both greater than or equal to 10 and less than or equal to 5. Therefore, there is no feasible solution.

## Basics of Simplex Method

The simplex method is an algebraic procedure for solving LP problems with any number of variables. It systematically moves from one basic feasible solution to another until an optimal solution is reached.

### Key Concepts:
- **Basic Solution**: Solution with n variables where (n-m) variables are set to zero (where n is the number of variables and m is the number of equality constraints)
- **Basic Feasible Solution**: Basic solution where all variables are non-negative
- **Pivot Element**: Element in the simplex tableau that determines which variable enters and leaves the basis
- **Reduced Cost Coefficients**: Values that determine if the current solution is optimal

## Simplex Method Computation

### Steps in the Simplex Method:
1. Convert the LP problem into standard form by adding slack/surplus variables
2. Set up the initial simplex tableau
3. Identify the entering variable (most negative coefficient in the objective row)
4. Identify the leaving variable (minimum ratio test)
5. Perform pivot operations to get a new tableau
6. Repeat steps 3-5 until an optimal solution is reached

### Example 7: Simplex Method Application

**Problem Statement:**
Maximize Z = 3x₁ + 2x₂
Subject to:
- x₁ + 2x₂ ≤ 10
- 3x₁ + x₂ ≤ 15
- x₁, x₂ ≥ 0

**Step 1:** Convert to standard form by adding slack variables
- Maximize Z = 3x₁ + 2x₂ + 0s₁ + 0s₂
- Subject to:
  - x₁ + 2x₂ + s₁ = 10
  - 3x₁ + x₂ + s₂ = 15
  - x₁, x₂, s₁, s₂ ≥ 0

**Step 2:** Set up the initial simplex tableau

| Basis | x₁ | x₂ | s₁ | s₂ | RHS |
|-------|----|----|----|----|-----|
| s₁    | 1  | 2  | 1  | 0  | 10  |
| s₂    | 3  | 1  | 0  | 1  | 15  |
| Z     | -3 | -2 | 0  | 0  | 0   |

**Step 3:** Identify the entering variable
The most negative coefficient in the objective row is -3, so x₁ enters the basis.

**Step 4:** Identify the leaving variable
- Ratio for s₁: 10/1 = 10
- Ratio for s₂: 15/3 = 5
The minimum ratio is 5, so s₂ leaves the basis.

**Step 5:** Perform pivot operations
Divide the s₂ row by 3 to make the pivot element (3,1) equal to 1.

| Basis | x₁ | x₂ | s₁ | s₂ | RHS |
|-------|----|----|----|----|-----|
| s₁    | 1  | 2  | 1  | 0  | 10  |
| x₁    | 1  | 1/3| 0  | 1/3| 5   |
| Z     | -3 | -2 | 0  | 0  | 0   |

Update the other rows:
- s₁ row: Subtract 1 times the x₁ row from the s₁ row
- Z row: Add 3 times the x₁ row to the Z row

| Basis | x₁ | x₂ | s₁ | s₂ | RHS |
|-------|----|----|----|----|-----|
| s₁    | 0  | 5/3| 1  | -1/3| 5  |
| x₁    | 1  | 1/3| 0  | 1/3| 5   |
| Z     | 0  | -1 | 0  | 1  | 15  |

**Step 6:** Continue the process
The coefficient -1 in the Z row indicates that we should introduce x₂ into the basis.

By following the simplex procedure to completion, we find the optimal solution is x₁ = 3, x₂ = 3.5, with Z = 16.

## Simplex Method with More Than Two Variables

The simplex method can be extended to problems with any number of variables following the same principles. The computation becomes more complex but the steps remain the same.

### Example 8: Three-Variable Problem

**Problem Statement:**
Maximize Z = 2x₁ + 3x₂ + 4x₃
Subject to:
- 3x₁ + 2x₂ + x₃ ≤ 30
- 2x₁ + 5x₂ + 3x₃ ≤ 60
- x₁, x₂, x₃ ≥ 0

This problem would require setting up a simplex tableau with 3 original variables and 2 slack variables, and following the same steps as in the two-variable case.

## Primal and Dual Problems

Every LP problem (primal) has an associated dual problem. The relationship between the primal and dual problems provides valuable economic insights and computational advantages.

### Properties of Primal-Dual Relationship:
- If the primal is a maximization problem, the dual is a minimization problem, and vice versa
- Variables in the dual correspond to constraints in the primal
- Constraints in the dual correspond to variables in the primal
- The optimal value of the objective function is the same for both problems

### Example 9: Primal-Dual Formulation

**Primal Problem:**
Maximize Z = 3x₁ + 2x₂
Subject to:
- x₁ + 2x₂ ≤ 10
- 3x₁ + x₂ ≤ 15
- x₁, x₂ ≥ 0

**Dual Problem:**
Minimize W = 10y₁ + 15y₂
Subject to:
- y₁ + 3y₂ ≥ 3
- 2y₁ + y₂ ≥ 2
- y₁, y₂ ≥ 0

## Economic Interpretation

The dual variables provide valuable economic interpretations:

### Shadow Prices:
The dual variables (y₁, y₂) represent the marginal value or shadow price of the respective resources. They indicate how much the objective function would change if the right-hand side of the constraint is increased by one unit.

### Reduced Costs:
The reduced costs in the final simplex tableau indicate the opportunity cost of introducing non-basic variables into the solution.

### Example 10: Economic Interpretation

In Example 9, if the optimal dual variables are y₁ = 0.5 and y₂ = 0.83, this means:
- Each additional unit of the first resource (associated with the first constraint) would increase the maximum profit by 0.5 units
- Each additional unit of the second resource would increase the maximum profit by 0.83 units

These interpretations help managers make informed decisions about resource allocation and investments.
