# M/M/1 Queuing Theory - Practice Questions

## Key Formulas for M/M/1 Queue:
- **Traffic Intensity (ρ)** = λ/μ (must be < 1 for steady state)
- **Average number in system (L)** = λ/(μ-λ) = ρ/(1-ρ)
- **Average number in queue (Lq)** = λ²/[μ(μ-λ)] = ρ²/(1-ρ)
- **Average time in system (W)** = 1/(μ-λ)
- **Average time in queue (Wq)** = λ/[μ(μ-λ)] = ρ/(μ-ρ)
- **Probability of n customers in system (Pn)** = ρⁿ(1-ρ)
- **Probability system is empty (P0)** = 1-ρ

Where: λ = arrival rate, μ = service rate

---

## **Question 1: Basic M/M/1 Problem**
A bank has a single teller. Customers arrive at an average rate of 20 per hour and the teller can serve customers at an average rate of 25 per hour. Both arrivals and service times follow Poisson and exponential distributions respectively.

Calculate:
a) Traffic intensity
b) Average number of customers in the system
c) Average number of customers waiting in queue
d) Average time a customer spends in the system
e) Average waiting time in queue
f) Probability that the system is empty
g) Probability that there are exactly 3 customers in the system

**Solution:**
- λ = 20 customers/hour, μ = 25 customers/hour
- a) ρ = λ/μ = 20/25 = 0.8
- b) L = ρ/(1-ρ) = 0.8/(1-0.8) = 0.8/0.2 = 4 customers
- c) Lq = ρ²/(1-ρ) = (0.8)²/(1-0.8) = 0.64/0.2 = 3.2 customers
- d) W = 1/(μ-λ) = 1/(25-20) = 1/5 = 0.2 hours = 12 minutes
- e) Wq = ρ/(μ-ρ) = 0.8/(25-20) = 0.8/5 = 0.16 hours = 9.6 minutes
- f) P0 = 1-ρ = 1-0.8 = 0.2 or 20%
- g) P3 = ρ³(1-ρ) = (0.8)³(0.2) = 0.512 × 0.2 = 0.1024 or 10.24%

---

## **Question 2: Service Rate Optimization**
A post office counter serves customers at a rate of 30 per hour. Customers arrive at 24 per hour. The management wants to reduce the average waiting time to 5 minutes. What should be the new service rate?

**Solution:**
Given: λ = 24 customers/hour, Current μ = 30 customers/hour
Required: Wq = 5 minutes = 5/60 = 1/12 hours

Using Wq = λ/[μ(μ-λ)] = 1/12
24/[μ(μ-24)] = 1/12
24 × 12 = μ(μ-24)
288 = μ² - 24μ
μ² - 24μ - 288 = 0

Using quadratic formula: μ = [24 ± √(576 + 1152)]/2 = [24 ± √1728]/2
μ = [24 ± 41.57]/2
Taking positive value: μ = 32.785 ≈ 33 customers/hour

**Answer:** New service rate should be 33 customers/hour

---

## **Question 3: Cost Analysis**
A barbershop has one barber. Customers arrive at 8 per hour and the barber serves 12 customers per hour. The cost of customer waiting is $15 per hour per customer, and the barber's wage is $20 per hour.

Calculate:
a) Total expected cost per hour
b) If a second barber is hired (making it M/M/2), would it be economical? (For M/M/2, use approximate L = 2.4 customers)

**Solution:**
**Part a) M/M/1 System:**
- λ = 8, μ = 12
- ρ = 8/12 = 2/3
- L = ρ/(1-ρ) = (2/3)/(1/3) = 2 customers in system
- Customer waiting cost = L × $15 = 2 × $15 = $30/hour
- Barber cost = $20/hour
- **Total cost = $30 + $20 = $50/hour**

**Part b) M/M/2 System:**
- L = 2.4 customers (given)
- Customer waiting cost = 2.4 × $15 = $36/hour
- Two barbers cost = 2 × $20 = $40/hour
- **Total cost = $36 + $40 = $76/hour**

