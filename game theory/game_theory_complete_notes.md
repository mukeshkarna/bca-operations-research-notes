# Game Theory - Complete Teaching Notes with Numerical Examples

## 1. Introduction to Game Theory

### Definition and Scope
Game theory is a mathematical framework for analyzing strategic interactions between rational decision-makers. It studies situations where the outcome for each participant depends not only on their own decisions but also on the decisions of others.

### Key Elements of a Game
1. **Players**: The decision-makers (individuals, companies, countries, etc.)
2. **Strategies**: The complete set of actions available to each player
3. **Payoffs**: The outcomes or utilities received by each player
4. **Information**: What each player knows when making decisions
5. **Rules**: The structure and sequence of the game

### Real-World Example: Netflix vs. Amazon Prime Video
Consider the streaming wars between Netflix and Amazon Prime Video deciding on content strategy:

**Players**: Netflix and Amazon Prime Video
**Strategies**: 
- Focus on Original Content
- Focus on Licensed Content

**Payoff Matrix** (in millions of subscriber growth):
```
                Amazon Prime Video
                Original    Licensed
Netflix
Original       (15, 12)    (25, 8)
Licensed       (10, 20)    (18, 15)
```

This represents how subscriber growth varies based on content strategies chosen by both companies.

### Historical Context
- **1928**: John von Neumann proved the minimax theorem
- **1944**: Von Neumann and Morgenstern published "Theory of Games and Economic Behavior"
- **1950s**: John Nash developed the concept of Nash equilibrium
- **1994**: Nash, Harsanyi, and Selten won Nobel Prize in Economics

## 2. Characteristics of Game Theory

### Classification of Games

#### 2.1 Based on Sum of Payoffs
**Zero-Sum Games**: One player's gain equals another's loss
- Example: Poker, chess, market share competition

**Non-Zero-Sum Games**: Players can have mutual gains or losses
- Example: Trade negotiations, environmental agreements

#### 2.2 Based on Number of Players
**Two-Person Games**: Only two players
**n-Person Games**: More than two players

#### 2.3 Based on Information
**Perfect Information**: All players know complete game history
- Example: Chess, checkers

**Imperfect Information**: Players have incomplete knowledge
- Example: Poker, sealed-bid auctions

#### 2.4 Based on Cooperation
**Cooperative Games**: Players can form binding agreements
**Non-Cooperative Games**: No binding agreements possible

### Real-World Example: Uber vs. Lyft Pricing War
During peak hours, both companies must decide on surge pricing:

**Payoff Matrix** (daily profit in thousands):
```
                Lyft
                Low Surge   High Surge
Uber
Low Surge      (50, 45)    (70, 30)
High Surge     (35, 65)    (40, 40)
```

**Analysis**:
- If both use low surge pricing: Uber earns $50k, Lyft earns $45k
- If Uber uses low surge and Lyft uses high surge: Uber captures more market share
- This demonstrates how competitive strategies affect outcomes

## 3. Two-Person, Zero-Sum Games

### Fundamental Concepts

In zero-sum games:
- Total payoffs sum to zero
- One player's gain = other player's loss
- Payoff matrix shows gains for row player (losses for column player)

### Real-World Example: Market Share Battle
Consider two smartphone companies (Apple vs. Samsung) competing for market share in emerging markets:

**Payoff Matrix** (market share percentage points gained/lost):
```
                Samsung
                Premium    Budget
Apple
Premium        (0, 0)     (8, -8)
Budget         (-5, 5)    (3, -3)
```

**Interpretation**:
- (Premium, Premium): Market share remains unchanged
- (Premium, Budget): Apple gains 8% market share, Samsung loses 8%
- (Budget, Premium): Apple loses 5% market share, Samsung gains 5%
- (Budget, Budget): Apple gains 3% market share, Samsung loses 3%

### Mathematical Representation

For a general 2×2 zero-sum game:
```
                Player B
                B1      B2
Player A
A1             a11     a12
A2             a21     a22
```

Where aij represents Player A's payoff when A plays strategy i and B plays strategy j.

## 4. Pure Strategy Games and Saddle Points

### Minimax Theorem
- **Player A (Maximizer)**: Chooses strategy to maximize minimum possible payoff
- **Player B (Minimizer)**: Chooses strategy to minimize maximum possible loss

