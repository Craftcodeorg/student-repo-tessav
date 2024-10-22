# Assignment: Design a Data Structure for Chelsea F.C. Player Statistics

### Problem Statement
Create a data structure that efficiently stores and retrieves player statistics for Chelsea F.C. This data structure should allow for the addition of new player statistics, retrieval of player information, and the ability to analyze player performance over time. You will implement this using concepts learned in the lecture on data structures, particularly focusing on arrays and dictionaries (hash maps) for efficient data storage and retrieval.

### Starter Code
Below is a basic framework to get you started. Your task is to expand this code by implementing the necessary methods to manage player statistics.

```python
class PlayerStats:
    def __init__(self):
        # Using a dictionary to store player statistics
        self.stats = {}

    def add_player(self, name, goals=0, assists=0):
        # Step 1: Add a new player with initial statistics
        self.stats[name] = {'goals': goals, 'assists': assists}

    def update_stats(self, name, goals=0, assists=0):
        # Step 2: Update existing player's statistics
        if name in self.stats:
            self.stats[name]['goals'] += goals
            self.stats[name]['assists'] += assists
        else:
            print(f"Player {name} not found.")

    def get_stats(self, name):
        # Step 3: Retrieve statistics for a specific player
        return self.stats.get(name, "Player not found.")

    def display_all_stats(self):
        # Step 4: Display all players' statistics
        for player, stats in self.stats.items():
            print(f"Player: {player}, Goals: {stats['goals']}, Assists: {stats['assists']}")

# Example usage:
team_stats = PlayerStats()
team_stats.add_player("Mason Mount", goals=5, assists=3)
team_stats.update_stats("Mason Mount", goals=1)
print(team_stats.get_stats("Mason Mount"))
team_stats.display_all_stats()
```

### Detailed Instructions
1. **Step 1: Add a Player**
   - Implement the `add_player` method to allow the addition of new players along with their initial goals and assists. Ensure that if a player already exists, you handle this gracefully.

2. **Step 2: Update Player Statistics**
   - Enhance the `update_stats` method to accept additional parameters for goals and assists. This method should increment the existing statistics for the player.

3. **Step 3: Retrieve Player Statistics**
   - The `get_stats` method should return the player's statistics in a user-friendly format. If the player does not exist, return a message indicating that.

4. **Step 4: Display All Player Statistics**
   - Implement the `display_all_stats` method to iterate through all players in the dictionary and print their statistics in a clear format.

5. **Step 5: Test Your Code**
   - After implementing the above methods, test your class by adding several players and updating their statistics. Ensure that you can retrieve and display the information correctly.

### Criteria for Success and Evaluation
Your assignment will be evaluated based on the following criteria:

- **Functionality**: All methods (add, update, retrieve, display) work correctly.
- **Code Quality**: The code is clean, well-organized, and follows Python best practices.
- **Documentation**: Adequate comments are provided to explain the purpose of each method and any complex logic.
- **Testing**: You have tested your implementation with various scenarios to ensure robustness.

### Conclusion
This assignment will help you apply the concepts learned in the lecture about data structures while focusing on a real-world application relevant to your interests in Premier League Soccer and your career goals in technology. By completing this task, you will gain hands-on experience with data manipulation and retrieval using Python.