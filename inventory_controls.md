# INVENTORY CONTROL - DETAILED NOTES

## 1. Introduction to Inventory Control

Inventory control refers to the process of managing stock levels to minimize costs while ensuring adequate supply to meet demand. It involves deciding:
- What items to stock
- When to place orders
- How much to order
- How to maintain optimal inventory levels

### Real-World Example: 
A retail clothing store must decide how many winter jackets to order for the upcoming season. Order too many, and they'll have unsold inventory taking up storage space; order too few, and they'll miss potential sales. Inventory control helps determine the optimal order quantity.

## 2. Inventory Classification

### 2.1 By Function:
- **Raw Materials**: Materials used in manufacturing (e.g., fabric, buttons for clothing)
- **Work-in-Progress (WIP)**: Partially completed products (e.g., half-assembled furniture)
- **Finished Goods**: Completed products ready for sale (e.g., smartphones in a warehouse)
- **Spare Parts**: Components kept for maintenance (e.g., replacement parts for machinery)
- **Consumables**: Items used in operations but not part of final product (e.g., office supplies)

### 2.2 By Nature:
- **Regular Inventory**: Normal stock for regular operations
- **Safety Stock**: Extra stock maintained to protect against uncertainties
- **Seasonal Inventory**: Stock accumulated for peak demand periods
- **Pipeline Inventory**: Items in transit between locations
- **Decoupling Inventory**: Stock used to separate dependent operations

### 2.3 ABC Analysis:
ABC Analysis categorizes inventory based on annual usage value:
- **A Items**: High-value items (typically 10-20% of items, representing 70-80% of value)
- **B Items**: Medium-value items (typically 30% of items, representing 15-20% of value)
- **C Items**: Low-value items (typically 50-60% of items, representing 5-10% of value)

#### Real-World Example of ABC Analysis:
A hospital pharmacy categorizes its medications:
- **A Items**: Expensive cancer treatments, specialized antibiotics
- **B Items**: Standard antibiotics, pain medications
- **C Items**: Bandages, cotton swabs, inexpensive generic medications

## 3. Costs Associated with Inventory

### 3.1 Ordering Cost (Co):
Costs incurred when placing an order, including:
- Paperwork and administrative costs
- Transportation and delivery charges
- Inspection costs
- Setup costs (for manufactured items)

### 3.2 Holding/Carrying Cost (Ch):
Costs associated with maintaining inventory, including:
- Storage space costs (rent, utilities)
- Insurance
- Taxes
- Handling costs
- Opportunity cost of capital
- Depreciation, obsolescence, and spoilage

### 3.3 Shortage/Stockout Cost:
Costs incurred when demand exceeds supply:
- Lost sales
- Loss of customer goodwill
- Expedited shipping costs
- Production downtime

### 3.4 Purchase Cost:
The actual cost of buying the inventory items.

### Real-World Example:
A coffee shop has the following costs associated with their coffee beans:
- **Ordering Cost**: $50 per order (including shipping and processing)
- **Holding Cost**: $2 per pound per month (including storage and potential spoilage)
- **Shortage Cost**: Estimated at $5 per pound (due to lost sales and customer dissatisfaction)
- **Purchase Cost**: $8 per pound of coffee beans

## 4. Economic Order Quantity (EOQ)

The EOQ model determines the optimal quantity to order that minimizes the total inventory costs.

### 4.1 Assumptions of EOQ Model:
- Demand is known, constant, and uniform
- Lead time is constant
- No quantity discounts
- No shortages allowed
- Order is received all at once

### 4.2 EOQ Formula:
EOQ = √(2DC₀/Cₕ)

Where:
- D = Annual demand
- C₀ = Ordering cost per order
- Cₕ = Holding cost per unit per year

### 4.3 Other Important Formulas:
- **Total Cost**: TC = Purchase Cost + Ordering Cost + Holding Cost
  - TC = DC + D/Q × C₀ + Q/2 × Cₕ

- **Optimal Number of Orders**: N = D/EOQ

- **Optimal Time Between Orders**: T = Working days per year/N

### Numerical Example 1: Basic EOQ Calculation

A bookstore sells 10,000 copies of a popular textbook annually. The ordering cost is $200 per order, and the holding cost is $4 per book per year. What is the optimal order quantity?

**Solution:**
- D = 10,000 books/year
- C₀ = $200/order
- Cₕ = $4/book/year

EOQ = √(2DC₀/Cₕ) = √(2 × 10,000 × 200/4) = √1,000,000 = 1,000 books

Therefore, the bookstore should order 1,000 books at a time.

Number of orders per year = D/EOQ = 10,000/1,000 = 10 orders

Time between orders = 365/10 = 36.5 days (assuming 365 working days)

## 5. Inventory Models with Deterministic Demand

### 5.1 Basic EOQ Model (Fixed Order Quantity)
- Orders placed when inventory reaches reorder point
- Order quantity remains constant
- Suitable when monitoring inventory levels is easy

#### Real-World Example:
A grocery store orders 200 boxes of cereal each time the stock drops to 50 boxes.

