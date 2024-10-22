### Assignment: Analyzing Game Data from Core Keeper

#### Problem Statement:
Create a Python program that analyzes game data from Core Keeper, focusing on player performance metrics. Your program should utilize arrays and lists to store and manipulate data efficiently. Specifically, it should implement searching and sorting algorithms to identify optimal strategies based on player statistics. This task will enhance your understanding of data structures while providing practical experience relevant to your interests in data analysis and gaming.

#### Starter Code:
Below is the starter code framework that you will build upon. It sets up the environment and includes comments to guide you on where to implement your solutions.

```python
# Starter code for analyzing game data from Core Keeper

def analyze_player_data(player_stats):
    """
    Analyze player statistics to find optimal strategies.
    
    :param player_stats: List of dictionaries containing player performance data
    :return: Sorted list of players based on a chosen metric (e.g., score)
    """
    
    # Step 1: Sort players based on their scores using a sorting algorithm
    sorted_players = sorted(player_stats, key=lambda x: x['score'], reverse=True)
    
    # Step 2: Identify players who exceed the average score by more than 10%
    average_score = sum(player['score'] for player in player_stats) / len(player_stats)
    top_players = [player for player in sorted_players if player['score'] > average_score * 1.1]
    
    return sorted_players, average_score, top_players

# Test the function with sample data
player_stats = [
    {'name': 'Player1', 'score': 150},
    {'name': 'Player2', 'score': 200},
    {'name': 'Player3', 'score': 180},
    {'name': 'Player4', 'score': 220},
]

sorted_players, average_score, top_players = analyze_player_data(player_stats)

print(f"Sorted Players: {sorted_players}")
print(f"Average Score: {average_score}")
print(f"Top Players Exceeding Average by 10%: {top_players}")
```

#### Detailed Instructions:
1. **Step 1**: Modify the `analyze_player_data` function to include additional metrics such as 'kills', 'deaths', or 'assists'. You can extend the `player_stats` list to include these metrics for each player.
   
2. **Step 2**: Implement a searching algorithm (e.g., binary search) to find a specific player's data based on their name. Ensure that the player data is sorted before performing the search.

3. **Step 3**: Enhance the output to include detailed feedback, such as the percentage by which each top player exceeds the average score. Format the output in a user-friendly manner.

4. **Step 4**: Add error handling to manage cases where the player name searched does not exist in the data.

#### Criteria for Success and Evaluation:
- **Success Criteria**:
  - The program correctly analyzes and sorts player data based on the chosen metrics.
  - The searching algorithm accurately finds specific player information.
  - The code is clean, well-documented, and follows best practices.
  - The output is formatted clearly and provides meaningful insights into player performance.

- **Evaluation Rubric**:
  - **Functionality (40%)**: Does the program perform all required tasks correctly?
  - **Code Quality (30%)**: Is the code clean, well-organized, and commented?
  - **Output Clarity (20%)**: Is the output user-friendly and informative?
  - **Error Handling (10%)**: Does the program handle potential errors gracefully?

This assignment aims to reinforce your understanding of arrays and lists while applying searching and sorting algorithms in a practical context relevant to your interests in gaming and data analysis.