# Assignment: Create a Data Processing Application for Minecraft Game Statistics

## Problem Statement
You are tasked with developing a Python application that reads game statistics from Minecraft and outputs key insights regarding player performance and game dynamics. This assignment will utilize the fundamental data types and structures covered in the lecture, such as lists, dictionaries, and floats, to analyze and present the data effectively. The insights generated will help players understand their gameplay better and optimize their strategies.

## Starter Code
Below is a basic code framework that you will expand upon. This starter code sets up the environment and includes comments to guide you on where to implement your solutions.

```python
# Starter code for analyzing Minecraft game statistics

def analyze_game_statistics(stats):
    """
    Analyzes game statistics and returns insights about player performance.
    
    Parameters:
    stats (list of dict): A list containing dictionaries of player statistics.
    
    Returns:
    dict: A dictionary containing average scores and top performers.
    """
    total_score = 0
    player_count = len(stats)
    player_performance = {}

    # Step 1: Calculate total scores and store player performance
    for player_stats in stats:
        player_name = player_stats['player_name']
        score = player_stats['score']
        total_score += score
        player_performance[player_name] = score

    # Step 2: Calculate average score
    average_score = total_score / player_count if player_count > 0 else 0
    
    # Step 3: Identify top performers (players with scores above average)
    top_performers = [name for name, score in player_performance.items() if score > average_score]

    # Return results (students will need to format the output)
    return {
        'average_score': average_score,
        'top_performers': top_performers
    }

# Test the function with sample data
game_stats = [
    {'player_name': 'Player1', 'score': 150},
    {'player_name': 'Player2', 'score': 200},
    {'player_name': 'Player3', 'score': 120},
]

results = analyze_game_statistics(game_stats)
print(f"Average Score: {results['average_score']}")
print(f"Top Performers: {results['top_performers']}")
```

## Detailed Instructions
1. **Step 1**: Modify the function to handle different types of statistics. Extend the `stats` list to include other metrics such as `kills`, `deaths`, and `time_played`. Update the calculation logic to include these metrics in your analysis.

2. **Step 2**: Enhance the output to provide more detailed feedback. For instance, return not only the average score but also the highest score, lowest score, and the number of players who achieved each of these scores.

3. **Step 3**: Implement error handling for cases where the input data may be incomplete or incorrectly formatted. Ensure your function can handle missing player statistics gracefully.

4. **Step 4**: Format the output to present insights in a user-friendly manner. You might want to print a summary report that includes all calculated metrics.

## Criteria for Success and Evaluation
Your assignment will be evaluated based on the following criteria:

- **Functionality**: The application correctly calculates and outputs the required statistics based on the input data.
- **Code Quality**: Your code should be clean, well-organized, and properly commented. Follow best practices for Python programming.
- **User Experience**: The output should be formatted clearly and be easy to understand.
- **Error Handling**: Your application should handle potential errors gracefully without crashing.

### Success Criteria:
- The function correctly calculates the average score, highest score, lowest score, and identifies top performers.
- The code is clean, well-documented, and follows best practices.
- The output is formatted in a clear and user-friendly manner, providing a comprehensive overview of player performance.

By completing this assignment, you will not only reinforce your understanding of Python data types and structures but also gain practical experience in data processing relevant to your interests in gaming analytics and robotics. Good luck!