### Finding Saddle Points - Step-by-Step Process

#### Complete Numerical Example 1: Technology Investment Game

**Scenario**: Two tech companies deciding on R&D investment strategies

**Payoff Matrix** (profit in millions):
```
                Company B
                AI      Blockchain    IoT
Company A
AI             12         8          15
Blockchain      6        10           4
IoT            18         5          12
```

**Step 1**: Calculate row minima (worst case for Company A)
- Row 1 (AI): min(12, 8, 15) = 8
- Row 2 (Blockchain): min(6, 10, 4) = 4
- Row 3 (IoT): min(18, 5, 12) = 5

**Step 2**: Calculate column maxima (worst case for Company B)
- Column 1 (AI): max(12, 6, 18) = 18
- Column 2 (Blockchain): max(8, 10, 5) = 10
- Column 3 (IoT): max(15, 4, 12) = 15

**Step 3**: Find maximin and minimax values
- Maximin (max of row minima) = max(8, 4, 5) = 8
- Minimax (min of column maxima) = min(18, 10, 15) = 10

**Step 4**: Check for saddle point
Since maximin (8) ≠ minimax (10), there is **no saddle point** in pure strategies.

#### Complete Numerical Example 2: Investment Portfolio Game

**Scenario**: Investor vs. Market conditions

**Payoff Matrix** (returns in percentage):
```
                Market
                Bull    Bear    Stable
Investor
Stocks          20      -10        5
Bonds            8        6        7
Cash             3        3        3
```

**Step 1**: Calculate row minima
- Stocks: min(20, -10, 5) = -10
- Bonds: min(8, 6, 7) = 6
- Cash: min(3, 3, 3) = 3

**Step 2**: Calculate column maxima
- Bull: max(20, 8, 3) = 20
- Bear: max(-10, 6, 3) = 6
- Stable: max(5, 7, 3) = 7

**Step 3**: Find maximin and minimax values
- Maximin = max(-10, 6, 3) = 6
- Minimax = min(20, 6, 7) = 6

**Step 4**: Check for saddle point
Since maximin (6) = minimax (6), there is a **saddle point** at (Bonds, Bear) with value 6.

**Solution**: Investor should choose Bonds, and the worst-case scenario gives 6% return.

## 5. Dominance Theory

### Types of Dominance

#### 5.1 Strict Dominance
Strategy A **strictly dominates** strategy B if A gives better payoffs than B against all opponent strategies.

#### 5.2 Weak Dominance
Strategy A **weakly dominates** strategy B if A gives at least as good payoffs as B against all opponent strategies, and strictly better against at least one.

### Complete Numerical Example: Advertising Campaign

**Scenario**: Two companies choosing advertising strategies

**Initial Payoff Matrix** (market share gain):
```
                Company B
                TV    Radio   Online   Print
Company A
TV              5       8       12       6
Radio           3       6        9       4
Online         10      12       15      11
Print           2       4        7       3
```

**Step 1**: Check for dominated strategies for Company A
- Compare TV vs. Online: Online dominates TV (10>5, 12>8, 15>12, 11>6)
- Compare Radio vs. Online: Online dominates Radio (10>3, 12>6, 15>9, 11>4)
- Compare Print vs. Online: Online dominates Print (10>2, 12>4, 15>7, 11>3)

**Step 2**: Eliminate dominated strategies
After eliminating TV, Radio, and Print, we have:
```
                Company B
                TV    Radio   Online   Print
Company A
Online         10      12       15      11
```

**Step 3**: Check Company B's strategies (minimize Company A's payoff)
- TV gives Company A: 10
- Radio gives Company A: 12
- Online gives Company A: 15
- Print gives Company A: 11

Company B should choose TV (gives lowest payoff to Company A).

**Solution**: Company A chooses Online, Company B chooses TV, payoff = 10.

### Real-World Application: Restaurant Location Strategy

**Scenario**: Two restaurant chains choosing locations in a city

**Payoff Matrix** (monthly profit in thousands):
```
                Chain B
                Mall    Downtown   Suburb   Airport
Chain A
Mall            15        25        35       20
Downtown        10        20        30       15
Suburb          40        50        60       45
Airport          8        18        28       13
```

