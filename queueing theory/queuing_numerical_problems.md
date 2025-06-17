# QUEUING THEORY - NUMERICAL PROBLEMS WITH SOLUTIONS

## TOPIC 1: BASIC QUEUING CONCEPTS AND LITTLE'S LAW

### Problem 1.1: Basic Relationships
A service system has the following observed data over a period:
- Average number of customers in the system: 8 customers
- Average arrival rate: 12 customers per hour
- Average service rate: 15 customers per hour

Calculate:
a) Average time a customer spends in the system
b) Average time a customer waits in the queue
c) Average number of customers waiting in the queue

**Solution:**

Given:
- L = 8 customers
- λ = 12 customers/hour
- μ = 15 customers/hour

a) Average time in system using Little's Law:
   W = L/λ = 8/12 = 0.667 hours = 40 minutes

b) Average time waiting in queue:
   W_q = W - 1/μ = 0.667 - 1/15 = 0.667 - 0.067 = 0.6 hours = 36 minutes

c) Average number waiting in queue using Little's Law:
   L_q = λ × W_q = 12 × 0.6 = 7.2 customers

### Problem 1.2: Traffic Intensity
A single-server system has:
- Customers arrive at 8 per hour
- Server can handle 10 customers per hour

Calculate:
a) Traffic intensity
b) Server utilization
c) Is the system stable?

**Solution:**

Given:
- λ = 8 customers/hour
- μ = 10 customers/hour

a) Traffic intensity:
   ρ = λ/μ = 8/10 = 0.8

b) Server utilization:
   U = ρ = 0.8 = 80%

c) System stability:
   Since ρ = 0.8 < 1, the system is stable.

---

## TOPIC 2: M/M/1 QUEUING MODEL (SINGLE SERVER)

### Problem 2.1: Complete M/M/1 Analysis
A small grocery store has one checkout counter. Customers arrive according to a Poisson distribution at a rate of 20 per hour. The checkout time follows an exponential distribution with a mean of 2.5 minutes.

Calculate:
a) Traffic intensity
b) Probability that the system is empty
c) Probability that there are exactly 3 customers in the system
d) Average number of customers in the system
e) Average number of customers waiting in the queue
f) Average time a customer spends in the system
g) Average waiting time in the queue
h) Probability that a customer waits more than 5 minutes in the queue

**Solution:**

Given:
- λ = 20 customers/hour
- Service time = 2.5 minutes = 2.5/60 hours
- μ = 1/(2.5/60) = 24 customers/hour

a) Traffic intensity:
   ρ = λ/μ = 20/24 = 0.833

b) Probability system is empty:
   P₀ = 1 - ρ = 1 - 0.833 = 0.167 or 16.7%

c) Probability of exactly 3 customers:
   P₃ = (1-ρ)ρ³ = 0.167 × (0.833)³ = 0.167 × 0.578 = 0.096 or 9.6%

d) Average number in system:
   L = ρ/(1-ρ) = 0.833/(1-0.833) = 0.833/0.167 = 5 customers

e) Average number waiting in queue:
   L_q = ρ²/(1-ρ) = (0.833)²/(1-0.833) = 0.694/0.167 = 4.16 customers

f) Average time in system:
   W = 1/(μ-λ) = 1/(24-20) = 1/4 = 0.25 hours = 15 minutes

g) Average waiting time in queue:
   W_q = λ/[μ(μ-λ)] = 20/[24(24-20)] = 20/96 = 0.208 hours = 12.5 minutes

h) Probability of waiting more than 5 minutes in queue:
   P(W_q > 5 minutes) = P(W_q > 1/12 hours) = ρe^(-μ(1-ρ)t)
   = 0.833 × e^(-24×0.167×1/12) = 0.833 × e^(-0.334) = 0.833 × 0.716 = 0.596 or 59.6%

