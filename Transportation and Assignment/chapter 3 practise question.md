Here are 2 balanced and 2 unbalanced questions each for the North West Corner method, Least Cost method, and Vogel's Approximation method:

## North West Corner Method Questions

### Balanced Problems:
1. A company has three factories (A, B, C) and four warehouses (W, X, Y, Z). The monthly production capacities of factories A, B, and C are 300, 400, and 500 units respectively. The monthly requirements of warehouses W, X, Y, and Z are 200, 300, 250, and 450 units respectively. Use the North West Corner method to find the initial basic feasible solution for this transportation problem.

2. Three suppliers P, Q, and R supply goods to four retail outlets S, T, U, and V. The supplies available at P, Q, and R are 120, 80, and 100 units respectively. The demands at S, T, U, and V are 60, 70, 90, and 80 units respectively. Use the North West Corner method to determine the initial allocation and calculate the transportation cost if the unit transportation costs (in $) are:
   ```
   To:  S  T  U  V
   P:  10 12  9 11
   Q:   8 10 11  7
   R:  14  9 12 10
   ```

### Unbalanced Problems:
1. Two manufacturers X and Y have production capacities of 150 and 200 units per month. Three retailers P, Q, and R require 80, 130, and 170 units per month. Find the initial basic feasible solution using the North West Corner method for this unbalanced transportation problem.

2. A company manufactures products at three plants A, B, and C with capacities of 50, 70, and 30 units per week respectively. These products are to be shipped to four distribution centers W, X, Y, and Z with weekly demands of 25, 35, 40, and 30 units respectively. Use the North West Corner method to obtain the initial basic feasible solution for this unbalanced transportation problem.

## Least Cost Method Questions

### Balanced Problems:
1. A company has three warehouses (W1, W2, W3) and four retail stores (S1, S2, S3, S4). The supply capacities of warehouses W1, W2, and W3 are 15, 25, and 10 units respectively. The demand requirements of stores S1, S2, S3, and S4 are 5, 15, 15, and 15 units respectively. Use the Least Cost method to determine the optimal allocation if the transportation costs per unit (in $) are:
   ```
   To:  S1  S2  S3  S4
   W1:  10   2    8   11
   W2:   7   9    4    5
   W3:   3   8    7    9
   ```

2. Three sources A, B, and C have supplies of 12, 17, and 11 units. Four destinations P, Q, R, and S have demands of 10, 8, 12, and 10 units respectively. Use the Least Cost method to determine the initial allocation with the following cost matrix:
   ```
   To:  P   Q   R   S
   A:   6   8   4   9
   B:   3   2   5   4
   C:   5   7   6   8
   ```

### Unbalanced Problems:
1. A company has two production plants P1 and P2 with production capacities of 200 and 300 units. There are three warehouses W1, W2, and W3 with demands of 150, 200, and 100 units. Find the initial basic feasible solution using the Least Cost method with the following transportation costs per unit:
   ```
   To:  W1  W2  W3
   P1:  8   6   10
   P2:  5   4    9
   ```

2. Four factories F1, F2, F3, and F4 manufacture the same product with monthly capacities of 40, 70, 90, and 30 units respectively. These products are to be shipped to three warehouses W1, W2, and W3 with monthly requirements of 50, 110, and 60 units respectively. Use the Least Cost method to determine the initial basic feasible solution with the following transportation costs (in $):
   ```
   To:  W1  W2  W3
   F1:  2   7    9
   F2:  5   8    6
   F3:  3   4    7
   F4:  6   9    3
   ```

## Vogel's Approximation Method Questions

### Balanced Problems:
1. A manufacturing company has three plants A, B, and C with monthly production capacities of 100, 80, and 90 units respectively. These products are shipped to four warehouses W, X, Y, and Z with monthly requirements of 70, 50, 70, and 80 units respectively. Use Vogel's Approximation Method to find the initial basic feasible solution with the following transportation costs per unit:
   ```
   To:  W   X   Y   Z
   A:   3   2   7   6
   B:   7   5   2   3
   C:   2   5   4   5
   ```

2. Three offices (O1, O2, O3) need to send documents to four branches (B1, B2, B3, B4). The number of documents available at offices O1, O2, and O3 are 30, 40, and 30 respectively. The number of documents required at branches B1, B2, B3, and B4 are 20, 30, 25, and 25 respectively. Use Vogel's Approximation Method to determine the initial allocation with the following cost matrix (in $):
   ```
   To:  B1  B2  B3  B4
   O1:  8   5   6   8
   O2:  15  10  9   10
   O3:  5   12  8   6
   ```

### Unbalanced Problems:
1. A company manufactures products at two plants P1 and P2 with daily capacities of 150 and 200 units respectively. These products are to be shipped to three warehouses W1, W2, and W3 with daily requirements of 100, 150, and 50 units respectively. Use Vogel's Approximation Method to obtain the initial basic feasible solution with the following transportation costs (in $):
   ```
   To:  W1  W2  W3
   P1:  5   3   8
   P2:  4   7   6
   ```

2. Four suppliers S1, S2, S3, and S4 have stocks of 80, 60, 70, and 40 units respectively. Three customers C1, C2, and C3 require 90, 120, and 50 units respectively. Use Vogel's Approximation Method to find the initial basic feasible solution if the transportation costs per unit are:
   ```
   To:  C1  C2  C3
   S1:  4   5   3
   S2:  6   8   5
   S3:  7   4   6
   S4:  9   6   7
   ```