**Analysis**:
- Suburb location dominates all other locations for Chain A
- Chain A should choose Suburb regardless of Chain B's choice
- Chain B, knowing this, should choose Mall to minimize Chain A's advantage

## 6. Mixed Strategies

### When to Use Mixed Strategies
Mixed strategies are used when:
1. No saddle point exists in pure strategies
2. Players want to be unpredictable
3. Randomization provides better expected payoffs

### Expected Value Calculation
For mixed strategies, we calculate expected payoffs using probability distributions.

### Complete Numerical Example 1: Security vs. Attacker Game

**Scenario**: Security company vs. potential attacker

**Payoff Matrix** (security effectiveness score):
```
                Attacker
                Physical   Cyber
Security
Physical          3        -2
Cyber            -1         4
```

**Step 1**: Check for saddle point
- Row minima: min(3, -2) = -2, min(-1, 4) = -1
- Column maxima: max(3, -1) = 3, max(-2, 4) = 4
- Maximin = max(-2, -1) = -1
- Minimax = min(3, 4) = 3
- Since -1 ≠ 3, no saddle point exists

**Step 2**: Set up mixed strategy equations
Let Security play Physical with probability p and Cyber with probability (1-p)
Let Attacker play Physical with probability q and Cyber with probability (1-q)

**Step 3**: Find Security's optimal strategy
For Attacker to be indifferent between Physical and Cyber:
E(Physical) = E(Cyber)
3p + (-1)(1-p) = (-2)p + 4(1-p)
3p - 1 + p = -2p + 4 - 4p
4p - 1 = -6p + 4
10p = 5
p = 0.5

**Step 4**: Find Attacker's optimal strategy
For Security to be indifferent between Physical and Cyber:
E(Physical) = E(Cyber)
3q + (-2)(1-q) = (-1)q + 4(1-q)
3q - 2 + 2q = -q + 4 - 4q
5q - 2 = -5q + 4
10q = 6
q = 0.6

**Step 5**: Calculate game value
V = 3(0.5)(0.6) + (-2)(0.5)(0.4) + (-1)(0.5)(0.6) + 4(0.5)(0.4)
V = 0.9 - 0.4 - 0.3 + 0.8 = 1.0

**Solution**:
- Security: Physical 50%, Cyber 50%
- Attacker: Physical 60%, Cyber 40%
- Expected security effectiveness: 1.0

### Complete Numerical Example 2: Market Entry Game

**Scenario**: Two companies deciding on market entry timing

**Payoff Matrix** (profit in millions):
```
                Company B
                Early    Late
Company A
Early           2        8
Late            6        4
```

**Step 1**: Verify no saddle point
- Row minima: min(2, 8) = 2, min(6, 4) = 4
- Column maxima: max(2, 6) = 6, max(8, 4) = 8
- Maximin = 4, Minimax = 6
- No saddle point (4 ≠ 6)

**Step 2**: Use algebraic formula
For payoff matrix:
```
    a  b
    c  d
```
Where a=2, b=8, c=6, d=4

**Step 3**: Calculate optimal probabilities
p = (d-c)/((a+d)-(b+c)) = (4-6)/((2+4)-(8+6)) = -2/(6-14) = -2/(-8) = 0.25

q = (d-b)/((a+d)-(b+c)) = (4-8)/((2+4)-(8+6)) = -4/(-8) = 0.5

**Step 4**: Calculate game value
V = (ad-bc)/((a+d)-(b+c)) = (2×4-8×6)/(6-14) = (8-48)/(-8) = -40/(-8) = 5

**Solution**:
- Company A: Early 25%, Late 75%
- Company B: Early 50%, Late 50%
- Expected value: 5 million

## 7. Algebraic Method for 2×2 Games

### General Formula for 2×2 Zero-Sum Games

For payoff matrix:
```
    a  b
    c  d
```

**Optimal strategies**:
- Row player plays first strategy with probability: p = (d-c)/((a+d)-(b+c))
- Column player plays first strategy with probability: q = (d-b)/((a+d)-(b+c))
- Game value: V = (ad-bc)/((a+d)-(b+c))

### Complete Numerical Example: Competitive Bidding

