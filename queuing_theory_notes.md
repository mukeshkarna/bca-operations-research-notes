# CHAPTER 4: QUEUING THEORY

## 4.1 BASICS OF QUEUING THEORY

### 4.1.1 Introduction to Queuing Theory

Queuing theory is a mathematical study of waiting lines or queues. It involves the analysis of several related processes including arrival at the queue, waiting in the queue, and being served by the server at the front of the queue. The theory enables the mathematical analysis of various processes, including arriving at the queue, waiting in the queue, and service at the facility. Queuing theory has applications in a wide variety of situations such as customer service centers, telecommunications, traffic engineering, computing, and the design of factories, shops, offices, and hospitals.

### 4.1.2 Historical Background

Queuing theory originated from the work of Danish mathematician A.K. Erlang in 1909 while working for the Copenhagen Telephone Company. Erlang was analyzing congestion and waiting times occurring in the completion of telephone calls. His pioneering work is now considered the foundation of queuing theory and traffic engineering.

## 4.2 ELEMENTS OF QUEUING THEORY

### 4.2.1 Arrival Process

The arrival process describes how customers arrive at the service facility:

1. **Source population** - Can be finite or infinite
   - *Finite*: Limited number of potential customers (e.g., machines needing repair in a factory)
   - *Infinite*: Unlimited potential customers (e.g., customers at a supermarket checkout)

2. **Arrival pattern** - Usually described by:
   - *Arrival rate (λ)*: Average number of arrivals per unit time
   - *Interarrival time*: Time between consecutive arrivals
   - *Distribution pattern*: Often follows Poisson distribution (random arrivals) or deterministic (fixed intervals)

### 4.2.2 Queue Characteristics

1. **Queue length** - May be limited or unlimited:
   - *Limited*: When there is a maximum capacity (e.g., waiting room with limited seats)
   - *Unlimited*: When there is theoretically no upper bound (e.g., phone calls on hold)

2. **Queue discipline** - The rule by which customers are selected for service:
   - *FIFO (First-In-First-Out)* or *FCFS (First-Come-First-Served)*: Most common queue discipline
   - *LIFO (Last-In-First-Out)*: Useful in certain inventory systems
   - *SIRO (Service In Random Order)*: Random selection
   - *Priority queuing*: Based on priority levels (e.g., emergency room triage)
   - *Processor sharing*: Service capacity is shared among customers (e.g., computer time-sharing systems)

3. **Customer behavior** - How customers react to waiting:
   - *Balking*: Deciding not to join the queue when it is too long
   - *Reneging*: Leaving the queue after joining due to excessive wait time
   - *Jockeying*: Moving between queues to reduce waiting time (in multi-queue systems)

### 4.2.3 Service Mechanism

1. **Number of servers** - Single or multiple:
   - *Single server*: One service facility (e.g., a single ATM)
   - *Multiple servers*: Several parallel service facilities (e.g., checkout counters at a store)

2. **Service pattern** - Characterized by:
   - *Service rate (μ)*: Average number of customers that can be served per unit time
   - *Service time*: Time taken to serve one customer
   - *Service time distribution*: Often exponential, constant, or general distributions

3. **Service arrangement**:
   - *Series arrangement*: Customers must go through multiple service phases in sequence
   - *Parallel arrangement*: Multiple servers performing the same service

## 4.3 KENDALL'S NOTATION

Kendall's notation is a standard method for describing and classifying queuing models. It is typically represented as:

**A/B/C/D/E/F**

Where:
- **A**: Distribution of interarrival times
- **B**: Distribution of service times
- **C**: Number of servers
- **D**: System capacity (maximum number allowed in system, including those in service)
- **E**: Size of calling population
- **F**: Queue discipline

Common symbols used for distributions (A and B):
- **M**: Markovian or exponential distribution (memoryless)
- **D**: Deterministic (constant) distribution
- **G**: General distribution (any arbitrary distribution)
- **E_k**: Erlang distribution with parameter k

In many cases, only the first three parameters (A/B/C) are used, with the assumptions that D = ∞, E = ∞, and F = FCFS.

**Examples of common queuing models:**
- **M/M/1**: Single server with Poisson arrivals and exponential service times
- **M/M/c**: Multiple servers with Poisson arrivals and exponential service times
- **M/D/1**: Single server with Poisson arrivals and constant service times
- **M/G/1**: Single server with Poisson arrivals and general service time distribution

