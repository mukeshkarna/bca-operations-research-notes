# Additional Numerical Examples - Inventory Control

## 5.2 Fixed Time Period Model - Additional Examples

### Example 1: Weekly Review System for a Pharmacy

A pharmacy reviews its inventory of a particular medicine every week (7 days). The average daily demand is 20 units with a standard deviation of 4 units. The lead time for receiving new stock is 3 days. The pharmacy wants to maintain a 90% service level (Z = 1.28).

**Given:**
- Review period (R) = 7 days
- Average daily demand (d) = 20 units
- Standard deviation of daily demand (σd) = 4 units
- Lead time (L) = 3 days
- Service level = 90% (Z = 1.28)
- Current inventory on hand = 50 units

**Solution:**

**Step 1:** Calculate expected demand during review period + lead time
Expected demand = d × (R + L) = 20 × (7 + 3) = 200 units

**Step 2:** Calculate safety stock
Standard deviation during (R + L) = σd × √(R + L) = 4 × √10 = 4 × 3.16 = 12.64 units
Safety stock = Z × σ(R+L) = 1.28 × 12.64 = 16.18 ≈ 16 units

**Step 3:** Calculate target inventory level (S)
S = Expected demand during (R + L) + Safety stock = 200 + 16 = 216 units

**Step 4:** Determine order quantity
Order quantity = S - Current inventory = 216 - 50 = 166 units

**Answer:** The pharmacy should order 166 units this week.

### Example 2: Monthly Review System for Office Supplies

An office manages its paper supply using a monthly review system. Historical data shows:
- Monthly demand: 500 reams (average)
- Standard deviation of monthly demand: 80 reams
- Lead time: 10 days (0.33 months)
- Desired service level: 95% (Z = 1.65)
- Current stock: 200 reams

**Solution:**

**Step 1:** Calculate expected demand during review period + lead time
Review period (R) = 1 month
Lead time (L) = 0.33 months
Expected demand = 500 × (1 + 0.33) = 500 × 1.33 = 665 reams

**Step 2:** Calculate safety stock
Standard deviation during (R + L) = 80 × √1.33 = 80 × 1.15 = 92 reams
Safety stock = 1.65 × 92 = 151.8 ≈ 152 reams

**Step 3:** Calculate target inventory level
S = 665 + 152 = 817 reams

**Step 4:** Determine order quantity
Order quantity = 817 - 200 = 617 reams

**Answer:** The office should order 617 reams of paper.

### Example 3: Seasonal Review System for Ice Cream Shop

An ice cream shop reviews its vanilla ice cream inventory every 2 weeks during summer. The demand varies significantly:
- Average daily demand: 15 gallons
- Standard deviation: 6 gallons
- Lead time: 4 days
- Service level: 98% (Z = 2.05)
- Current inventory: 40 gallons

**Solution:**

**Step 1:** Expected demand during review period + lead time
Expected demand = 15 × (14 + 4) = 15 × 18 = 270 gallons

**Step 2:** Safety stock calculation
Standard deviation during (R + L) = 6 × √18 = 6 × 4.24 = 25.44 gallons
Safety stock = 2.05 × 25.44 = 52.15 ≈ 52 gallons

**Step 3:** Target inventory level
S = 270 + 52 = 322 gallons

**Step 4:** Order quantity
Order quantity = 322 - 40 = 282 gallons

**Answer:** The ice cream shop should order 282 gallons of vanilla ice cream.

## 5.3 EOQ with Planned Shortages - Additional Examples

### Example 1: Electronics Store Backorder System

An electronics store sells 3,600 gaming consoles annually. The store allows backorders (planned shortages) for this item to reduce inventory costs.

**Given:**
- Annual demand (D) = 3,600 units
- Ordering cost (Co) = $150 per order
- Holding cost (Ch) = $20 per unit per year
- Shortage cost (Cs) = $8 per unit per year

**Solution:**

**Step 1:** Calculate optimal order quantity with shortages
Q* = √(2DCo/Ch) × √((Ch + Cs)/Cs)
Q* = √(2 × 3,600 × 150/20) × √((20 + 8)/8)
Q* = √54,000 × √(28/8)
Q* = 232.38 × √3.5
Q* = 232.38 × 1.87 = 434.5 ≈ 435 units

