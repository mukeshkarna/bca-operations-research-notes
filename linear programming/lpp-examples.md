# LINEAR PROGRAMMING PROBLEM - EXAMPLE NOTES

## Example 1: Manufacturing Problem (Formulation)

**Problem Statement:**
A furniture manufacturer produces dining tables and chairs. Each table requires 8 hours of carpentry and 2 hours of finishing. Each chair requires 4 hours of carpentry and 1 hour of finishing. The workshop has 400 hours of carpentry time and 120 hours of finishing time available per week. The profit is $300 per table and $120 per chair. How many tables and chairs should be produced to maximize profit?

**Step 1: Define the decision variables**
- Let x₁ = number of tables to produce
- Let x₂ = number of chairs to produce

**Step 2: Formulate the objective function**
- Maximize Z = 300x₁ + 120x₂ (total profit)

**Step 3: Identify and formulate the constraints**
- Carpentry constraint: 8x₁ + 4x₂ ≤ 400 (available carpentry hours)
- Finishing constraint: 2x₁ + x₂ ≤ 120 (available finishing hours)
- Non-negativity: x₁, x₂ ≥ 0 (cannot produce negative quantities)

**Step 4: State the complete LP model**
- Maximize Z = 300x₁ + 120x₂
- Subject to:
  - 8x₁ + 4x₂ ≤ 400
  - 2x₁ + x₂ ≤ 120
  - x₁, x₂ ≥ 0

## Example 2: Investment Problem (Formulation)

**Problem Statement:**
An investor has $100,000 to invest in two types of investments: bonds and stocks. The bonds yield an annual return of 5%, while stocks yield 8%. Due to risk considerations, the investor wants to invest at least $30,000 in bonds. Additionally, the amount invested in stocks should not exceed twice the amount invested in bonds. How much should be invested in each type to maximize the annual return?

**Step 1: Define decision variables**
- Let x₁ = amount invested in bonds ($)
- Let x₂ = amount invested in stocks ($)

**Step 2: Formulate objective function**
- Maximize Z = 0.05x₁ + 0.08x₂ (total annual return)

**Step 3: Identify and formulate constraints**
- Total investment: x₁ + x₂ ≤ 100,000 
- Minimum bond investment: x₁ ≥ 30,000
- Stock limitation: x₂ ≤ 2x₁ → x₂ - 2x₁ ≤ 0
- Non-negativity: x₁, x₂ ≥ 0

**Step 4: State the complete LP model**
- Maximize Z = 0.05x₁ + 0.08x₂
- Subject to:
  - x₁ + x₂ ≤ 100,000
  - x₁ ≥ 30,000
  - x₂ - 2x₁ ≤ 0
  - x₁, x₂ ≥ 0

## Example 3: Diet Problem (Formulation with Different Constraints)

**Problem Statement:**
A dietitian needs to create a meal plan using two food types. Food A provides 2 units of protein, 4 units of carbohydrates, and 1 unit of fat per serving. Food B provides 3 units of protein, 2 units of carbohydrates, and 2 units of fat per serving. The meal plan must provide at least 12 units of protein, exactly 16 units of carbohydrates, and at most 8 units of fat. If Food A costs $2 per serving and Food B costs $3 per serving, how many servings of each food should be included to minimize cost?

**Step 1: Define decision variables**
- Let x₁ = number of servings of Food A
- Let x₂ = number of servings of Food B

**Step 2: Formulate objective function**
- Minimize Z = 2x₁ + 3x₂ (total cost)

**Step 3: Identify and formulate constraints with different types**
- Protein (≥): 2x₁ + 3x₂ ≥ 12 (minimum requirement)
- Carbohydrates (=): 4x₁ + 2x₂ = 16 (exact requirement)
- Fat (≤): x₁ + 2x₂ ≤ 8 (maximum limit)
- Non-negativity: x₁, x₂ ≥ 0