## 4.4 OPERATING CHARACTERISTICS OF A QUEUING SYSTEM

The performance of a queuing system is measured by several operating characteristics:

1. **Traffic intensity (ρ)**: 
   - ρ = λ/(cμ), where c is the number of servers
   - If ρ < 1, the system is stable; if ρ ≥ 1, queue will grow infinitely over time

2. **Server utilization**: 
   - Proportion of time the server is busy
   - For single server: U = λ/μ (same as ρ)

3. **Average number of customers in the system (L)**: 
   - Total number of customers in queue and in service

4. **Average number of customers in the queue (L_q)**: 
   - Number of customers waiting for service

5. **Average time spent in the system (W)**: 
   - Total time from arrival to departure

6. **Average waiting time in queue (W_q)**: 
   - Time spent waiting before service begins

7. **Probability of n customers in the system (P_n)**

**Little's Law** connects these measures:
- L = λW
- L_q = λW_q

This fundamental relationship states that the average number of customers in a system equals the arrival rate multiplied by the average time a customer spends in the system.

## 4.5 CLASSIFICATION OF QUEUING MODELS

### 4.5.1 M/M/1 Queuing Model (Single Server)

This is the simplest queuing model with:
- Poisson arrival process (rate λ)
- Exponential service times (rate μ)
- Single server
- Infinite capacity and population
- FCFS queue discipline

Key formulas:
- Traffic intensity: ρ = λ/μ (must be < 1 for stability)
- Probability of n customers in system: P_n = (1-ρ)ρ^n
- Probability of empty system: P_0 = 1-ρ
- Average number in system: L = ρ/(1-ρ)
- Average number in queue: L_q = ρ²/(1-ρ)
- Average time in system: W = 1/(μ-λ)
- Average waiting time in queue: W_q = λ/[μ(μ-λ)] = W - 1/μ

### 4.5.2 M/M/c Queuing Model (Multiple Servers)

This model extends M/M/1 to c identical servers in parallel:
- Poisson arrival process (rate λ)
- Exponential service times (rate μ per server)
- c servers
- Infinite capacity and population
- FCFS queue discipline

Key formulas:
- Traffic intensity: ρ = λ/(cμ)
- Probability of empty system: P_0 = [∑_(n=0)^(c-1) (cρ)^n/n! + (cρ)^c/(c!(1-ρ))]^(-1)
- Average number in queue: L_q = P_0(λ/μ)^c·ρ/[c!(1-ρ)²]
- Average number in system: L = L_q + λ/μ
- Average waiting time in queue: W_q = L_q/λ
- Average time in system: W = W_q + 1/μ

### 4.5.3 M/M/1/K Queuing Model (Limited Capacity)

This model is similar to M/M/1 but with limited system capacity K:
- Poisson arrival process (rate λ)
- Exponential service times (rate μ)
- Single server
- Maximum of K customers allowed in system
- FCFS queue discipline

Key formulas:
- Probability of n customers: P_n = (1-ρ)ρ^n/(1-ρ^(K+1)) for n ≤ K
- Average number in system: L = ρ[1-(K+1)ρ^K+Kρ^(K+1)]/[(1-ρ)(1-ρ^(K+1))]
- Effective arrival rate: λ_eff = λ(1-P_K)

### 4.5.4 M/M/c/K Queuing Model

This combines multiple servers with limited capacity:
- Poisson arrival process (rate λ)
- Exponential service times (rate μ per server)
- c servers
- Maximum of K customers allowed in system (K ≥ c)
- FCFS queue discipline

### 4.5.5 M/G/1 Queuing Model

This model allows for general service time distribution:
- Poisson arrival process (rate λ)
- General service time distribution with mean 1/μ and variance σ²
- Single server
- Infinite capacity and population
- FCFS queue discipline

Key formula (Pollaczek-Khinchin formula):
- Average number in queue: L_q = λ²σ² + ρ²/[2(1-ρ)]

## 4.6 REAL-WORLD APPLICATIONS

### 4.6.1 Customer Service Systems

**Example 1: Bank Teller Service**

A bank has 3 tellers. Customers arrive at a rate of 40 per hour (Poisson distribution). Each teller can serve an average of 15 customers per hour (exponential service time).

Analysis:
- Arrival rate λ = 40 customers/hour
- Service rate μ = 15 customers/hour per teller
- Number of servers c = 3
- Traffic intensity ρ = λ/(cμ) = 40/(3×15) = 0.89

