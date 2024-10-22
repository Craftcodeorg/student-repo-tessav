### Module Title: Python Fundamentals and Optimization Techniques

### Exercise Requirements

#### 1. Problem Statement
You are tasked with optimizing a Python script that processes game data from Valorant. The script collects player statistics, including kills, deaths, and assists, and calculates the KDA (Kill/Death/Assist) ratio for each player. Your goal is to improve the script's efficiency by utilizing appropriate data types and structures learned in the lecture, while also ensuring it adheres to best practices in Python programming.

#### 2. Fill-in-the-Blank Starter Code
```python
# Starter code for processing Valorant player statistics

def calculate_kda(player_stats):
    """
    Calculate the KDA ratio for each player based on their statistics.
    
    Args:
    player_stats (dict): A dictionary containing player names as keys and 
                         a dictionary of their kills, deaths, and assists as values.
    
    Returns:
    dict: A dictionary with player names as keys and their KDA ratios as values.
    """
    kda_ratios = {}  # Initialize an empty dictionary to store KDA ratios
    
    for player, stats in player_stats.items():
        # Extract kills, deaths, and assists from the player's stats
        kills = _______  # Fill in the appropriate key from stats
        deaths = _______  # Fill in the appropriate key from stats
        assists = _______  # Fill in the appropriate key from stats
        
        # Calculate KDA ratio
        if deaths > 0:  # To avoid division by zero
            kda_ratio = (kills + assists) / deaths
        else:
            kda_ratio = _______  # Define a KDA ratio for players with zero deaths
        
        # Store the KDA ratio in the kda_ratios dictionary
        kda_ratios[player] = kda_ratio
    
    return kda_ratios

# Sample player statistics for testing the function
player_stats = {
    "Player1": {"kills": 10, "deaths": 2, "assists": 5},
    "Player2": {"kills": 8, "deaths": 0, "assists": 3},
    "Player3": {"kills": 5, "deaths": 4, "assists": 2}
}

# Test the function with the sample data
print(calculate_kda(player_stats))
```

#### 3. Hints
- **Hint 1**: Remember that you can access values in a dictionary using their keys. Look closely at how the player statistics are structured.
- **Hint 2**: When calculating the KDA ratio, consider what should happen if a player has no deaths. What value would make sense in that scenario?
- **Hint 3**: Ensure that you include error handling for cases where the data might not be as expected (e.g., missing keys).

#### 4. Expected Outcome
The student should be able to fill in the blanks correctly to complete the function. The completed function should:
- Efficiently calculate the KDA ratio for each player using dictionary data structures.
- Handle cases where a player has zero deaths gracefully.
- Return a well-structured dictionary with player names as keys and their KDA ratios as values.

The final solution should demonstrate an understanding of how to apply Python's data types and structures effectively in a real-world scenario related to gaming analytics. Additionally, it should include comments explaining each step of the process, following best practices for code readability and maintenance.

### Integration
This exercise is structured to promote critical thinking and application of Python fundamentals while resonating with your interests in gaming and data analysis. It aligns with your goal of mastering Python optimizations and real-world data processing projects in your field of work.