**Step 4: State the complete LP model**
- Minimize Z = 2x₁ + 3x₂
- Subject to:
  - 2x₁ + 3x₂ ≥ 12
  - 4x₁ + 2x₂ = 16
  - x₁ + 2x₂ ≤ 8
  - x₁, x₂ ≥ 0

## Example 4: Graphical Solution Method (Detailed)

Let's solve Example 1 graphically:

**The Problem:**
- Maximize Z = 300x₁ + 120x₂
- Subject to:
  - 8x₁ + 4x₂ ≤ 400
  - 2x₁ + x₂ ≤ 120
  - x₁, x₂ ≥ 0

**Step 1: Plot the constraints**
Plot the following lines:
- 8x₁ + 4x₂ = 400 (Carpentry constraint)
  - When x₁ = 0: x₂ = 100
  - When x₂ = 0: x₁ = 50
- 2x₁ + x₂ = 120 (Finishing constraint)
  - When x₁ = 0: x₂ = 120
  - When x₂ = 0: x₁ = 60
- x₁ = 0 (y-axis)
- x₂ = 0 (x-axis)

**Step 2: Identify the feasible region**
The feasible region is the area bounded by all constraints, which is the polygon formed by the points (0,0), (0,100), (40,60), (60,0).

**Step 3: Find corner points**
The corner points of the feasible region are:
- (0,0): Origin
- (0,100): Intersection of x₁ = 0 and 8x₁ + 4x₂ = 400
- (40,60): Intersection of 8x₁ + 4x₂ = 400 and 2x₁ + x₂ = 120
- (60,0): Intersection of x₂ = 0 and 2x₁ + x₂ = 120

Let's verify the intersection point (40,60):
- From 8x₁ + 4x₂ = 400:
  - 8(40) + 4(60) = 320 + 240 = 560 ≠ 400
  - This is incorrect. Let's recalculate:
  - If 8x₁ + 4x₂ = 400 and 2x₁ + x₂ = 120
  - From second equation: x₂ = 120 - 2x₁
  - Substitute into first: 8x₁ + 4(120 - 2x₁) = 400
  - 8x₁ + 480 - 8x₁ = 400
  - 480 = 400 (inconsistent)

Let's correctly find this intersection:
- From 8x₁ + 4x₂ = 400: x₂ = (400 - 8x₁)/4 = 100 - 2x₁
- From 2x₁ + x₂ = 120: x₂ = 120 - 2x₁
- Setting equal: 100 - 2x₁ = 120 - 2x₁
- 100 = 120 (inconsistent)

This means the lines don't intersect where we expected. Let's recalculate all points correctly:

Carpentry constraint (8x₁ + 4x₂ = 400):
- When x₁ = 0: x₂ = 100
- When x₂ = 0: x₁ = 50

Finishing constraint (2x₁ + x₂ = 120):
- When x₁ = 0: x₂ = 120
- When x₂ = 0: x₁ = 60

The actual corner points are:
- (0,0): Origin
- (0,100): Intersection of x₁ = 0 and 8x₁ + 4x₂ = 400
- (50,0): Intersection of x₂ = 0 and 8x₁ + 4x₂ = 400
- (60,0): Intersection of x₂ = 0 and 2x₁ + x₂ = 120

To find the remaining intersection point:
- From 8x₁ + 4x₂ = 400: x₂ = 100 - 2x₁
- From 2x₁ + x₂ = 120: x₂ = 120 - 2x₁
- Setting equal: 100 - 2x₁ = 120 - 2x₁
- 100 = 120 (inconsistent)

The lines are parallel and don't intersect. Let's look at the constraints again:
- The line 2x₁ + x₂ = 120 lies above the line 8x₁ + 4x₂ = 400 in the first quadrant
- Therefore, the actual feasible region is bounded by:
  - x₁ = 0 (y-axis)
  - x₂ = 0 (x-axis)
  - 8x₁ + 4x₂ = 400 (Carpentry constraint)