**Scenario**: Two contractors bidding for projects

**Payoff Matrix** (profit margin percentage):
```
                Contractor B
                Low Bid   High Bid
Contractor A
Low Bid          1         9
High Bid         7         3
```

**Step 1**: Apply algebraic formula
a = 1, b = 9, c = 7, d = 3

**Step 2**: Calculate denominator
(a+d)-(b+c) = (1+3)-(9+7) = 4-16 = -12

**Step 3**: Calculate optimal probabilities
p = (d-c)/((a+d)-(b+c)) = (3-7)/(-12) = -4/(-12) = 1/3 ≈ 0.333

q = (d-b)/((a+d)-(b+c)) = (3-9)/(-12) = -6/(-12) = 1/2 = 0.5

**Step 4**: Calculate game value
V = (ad-bc)/((a+d)-(b+c)) = (1×3-9×7)/(-12) = (3-63)/(-12) = -60/(-12) = 5

**Solution**:
- Contractor A: Low Bid 33.3%, High Bid 66.7%
- Contractor B: Low Bid 50%, High Bid 50%
- Expected profit margin: 5%

**Verification**:
Expected payoff for A's Low Bid: 1(0.5) + 9(0.5) = 5 ✓
Expected payoff for A's High Bid: 7(0.5) + 3(0.5) = 5 ✓

## 8. Graphical Method for 2×n and m×2 Games

### Solving 2×n Games (Row player has 2 strategies)

#### Complete Numerical Example: Investment Strategy

**Scenario**: Investor with two strategies against three market conditions

**Payoff Matrix** (returns in percentage):
```
                Market Conditions
                Bull    Bear    Volatile
Investor
Conservative     6       4        5
Aggressive      12      -2        8
```

**Step 1**: Set up probability variable
Let investor play Conservative with probability p and Aggressive with probability (1-p)

**Step 2**: Calculate expected returns for each market condition
- E(Bull) = 6p + 12(1-p) = 6p + 12 - 12p = 12 - 6p
- E(Bear) = 4p + (-2)(1-p) = 4p - 2 + 2p = 6p - 2
- E(Volatile) = 5p + 8(1-p) = 5p + 8 - 8p = 8 - 3p

**Step 3**: Plot the functions
- Bull market line: y = 12 - 6p (slope = -6, y-intercept = 12)
- Bear market line: y = 6p - 2 (slope = 6, y-intercept = -2)
- Volatile market line: y = 8 - 3p (slope = -3, y-intercept = 8)

**Step 4**: Find intersection points
Bull = Bear: 12 - 6p = 6p - 2 → 14 = 12p → p = 7/6 ≈ 1.17 (outside [0,1])
Bull = Volatile: 12 - 6p = 8 - 3p → 4 = 3p → p = 4/3 ≈ 1.33 (outside [0,1])
Bear = Volatile: 6p - 2 = 8 - 3p → 9p = 10 → p = 10/9 ≈ 1.11 (outside [0,1])

**Step 5**: Evaluate at boundary points
At p = 0 (Pure Aggressive):
- Bull: 12, Bear: -2, Volatile: 8
- Minimum = -2

At p = 1 (Pure Conservative):
- Bull: 6, Bear: 4, Volatile: 5
- Minimum = 4

**Step 6**: Find optimal mixed strategy
Since all intersections are outside [0,1], check which pure strategy is better:
- Pure Conservative gives minimum return of 4%
- Pure Aggressive gives minimum return of -2%

**Solution**: Investor should play Pure Conservative strategy for guaranteed 4% minimum return.

### Solving m×2 Games (Column player has 2 strategies)

#### Complete Numerical Example: Advertising Competition

**Scenario**: Company A (3 strategies) vs. Company B (2 strategies)

**Payoff Matrix** (market share gain):
```
                Company B
                Online    Traditional
Company A
Social Media     8           4
Email            6           9
Influencer      10           2
```

**Step 1**: Set up Company B's mixed strategy
Let Company B play Online with probability q and Traditional with probability (1-q)

**Step 2**: Calculate Company A's expected payoffs
- E(Social Media) = 8q + 4(1-q) = 8q + 4 - 4q = 4q + 4
- E(Email) = 6q + 9(1-q) = 6q + 9 - 9q = 9 - 3q
- E(Influencer) = 10q + 2(1-q) = 10q + 2 - 2q = 8q + 2