### Problem 2.2: M/M/1 System Design
A bank wants to install an ATM. Expected customers arrive at 25 per hour (Poisson). The bank is considering two ATM models:
- Model A: Service rate = 30 customers/hour, Cost = $50,000
- Model B: Service rate = 40 customers/hour, Cost = $75,000

The bank estimates that each minute of customer waiting costs $2 in lost goodwill. Which ATM should they choose if they operate 12 hours per day, 365 days per year?

**Solution:**

Given:
- λ = 25 customers/hour
- Operating hours = 12 × 365 = 4,380 hours/year
- Waiting cost = $2/minute = $120/hour per customer

**For Model A (μ = 30):**
- ρ = 25/30 = 0.833
- W_q = λ/[μ(μ-λ)] = 25/[30(30-25)] = 25/150 = 0.167 hours per customer
- Total customers per year = 25 × 4,380 = 109,500
- Annual waiting cost = 109,500 × 0.167 × $120 = $2,194,600
- Total cost = $50,000 + $2,194,600 = $2,244,600

**For Model B (μ = 40):**
- ρ = 25/40 = 0.625
- W_q = λ/[μ(μ-λ)] = 25/[40(40-25)] = 25/600 = 0.0417 hours per customer
- Annual waiting cost = 109,500 × 0.0417 × $120 = $547,614
- Total cost = $75,000 + $547,614 = $622,614

**Decision:** Choose Model B as it has lower total cost ($622,614 vs $2,244,600).

---

## TOPIC 3: M/M/c QUEUING MODEL (MULTIPLE SERVERS)

### Problem 3.1: M/M/2 System
A service center has 2 identical servers. Customers arrive according to a Poisson process at a rate of 16 per hour. Each server can handle customers at a rate of 10 per hour (exponentially distributed).

Calculate:
a) Traffic intensity
b) Probability that the system is empty
c) Probability that both servers are busy
d) Average number of customers in the system
e) Average waiting time in the queue
f) Probability that an arriving customer has to wait

**Solution:**

Given:
- λ = 16 customers/hour
- μ = 10 customers/hour per server
- c = 2 servers

a) Traffic intensity:
   ρ = λ/(cμ) = 16/(2×10) = 16/20 = 0.8

b) Probability system is empty:
   For M/M/c: P₀ = [Σ(n=0 to c-1) (λ/μ)ⁿ/n! + (λ/μ)ᶜ/(c!(1-ρ))]⁻¹
   
   λ/μ = 16/10 = 1.6
   P₀ = [1.6⁰/0! + 1.6¹/1! + (1.6)²/(2!(1-0.8))]⁻¹
   P₀ = [1 + 1.6 + 2.56/(2×0.2)]⁻¹
   P₀ = [1 + 1.6 + 6.4]⁻¹ = [9]⁻¹ = 0.111 or 11.1%

c) Probability both servers are busy:
   P(n ≥ 2) = 1 - P₀ - P₁
   P₁ = (λ/μ)¹/1! × P₀ = 1.6 × 0.111 = 0.178
   P(n ≥ 2) = 1 - 0.111 - 0.178 = 0.711 or 71.1%

d) Average number in system:
   First calculate L_q:
   L_q = P₀(λ/μ)ᶜρ/[c!(1-ρ)²] = 0.111 × (1.6)² × 0.8/[2 × (0.2)²]
   L_q = 0.111 × 2.56 × 0.8/(2 × 0.04) = 0.228/0.08 = 2.84 customers
   
   L = L_q + λ/μ = 2.84 + 1.6 = 4.44 customers

e) Average waiting time in queue:
   W_q = L_q/λ = 2.84/16 = 0.178 hours = 10.67 minutes

f) Probability of waiting:
   P(wait) = (λ/μ)ᶜ/(c!(1-ρ)) × P₀ = (1.6)²/(2×0.2) × 0.111 = 2.56/0.4 × 0.111 = 0.711 or 71.1%

