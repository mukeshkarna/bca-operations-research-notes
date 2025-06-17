# JIT Inventory System - Numerical Examples and Calculations

## 1. JIT vs Traditional Inventory Cost Comparison

### Example 1: Manufacturing Company Cost Analysis

A manufacturing company is considering implementing JIT for one of its components. Compare the costs under traditional and JIT systems.

**Given Data:**
- Annual demand: 12,000 units
- Unit cost: $50
- Traditional ordering cost: $200 per order
- JIT setup cost: $50 per delivery (more frequent, smaller orders)
- Traditional holding cost: 25% of unit cost per year
- JIT holding cost: 5% of unit cost per year (much lower inventory)
- Traditional safety stock: 500 units
- JIT safety stock: 50 units

**Solution:**

### Traditional System:
**Step 1:** Calculate EOQ
EOQ = √(2DC₀/Cₕ) = √(2 × 12,000 × 200 / (0.25 × 50)) = √(4,800,000/12.5) = √384,000 = 620 units

**Step 2:** Calculate costs
- Annual ordering cost = (D/EOQ) × C₀ = (12,000/620) × 200 = $3,871
- Average inventory = EOQ/2 + Safety stock = 620/2 + 500 = 810 units
- Annual holding cost = 810 × (0.25 × 50) = 810 × 12.5 = $10,125
- Annual purchase cost = 12,000 × $50 = $600,000
- **Total traditional cost = $600,000 + $3,871 + $10,125 = $613,996**

### JIT System:
**Step 1:** Assume daily deliveries (250 working days)
Order quantity = 12,000/250 = 48 units per delivery

**Step 2:** Calculate costs
- Annual ordering cost = 250 × $50 = $12,500
- Average inventory = 48/2 + 50 = 74 units
- Annual holding cost = 74 × (0.05 × 50) = 74 × 2.5 = $185
- Annual purchase cost = 12,000 × $50 = $600,000
- **Total JIT cost = $600,000 + $12,500 + $185 = $612,685**

**Result:** JIT saves $613,996 - $612,685 = $1,311 annually, plus additional benefits like reduced storage space and improved cash flow.

## 2. Kanban Calculation

### Example 2: Kanban Card Calculation

A production line uses Kanban cards to control material flow. Calculate the number of Kanban cards needed.

**Given Data:**
- Daily demand: 200 units
- Lead time: 2 days
- Safety factor: 10%
- Container size: 50 units

**Formula:**
Number of Kanban cards = (Demand during lead time × (1 + Safety factor)) / Container size

**Solution:**
- Demand during lead time = 200 × 2 = 400 units
- Safety stock = 400 × 0.10 = 40 units
- Total requirement = 400 + 40 = 440 units
- Number of Kanban cards = 440 / 50 = 8.8 ≈ 9 cards

**Answer:** 9 Kanban cards are needed for this production line.

### Example 3: Kanban with Variable Demand

A company experiences variable daily demand for a component used in JIT production.

**Given Data:**
- Average daily demand: 150 units
- Standard deviation of daily demand: 30 units
- Lead time: 3 days
- Service level desired: 95% (Z = 1.65)
- Container size: 25 units

**Solution:**
**Step 1:** Calculate safety stock
Safety stock = Z × σ × √Lead time = 1.65 × 30 × √3 = 1.65 × 30 × 1.73 = 85.6 ≈ 86 units

**Step 2:** Calculate total requirement
Expected demand during lead time = 150 × 3 = 450 units
Total requirement = 450 + 86 = 536 units

**Step 3:** Calculate Kanban cards
Number of cards = 536 / 25 = 21.4 ≈ 22 cards

**Answer:** 22 Kanban cards are required.

## 3. JIT Supplier Delivery Schedule

### Example 4: Optimal Delivery Frequency

A company wants to determine the optimal delivery frequency for JIT implementation.

**Given Data:**
- Annual demand: 24,000 units
- Holding cost: $8 per unit per year
- Delivery cost: $150 per delivery
- Working days per year: 250 days