**Answer:** M/M/1 is more economical ($50/hour vs $76/hour)

---

## **Question 4: Probability Questions**
A gas station has one pump. Cars arrive at 10 per hour and are served at 15 per hour.

Find:
a) Probability that an arriving customer has to wait
b) Probability that there are more than 2 cars at the station
c) Probability that there are between 1 and 3 cars (inclusive)

**Solution:**
- λ = 10, μ = 15, ρ = 10/15 = 2/3

a) P(customer waits) = P(system not empty) = 1 - P0 = 1 - (1-ρ) = ρ = 2/3 = 0.667

b) P(n > 2) = 1 - P(n ≤ 2) = 1 - [P0 + P1 + P2]
   - P0 = 1-ρ = 1/3
   - P1 = ρ(1-ρ) = (2/3)(1/3) = 2/9
   - P2 = ρ²(1-ρ) = (2/3)²(1/3) = 4/27
   - P(n ≤ 2) = 1/3 + 2/9 + 4/27 = 9/27 + 6/27 + 4/27 = 19/27
   - **P(n > 2) = 1 - 19/27 = 8/27 = 0.296**

c) P(1 ≤ n ≤ 3) = P1 + P2 + P3
   - P1 = 2/9, P2 = 4/27
   - P3 = ρ³(1-ρ) = (2/3)³(1/3) = 8/81
   - **P(1 ≤ n ≤ 3) = 2/9 + 4/27 + 8/81 = 18/81 + 12/81 + 8/81 = 38/81 = 0.469**

---

## **Question 5: Break-even Analysis**
A restaurant is considering hiring an additional server. Currently, with one server:
- Customers arrive at 20/hour
- Service rate is 25/hour
- Average customer spends $12
- Customer dissatisfaction cost when waiting = $8/hour per customer in queue

With two servers, the total service rate becomes 50/hour. Should they hire the additional server if the server's wage is $15/hour?

**Solution:**
**Current System (M/M/1):**
- λ = 20, μ = 25, ρ = 0.8
- Lq = ρ²/(1-ρ) = 0.64/0.2 = 3.2 customers
- Dissatisfaction cost = 3.2 × $8 = $25.6/hour
- Server cost = $15/hour (assuming current server wage)
- **Total cost = $25.6 + $15 = $40.6/hour**

**With Additional Server (M/M/2):**
For M/M/2 with λ = 20, μ = 50 (total):
- ρ = 20/50 = 0.4
- For M/M/2: Lq ≈ ρ³/[2(1-ρ)²] = (0.4)³/[2(0.6)²] = 0.064/0.72 = 0.089 customers
- Dissatisfaction cost = 0.089 × $8 = $0.71/hour
- Two servers cost = 2 × $15 = $30/hour
- **Total cost = $0.71 + $30 = $30.71/hour**

**Answer:** Yes, hire the additional server (saves $40.60 - $30.71 = $9.89/hour)

---

---

## **Question 6: Hospital Emergency Room**
A hospital emergency room has one doctor on duty. Patients arrive at an average rate of 8 per hour. The doctor can treat patients at an average rate of 12 per hour. Both arrivals and service times are exponentially distributed.

Calculate:
a) Traffic intensity
b) Average number of patients in the emergency room
c) Average number of patients waiting to be treated
d) Average time a patient spends in the emergency room
e) Average waiting time before treatment
f) Probability that the emergency room is empty
g) Probability that there are exactly 2 patients in the emergency room
h) Probability that there are at least 4 patients in the emergency room