### Problem 3.2: Optimal Number of Servers
A post office needs to determine the optimal number of clerks. Customers arrive at 30 per hour (Poisson). Each clerk serves at 12 customers per hour (exponential). Each clerk costs $25/hour. Customer waiting time is valued at $20/hour per customer.

Compare the total costs for 2, 3, and 4 clerks and recommend the optimal number.

**Solution:**

Given:
- λ = 30 customers/hour
- μ = 12 customers/hour per clerk
- Clerk cost = $25/hour
- Waiting cost = $20/hour per customer

**For c = 2 clerks:**
- ρ = 30/(2×12) = 1.25 > 1 → System is unstable (Not feasible)

**For c = 3 clerks:**
- ρ = 30/(3×12) = 30/36 = 0.833
- P₀ calculation: λ/μ = 30/12 = 2.5
- P₀ = [2.5⁰/0! + 2.5¹/1! + (2.5)²/2! + (2.5)³/(3!(1-0.833))]⁻¹
- P₀ = [1 + 2.5 + 3.125 + 15.625/(6×0.167)]⁻¹
- P₀ = [1 + 2.5 + 3.125 + 15.625]⁻¹ = [22.25]⁻¹ = 0.045

- L_q = 0.045 × (2.5)³ × 0.833/[6 × (0.167)²] = 0.045 × 15.625 × 0.833/0.167 = 3.47 customers
- W_q = L_q/λ = 3.47/30 = 0.116 hours

- Total cost = 3×$25 + 30×0.116×$20 = $75 + $69.6 = $144.6/hour

**For c = 4 clerks:**
- ρ = 30/(4×12) = 30/48 = 0.625
- Following similar calculations: P₀ ≈ 0.070, L_q ≈ 0.95 customers
- W_q = 0.95/30 = 0.032 hours
- Total cost = 4×$25 + 30×0.032×$20 = $100 + $19.2 = $119.2/hour

**Decision:** Use 4 clerks (lowest total cost of $119.2/hour).

---

## TOPIC 4: M/M/1/K QUEUING MODEL (LIMITED CAPACITY)

### Problem 4.1: Barbershop with Limited Capacity
A barbershop has one barber and can accommodate a maximum of 5 customers (including the one being served). Customers arrive at 8 per hour (Poisson) and service time is exponentially distributed with mean 20 minutes.

Calculate:
a) Probability that the shop is full
b) Effective arrival rate
c) Average number of customers in the shop
d) Probability that an arriving customer is turned away
e) Average time a customer spends in the shop

**Solution:**

Given:
- λ = 8 customers/hour
- μ = 60/20 = 3 customers/hour
- K = 5 (maximum capacity)
- ρ = λ/μ = 8/3 = 2.667

a) Probability shop is full:
   For M/M/1/K when ρ ≠ 1:
   P_K = P₅ = (1-ρ)ρᴷ/(1-ρᴷ⁺¹)
   P₅ = (1-2.667)(2.667)⁵/(1-(2.667)⁶)
   P₅ = (-1.667)(142.23)/(1-759.12)
   P₅ = -237.06/(-758.12) = 0.313 or 31.3%

b) Effective arrival rate:
   λ_eff = λ(1-P_K) = 8(1-0.313) = 8(0.687) = 5.496 customers/hour

c) Average number in shop:
   L = ρ[1-(K+1)ρᴷ+Kρᴷ⁺¹]/[(1-ρ)(1-ρᴷ⁺¹)]
   L = 2.667[1-6(2.667)⁵+5(2.667)⁶]/[(1-2.667)(1-(2.667)⁶)]
   L = 2.667[1-6(142.23)+5(379.27)]/[(-1.667)(-758.12)]
   L = 2.667[1-853.38+1896.35]/1264.29
   L = 2.667(1043.97)/1264.29 = 2.202 customers

d) Probability of being turned away:
   Same as probability shop is full = 31.3%

e) Average time in shop:
   W = L/λ_eff = 2.202/5.496 = 0.401 hours = 24.06 minutes