**Solution:**

**Step 1:** Calculate optimal order quantity (modified EOQ for JIT)
EOQ = √(2DC₀/Cₕ) = √(2 × 24,000 × 150 / 8) = √900,000 = 949 units

**Step 2:** Calculate optimal delivery frequency
Number of deliveries per year = 24,000 / 949 = 25.3 ≈ 25 deliveries

**Step 3:** Calculate delivery schedule
Days between deliveries = 250 / 25 = 10 days

**Answer:** Optimal schedule is one delivery every 10 working days with 960 units per delivery.

## 4. JIT Setup Time and Cost Reduction

### Example 5: Setup Time Reduction Analysis

A company is implementing JIT and needs to reduce setup times to make frequent changeovers economical.

**Current Situation:**
- Setup time: 4 hours
- Setup cost: $200 per hour
- Current batch size: 2,000 units
- Daily demand: 500 units

**Target JIT Situation:**
- Target batch size: 250 units (daily demand × 0.5)
- Same setup cost per hour: $200

**Solution:**

**Step 1:** Calculate current setup cost per unit
Current setup cost = 4 hours × $200 = $800 per setup
Current setup cost per unit = $800 / 2,000 = $0.40 per unit

**Step 2:** Calculate required setup time for JIT
To maintain same setup cost per unit:
Target setup cost per batch = $0.40 × 250 = $100
Required setup time = $100 / $200 per hour = 0.5 hours = 30 minutes

**Step 3:** Setup time reduction needed
Reduction required = 4 hours - 0.5 hours = 3.5 hours (87.5% reduction)

**Answer:** Setup time must be reduced from 4 hours to 30 minutes to make JIT economical.

## 5. JIT Inventory Turnover Analysis

### Example 6: Inventory Turnover Improvement

Compare inventory turnover between traditional and JIT systems.

**Given Data:**
- Annual sales: $2,400,000
- Traditional average inventory: $400,000
- JIT average inventory: $50,000

**Solution:**

**Formula:** Inventory Turnover = Annual Sales / Average Inventory

**Traditional System:**
Inventory Turnover = $2,400,000 / $400,000 = 6 times per year

**JIT System:**
Inventory Turnover = $2,400,000 / $50,000 = 48 times per year

**Improvement:**
- Improvement factor = 48 / 6 = 8 times better
- Additional benefits: Freed up cash = $400,000 - $50,000 = $350,000

**Answer:** JIT improves inventory turnover from 6 to 48 times per year, freeing up $350,000 in working capital.

## 6. JIT Line Balancing Calculation

### Example 7: Production Line Balancing for JIT

A company implements JIT and needs to balance its production line.

**Given Data:**
- Daily demand: 240 units
- Working time per day: 8 hours = 480 minutes
- Number of workstations: 6

**Solution:**

**Step 1:** Calculate takt time
Takt time = Available working time / Customer demand
Takt time = 480 minutes / 240 units = 2 minutes per unit

**Step 2:** Calculate cycle time for each station
For balanced line, each station should complete work in ≤ 2 minutes

**Step 3:** Calculate line efficiency
If actual cycle times are: Station 1: 1.8 min, Station 2: 2.0 min, Station 3: 1.5 min, 
Station 4: 1.9 min, Station 5: 1.7 min, Station 6: 2.0 min

Bottleneck time = 2.0 minutes (stations 2 and 6)
Line efficiency = (Sum of all station times) / (Number of stations × Bottleneck time)
Line efficiency = (1.8 + 2.0 + 1.5 + 1.9 + 1.7 + 2.0) / (6 × 2.0) = 10.9 / 12 = 90.8%

**Answer:** The line is 90.8% efficient with a takt time of 2 minutes per unit.

## 7. JIT Cash Flow Analysis

### Example 8: Cash Flow Improvement with JIT

Calculate the cash flow improvement from implementing JIT.

