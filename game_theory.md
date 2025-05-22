# Game Theory - Detailed Teaching Notes

## 1. Introduction to Game Theory

Game theory is a mathematical framework for analyzing strategic interactions among rational decision-makers. It provides tools to understand situations where the outcome of one's decision depends not only on their own actions but also on the actions of others.

### Key Concepts:

- **Game**: A situation involving two or more players where each player's payoff depends on the strategies chosen by all players.
- **Player**: A decision-maker in the game.
- **Strategy**: A complete plan of action that specifies what a player will do in every possible situation.
- **Payoff**: The reward or utility a player receives after all players have chosen their strategies.
- **Solution**: The outcome or set of strategies that players are likely to choose.

### Historical Development:

Game theory was formally developed by mathematician John von Neumann and economist Oskar Morgenstern in their 1944 book "Theory of Games and Economic Behavior." It was further expanded by John Nash in the 1950s with his concept of Nash equilibrium.

## 2. Characteristics of Game Theory

### Essential Elements of a Game:

1. **Players**: The decision-makers (individuals, firms, countries, etc.)
2. **Strategies**: Available choices for each player
3. **Payoffs**: Outcomes or utilities for each player
4. **Information**: What each player knows when making decisions
5. **Rules**: How the game is played

### Types of Games:

1. **Based on player interaction**:
   - **Cooperative games**: Players can form binding agreements
   - **Non-cooperative games**: Players cannot form binding agreements

2. **Based on timing**:
   - **Simultaneous games**: Players move simultaneously
   - **Sequential games**: Players move in a specific order

3. **Based on information**:
   - **Perfect information**: All players know the complete history of the game
   - **Imperfect information**: Players have incomplete knowledge

4. **Based on payoff structure**:
   - **Zero-sum games**: One player's gain equals another's loss
   - **Non-zero-sum games**: Total payoffs can vary

## 3. Two-Person, Zero-Sum Games

In these games:
- There are exactly two players
- What one player wins, the other loses (the sum of payoffs equals zero)
- These games are strictly competitive

### Payoff Matrix:

The payoff matrix represents the game in normal form, showing:
- Rows for Player A's strategies
- Columns for Player B's strategies
- Entries for Player A's payoffs (Player B's payoffs are the negative of these)

### Example Payoff Matrix:
```
          Player B
          B1    B2
Player A
A1       5    -3
A2      -2     4
```

In this example:
- If A plays A1 and B plays B1, A wins 5 units and B loses 5 units
- If A plays A1 and B plays B2, A loses 3 units and B wins 3 units
- If A plays A2 and B plays B1, A loses 2 units and B wins 2 units
- If A plays A2 and B plays B2, A wins 4 units and B loses 4 units

## 4. Pure Strategy Games

A pure strategy is a specific action that a player will follow with certainty.

### Saddle Point (Equilibrium Point):

A saddle point occurs when the minimum value of a row equals the maximum value of a column. This represents an equilibrium where neither player has an incentive to change their strategy.

### Steps to Find Saddle Point:

1. Find the minimum value in each row (row minima)
2. Find the maximum value in each column (column maxima)
3. If the maximum of row minima equals the minimum of column maxima, this is the saddle point

### Minimax Principle:

- **Player A (row player)**: Chooses the strategy that maximizes the minimum possible payoff
- **Player B (column player)**: Chooses the strategy that minimizes the maximum possible loss

### Numerical Example 1:

Consider this payoff matrix:
```
          Player B
          B1    B2    B3
Player A
A1       3     2     4
A2       2     4     0
A3       5     1     3
```

**Step 1**: Find row minima:
- Row 1 minimum: 2
- Row 2 minimum: 0
- Row 3 minimum: 1

**Step 2**: Find column maxima:
- Column 1 maximum: 5
- Column 2 maximum: 4
- Column 3 maximum: 4

**Step 3**: Maximum of row minima = 2
**Step 4**: Minimum of column maxima = 4

Since maximum of row minima ≠ minimum of column maxima, there is no saddle point in pure strategy.

### Numerical Example 2:

Consider this payoff matrix:
```
          Player B
          B1    B2    B3
Player A
A1       8     6     2
A2       6     7     3
A3       5     8     7
```