**Step 3**: Find intersections
Social Media = Email: 4q + 4 = 9 - 3q → 7q = 5 → q = 5/7 ≈ 0.714
Social Media = Influencer: 4q + 4 = 8q + 2 → 2 = 4q → q = 0.5
Email = Influencer: 9 - 3q = 8q + 2 → 7 = 11q → q = 7/11 ≈ 0.636

**Step 4**: Evaluate at intersection points
At q = 0.5:
- Social Media: 4(0.5) + 4 = 6
- Email: 9 - 3(0.5) = 7.5
- Influencer: 8(0.5) + 2 = 6

At q = 5/7:
- Social Media: 4(5/7) + 4 = 20/7 + 28/7 = 48/7 ≈ 6.86
- Email: 9 - 3(5/7) = 9 - 15/7 = 63/7 - 15/7 = 48/7 ≈ 6.86
- Influencer: 8(5/7) + 2 = 40/7 + 14/7 = 54/7 ≈ 7.71

**Step 5**: Determine upper envelope
The upper envelope (maximum expected payoff for Company A) is:
- For q < 0.5: Influencer strategy
- For 0.5 < q < 5/7: Email strategy
- For q > 5/7: Social Media strategy

**Step 6**: Find Company B's optimal strategy
Company B wants to minimize Company A's maximum payoff.
The minimum of the upper envelope occurs at q = 5/7, giving Company A a payoff of 48/7 ≈ 6.86.

**Solution**:
- Company B: Online 5/7 ≈ 71.4%, Traditional 2/7 ≈ 28.6%
- Company A can use Social Media or Email strategies (both give same expected payoff)
- Expected market share gain for Company A: 48/7 ≈ 6.86%

## 9. Extended Real-World Applications

### 9.1 Cybersecurity Game Theory

**Scenario**: Corporate cybersecurity vs. hackers

**Players**: Security team vs. hacker group
**Strategies**:
- Security: Firewall focus, Endpoint focus, Network monitoring
- Hackers: Malware attack, Social engineering, Physical breach

**Payoff Matrix** (security breach cost in thousands):
```
                    Hackers
                Malware  Social Eng  Physical
Security
Firewall          -50       -80        -20
Endpoint          -30       -60        -40
Network           -70       -40        -30
```

**Analysis**: This helps determine optimal security resource allocation based on expected attack vectors.

### 9.2 Supply Chain Management

**Scenario**: Supplier vs. manufacturer contract negotiation

**Payoff Matrix** (profit margins):
```
                Manufacturer
                Short-term   Long-term
Supplier
Low Price        (3,8)       (5,12)
High Price       (7,4)       (9,6)
```

**Real-world insight**: Long-term contracts with moderate pricing often benefit both parties more than short-term aggressive pricing.

### 9.3 Environmental Policy Games

**Scenario**: Two countries deciding on environmental policies

**Payoff Matrix** (economic benefit - environmental cost):
```
                Country B
                Strict    Lenient
Country A
Strict         (5,5)     (2,8)
Lenient        (8,2)     (3,3)
```

**Analysis**: This represents the classic "tragedy of the commons" where individual rational choices lead to collectively irrational outcomes.

### 9.4 Pharmaceutical R&D Competition

**Scenario**: Two pharmaceutical companies investing in drug development

**Payoff Matrix** (expected profit in millions):
```
                Company B
                Alzheimer's  Cancer  Diabetes
Company A
Alzheimer's        50        120       80
Cancer             80        100       90
Diabetes          100         90       70
```

**Strategic considerations**:
- First-mover advantage in drug development
- Patent protection periods
- Regulatory approval timelines
- Market size and competition

### 9.5 Political Campaign Strategy

**Scenario**: Two political candidates allocating campaign resources

**Payoff Matrix** (vote share percentage):
```
                Candidate B
                Urban    Suburban   Rural
Candidate A
Urban           45        60        35
Suburban        40        50        45
Rural           55        40        55
```

**Analysis**: Shows how campaign resource allocation affects vote outcomes in different demographics.