**Step 2:** Calculate maximum shortage level
S* = Q* × (Ch/(Ch + Cs))
S* = 435 × (20/(20 + 8))
S* = 435 × (20/28)
S* = 435 × 0.714 = 310.6 ≈ 311 units

**Step 3:** Calculate maximum inventory level
I* = Q* - S* = 435 - 311 = 124 units

**Step 4:** Calculate total annual cost
TC = √(2DCoCh) × √(Cs/(Ch + Cs))
TC = √(2 × 3,600 × 150 × 20) × √(8/(20 + 8))
TC = √21,600,000 × √(8/28)
TC = 4,648 × 0.535 = $2,487

**Answer:** 
- Optimal order quantity: 435 units
- Maximum shortage: 311 units
- Maximum inventory: 124 units
- Total annual cost: $2,487

### Example 2: Auto Parts Store with Planned Shortages

An auto parts store sells 2,400 brake pads annually and allows customers to backorder this item.

**Given:**
- Annual demand (D) = 2,400 units
- Ordering cost (Co) = $80 per order
- Holding cost (Ch) = $12 per unit per year
- Shortage cost (Cs) = $15 per unit per year

**Solution:**

**Step 1:** Optimal order quantity
Q* = √(2 × 2,400 × 80/12) × √((12 + 15)/15)
Q* = √32,000 × √(27/15)
Q* = 178.9 × √1.8
Q* = 178.9 × 1.34 = 239.7 ≈ 240 units

**Step 2:** Maximum shortage level
S* = 240 × (12/(12 + 15)) = 240 × (12/27) = 240 × 0.444 = 106.7 ≈ 107 units

**Step 3:** Maximum inventory level
I* = 240 - 107 = 133 units

**Step 4:** Time analysis
- Time with positive inventory = (I*/D) × 365 = (133/2,400) × 365 = 20.2 days
- Time with shortages = (S*/D) × 365 = (107/2,400) × 365 = 16.3 days
- Total cycle time = (Q*/D) × 365 = (240/2,400) × 365 = 36.5 days

**Answer:**
- Order 240 units when shortage reaches 107 units
- Maximum inventory will be 133 units
- Store will be out of stock for 16.3 days per cycle

### Example 3: Furniture Store Planned Shortage Model

A furniture store sells 1,800 dining sets per year and uses a planned shortage policy.

**Given:**
- Annual demand (D) = 1,800 units
- Ordering cost (Co) = $200 per order
- Holding cost (Ch) = $50 per unit per year
- Shortage cost (Cs) = $30 per unit per year

**Solution:**

**Step 1:** Optimal order quantity
Q* = √(2 × 1,800 × 200/50) × √((50 + 30)/30)
Q* = √14,400 × √(80/30)
Q* = 120 × √2.67
Q* = 120 × 1.63 = 195.6 ≈ 196 units

**Step 2:** Maximum shortage level
S* = 196 × (50/(50 + 30)) = 196 × (50/80) = 196 × 0.625 = 122.5 ≈ 123 units

**Step 3:** Maximum inventory level
I* = 196 - 123 = 73 units

**Step 4:** Cost comparison with regular EOQ
Regular EOQ = √(2 × 1,800 × 200/50) = √14,400 = 120 units
Regular EOQ total cost = √(2 × 1,800 × 200 × 50) = √36,000,000 = $6,000

Planned shortage total cost = √(2 × 1,800 × 200 × 50) × √(30/(50 + 30))
= 6,000 × √(30/80) = 6,000 × 0.612 = $3,672

**Savings = $6,000 - $3,672 = $2,328 per year**

**Answer:** The planned shortage model saves $2,328 annually compared to regular EOQ.

## ABC Analysis - Additional Examples

### Example 1: Restaurant ABC Analysis

A restaurant analyzes its 15 key ingredients for ABC classification:

| Item | Annual Usage (kg) | Cost per kg ($) | Annual Value ($) |
|------|------------------|----------------|-----------------|
| Beef | 2,000 | 25 | 50,000 |
| Salmon | 800 | 35 | 28,000 |
| Chicken | 3,000 | 8 | 24,000 |
| Lobster | 200 | 60 | 12,000 |
| Pork | 1,500 | 7 | 10,500 |
| Shrimp | 600 | 15 | 9,000 |
| Flour | 5,000 | 1.5 | 7,500 |
| Cheese | 1,000 | 6 | 6,000 |
| Tomatoes | 2,500 | 2 | 5,000 |
| Potatoes | 4,000 | 1 | 4,000 |
| Rice | 2,000 | 1.8 | 3,600 |
| Onions | 3,000 | 0.8 | 2,400 |
| Oil | 800 | 2.5 | 2,000 |
| Salt | 1,000 | 0.5 | 500 |
| Pepper | 100 | 4 | 400 |