**Given Data:**
- Average inventory before JIT: $800,000
- Average inventory after JIT: $120,000
- Cost of capital: 12% per year
- Additional JIT implementation costs: $50,000 (one-time)

**Solution:**

**Step 1:** Calculate inventory reduction
Inventory reduction = $800,000 - $120,000 = $680,000

**Step 2:** Calculate annual savings from reduced inventory
Annual savings = Inventory reduction × Cost of capital
Annual savings = $680,000 × 0.12 = $81,600 per year

**Step 3:** Calculate payback period
Payback period = Implementation cost / Annual savings
Payback period = $50,000 / $81,600 = 0.61 years ≈ 7.3 months

**Answer:** JIT implementation pays back in 7.3 months and saves $81,600 annually.

## 8. JIT Quality Cost Analysis

### Example 9: Quality Cost Reduction with JIT

Analyze quality cost improvements with JIT implementation.

**Before JIT:**
- Defect rate: 3%
- Annual production: 100,000 units
- Cost per defective unit: $25
- Inspection cost: $2 per unit

**After JIT:**
- Defect rate: 0.5% (due to immediate detection)
- Annual production: 100,000 units
- Cost per defective unit: $15 (caught earlier)
- Inspection cost: $1.50 per unit (integrated in process)

**Solution:**

**Before JIT:**
- Defective units = 100,000 × 0.03 = 3,000 units
- Defect cost = 3,000 × $25 = $75,000
- Inspection cost = 100,000 × $2 = $200,000
- Total quality cost = $75,000 + $200,000 = $275,000

**After JIT:**
- Defective units = 100,000 × 0.005 = 500 units
- Defect cost = 500 × $15 = $7,500
- Inspection cost = 100,000 × $1.50 = $150,000
- Total quality cost = $7,500 + $150,000 = $157,500

**Savings = $275,000 - $157,500 = $117,500 per year**

**Answer:** JIT reduces quality costs by $117,500 annually (42.7% reduction).

## 10. JIT Supplier Performance Metrics

### Example 10: Supplier Performance Calculation

Calculate supplier performance metrics for JIT implementation.

**Given Data for Supplier A:**
- Total deliveries in month: 20
- On-time deliveries: 19
- Defect-free deliveries: 18
- Complete deliveries (right quantity): 20

**Solution:**

**Step 1:** Calculate On-Time Delivery Rate
On-Time Delivery Rate = (On-time deliveries / Total deliveries) × 100
On-Time Delivery Rate = (19/20) × 100 = 95%

**Step 2:** Calculate Quality Rate
Quality Rate = (Defect-free deliveries / Total deliveries) × 100
Quality Rate = (18/20) × 100 = 90%

**Step 3:** Calculate Fill Rate
Fill Rate = (Complete deliveries / Total deliveries) × 100
Fill Rate = (20/20) × 100 = 100%

**Step 4:** Calculate Overall Supplier Performance
Overall Performance = (On-time Rate + Quality Rate + Fill Rate) / 3
Overall Performance = (95% + 90% + 100%) / 3 = 95%

**Answer:** Supplier A has a 95% overall performance rating. For JIT, suppliers typically need >98% performance.

## Summary of JIT Numerical Applications

1. **Cost Comparison Analysis** - Compare traditional vs JIT costs
2. **Kanban Calculations** - Determine number of cards needed
3. **Delivery Frequency Optimization** - Find optimal delivery schedule
4. **Setup Time Reduction Targets** - Calculate required setup improvements
5. **Inventory Turnover Analysis** - Measure JIT effectiveness
6. **Line Balancing** - Calculate takt time and efficiency
7. **Cash Flow Analysis** - Quantify financial benefits
8. **Quality Cost Analysis** - Measure quality improvements
9. **Supplier Performance Metrics** - Evaluate JIT supplier effectiveness

These numerical examples demonstrate that while JIT is primarily an operational philosophy, there are important quantitative aspects that can be measured and optimized.