Since ρ < 1, the system is stable. Using M/M/c formulas, we can determine:
- Average queue length
- Average waiting time
- Probability of waiting more than a certain time

**Example 2: Call Center Operations**

A call center receives calls at an average rate of 120 calls per hour. Calls are randomly distributed (Poisson). The average service time is 3 minutes (exponentially distributed). The call center needs to determine how many operators to employ to ensure that the average waiting time is less than 30 seconds.

Analysis:
- Arrival rate λ = 120 calls/hour = 2 calls/minute
- Service rate μ = 1/(3 minutes) = 0.333 calls/minute
- Required: W_q < 0.5 minutes

Using M/M/c formulas and iterating through different values of c, we find the minimum number of operators needed.

### 4.6.2 Manufacturing and Production Systems

**Example: Machine Repair Model**

A factory has 8 machines that occasionally break down. The time between breakdowns follows an exponential distribution with a mean of 5 hours. There are 2 repair technicians, and repair times are exponentially distributed with a mean of 2 hours.

Analysis:
- This is an M/M/c/K/K model (finite source)
- Population K = 8 machines
- Number of servers c = 2 repair technicians
- Breakdown rate per machine λ = 1/5 per hour
- Repair rate μ = 1/2 per hour

Key metrics to calculate:
- Machine availability (percentage of time machines are operational)
- Average number of machines waiting for repair
- Average time a broken machine waits for repair

### 4.6.3 Transportation and Traffic Management

**Example: Highway Toll Plaza**

A highway toll plaza has 5 booths. Vehicles arrive at a rate of 600 per hour during peak time. The service time at each booth follows an exponential distribution with a mean of 24 seconds.

Analysis:
- Arrival rate λ = 600 vehicles/hour = 10 vehicles/minute
- Service rate μ = 60/24 = 2.5 vehicles/minute per booth
- Number of servers c = 5
- Traffic intensity ρ = λ/(cμ) = 10/(5×2.5) = 0.80

Using M/M/c formulas:
- Calculate average queue length and waiting times
- Determine if additional booths are needed during peak hours

### 4.6.4 Healthcare Systems

**Example: Emergency Room Triage**

An emergency room receives patients at an average rate of 6 per hour (Poisson distribution). There are 3 triage nurses, and the triage process takes an average of 10 minutes per patient (exponential distribution).

Analysis:
- Arrival rate λ = 6 patients/hour
- Service rate μ = 60/10 = 6 patients/hour per nurse
- Number of servers c = 3
- Traffic intensity ρ = λ/(cμ) = 6/(3×6) = 0.33

Using M/M/c formulas:
- Calculate average waiting time for triage
- Determine probability that a patient will wait more than 15 minutes

## 4.7 NUMERICAL EXAMPLES WITH SOLUTIONS

### Problem 1: Single Server Queue (M/M/1)

A small convenience store has one checkout counter. Customers arrive at a rate of 15 per hour (Poisson distribution), and the cashier can serve customers at a rate of 20 per hour (exponential service times). Calculate:
a) Probability that the system is empty
b) Average number of customers in the system
c) Average time a customer spends in the system
d) Probability that there are more than 3 customers in the system

**Solution:**

Given:
- Arrival rate λ = 15 customers/hour
- Service rate μ = 20 customers/hour

a) Probability that the system is empty:
   - Traffic intensity ρ = λ/μ = 15/20 = 0.75
   - P_0 = 1 - ρ = 1 - 0.75 = 0.25 or 25%

b) Average number of customers in the system:
   - L = ρ/(1-ρ) = 0.75/(1-0.75) = 0.75/0.25 = 3 customers

c) Average time a customer spends in the system:
   - W = 1/(μ-λ) = 1/(20-15) = 1/5 = 0.2 hours = 12 minutes

d) Probability that there are more than 3 customers in the system:
   - P(n > 3) = ρ^(3+1) = 0.75^4 = 0.316 or 31.6%

### Problem 2: Multiple Server Queue (M/M/c)

A post office has 3 clerks. Customers arrive according to a Poisson distribution at a rate of 40 per hour. Each clerk can serve customers at a rate of 15 per hour (exponentially distributed). Calculate:
a) Traffic intensity
b) Probability that the system is empty
c) Average number of customers waiting in the queue
d) Average waiting time in the queue
e) Probability that an arriving customer has to wait