**Solution:**
- λ = 8 patients/hour, μ = 12 patients/hour
- a) ρ = λ/μ = 8/12 = 2/3 ≈ 0.667
- b) L = ρ/(1-ρ) = (2/3)/(1/3) = 2 patients
- c) Lq = ρ²/(1-ρ) = (2/3)²/(1/3) = (4/9)/(1/3) = 4/3 ≈ 1.33 patients
- d) W = 1/(μ-λ) = 1/(12-8) = 1/4 = 0.25 hours = 15 minutes
- e) Wq = ρ/(μ-ρ) = (2/3)/(12-8) = (2/3)/4 = 1/6 ≈ 0.167 hours = 10 minutes
- f) P0 = 1-ρ = 1-(2/3) = 1/3 ≈ 0.333 or 33.33%
- g) P2 = ρ²(1-ρ) = (2/3)²(1/3) = (4/9)(1/3) = 4/27 ≈ 0.148 or 14.8%
- h) P(n ≥ 4) = ρ⁴ = (2/3)⁴ = 16/81 ≈ 0.198 or 19.8%

---

## **Question 7: Supermarket Checkout**
A supermarket has one express checkout lane. Customers arrive at this lane at a rate of 18 per hour. The cashier can serve customers at a rate of 24 per hour. Assume Poisson arrivals and exponential service times.

Calculate:
a) Utilization factor of the cashier
b) Average number of customers in the checkout line (including the one being served)
c) Average number of customers waiting in line
d) Average time a customer spends at the checkout (including service time)
e) Average time a customer waits before being served
f) Probability that an arriving customer finds the system empty
g) Probability that there are exactly 5 customers in the system
h) Probability that there are more than 3 customers in the system

**Solution:**
- λ = 18 customers/hour, μ = 24 customers/hour
- a) ρ = λ/μ = 18/24 = 3/4 = 0.75
- b) L = ρ/(1-ρ) = 0.75/(1-0.75) = 0.75/0.25 = 3 customers
- c) Lq = ρ²/(1-ρ) = (0.75)²/(1-0.75) = 0.5625/0.25 = 2.25 customers
- d) W = 1/(μ-λ) = 1/(24-18) = 1/6 ≈ 0.167 hours = 10 minutes
- e) Wq = ρ/(μ-ρ) = 0.75/(24-18) = 0.75/6 = 0.125 hours = 7.5 minutes
- f) P0 = 1-ρ = 1-0.75 = 0.25 or 25%
- g) P5 = ρ⁵(1-ρ) = (0.75)⁵(0.25) = 0.2373 × 0.25 = 0.0593 or 5.93%
- h) P(n > 3) = ρ⁴ = (0.75)⁴ = 0.3164 or 31.64%

---

## **Question 8: Car Wash Service**
A car wash facility has one automatic washing bay. Cars arrive at an average rate of 15 per hour. The washing process takes an average of 3 minutes per car. Both arrivals and service times follow the appropriate exponential distributions.

Calculate:
a) Service rate per hour
b) Traffic intensity
c) Average number of cars in the system
d) Average number of cars waiting to be washed
e) Average time a car spends at the facility
f) Average waiting time in queue
g) Probability that the facility is idle
h) Probability of exactly 1 car in the system
i) Probability of more than 4 cars in the system

**Solution:**
- λ = 15 cars/hour, Service time = 3 minutes = 3/60 = 0.05 hours
- a) μ = 1/0.05 = 20 cars/hour
- b) ρ = λ/μ = 15/20 = 3/4 = 0.75
- c) L = ρ/(1-ρ) = 0.75/(1-0.75) = 0.75/0.25 = 3 cars
- d) Lq = ρ²/(1-ρ) = (0.75)²/(1-0.75) = 0.5625/0.25 = 2.25 cars
- e) W = 1/(μ-λ) = 1/(20-15) = 1/5 = 0.2 hours = 12 minutes
- f) Wq = ρ/(μ-ρ) = 0.75/(20-15) = 0.75/5 = 0.15 hours = 9 minutes
- g) P0 = 1-ρ = 1-0.75 = 0.25 or 25%
- h) P1 = ρ(1-ρ) = 0.75 × 0.25 = 0.1875 or 18.75%
- i) P(n > 4) = ρ⁵ = (0.75)⁵ = 0.2373 or 23.73%

