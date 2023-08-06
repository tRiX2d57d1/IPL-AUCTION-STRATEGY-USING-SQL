# IPL-AUCTION-STRATEGY-USING-POSTGRESQL
<details>
 <summary><h2>Table Of Contents</h2></summary>

   - [Aim](#aim) 
   - [Prerequisites](#pre)
   - [History](#his) 
   - [Implementation](#imp)
   - [Dashboard Link](#link)
   - [Result](#res)

</details>

<a id="aim"></a>
### Aim 
The motive behind this project was to develop an auction strategy for new IPL franchise by analyzing past IPL data to create a balanced and powerful team.

<a id="pre"></a>
### Prerequisites
  - Understanding of GROUP BY, ORDER BY clauses and aggregate functions.
  - Knowledge about conditional statements
  - In-depth knowledge of Joins and Subqueries.
   
<a id="his"></a>
### History
Indian Premier League (IPL) is a professional Twenty20 cricket league in India contested during March or April and May of every year by eight teams representing eight different cities or states in India. The league was founded by the Board of Control for Cricket in India (BCCI) in 2007. The IPL tournament involves each team playing every other team twice in a home-and-away, double round-robin format. At the conclusion of the double round-robin league, on the basis of aggregate
points, the top four teams qualify for the playoffs. In this stage, the top two teams compete with each other (in a match titled "Qualifier 1"), as do the remaining two teams (in a match titled "Eliminator"). While the winner of Qualifier 1 directly qualifies for the final match, the losing team gets another chance to qualify for the final match by playing the winning team of the Eliminator match; this match is titled Qualifier 2. The winner of this subsequent Qualifier 2 match moves onto the final match. The team that wins the final match is crowned the Indian Premier League champion. In a coming season a new team is being added to the Indian Premier League (IPL) and a mega auction is being held to build the team's squad, there are a few factors that the team's management and auction strategy would likely consider:
1. Budget: The team would need to allocate a budget for the auction and decide how much money to spend on each player.
2. Team needs: The team would need to identify the positions and types of players they need to fill out their squad and target those players in the auction.
3. Player availability: The team would need to assess the availability of players, including their current contracts with other teams and their international commitments.
4. Player form: The team would need to consider the recent form and performances of the players they are targeting.
5. Player value: The team would need to consider the market value of the players they are interested in and decide how much they are willing to pay for them.
To build a strong and balanced squad, the team's management would likely need to strike a balance between all of these factors and come up with a well-thought-out auction strategy.

<a id="imp"></a>
### Implementation
1. There are various kinds of batsman who can add value to the team. The first step is to get aggressive batsman by finding the strike rate of atleast 10 players who have faced atleast 500 balls. To find the Strike Rate of a player, the following formula has to be used:
```
Strike Rate of batsman = (Total Runs Scored \ Number of balls faced ) * 100
```

2. The next step is to find good anchor batsman with good average batting score and that can be found by using the formula:
```
Average = Total Runs Scored \ Number of times the player has been dismissed
```

3. Hard-hitting players are batsman who have scored most runs in boundary (4 and 6), we can also found the boundary percentage using the formula:
```
Boundary Percentage = Runs in Boundary \ Total Runs Scored 
```
  
4. Bidding on bowlers is as important as bidding on batsman and lower the economy of the bowler, better the bowler is so, to bid on bowlers with good economy, the formula to be used is as follows:
```
Economy of Bowler = Total Runs Conceded \ Total Overs Bowled
```
  
5. To get bowlers who have taken most wickets, we have to calculate the Strike Rate of the bowler and that can be done by using the formula:
```
Strike Rate of bowler = Number of Balls Bowled \ Total Wickets Taken
```
  
6. There are batsman with good strike rate,who can score runs and bowlers with amazing strike rate, who have taken most wickets with minimum balls and there are all-rounders who can do both. To find all-rounders for the team, we have to find the batsman strike rate and bowler strike rate and use inner join to query out players who are good common strike rates.

<a id="link"></a>
### Link to Tableau Dashboard
[IPL Auction Strategy Dashboard](https://public.tableau.com/views/IPLAuctionStrategyDashboard/IPLDashboard?:language=en-US&:display_count=n&:origin=viz_share_link)

<a id="res"></a>
### Result
By leveraging the power of Postgresql, I developed an auction strategy for the new IPL franchise by creating a powerful team.