### Problem 4.2: Computer System with Buffer
A computer system can process jobs at 20 per hour (exponential). Jobs arrive at 25 per hour (Poisson). The system buffer can hold at most 8 jobs (including the one being processed).

Calculate:
a) System utilization
b) Probability of job rejection
c) Throughput of the system
d) Average response time

**Solution:**

Given:
- λ = 25 jobs/hour
- μ = 20 jobs/hour
- K = 8
- ρ = λ/μ = 25/20 = 1.25

a) System utilization:
   First calculate P₀:
   For ρ ≠ 1: P₀ = (1-ρ)/(1-ρᴷ⁺¹) = (1-1.25)/(1-(1.25)⁹) = -0.25/(1-7.45) = -0.25/(-6.45) = 0.039
   
   Utilization = 1 - P₀ = 1 - 0.039 = 0.961 or 96.1%

b) Probability of job rejection:
   P_rejection = P₈ = P₀ρᴷ = 0.039 × (1.25)⁸ = 0.039 × 5.96 = 0.232 or 23.2%

c) Throughput:
   λ_eff = λ(1-P₈) = 25(1-0.232) = 25(0.768) = 19.2 jobs/hour

d) Average response time:
   L = ρ(1-(K+1)ρᴷ+Kρᴷ⁺¹)/[(1-ρ)(1-ρᴷ⁺¹)]
   L = 1.25[1-9(1.25)⁸+8(1.25)⁹]/[(-0.25)(-6.45)]
   L = 1.25[1-53.64+59.6]/1.6125 = 1.25(6.96)/1.6125 = 5.39 jobs
   
   W = L/λ_eff = 5.39/19.2 = 0.281 hours = 16.86 minutes

---

## TOPIC 5: M/M/c/K QUEUING MODEL

### Problem 5.1: Multi-Server Limited Capacity
A call center has 3 operators and can handle at most 10 calls in the system (including those being served). Calls arrive at 15 per hour (Poisson) and each operator handles calls at 6 per hour (exponential).

Calculate:
a) Traffic intensity
b) Probability that all operators are busy
c) Probability that the system is full
d) Average number of calls in the system

**Solution:**

Given:
- λ = 15 calls/hour
- μ = 6 calls/hour per operator
- c = 3 operators
- K = 10
- ρ = λ/(cμ) = 15/(3×6) = 15/18 = 0.833

a) Traffic intensity: ρ = 0.833

b&c) For M/M/c/K, we need to calculate probabilities:
   
   Let r = λ/μ = 15/6 = 2.5
   
   For n ≤ c: P_n = (rⁿ/n!)P₀
   For c < n ≤ K: P_n = (rⁿ/(c!cⁿ⁻ᶜ))P₀
   
   P₀ = [Σ(n=0 to c) rⁿ/n! + Σ(n=c+1 to K) rⁿ/(c!cⁿ⁻ᶜ)]⁻¹
   
   P₀ = [2.5⁰/0! + 2.5¹/1! + 2.5²/2! + 2.5³/3! + Σ(n=4 to 10) (2.5)ⁿ/(6×3ⁿ⁻³)]⁻¹
   
   After calculations: P₀ ≈ 0.065
   
   P(all busy) = P(n ≥ 3) = 1 - P₀ - P₁ - P₂
   P₁ = 2.5 × 0.065 = 0.163
   P₂ = (2.5)²/2 × 0.065 = 0.203
   P(all busy) = 1 - 0.065 - 0.163 - 0.203 = 0.569 or 56.9%
   
   P₁₀ = (2.5)¹⁰/(6×3⁷) × 0.065 ≈ 0.024 or 2.4%

d) Average number in system requires summing nP_n for all states, which yields approximately L ≈ 4.2 calls.

---

## TOPIC 6: M/G/1 QUEUING MODEL

### Problem 6.1: General Service Time Distribution
A single-server system has Poisson arrivals at 10 per hour. Service times follow a general distribution with mean 4 minutes and standard deviation 2 minutes.