**Step 1**: Find row minima:
- Row 1 minimum: 2
- Row 2 minimum: 3
- Row 3 minimum: 5

**Step 2**: Find column maxima:
- Column 1 maximum: 8
- Column 2 maximum: 8
- Column 3 maximum: 7

**Step 3**: Maximum of row minima = 5 (strategy A3)
**Step 4**: Minimum of column maxima = 7 (strategy B3)

Since maximum of row minima ≠ minimum of column maxima, there is no saddle point in pure strategy.

## 5. Dominance Theory

A strategy dominates another if it provides a better payoff regardless of what the opponent does.

### Types of Dominance:

1. **Strict Dominance**: Strategy A strictly dominates strategy B if A yields strictly better payoffs against all opponent strategies
2. **Weak Dominance**: Strategy A weakly dominates strategy B if A yields at least as good payoffs as B against all opponent strategies, and strictly better against at least one

### Dominance Elimination Process:

1. Identify dominated strategies for each player
2. Eliminate these strategies from the game
3. Repeat until no more strategies can be eliminated

### Numerical Example:

Consider this payoff matrix:
```
          Player B
          B1    B2    B3
Player A
A1       4     6     8
A2       3     5     7
A3       2     3     4
```

For Player A:
- A1 dominates A2 (every element in A1 is larger than corresponding element in A2)
- A2 dominates A3 (every element in A2 is larger than corresponding element in A3)
- Therefore, A1 is the dominant strategy for Player A