The corrected corner points are:
- (0,0): Origin
- (0,100): Intersection of x₁ = 0 and 8x₁ + 4x₂ = 400
- (50,0): Intersection of x₂ = 0 and 8x₁ + 4x₂ = 400

**Step 4: Evaluate objective function at each corner point**
- Z(0,0) = 300(0) + 120(0) = 0
- Z(0,100) = 300(0) + 120(100) = 12,000
- Z(50,0) = 300(50) + 120(0) = 15,000

**Step 5: Identify the optimal solution**
The maximum value of Z = 15,000 occurs at the point (50,0).
Therefore, the optimal solution is to produce 50 tables and 0 chairs, resulting in a maximum profit of $15,000.

## Example 5: Multiple Optimal Solutions

**Problem Statement:**
A company manufactures two products, A and B. Each unit of Product A requires 2 hours of labor and 1 unit of raw material. Each unit of Product B requires 2 hours of labor and 3 units of raw material. The company has 100 hours of labor and 90 units of raw material available. Both products generate the same profit of $40 per unit. How many units of each product should be produced to maximize profit?

**Step 1: Formulate the LP model**
- Let x₁ = number of units of Product A
- Let x₂ = number of units of Product B
- Maximize Z = 40x₁ + 40x₂
- Subject to:
  - 2x₁ + 2x₂ ≤ 100 (labor constraint)
  - x₁ + 3x₂ ≤ 90 (raw material constraint)
  - x₁, x₂ ≥ 0

**Step 2: Graph the constraints and identify the feasible region**
- Labor constraint (2x₁ + 2x₂ = 100): x₁ + x₂ = 50
  - When x₁ = 0: x₂ = 50
  - When x₂ = 0: x₁ = 50
- Raw material constraint (x₁ + 3x₂ = 90):
  - When x₁ = 0: x₂ = 30
  - When x₂ = 0: x₁ = 90

The corner points are:
- (0,0): Origin
- (0,30): Intersection of x₁ = 0 and x₁ + 3x₂ = 90
- (45,15): Intersection of x₁ + x₂ = 50 and x₁ + 3x₂ = 90
- (50,0): Intersection of x₂ = 0 and x₁ + x₂ = 50

**Step 3: Evaluate objective function at each corner point**
- Z(0,0) = 40(0) + 40(0) = 0
- Z(0,30) = 40(0) + 40(30) = 1,200
- Z(45,5) = 40(45) + 40(5) = 2,000
- Z(50,0) = 40(50) + 40(0) = 2,000

**Step 4: Identify the optimal solution**
The maximum value of Z = 2,000 occurs at both points (45,5) and (50,0).

This is a case of multiple optimal solutions. Any point on the line segment connecting (45,5) and (50,0) will also yield the maximum profit of $2,000.

The general form of these solutions is:
- x₁ = 45 + 5λ
- x₂ = 5 - 5λ
- Where 0 ≤ λ ≤ 1

This occurs because the objective function line (40x₁ + 40x₂ = 2,000) is parallel to the labor constraint line (x₁ + x₂ = 50).

## Example 6: Unbounded Solution

**Problem Statement:**
Maximize Z = 3x₁ + 2x₂
Subject to:
- -x₁ + x₂ ≤ 10
- x₁ - 2x₂ ≤ 40
- x₁, x₂ ≥ 0

**Graphical Analysis:**
- Constraint 1 (-x₁ + x₂ = 10): x₂ = 10 + x₁
  - When x₁ = 0: x₂ = 10
  - When x₂ = 0: x₁ = -10 (outside first quadrant)
- Constraint 2 (x₁ - 2x₂ = 40): x₁ = 40 + 2x₂
  - When x₁ = 0: x₂ = -20 (outside first quadrant)
  - When x₂ = 0: x₁ = 40