**Solution:**

Given:
- Arrival rate λ = 40 customers/hour
- Service rate μ = 15 customers/hour per clerk
- Number of servers c = 3

a) Traffic intensity:
   - ρ = λ/(cμ) = 40/(3×15) = 40/45 = 0.889

b) Probability that the system is empty:
   - P_0 = [∑_(n=0)^(c-1) (λ/μ)^n/n! + (λ/μ)^c/(c!(1-ρ))]^(-1)
   - = [∑_(n=0)^2 (40/15)^n/n! + (40/15)^3/(3!(1-0.889))]^(-1)
   - = [1 + 40/15 + (40/15)^2/2 + (40/15)^3/(6×0.111)]^(-1)
   - = [1 + 2.667 + 3.556 + 211.549]^(-1)
   - = 1/218.772 = 0.0046 or 0.46%

c) Average number of customers waiting in the queue:
   - L_q = P_0(λ/μ)^c·ρ/[c!(1-ρ)²]
   - = 0.0046 × (40/15)^3 × 0.889/[6 × (1-0.889)²]
   - = 0.0046 × 7.111 × 0.889/[6 × 0.012]
   - = 0.0046 × 7.111 × 0.889/0.072
   - = 4.03 customers

d) Average waiting time in the queue:
   - W_q = L_q/λ = 4.03/40 = 0.101 hours = 6.06 minutes

e) Probability that an arriving customer has to wait:
   - P(wait > 0) = (λ/μ)^c/(c!(1-ρ)) × P_0
   - = (40/15)^3/(6×0.111) × 0.0046
   - = 7.111/0.666 × 0.0046
   - = 10.677 × 0.0046
   - = 0.049 or 49%

### Problem 3: Limited Capacity Queue (M/M/1/K)

A small barbershop has one barber and space for at most 4 customers in the shop (including the one being served). Customers arrive at a rate of 10 per hour (Poisson distribution). The barber takes an average of 15 minutes to cut a customer's hair (exponentially distributed). Calculate:
a) Probability that the shop is full
b) Effective arrival rate (actual throughput)
c) Average number of customers in the shop
d) Probability that an arriving customer will be turned away

**Solution:**

Given:
- Arrival rate λ = 10 customers/hour
- Service rate μ = 60/15 = 4 customers/hour
- Maximum capacity K = 4
- Single server

a) Probability that the shop is full:
   - Traffic intensity ρ = λ/μ = 10/4 = 2.5
   - Since ρ > 1 and K is finite, we use M/M/1/K formulas:
   - P_K = P_4 = (1-ρ)ρ^K/(1-ρ^(K+1)) when ρ ≠ 1
   - = (1-2.5)×2.5^4/(1-2.5^5)
   - = (-1.5)×39.0625/(-95.3674)
   - = 58.594/95.3674
   - = 0.614 or 61.4%

b) Effective arrival rate:
   - λ_eff = λ(1-P_K) = 10(1-0.614) = 10×0.386 = 3.86 customers/hour

c) Average number of customers in the shop:
   - For M/M/1/K with ρ ≠ 1:
   - L = ρ[1-(K+1)ρ^K+Kρ^(K+1)]/[(1-ρ)(1-ρ^(K+1))]
   - = 2.5[1-(4+1)×2.5^4+4×2.5^5]/[(1-2.5)(1-2.5^5)]
   - = 2.5[1-5×39.0625+4×97.6563]/[(-1.5)×(-95.3674)]
   - = 2.5[1-195.3125+390.6252]/[1.5×95.3674]
   - = 2.5[196.3127]/143.0511
   - = 2.5 × 1.3724
   - = 3.431 customers

d) Probability that an arriving customer will be turned away:
   - This is the same as the probability that the shop is full: 61.4%

### Problem 4: Multiple Server Queue with Multiple Priorities

A hospital emergency department has 2 doctors. Patients arrive in two priority classes: emergency (high priority) and non-emergency (low priority). Emergency patients arrive at a rate of 3 per hour, and non-emergency patients arrive at a rate of 8 per hour. Both follow Poisson distributions. The service time for all patients follows an exponential distribution with a mean of 12 minutes. Emergency patients are always served before non-emergency patients. Calculate:
a) Average waiting time for emergency patients
b) Average waiting time for non-emergency patients

**Solution:**