**Solution:**

**Step 1:** Arrange in descending order of annual value

| Rank | Item | Annual Value ($) | % of Total | Cumulative % | Items % | Cumulative Items % |
|------|------|-----------------|------------|--------------|---------|-------------------|
| 1 | Beef | 50,000 | 30.3% | 30.3% | 6.7% | 6.7% |
| 2 | Salmon | 28,000 | 17.0% | 47.3% | 6.7% | 13.3% |
| 3 | Chicken | 24,000 | 14.5% | 61.8% | 6.7% | 20.0% |
| 4 | Lobster | 12,000 | 7.3% | 69.1% | 6.7% | 26.7% |
| 5 | Pork | 10,500 | 6.4% | 75.5% | 6.7% | 33.3% |
| 6 | Shrimp | 9,000 | 5.5% | 81.0% | 6.7% | 40.0% |
| 7 | Flour | 7,500 | 4.5% | 85.5% | 6.7% | 46.7% |
| 8 | Cheese | 6,000 | 3.6% | 89.1% | 6.7% | 53.3% |
| 9 | Tomatoes | 5,000 | 3.0% | 92.1% | 6.7% | 60.0% |
| 10 | Potatoes | 4,000 | 2.4% | 94.5% | 6.7% | 66.7% |
| 11 | Rice | 3,600 | 2.2% | 96.7% | 6.7% | 73.3% |
| 12 | Onions | 2,400 | 1.5% | 98.2% | 6.7% | 80.0% |
| 13 | Oil | 2,000 | 1.2% | 99.4% | 6.7% | 86.7% |
| 14 | Salt | 500 | 0.3% | 99.7% | 6.7% | 93.3% |
| 15 | Pepper | 400 | 0.2% | 100% | 6.7% | 100% |

**Total Value: $164,900**

**Step 2:** Classification
- **A Items (75.5% of value):** Beef, Salmon, Chicken, Lobster, Pork (33.3% of items)
- **B Items (13.6% of value):** Shrimp, Flour, Cheese, Tomatoes (26.7% of items)
- **C Items (10.9% of value):** Potatoes, Rice, Onions, Oil, Salt, Pepper (40.0% of items)

**Management Strategy:**
- **A Items:** Daily inventory checks, precise forecasting, multiple suppliers
- **B Items:** Weekly reviews, moderate safety stock
- **C Items:** Monthly bulk orders, high safety stock, simple reorder systems

### Example 2: Hospital Pharmacy ABC Analysis

A hospital pharmacy analyzes 20 medications for inventory control:

| Medicine | Annual Usage (units) | Cost per unit ($) | Annual Value ($) |
|----------|---------------------|------------------|-----------------|
| Insulin | 10,000 | 45 | 450,000 |
| Antibiotics-A | 5,000 | 60 | 300,000 |
| Cancer Drug-X | 500 | 400 | 200,000 |
| Heart Medicine | 8,000 | 20 | 160,000 |
| Pain Killer-A | 15,000 | 8 | 120,000 |
| Antibiotics-B | 12,000 | 9 | 108,000 |
| Blood Thinner | 6,000 | 15 | 90,000 |
| Diabetes Med | 20,000 | 4 | 80,000 |
| Vitamins | 50,000 | 1.5 | 75,000 |
| Anti-inflammatory | 25,000 | 2.5 | 62,500 |
| Cough Syrup | 8,000 | 6 | 48,000 |
| Antacid | 30,000 | 1.2 | 36,000 |
| Eye Drops | 5,000 | 7 | 35,000 |
| Skin Cream | 10,000 | 3 | 30,000 |
| Allergy Med | 6,000 | 4.5 | 27,000 |
| Sleep Aid | 4,000 | 5 | 20,000 |
| Laxative | 8,000 | 2 | 16,000 |
| Throat Lozenges | 20,000 | 0.75 | 15,000 |
| Bandages | 100,000 | 0.1 | 10,000 |
| Cotton Swabs | 200,000 | 0.02 | 4,000 |