## Modified Distribution (MODI) Method Questions

### Balanced Problems:

1. Consider the following balanced transportation problem with sources A, B, C and destinations P, Q, R, S. The initial basic feasible solution using the Northwest Corner method is given below. Use the MODI method to check if this solution is optimal. If not, find the optimal solution.

   Supply quantities: A=15, B=25, C=10
   Demand quantities: P=5, Q=15, R=15, S=15
   
   Cost matrix:
   ```
   To:  P   Q   R   S
   A:   10  2   8   11
   B:   7   9   4   5
   C:   3   8   7   9
   ```
   
   Initial solution:
   A→P: 5, A→Q: 10
   B→Q: 5, B→R: 15, B→S: 5
   C→S: 10

2. A company manufactures products at three factories and distributes them to four warehouses. The transportation costs per unit (in $), supply capacities, and demand requirements are given below. The initial solution using Vogel's Approximation Method is provided. Apply the MODI method to test whether this solution is optimal and if not, find the optimal solution.

   Supply: Factory 1=100, Factory 2=80, Factory 3=90
   Demand: Warehouse 1=70, Warehouse 2=50, Warehouse 3=70, Warehouse 4=80
   
   Cost matrix:
   ```
   To:      W1  W2  W3  W4
   Factory1: 3   2   7   6
   Factory2: 7   5   2   3
   Factory3: 2   5   4   5
   ```
   
   Initial solution:
   Factory1→W2: 50, Factory1→W3: 50
   Factory2→W3: 20, Factory2→W4: 60
   Factory3→W1: 70, Factory3→W4: 20

### Unbalanced Problems:

1. A company has three production plants with capacities of 60, 70, and 50 units. Four customers have demands of 40, 30, 60, and 45 units. The transportation costs (in $) per unit are given in the following table. An initial basic feasible solution using the Least Cost method is provided. Use the MODI method to determine if this solution is optimal. If not, find the optimal solution.

   Cost matrix:
   ```
   To:      C1  C2  C3  C4
   Plant1:  6   4   5   8
   Plant2:  9   7   3   6
   Plant3:  5   8   6   4
   ```
   
   Initial solution:
   Plant1→C2: 30, Plant1→C3: 30
   Plant2→C3: 30, Plant2→C4: 40
   Plant3→C1: 40, Plant3→C4: 5
   
   Note: This is unbalanced with total supply (180) > total demand (175)

2. A company distributes products from three warehouses to five retail stores. The warehouses have capacities of 80, 120, and 70 units, while the retail stores have demands of 50, 60, 40, 70, and 30 units. The transportation costs (in $) per unit are as follows. Given an initial basic feasible solution, use the MODI method to test for optimality and find the optimal solution if necessary.

   Cost matrix:
   ```
   To:         S1  S2  S3  S4  S5
   Warehouse1: 4   5   3   6   2
   Warehouse2: 6   4   7   8   5
   Warehouse3: 8   3   5   4   7
   ```
   
   Initial solution:
   Warehouse1→S1: 50, Warehouse1→S5: 30
   Warehouse2→S2: 60, Warehouse2→S3: 40, Warehouse2→S4: 20
   Warehouse3→S4: 50, Warehouse3→S5: 0
   
   Note: This is unbalanced with total supply (270) > total demand (250)

3. An electronics company manufactures components at two plants and ships them to four distribution centers. The plants can produce 300 and 400 units respectively, while the distribution centers require 150, 200, 250, and 100 units. The unit transportation costs (in $) are given in the table below. Given the initial solution using Northwest Corner method, apply the MODI method to check for optimality.

   Cost matrix:
   ```
   To:      D1  D2  D3  D4
   Plant1:  8   6   10  9
   Plant2:  9   12  7   5
   ```
   
   Initial solution:
   Plant1→D1: 150, Plant1→D2: 150
   Plant2→D2: 50, Plant2→D3: 250, Plant2→D4: 100

4. A manufacturing company produces items at four production centers with capacities of 150, 200, 175, and 125 units. These items are to be shipped to three warehouses with requirements of 200, 300, and 100 units. The transportation costs (in $) per unit are given below. An initial feasible solution using Vogel's Approximation Method is provided. Use the MODI method to determine whether this solution is optimal.

   Cost matrix:
   ```
   To:        W1   W2   W3
   Center1:   10   4    11
   Center2:   5    8    9
   Center3:   12   6    7
   Center4:   8    10   6
   ```
   
   Initial solution:
   Center1→W2: 150
   Center2→W1: 200
   Center3→W2: 150, Center3→W3: 25
   Center4→W3: 75, Center4→W2: 0
   
   Note: This is unbalanced with total supply (650) > total demand (600)

5. A company has two suppliers with capacities of 250 and 350 units, and four customers with demands of 150, 200, 100, and 200 units. The transportation costs (in $) per unit are given in the table below. An initial solution using the Least Cost method is provided. Apply the MODI method to test for optimality and improve the solution if possible.

   Cost matrix:
   ```
   To:        C1   C2   C3   C4
   Supplier1: 6    8    10   9
   Supplier2: 12   7    4    5
   ```
   
   Initial solution:
   Supplier1→C1: 150, Supplier1→C2: 100
   Supplier2→C2: 100, Supplier2→C3: 100, Supplier2→C4: 150
   
   Note: This is unbalanced because total supply (600) exceeds total demand (550)