Given:
- Arrival rate for emergency patients λ_1 = 3 patients/hour
- Arrival rate for non-emergency patients λ_2 = 8 patients/hour
- Total arrival rate λ = λ_1 + λ_2 = 11 patients/hour
- Service rate μ = 60/12 = 5 patients/hour per doctor
- Number of servers c = 2

a) For emergency patients in a priority queue:
   - Traffic intensity ρ = λ/(cμ) = 11/(2×5) = 11/10 = 1.1
   - Since ρ > 1, this system is unstable in the long run. However, for illustrative purposes:
   - W_q1 = W_q × c/(c - λ_1/μ)
   - Where W_q is the waiting time without priorities
   - W_q = P_0(λ/μ)^c·ρ/[c!λ(1-ρ)²]
   - Calculating W_q and then W_q1...
   
   Note: This problem requires a modification for stability. Either the arrival rates should be reduced or the service capacity increased.

b) For non-emergency patients:
   - W_q2 would be calculated using the appropriate formula for lower priority customers in a priority queue system, but since the system is unstable, these calculations wouldn't yield meaningful results.

## 4.8 DECISION MAKING USING QUEUING THEORY

### 4.8.1 Cost Analysis and Optimization

In practical applications, queuing theory helps balance the cost of providing service with the cost of waiting:

1. **Service cost** increases with more servers or faster service rate
2. **Waiting cost** decreases with more servers or faster service rate

The total cost is the sum of these two costs: TC = SC + WC

Optimization involves finding the number of servers or service rate that minimizes the total cost.

### 4.8.2 Performance Analysis and Improvement

Queuing theory helps evaluate system performance with metrics like:

1. **Server utilization**: Percentage of time servers are busy
2. **Average queue length**: Average number of customers waiting
3. **Average waiting time**: Average time customers spend waiting
4. **Probability of waiting**: Chance an arriving customer has to wait

These metrics can identify bottlenecks and suggest improvements like:
- Adding servers during peak periods
- Adjusting service rates
- Modifying arrival patterns through appointments or incentives
- Implementing express lanes for short service times
- Using priority queuing for urgent cases

## 4.9 LIMITATIONS OF QUEUING THEORY

1. **Assumptions**: Many queuing models make simplifying assumptions (like Poisson arrivals or exponential service times) that may not hold in practice.

2. **Steady-state analysis**: Most formulas apply to steady-state conditions, not to startup or transition periods.

3. **Non-standard behaviors**: Real customers may balk, renege, or jockey between queues, complicating the analysis.

4. **Complex systems**: Some systems with multiple queues, priorities, or feedback loops require simulation rather than analytical solutions.

5. **Human factors**: Psychological factors like perceived wait time versus actual wait time aren't captured in mathematical models.

## 4.10 CONCLUSION

Queuing theory provides powerful tools for analyzing waiting line systems across many applications. By understanding the mathematical relationships between arrival patterns, service mechanisms, and waiting times, managers can make informed decisions about resource allocation, facility design, and operational policies. Despite its limitations, queuing theory remains one of the most useful branches of operations research for service system design and management.

---

## PRACTICE PROBLEMS

1. A small clinic has one doctor who sees patients at a rate of 6 per hour (exponentially distributed). Patients arrive randomly (Poisson distribution) at a rate of 5 per hour. Calculate:
   a) Probability that the clinic is empty
   b) Average number of patients in the clinic
   c) Average time a patient spends in the clinic
   d) Probability that a patient will have to wait more than 10 minutes before seeing the doctor

2. A fast-food restaurant has 3 service counters. Customers arrive at a rate of 72 per hour (Poisson distribution). Each server can process orders at a rate of 30 per hour (exponentially distributed). Calculate:
   a) Average waiting time in the queue
   b) Probability that an arriving customer will find all servers busy
   c) Average number of customers waiting in line

3. A computer system can process jobs at a rate of 50 per hour (exponentially distributed). Jobs arrive at a rate of 40 per hour (Poisson distribution). The system can hold at most 10 jobs including the one being processed. Calculate:
   a) Probability that the system is full
   b) Average number of jobs in the system
   c) Percentage of jobs rejected due to system being full

4. A manufacturing company has 5 machines that break down according to a Poisson process with a mean time between failures of 8 hours. There are 2 repair technicians, and repair times are exponentially distributed with a mean of 3 hours. Calculate:
   a) Probability that all machines are operational
   b) Average number of machines waiting for repair
   c) Machine availability (percentage of time a machine is operational)