Calculate:
a) Traffic intensity
b) Average number of customers waiting in queue
c) Average waiting time in queue
d) Average number in system

**Solution:**

Given:
- λ = 10 customers/hour
- Mean service time = 4 minutes = 1/15 hour → μ = 15 customers/hour
- Standard deviation = 2 minutes = 1/30 hour → σ = 1/30 hour
- Variance σ² = (1/30)² = 1/900 hour²

a) Traffic intensity:
   ρ = λ/μ = 10/15 = 0.667

b) Average number waiting (Pollaczek-Khinchin formula):
   L_q = λ²σ² + ρ²/[2(1-ρ)]
   L_q = (10)²(1/900) + (0.667)²/[2(1-0.667)]
   L_q = 100/900 + 0.445/0.666 = 0.111 + 0.668 = 0.779 customers

c) Average waiting time:
   W_q = L_q/λ = 0.779/10 = 0.078 hours = 4.67 minutes

d) Average number in system:
   L = L_q + ρ = 0.779 + 0.667 = 1.446 customers

### Problem 6.2: Comparison with M/M/1
Compare the M/G/1 system above with an equivalent M/M/1 system (same λ and μ).

**Solution:**

**M/M/1 system (exponential service):**
- ρ = 10/15 = 0.667
- L_q = ρ²/(1-ρ) = (0.667)²/(1-0.667) = 0.445/0.333 = 1.337 customers
- W_q = ρ/[μ(1-ρ)] = 0.667/[15(0.333)] = 0.134 hours = 8.04 minutes

**Comparison:**
- M/G/1: L_q = 0.779, W_q = 4.67 minutes
- M/M/1: L_q = 1.337, W_q = 8.04 minutes

The M/G/1 system with lower service time variability performs better than M/M/1, demonstrating that reducing service time variability improves system performance.

---

## TOPIC 7: FINITE SOURCE QUEUING MODEL (M/M/c/K/K)

### Problem 7.1: Machine Repair Model
A factory has 6 machines that break down according to an exponential distribution with mean time between failures of 8 hours per machine. There are 2 repair technicians, each capable of repairing machines at a rate of 3 machines per 8-hour shift (exponentially distributed).

Calculate:
a) Average number of machines being repaired
b) Average number of machines waiting for repair
c) Machine availability (percentage of time operational)
d) Probability that all machines are operational

**Solution:**

Given:
- N = 6 machines (finite source)
- λ = 1/8 per hour per machine (failure rate)
- c = 2 repair technicians
- μ = 3/8 per hour per technician (repair rate)

This is an M/M/c/N/N model (finite source, finite capacity).

For finite source models, the effective arrival rate depends on the number of operational machines:
- When n machines are down, (N-n) machines can fail
- Effective arrival rate = (N-n)λ

Steady-state equations become complex. Using finite source formulas:

a) Let ρ₀ = λ/μ = (1/8)/(3/8) = 1/3

The steady-state probabilities require solving:
P_n = (N!)/(N-n)! × (ρ₀ⁿ/n!) × P₀ for n ≤ c
P_n = (N!)/(N-n)! × (ρ₀ⁿ/(c!cⁿ⁻ᶜ)) × P₀ for c < n ≤ N

After solving (requires iteration): Average number being repaired ≈ 0.8 machines

b) Average waiting for repair ≈ 0.3 machines

c) Machine availability = (N - Average down)/N = (6 - 1.1)/6 = 81.7%

d) P₀ (all operational) ≈ 0.24 or 24%

---

## TOPIC 8: PRIORITY QUEUING

### Problem 8.1: Two-Priority System
A computer system processes two types of jobs: high priority (arriving at 5 per hour) and low priority (arriving at 10 per hour). All jobs have exponential service times with mean 3 minutes. High priority jobs are served first.

Calculate:
a) Average waiting time for high priority jobs
b) Average waiting time for low priority jobs
c) Overall average waiting time

**Solution:**