### 5.2 Fixed Time Period Model
- Orders placed at fixed time intervals
- Order quantity varies based on consumption
- Suitable when regular inventory reviews are preferred

#### Real-World Example:
A restaurant orders fresh produce every Monday, adjusting quantities based on projected needs.

### 5.3 EOQ with Planned Shortages
- Allows for controlled stockouts to reduce holding costs
- Suitable for non-essential items where stockouts are acceptable

### 5.4 EOQ with Quantity Discounts
- Considers price breaks for larger order quantities
- Evaluates trade-offs between holding costs and purchase cost savings

#### Numerical Example 2: EOQ with Quantity Discounts

A manufacturing company uses 5,000 components annually. The supplier offers the following price structure:
- Less than 500 units: $10 per unit
- 500 to 999 units: $9.50 per unit
- 1,000 or more units: $9 per unit

The ordering cost is $100 per order, and the annual holding cost is 20% of the unit price. Determine the optimal order quantity.

**Solution:**
First, calculate EOQ for each price break:

**For price = $10:**
- Cₕ = 20% × $10 = $2 per unit per year
- EOQ = √(2 × 5,000 × 100/2) = √500,000 = 707 units

**For price = $9.50:**
- Cₕ = 20% × $9.50 = $1.90 per unit per year
- EOQ = √(2 × 5,000 × 100/1.90) = √526,316 = 725 units

**For price = $9:**
- Cₕ = 20% × $9 = $1.80 per unit per year
- EOQ = √(2 × 5,000 × 100/1.80) = √555,556 = 745 units

Now, calculate total annual cost for each price break:

**Case 1: Q = 707 units at $10 per unit**
- Annual purchase cost = 5,000 × $10 = $50,000
- Annual ordering cost = (5,000/707) × $100 = $707
- Annual holding cost = (707/2) × $2 = $707
- Total cost = $50,000 + $707 + $707 = $51,414

**Case 2: Q = 725 units at $9.50 per unit**
- Annual purchase cost = 5,000 × $9.50 = $47,500
- Annual ordering cost = (5,000/725) × $100 = $690
- Annual holding cost = (725/2) × $1.90 = $689
- Total cost = $47,500 + $690 + $689 = $48,879

**Case 3: Q = 1,000 units at $9 per unit** (using 1,000 as minimum for this price break)
- Annual purchase cost = 5,000 × $9 = $45,000
- Annual ordering cost = (5,000/1,000) × $100 = $500
- Annual holding cost = (1,000/2) × $1.80 = $900
- Total cost = $45,000 + $500 + $900 = $46,400

The lowest total cost is $46,400 with an order quantity of 1,000 units.

## 6. ABC Analysis Method

### 6.1 Procedure:
1. List all inventory items with their annual usage value (unit cost × annual usage)
2. Arrange items in descending order of annual usage value
3. Calculate cumulative percentage of items and value
4. Classify items:
   - A items: Top 10-20% of items (70-80% of value)
   - B items: Next 30% of items (15-20% of value)
   - C items: Remaining 50-60% of items (5-10% of value)

### Numerical Example 3: ABC Analysis

A retailer tracks 10 products with the following annual usage data:

| Item | Annual Usage | Unit Cost ($) | Annual Value ($) |
|------|--------------|--------------|-----------------|
| P1   | 1,000        | 100          | 100,000         |
| P2   | 5,000        | 5            | 25,000          |
| P3   | 2,000        | 40           | 80,000          |
| P4   | 10,000       | 2            | 20,000          |
| P5   | 800          | 60           | 48,000          |
| P6   | 300          | 30           | 9,000           |
| P7   | 100          | 90           | 9,000           |
| P8   | 4,000        | 3            | 12,000          |
| P9   | 500          | 8            | 4,000           |
| P10  | 700          | 4            | 2,800           |

**Solution:**
Step 1: Arrange items in descending order of annual value

| Item | Annual Value ($) | % of Total Value | Cumulative % Value |
|------|-----------------|-----------------|-------------------|
| P1   | 100,000         | 32.3%           | 32.3%             |
| P3   | 80,000          | 25.8%           | 58.1%             |
| P5   | 48,000          | 15.5%           | 73.6%             |
| P2   | 25,000          | 8.1%            | 81.7%             |
| P4   | 20,000          | 6.5%            | 88.2%             |
| P8   | 12,000          | 3.9%            | 92.1%             |
| P6   | 9,000           | 2.9%            | 95.0%             |
| P7   | 9,000           | 2.9%            | 97.9%             |
| P9   | 4,000           | 1.3%            | 99.2%             |
| P10  | 2,800           | 0.8%            | 100%              |
| Total| 309,800         | 100%            |                   |

Step 2: Classify items
- A Items (73.6% of value): P1, P3, P5 (30% of items)
- B Items (14.6% of value): P2, P4 (20% of items)
- C Items (11.8% of value): P8, P6, P7, P9, P10 (50% of items)

### 6.2 Control Strategies Based on ABC Classification:

**A Items:**
- Tight control with frequent reviews
- Accurate forecasting and detailed record-keeping
- Special attention from management
- Safety stock calculation with careful consideration