**Total Annual Value: $1,986,500**

**Solution:**

After arranging in descending order and calculating percentages:

**Classification:**
- **A Items (70.8% of value, 20% of items):** Insulin, Antibiotics-A, Cancer Drug-X, Heart Medicine
- **B Items (20.7% of value, 30% of items):** Pain Killer-A, Antibiotics-B, Blood Thinner, Diabetes Med, Vitamins, Anti-inflammatory
- **C Items (8.5% of value, 50% of items):** Remaining 10 items

**Control Strategy:**
- **A Items:** 
  - Daily monitoring
  - Automated reorder systems
  - Multiple suppliers for critical items
  - Cold storage requirements (insulin)
  - Expiry date tracking

- **B Items:**
  - Weekly inventory reviews
  - Standard safety stock levels
  - Regular supplier evaluations

- **C Items:**
  - Monthly bulk orders
  - High safety stock (3-6 months supply)
  - Simple min-max inventory systems

### Example 3: Manufacturing Company ABC Analysis

A manufacturing company analyzes 25 raw materials and components:

| Component | Annual Usage | Unit Cost ($) | Annual Value ($) |
|-----------|-------------|--------------|-----------------|
| Steel Sheets | 50,000 | 120 | 6,000,000 |
| Electric Motors | 5,000 | 800 | 4,000,000 |
| Control Panels | 5,000 | 600 | 3,000,000 |
| Copper Wire | 100,000 | 25 | 2,500,000 |
| Aluminum Bars | 30,000 | 60 | 1,800,000 |
| Hydraulic Pumps | 2,000 | 750 | 1,500,000 |
| Bearings | 20,000 | 50 | 1,000,000 |
| Rubber Seals | 80,000 | 12 | 960,000 |
| Welding Rods | 40,000 | 20 | 800,000 |
| Paint | 10,000 | 75 | 750,000 |
| Bolts | 200,000 | 3 | 600,000 |
| Gaskets | 50,000 | 10 | 500,000 |
| Filters | 15,000 | 30 | 450,000 |
| Lubricants | 5,000 | 80 | 400,000 |
| Springs | 25,000 | 15 | 375,000 |
| Plastic Parts | 100,000 | 3.5 | 350,000 |
| Screws | 500,000 | 0.6 | 300,000 |
| Washers | 300,000 | 0.8 | 240,000 |
| Electrical Wire | 50,000 | 4 | 200,000 |
| Insulation | 20,000 | 8 | 160,000 |
| Adhesive | 8,000 | 18 | 144,000 |
| Safety Glasses | 2,000 | 45 | 90,000 |
| Gloves | 10,000 | 5 | 50,000 |
| Labels | 100,000 | 0.3 | 30,000 |
| Cleaning Cloth | 5,000 | 2 | 10,000 |

**Total Annual Value: $26,244,000**

**Classification Results:**
- **A Items (80.1% of value, 28% of items):** Steel Sheets, Electric Motors, Control Panels, Copper Wire, Aluminum Bars, Hydraulic Pumps, Bearings
- **B Items (12.4% of value, 32% of items):** Rubber Seals, Welding Rods, Paint, Bolts, Gaskets, Filters, Lubricants, Springs
- **C Items (7.5% of value, 40% of items):** Remaining 10 items

**Inventory Management Strategy:**

**A Items:**
- JIT delivery arrangements with suppliers
- Weekly inventory reviews with management approval for orders
- Multiple supplier sources for risk mitigation
- Precise demand forecasting
- Low safety stock (5-10 days supply)

**B Items:**
- Bi-weekly inventory reviews
- Moderate safety stock (2-3 weeks supply)
- Quarterly supplier performance reviews
- Standard reorder procedures

**C Items:**
- Monthly or quarterly bulk orders
- High safety stock (2-3 months supply)
- Annual supplier negotiations
- Simplified procurement procedures
- Focus on cost minimization rather than service level

**Key Insights:**
1. 28% of items account for over 80% of inventory value
2. Steel sheets alone represent 22.9% of total inventory value
3. Bottom 40% of items represent only 7.5% of inventory value
4. Significant cost savings possible through differentiated control strategies