Given:
- λ₁ = 5 high priority jobs/hour
- λ₂ = 10 low priority jobs/hour
- λ = λ₁ + λ₂ = 15 jobs/hour
- μ = 20 jobs/hour (service rate)
- ρ₁ = λ₁/μ = 5/20 = 0.25
- ρ₂ = λ₂/μ = 10/20 = 0.5
- ρ = ρ₁ + ρ₂ = 0.75

For non-preemptive priority queuing:

a) High priority waiting time:
   W_q1 = ρ₁/(μ(1-ρ₁)) = 0.25/[20(1-0.25)] = 0.25/15 = 0.0167 hours = 1 minute

b) Low priority waiting time:
   W_q2 = ρ/(μ(1-ρ₁)(1-ρ)) = 0.75/[20(1-0.25)(1-0.75)] = 0.75/[20×0.75×0.25] = 0.75/3.75 = 0.2 hours = 12 minutes

c) Overall average waiting time:
   W_q = (λ₁W_q1 + λ₂W_q2)/λ = (5×0.0167 + 10×0.2)/15 = (0.0835 + 2)/15 = 0.139 hours = 8.33 minutes

---

## TOPIC 9: NETWORK OF QUEUES

### Problem 9.1: Jackson Network
A production system has two workstations in series. Jobs arrive at station 1 at 8 per hour (Poisson). Station 1 processes jobs at 12 per hour, and all jobs go to station 2. Station 2 processes at 10 per hour, and 20% of jobs return to station 1 for rework, while 80% leave the system.

Calculate the effective arrival rates and average number of jobs at each station.

**Solution:**

Given:
- External arrival to station 1: λ₀ = 8 jobs/hour
- μ₁ = 12 jobs/hour, μ₂ = 10 jobs/hour
- Routing: 100% from station 1 to station 2
- 80% leave from station 2, 20% return to station 1

Setting up traffic equations:
- λ₁ = λ₀ + 0.2λ₂ = 8 + 0.2λ₂
- λ₂ = λ₁

Solving:
- λ₂ = λ₁
- λ₁ = 8 + 0.2λ₁
- 0.8λ₁ = 8
- λ₁ = 10 jobs/hour
- λ₂ = 10 jobs/hour

For each station (treating as M/M/1):

**Station 1:**
- ρ₁ = λ₁/μ₁ = 10/12 = 0.833
- L₁ = ρ₁/(1-ρ₁) = 0.833/0.167 = 5 jobs

**Station 2:**
- ρ₂ = λ₂/μ₂ = 10/10 = 1.0

Since ρ₂ = 1, station 2 is at the stability boundary and would have infinite queue length in practice. The system needs redesign.

---

## PRACTICE PROBLEMS FOR STUDENTS

### Practice Set 1: M/M/1 Systems

1. A drive-through bank has arrival rate 18 customers/hour and service rate 24 customers/hour. Find: system utilization, average queue length, average waiting time.

2. A help desk receives calls at 15/hour and resolves them at 20/hour. What's the probability a caller waits more than 6 minutes?

### Practice Set 2: M/M/c Systems

3. A supermarket has 4 checkout lanes, customers arrive at 60/hour, each cashier serves 18/hour. Find average waiting time and probability all cashiers are busy.

4. Determine optimal number of tellers for a bank with 45 customers/hour arrival, 20/hour service rate per teller, $30/hour teller cost, $25/hour customer waiting cost.

### Practice Set 3: Limited Capacity

5. A restaurant seats 20 people, customers arrive at 25/hour, service rate 30/hour. Find probability of turning customers away and average occupancy.

### Practice Set 4: Applications

6. Design a call center: 180 calls/hour, 8-minute average call duration, target: 80% of callers wait less than 30 seconds. How many agents needed?

---

**Note for Teaching:**
Each problem type builds complexity gradually. Start with basic concepts, then move to single-server, multi-server, and finally special cases. Always emphasize the practical interpretation of results and when each model applies in real situations.