When we graph these constraints, we notice that the feasible region extends infinitely in the positive x₁ direction. Since the coefficient of x₁ in the objective function is positive (3), the value of Z can increase without bound as x₁ increases.

Therefore, this problem has an unbounded solution - there is no finite maximum value for Z.

## Example 7: Infeasible Solution

**Problem Statement:**
Maximize Z = 5x₁ + 3x₂
Subject to:
- x₁ + x₂ ≥ 10
- x₁ + x₂ ≤ 5
- x₁, x₂ ≥ 0

**Analysis:**
Let's analyze the constraints:
- Constraint 1: x₁ + x₂ ≥ 10
- Constraint 2: x₁ + x₂ ≤ 5

These constraints are contradictory. The first constraint requires the sum x₁ + x₂ to be at least 10, while the second constraint requires the same sum to be at most 5. No solution can satisfy both constraints simultaneously.

Therefore, this problem has no feasible solution - the feasible region is empty.

## Example 8: Simplex Method (Step-by-Step)

**Problem Statement:**
Maximize Z = 4x₁ + 6x₂
Subject to:
- 2x₁ + 3x₂ ≤ 12
- 4x₁ + 2x₂ ≤ 16
- x₁, x₂ ≥ 0

**Step 1: Convert to standard form by adding slack variables**
- Maximize Z = 4x₁ + 6x₂ + 0s₁ + 0s₂
- Subject to:
  - 2x₁ + 3x₂ + s₁ = 12
  - 4x₁ + 2x₂ + s₂ = 16
  - x₁, x₂, s₁, s₂ ≥ 0

**Step 2: Set up the initial simplex tableau**

| Basic | x₁ | x₂ | s₁ | s₂ | RHS |
|-------|----|----|----|----|-----|
| s₁    | 2  | 3  | 1  | 0  | 12  |
| s₂    | 4  | 2  | 0  | 1  | 16  |
| Z     | -4 | -6 | 0  | 0  | 0   |

**Step 3: Select entering variable (most negative coefficient in Z row)**
The coefficient -6 for x₂ is most negative, so x₂ enters the basis.

**Step 4: Select leaving variable (minimum ratio test)**
- For s₁: 12/3 = 4
- For s₂: 16/2 = 8
The minimum ratio is 4, so s₁ leaves the basis.

**Step 5: Perform pivot operations (Row operations to make pivot element = 1)**
Divide Row 1 by 3 to make the pivot element (in position x₂, s₁) equal to 1:

| Basic | x₁   | x₂ | s₁   | s₂ | RHS  |
|-------|------|----|------|----|----- |
| x₂    | 2/3  | 1  | 1/3  | 0  | 4    |
| s₂    | 4    | 2  | 0    | 1  | 16   |
| Z     | -4   | -6 | 0    | 0  | 0    |

Now perform row operations to make other elements in the x₂ column zero:
- Row 2 = Row 2 - (2 × Row 1)
- Row 3 = Row 3 + (6 × Row 1)

| Basic | x₁      | x₂ | s₁      | s₂ | RHS     |
|-------|---------|----|---------|----|---------|
| x₂    | 2/3     | 1  | 1/3     | 0  | 4       |
| s₂    | 4-4/3=8/3 | 0  | -2/3    | 1  | 16-8=8  |
| Z     | -4+4=-0.67 | 0  | 2       | 0  | 0+24=24 |

**Step 6: Check optimality and continue if needed**
There is still a negative coefficient (-0.67) in the Z row, so we continue.

**Step 7: Second iteration**
- Entering variable: x₁ (coefficient -0.67)
- Leaving variable: 
  - For x₂: 4/(2/3) = 6
  - For s₂: 8/(8/3) = 3
  The minimum ratio is 3, so s₂ leaves.

Pivot on the element (8/3) in position (s₂, x₁):
- Divide Row 2 by 8/3 to make pivot element = 1