**B Items:**
- Moderate control
- Regular reviews but less frequent than A items
- Use of computerized systems for tracking

**C Items:**
- Simplified control procedures
- Bulk ordering with high safety stocks
- Infrequent reviews
- Simpler forecasting methods

#### Real-World Example:
An electronics retailer applies ABC analysis:
- A Items: High-end smartphones and laptops (strict inventory control, weekly reviews)
- B Items: Mid-range electronics, accessories (monthly reviews)
- C Items: Phone cases, screen protectors, cables (ordered in bulk every quarter)

## 7. Safety Stock and Reorder Point

### 7.1 Safety Stock:
Extra inventory maintained to protect against uncertainties in demand and lead time.

**Formula:**
Safety Stock (SS) = Z × σ × √L

Where:
- Z = Safety factor based on service level
- σ = Standard deviation of demand
- L = Lead time

### 7.2 Reorder Point:
Inventory level at which a new order should be placed.

**Formula:**
Reorder Point (ROP) = Average demand during lead time + Safety stock
                     = d × L + SS

Where:
- d = Average daily demand
- L = Lead time in days
- SS = Safety stock

### Numerical Example 4: Safety Stock and Reorder Point

A retail store sells 50 units of a product per day with a standard deviation of 5 units. The lead time is 6 days. If the store wants a 95% service level (Z = 1.65), calculate the safety stock and reorder point.

**Solution:**
- Average daily demand (d) = 50 units
- Standard deviation of demand (σ) = 5 units
- Lead time (L) = 6 days
- Z = 1.65 (for 95% service level)

Safety Stock (SS) = Z × σ × √L = 1.65 × 5 × √6 = 1.65 × 5 × 2.45 = 20.2 ≈ 20 units

Reorder Point (ROP) = d × L + SS = 50 × 6 + 20 = 300 + 20 = 320 units

Therefore, the store should place a new order when the inventory level reaches 320 units.

## 8. Just-In-Time (JIT) Inventory System

### 8.1 Principles:
- Minimize inventory levels
- Receive goods only when needed
- Reduce waste and inefficiency
- Improve quality and productivity

### 8.2 Benefits:
- Reduced holding costs
- Less warehouse space needed
- Improved cash flow
- Reduced risk of obsolescence
- Faster detection of quality issues

### 8.3 Challenges:
- Requires reliable suppliers
- Vulnerable to supply chain disruptions
- Needs accurate demand forecasting
- Requires efficient communication systems

#### Real-World Example:
Toyota's production system pioneered JIT inventory. Parts arrive at assembly stations just as they're needed, minimizing storage requirements and reducing waste. For this to work, Toyota developed strong supplier relationships and implemented Kanban systems to signal when new parts are needed.

## 9. Economic Production Quantity (EPQ) Model

The EPQ model is an extension of EOQ for companies that produce their own inventory rather than purchasing it.

### 9.1 EPQ Formula:
EPQ = √(2DC₀/Cₕ(1-d/p))

Where:
- D = Annual demand
- C₀ = Setup cost per production run
- Cₕ = Holding cost per unit per year
- d = Daily demand rate
- p = Daily production rate

### Numerical Example 5: EPQ Model

A company produces a component with an annual demand of 12,000 units. The company can produce 100 units per day, and the daily demand is 40 units. The setup cost is $400, and the holding cost is $2 per unit per year. Calculate the economic production quantity.

**Solution:**
- D = 12,000 units/year
- C₀ = $400 per setup
- Cₕ = $2 per unit per year
- d = 40 units/day
- p = 100 units/day

EPQ = √(2DC₀/Cₕ(1-d/p))
    = √(2 × 12,000 × 400 / (2 × (1-40/100)))
    = √(9,600,000 / (2 × 0.6))
    = √(9,600,000 / 1.2)
    = √8,000,000
    = 2,828 units

Therefore, the optimal production quantity is 2,828 units per production run.

## 10. Dynamic Inventory Models

### 10.1 Dynamic EOQ:
Modified EOQ model that accounts for varying demand.

### 10.2 Wagner-Whitin Algorithm:
Dynamic programming approach for determining optimal order quantities when demand varies over time.

#### Real-World Example:
A fashion retailer uses dynamic inventory models to manage seasonal clothing. Demand patterns change throughout the year, requiring different ordering strategies for each season.

## Summary

Effective inventory control is crucial for businesses to minimize costs while ensuring adequate supply. The key concepts include:

1. **Inventory Classification**: Understanding the different types of inventory and using ABC analysis to prioritize control efforts.

2. **Cost Analysis**: Recognizing the various costs associated with inventory management, including ordering, holding, shortage, and purchase costs.

3. **EOQ Model**: Determining the optimal order quantity that minimizes total inventory costs.

4. **Safety Stock and Reorder Point**: Protecting against uncertainties in demand and lead time.

5. **JIT System**: Minimizing inventory levels by receiving goods only when needed.

6. **Dynamic Models**: Adapting inventory strategies to changing demand patterns.

By applying these concepts and techniques, organizations can achieve efficient inventory management, reducing costs while maintaining satisfactory service levels.