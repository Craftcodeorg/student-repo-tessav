# Assignment: Basketball Game Simulation and Performance Metrics

## Problem Statement
Create a Python program that simulates a basketball game and calculates player performance metrics such as points scored, assists, and rebounds. The program should utilize conditionals and loops to manage the game flow and player statistics. This task is designed to reinforce the concepts of control flow, conditionals, and loops discussed in Lecture 3, while also providing a practical application relevant to your interests in sports analytics.

## Starter Code
Below is the basic framework for your basketball game simulation. You will need to expand upon this code to implement the full functionality as described in the instructions.

```python
# Starter code for simulating a basketball game

# Define player statistics
players = {
    'Player 1': {'points': 0, 'assists': 0, 'rebounds': 0},
    'Player 2': {'points': 0, 'assists': 0, 'rebounds': 0},
    'Player 3': {'points': 0, 'assists': 0, 'rebounds': 0}
}

def simulate_game():
    # Step 1: Simulate a series of plays in the game
    for quarter in range(1, 5):
        print(f"Quarter {quarter}:")
        for player in players:
            # Simulate random performance metrics (you can replace this with actual game logic)
            players[player]['points'] += random.randint(0, 10)  # Points scored
            players[player]['assists'] += random.randint(0, 5)  # Assists made
            players[player]['rebounds'] += random.randint(0, 3)  # Rebounds made
            
            # Step 2: Print each player's performance after each play
            print(f"{player} - Points: {players[player]['points']}, Assists: {players[player]['assists']}, Rebounds: {players[player]['rebounds']}")
    
    # Step 3: Calculate and display total performance metrics
    display_performance_metrics()

def display_performance_metrics():
    print("\nFinal Performance Metrics:")
    for player, stats in players.items():
        print(f"{player}: {stats['points']} points, {stats['assists']} assists, {stats['rebounds']} rebounds")

# Start the game simulation
simulate_game()
```

## Detailed Instructions
1. **Import Required Libraries**: At the beginning of your code, import the `random` library to simulate random performance metrics.
   ```python
   import random
   ```

2. **Enhance Player Statistics**: Modify the `simulate_game` function to include more realistic scoring logic. For example, introduce conditions that determine whether a player scores based on their current points or assists.

3. **Implement Conditional Logic**: After updating player stats, use conditionals to determine if a player has achieved a certain milestone (e.g., scoring over 20 points). If they do, print a congratulatory message.

   Example:
   ```python
   if players[player]['points'] > 20:
       print(f"Congratulations {player}! You've scored over 20 points!")
   ```

4. **Loop Through Game Quarters**: Ensure your simulation accurately represents four quarters of play. Use nested loops to simulate plays within each quarter.

5. **Calculate Total Performance**: In the `display_performance_metrics` function, calculate the total points scored by all players combined and display it alongside individual player stats.

6. **Code Quality and Documentation**: Ensure that your code is well-documented with comments explaining each section's purpose. Follow best practices for naming conventions and code structure.

## Criteria for Success and Evaluation
Your assignment will be evaluated based on the following criteria:

- **Functionality**: The program should correctly simulate a basketball game and accurately calculate player performance metrics.
- **Use of Control Flow**: Effective use of conditionals and loops to manage game logic.
- **Code Quality**: The code should be clean, well-organized, and include appropriate comments.
- **Output Clarity**: The final output should be user-friendly and clearly present player statistics and milestones.

### Success Criteria:
- The program runs without errors and simulates a basketball game.
- Player statistics are updated correctly throughout the game.
- Conditional messages are displayed when players reach performance milestones.
- The final performance metrics are clearly presented.

This assignment will help you apply your knowledge of Python control flow while engaging with a real-world scenario related to sports analytics. Good luck!