| Basic | x₁ | x₂  | s₁   | s₂      | RHS |
|-------|----|----|------|---------|-----|
| x₂    | 2/3| 1  | 1/3  | 0       | 4   |
| x₁    | 1  | 0  | -1/4 | 3/8     | 3   |
| Z     | 0  | 0  | 1.83 | 0.25    | 26  |

**Step 8: Check optimality**
All coefficients in the Z row are non-negative, so we have reached an optimal solution.

**Optimal solution:**
- x₁ = 3
- x₂ = 4 - (2/3)(3) = 4 - 2 = 2
- Maximum Z = 26

## Example 9: Primal-Dual Relationship

**Primal Problem:**
Maximize Z = 3x₁ + 4x₂
Subject to:
- 2x₁ + 3x₂ ≤ 18
- 3x₁ + 2x₂ ≤ 17
- x₁, x₂ ≥ 0

**Dual Formulation:**
To formulate the dual:
1. Make it a minimization problem
2. Create a dual variable for each primal constraint
3. Create a dual constraint for each primal variable
4. The right-hand sides of dual constraints are coefficients from the primal objective
5. The coefficients in dual constraints come from primal constraint coefficients

Let y₁, y₂ be the dual variables corresponding to the two primal constraints.

**The Dual Problem:**
Minimize W = 18y₁ + 17y₂
Subject to:
- 2y₁ + 3y₂ ≥ 3 (from x₁ in primal)
- 3y₁ + 2y₂ ≥ 4 (from x₂ in primal)
- y₁, y₂ ≥ 0

**Economic Interpretation:**
- If the optimal solution to the primal is x₁ = 3, x₂ = 4 with Z = 25
- And the optimal solution to the dual is y₁ = 0.5, y₂ = 0.67 with W = 25
- Then:
  1. y₁ = 0.5 means an additional unit of the first resource (increasing 18 to 19) would increase maximum profit by 0.5 units
  2. y₂ = 0.67 means an additional unit of the second resource (increasing 17 to 18) would increase maximum profit by 0.67 units
  3. These values represent the "shadow prices" or marginal values of the resources

## Example 10: Economic Interpretation Using Sensitivity Analysis

**Problem Statement:**
A company produces two products, A and B, using two resources: labor and material. Each unit of Product A requires 3 hours of labor and 2 kg of material. Each unit of Product B requires 4 hours of labor and 1 kg of material. The company has 240 hours of labor and 140 kg of material available. The profit is $5 per unit for Product A and $4 per unit for Product B. 

**The LP model:**
- Maximize Z = 5x₁ + 4x₂
- Subject to:
  - 3x₁ + 4x₂ ≤ 240 (labor constraint)
  - 2x₁ + x₂ ≤ 140 (material constraint)
  - x₁, x₂ ≥ 0

**Optimal solution (using simplex method):**
- x₁ = 60, x₂ = 15
- Maximum profit Z = 5(60) + 4(15) = 300 + 60 = 360
- Shadow prices: y₁ = 1 (labor), y₂ = 0.5 (material)

**Economic interpretations:**
1. **Shadow prices:**
   - y₁ = 1 means each additional hour of labor would increase maximum profit by $1
   - y₂ = 0.5 means each additional kg of material would increase maximum profit by $0.5

2. **Resource valuation:**
   - Total value of resources = 240(1) + 140(0.5) = 240 + 70 = 310
   - Total profit = 360
   - Producer surplus = 360 - 310 = 50

3. **Decision making:**
   - If additional labor costs less than $1 per hour, the company should acquire more
   - If additional material costs less than $0.5 per kg, the company should acquire more
   - If a new Product C uses 5 hours of labor and 3 kg of material per unit with a profit of $7:
     - Resource value used = 5(1) + 3(0.5) = 5 + 1.5 = $6.5
     - Since profit ($7) > resource value ($6.5), it may be profitable to produce C