---

## **Question 9: Coffee Shop Drive-Through**
A coffee shop's drive-through window serves customers at an average rate of 36 per hour. Customers arrive at an average rate of 30 per hour. Both processes follow Poisson and exponential distributions respectively.

Calculate:
a) System utilization
b) Average number of cars in the drive-through system
c) Average number of cars waiting in line
d) Average time a customer spends in the drive-through system
e) Average waiting time before being served
f) Probability that there are no cars in the system
g) Probability that there are exactly 3 cars in the system
h) Probability that a customer has to wait (system is not empty when they arrive)

**Solution:**
- λ = 30 customers/hour, μ = 36 customers/hour
- a) ρ = λ/μ = 30/36 = 5/6 ≈ 0.833
- b) L = ρ/(1-ρ) = (5/6)/(1/6) = 5 cars
- c) Lq = ρ²/(1-ρ) = (5/6)²/(1/6) = (25/36)/(1/6) = 25/6 ≈ 4.17 cars
- d) W = 1/(μ-λ) = 1/(36-30) = 1/6 ≈ 0.167 hours = 10 minutes
- e) Wq = ρ/(μ-ρ) = (5/6)/(36-30) = (5/6)/6 = 5/36 ≈ 0.139 hours = 8.33 minutes
- f) P0 = 1-ρ = 1-(5/6) = 1/6 ≈ 0.167 or 16.67%
- g) P3 = ρ³(1-ρ) = (5/6)³(1/6) = (125/216)(1/6) = 125/1296 ≈ 0.096 or 9.6%
- h) P(wait) = 1-P0 = 1-1/6 = 5/6 ≈ 0.833 or 83.33%

---

## **Question 10: Airline Check-in Counter**
An airline check-in counter serves passengers at a rate of 40 per hour. Passengers arrive at a rate of 32 per hour. Both arrival and service processes are exponentially distributed.

Calculate:
a) Traffic intensity
b) Average number of passengers at the check-in area
c) Average number of passengers waiting in queue
d) Average time a passenger spends at check-in
e) Average waiting time in queue
f) Probability that the counter is free
g) Probability that there are exactly 4 passengers in the system
h) Probability that there are at least 6 passengers in the system
i) What percentage of time is the server busy?

**Solution:**
- λ = 32 passengers/hour, μ = 40 passengers/hour
- a) ρ = λ/μ = 32/40 = 4/5 = 0.8
- b) L = ρ/(1-ρ) = 0.8/(1-0.8) = 0.8/0.2 = 4 passengers
- c) Lq = ρ²/(1-ρ) = (0.8)²/(1-0.8) = 0.64/0.2 = 3.2 passengers
- d) W = 1/(μ-λ) = 1/(40-32) = 1/8 = 0.125 hours = 7.5 minutes
- e) Wq = ρ/(μ-ρ) = 0.8/(40-32) = 0.8/8 = 0.1 hours = 6 minutes
- f) P0 = 1-ρ = 1-0.8 = 0.2 or 20%
- g) P4 = ρ⁴(1-ρ) = (0.8)⁴(0.2) = 0.4096 × 0.2 = 0.08192 or 8.19%
- h) P(n ≥ 6) = ρ⁶ = (0.8)⁶ = 0.2621 or 26.21%
- i) Server busy = ρ = 0.8 or 80% of the time

---

## **Practice Problems (Try These Yourself):**

**Problem A:** A library help desk serves students at 25/hour. Students arrive at 18/hour. Calculate all basic performance measures.

**Problem B:** A pharmacy serves customers at 42/hour. Customers arrive at 35/hour. Find the probability that exactly 2 customers are in the system.

**Problem C:** A service center has arrival rate 16/hour and service rate 20/hour. What is the probability that a customer waits more than 15 minutes?