## 10. Advanced Concepts and Extensions

### 10.1 Repeated Games
In repeated games, players interact multiple times, allowing for:
- Reputation building
- Punishment strategies
- Cooperation development

**Example**: Airline pricing over multiple periods
- Short-term: Price competition
- Long-term: Possible tacit collusion

### 10.2 Incomplete Information Games
Players don't know opponents' payoffs or types.

**Example**: Job market signaling
- Employers can't observe worker productivity directly
- Workers signal through education, experience
- Creates separating or pooling equilibria

### 10.3 Evolutionary Game Theory
Applied to biological and social evolution:
- Strategies evolve based on success
- Stable strategies persist
- Applications in biology, sociology, economics

## 11. Computational Methods and Software

### 11.1 Linear Programming Approach
Large games can be solved using linear programming:
- Convert game to LP problem
- Use simplex method
- Handles games with many strategies

### 11.2 Monte Carlo Simulation
For complex games:
- Simulate random strategy combinations
- Estimate expected payoffs
- Useful for n-player games

### 11.3 Software Tools
- **GAMBIT**: Comprehensive game theory software
- **Mathematica**: Built-in game theory functions
- **R**: Game theory packages
- **MATLAB**: Optimization toolboxes

## 12. Common Mistakes and Pitfalls

### 12.1 Calculation Errors
- Always verify mixed strategy probabilities sum to 1
- Check that expected payoffs are equal for mixed strategies
- Ensure saddle point calculations are correct

### 12.2 Interpretation Errors
- Zero-sum assumption may not hold in real situations
- Perfect rationality assumption is often violated
- Nash equilibrium may not be unique

### 12.3 Application Limitations
- Static models may not capture dynamic interactions
- Incomplete information often ignored
- Behavioral factors not considered

## 13. Practice Problems with Solutions

### Problem 1: Restaurant Competition
Two restaurants choose between premium and budget menus:

**Payoff Matrix** (daily profit):
```
                Restaurant B
                Premium   Budget
Restaurant A
Premium       (200,180)  (300,100)
Budget        (150,250)  (220,200)
```

**Solution Steps**:
1. Check for dominant strategies
2. Find pure strategy equilibrium if exists
3. Calculate mixed strategy equilibrium
4. Interpret results

**Answer**: Mixed strategy equilibrium exists with specific probabilities.

### Problem 2: Technology Adoption
Two companies deciding on technology adoption timing:

**Payoff Matrix**:
```
                Company B
                Early    Late
Company A
Early           3        7
Late            5        4
```

**Solution**: Calculate optimal mixed strategies and game value.

## 14. Exam Preparation Guide

### Key Formulas to Remember
1. **Saddle Point**: Maximin = Minimax
2. **2×2 Mixed Strategy**: p = (d-c)/((a+d)-(b+c))
3. **Game Value**: V = (ad-bc)/((a+d)-(b+c))
4. **Expected Payoff**: E = Σ(probability × payoff)

### Problem-Solving Steps
1. **Identify game type** (zero-sum, number of strategies)
2. **Check for saddle point** (pure strategy solution)
3. **Apply dominance** (eliminate inferior strategies)
4. **Calculate mixed strategies** (if no pure strategy solution)
5. **Interpret results** (economic/strategic meaning)

### Common Exam Questions
1. Find saddle point in given payoff matrix
2. Calculate optimal mixed strategies for 2×2 game
3. Solve using graphical method for 2×n games
4. Apply dominance principle to reduce game size
5. Interpret real-world scenarios using game theory

## 15. Summary and Conclusion

Game theory provides powerful tools for analyzing strategic interactions in various fields:

### Key Takeaways
1. **Strategic thinking**: Consider opponents' likely actions
2. **Mathematical rigor**: Use formal methods to find solutions
3. **Real-world applications**: Wide applicability across disciplines
4. **Limitations awareness**: Understand when models apply

### Future Directions
- Behavioral game theory
- Mechanism design
- Algorithmic game theory
- Network games
- Experimental validation

### Practical Applications
- Business strategy
- Economic policy
- International relations
- Environmental management
- Technology adoption

Game theory continues to evolve, incorporating insights from psychology, computer science, and other fields to better understand strategic decision-making in complex, real-world environments.