For Player B (looking at negative values since B wants to minimize A's payoff):
- B1 dominates B2 and B3 (gives lowest payoff to A)
- Therefore, B1 is the dominant strategy for Player B

Solution: (A1, B1) with payoff 4

## 6. Mixed Strategies

When there's no saddle point in pure strategies, players should randomize their choices using mixed strategies.

### Mixed Strategy:

A probability distribution over the set of pure strategies, indicating the likelihood of playing each strategy.

### Key Principle:

In a mixed strategy equilibrium, each player's expected payoff must be the same regardless of which pure strategy in their support they play.

### Solving 2×2 Games with Mixed Strategies:

Let's say Player A uses strategies A1 and A2 with probabilities p and (1-p), and Player B uses strategies B1 and B2 with probabilities q and (1-q).

Steps:
1. Calculate expected payoff for Player A's strategies against Player B's mixed strategy
2. Set these expected payoffs equal (Player A must be indifferent)
3. Solve for q
4. Similarly, calculate expected payoff for Player B's strategies and solve for p

### Numerical Example:

Consider this payoff matrix:
```
          Player B
          B1    B2
Player A
A1       3    -2
A2      -1     4
```

**Step 1**: Let Player A use A1 with probability p and A2 with probability (1-p)
**Step 2**: Let Player B use B1 with probability q and B2 with probability (1-q)

**Step 3**: For Player B to be indifferent:
- Expected payoff from B1 = Expected payoff from B2
- p(-3) + (1-p)(1) = p(2) + (1-p)(-4)
- -3p + 1 - p = 2p - 4 + 4p
- -3p + 1 - p = 6p - 4
- -4p = 6p - 5
- -10p = -5
- p = 5/10 = 0.5

**Step 4**: For Player A to be indifferent:
- Expected payoff from A1 = Expected payoff from A2
- q(3) + (1-q)(-2) = q(-1) + (1-q)(4)
- 3q - 2 + 2q = -q + 4 - 4q
- 5q - 2 = -5q + 4
- 10q = 6
- q = 0.6

**Step 5**: Calculate expected value of the game:
- E = q(3p + (-1)(1-p)) + (1-q)((-2)p + 4(1-p))
- With p = 0.5 and q = 0.6:
- E = 0.6(3(0.5) + (-1)(0.5)) + 0.4((-2)(0.5) + 4(0.5))
- E = 0.6(1) + 0.4(1) = 1

Therefore, the value of the game is 1, and the optimal mixed strategies are:
- Player A: p = 0.5 (play A1 with probability 0.5, A2 with probability 0.5)
- Player B: q = 0.6 (play B1 with probability 0.6, B2 with probability 0.4)

## 7. Algebraic Method for Solving Mixed Strategy Games

For a 2×2 game with payoff matrix:
```
          Player B
          B1    B2
Player A
A1       a    b
A2       c    d
```

If there's no saddle point and (a-c)(b-d) < 0, the optimal mixed strategies are:

- Player A plays A1 with probability p = (d-c)/((a-c)-(b-d))
- Player B plays B1 with probability q = (d-b)/((a-b)-(c-d))
- Value of the game = (ad-bc)/((a-c)-(b-d))

### Numerical Example:

Consider this payoff matrix:
```
          Player B
          B1    B2
Player A
A1       4     1
A2       2     6
```

Here, a = 4, b = 1, c = 2, d = 6

**Step 1**: Check if there's a saddle point:
- Row minima: min(4,1) = 1, min(2,6) = 2
- Column maxima: max(4,2) = 4, max(1,6) = 6
- Maximum of row minima = 2
- Minimum of column maxima = 4
- Since 2 ≠ 4, there's no saddle point

**Step 2**: Check if (a-c)(b-d) < 0:
- (4-2)(1-6) = 2(-5) = -10 < 0, so we can use mixed strategies

**Step 3**: Calculate optimal strategies:
- p = (d-c)/((a-c)-(b-d))
- p = (6-2)/((4-2)-(1-6))
- p = 4/(2-(-5))
- p = 4/7

- q = (d-b)/((a-b)-(c-d))
- q = (6-1)/((4-1)-(2-6))
- q = 5/(3-(-4))
- q = 5/7

**Step 4**: Calculate value of the game:
- V = (ad-bc)/((a-c)-(b-d))
- V = ((4×6)-(1×2))/((4-2)-(1-6))
- V = (24-2)/(2-(-5))
- V = 22/7

Therefore:
- Player A plays A1 with probability 4/7 and A2 with probability 3/7
- Player B plays B1 with probability 5/7 and B2 with probability 2/7
- Value of the game = 22/7 ≈ 3.14

## 8. Graphical Method for Solving 2×n or m×2 Games

When one player has exactly two strategies, we can use a graphical approach.

### Steps for 2×n games:

1. Let Player A mix strategies A1 and A2 with probabilities p and (1-p)
2. Calculate expected payoffs for each of Player B's strategies
3. Plot these expected payoffs as functions of p
4. The lower envelope of these lines represents Player B's best response
5. The maximum of this lower envelope is the optimal value of p

### Numerical Example:

Consider this payoff matrix:
```
          Player B
          B1    B2    B3
Player A
A1       3     1     4
A2       2     5     0
```

**Step 1**: Let Player A play A1 with probability p and A2 with probability (1-p)

**Step 2**: Calculate expected payoffs for each of Player B's strategies:
- E(B1) = 3p + 2(1-p) = 3p + 2 - 2p = p + 2
- E(B2) = 1p + 5(1-p) = p + 5 - 5p = 5 - 4p
- E(B3) = 4p + 0(1-p) = 4p

**Step 3**: Plot these functions:
- E(B1) = p + 2 (line with slope 1, y-intercept 2)
- E(B2) = 5 - 4p (line with slope -4, y-intercept 5)
- E(B3) = 4p (line with slope 4, y-intercept 0)

**Step 4**: Find intersections:
- E(B1) = E(B2): p + 2 = 5 - 4p → 5p = 3 → p = 3/5 = 0.6
- E(B1) = E(B3): p + 2 = 4p → 2 = 3p → p = 2/3 ≈ 0.67
- E(B2) = E(B3): 5 - 4p = 4p → 5 = 8p → p = 5/8 = 0.625

**Step 5**: Determine the lower envelope:
- For p < 0.6, B2 gives the lowest expected payoff
- For 0.6 < p < 0.625, B1 gives the lowest expected payoff
- For p > 0.625, B3 gives the lowest expected payoff

**Step 6**: Find the maximin value:
- At p = 0.6: E(B1) = E(B2) = 0.6 + 2 = 5 - 4(0.6) = 2.6
- At p = 0.625: E(B1) = E(B3) = 0.625 + 2 = 4(0.625) = 2.625

The maximum value is 2.625 at p = 0.625. Therefore:
- Player A should play A1 with probability 0.625 and A2 with probability 0.375
- Player B should play B1 and B3 with probabilities determined by finding q1 and q3 such that:
  - 3q1 + 1q2 + 4q3 = 2.625 (from A1)
  - 2q1 + 5q2 + 0q3 = 2.625 (from A2)
  - q1 + q2 + q3 = 1

## 9. Real-World Applications of Game Theory

### 1. Business Competition:

**Example: Pricing Strategies**

Two competing firms (Firm A and Firm B) must decide whether to set high or low prices for their products.

Payoff Matrix:
```
            Firm B
            Low     High
Firm A
Low        (5,5)   (8,3)
High       (3,8)   (7,7)
```

Analysis:
- If both firms choose low prices, they share the market and earn moderate profits (5,5)
- If both choose high prices, they earn higher profits (7,7)
- If one chooses low and the other high, the low-price firm captures more market share (8,3)

This is a Prisoner's Dilemma situation where the Nash equilibrium is (Low, Low), though (High, High) would be better for both firms. This explains why price wars occur even though they hurt all participants.

### 2. International Relations:

**Example: Arms Race**

Two countries must decide whether to increase military spending or maintain current levels.

Payoff Matrix:
```
                Country B
                Maintain   Increase
Country A
Maintain       (3,3)      (1,4)
Increase       (4,1)      (2,2)
```

Analysis:
- Both countries maintaining current spending levels leads to peaceful coexistence (3,3)
- If one country increases spending while the other doesn't, the militarizing country gains advantage (4,1)
- Both countries increasing spending leads to an arms race with mutual disadvantage (2,2)

This explains why arms races occur despite their ultimate disadvantage to all parties.

### 3. Auction Bidding:

**Example: Sealed-Bid Auction**

Bidders must decide on their bidding strategies without knowing others' bids.

In a common value auction (where the item has the same value to all bidders), bidders must account for the "winner's curse" - the fact that winning might mean they've overestimated the value.

Game theory helps determine optimal bidding strategies that balance winning probability with profit margins.

### 4. Market Entry:

**Example: New Product Launch**

Two companies consider entering a new market segment.

Payoff Matrix:
```
              Company B
              Enter    Stay Out
Company A
Enter        (-2,-2)  (5,0)
Stay Out     (0,5)    (0,0)
```

Analysis:
- If both enter, they share the market and incur losses due to high competition (-2,-2)
- If only one enters, that company profits while the other earns nothing (5,0)
- If neither enters, both earn zero (0,0)

This explains why companies often use mixed strategies when deciding whether to enter new markets.

### 5. Labor Negotiations:

**Example: Union-Management Bargaining**

A union and management negotiate over wage increases.

Payoff Matrix:
```
             Management
             Accept    Reject
Union
High Demand  (2,1)    (-1,-2)
Low Demand   (1,2)    (0,0)
```

Analysis:
- Union demanding high wages that management accepts benefits union more (2,1)
- Union demanding low wages that management accepts benefits management more (1,2)
- Rejection of high demands hurts both sides due to strikes/lockouts (-1,-2)
- Rejection of low demands maintains status quo (0,0)

Game theory helps predict negotiation outcomes and explains the strategic nature of labor relations.

## 10. Limitations of Game Theory

1. **Assumption of Rationality**: Game theory assumes all players are rational, which may not always be true in real-world scenarios.

2. **Complete Information**: Many models assume players have complete information about payoffs, which is often not the case.

3. **Complexity**: As the number of players and strategies increases, games become exponentially more complex to solve.

4. **Equilibrium Selection**: Games may have multiple equilibria, making it difficult to predict which one will occur.

5. **Dynamic Aspects**: Static models may not capture the evolving nature of real-world strategic interactions.

## 11. Summary

Game theory provides a mathematical framework for analyzing strategic decision-making in competitive situations. Key concepts include:

1. **Two-person, zero-sum games**: Strictly competitive situations where one player's gain equals the other's loss

2. **Pure strategies**: Deterministic choices where players select a single strategy

3. **Mixed strategies**: Probabilistic choices where players randomize between strategies

4. **Dominance**: Identifying and eliminating inferior strategies

5. **Saddle points**: Equilibrium points in pure strategy games

6. **Minimax principle**: Maximizing the minimum payoff (for row player) or minimizing the maximum loss (for column player)

7. **Solution methods**: Algebraic and graphical approaches for finding optimal strategies

Game theory has wide applications in economics, business, political science, biology, and other fields where strategic interactions occur.