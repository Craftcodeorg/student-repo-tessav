# Python Fundamentals and Optimization Techniques: Assignment

## Assignment Title: Analyzing Chelsea F.C. Player Statistics from the Premier League API

### Problem Statement
Develop a Python script that fetches player statistics for Chelsea F.C. from the Premier League API. The script should analyze the data to calculate key performance metrics such as average goals, assists, and minutes played. Additionally, optimize the code for performance to handle large datasets efficiently. This task will help you apply your knowledge of Python libraries and data analysis techniques, relevant to your career goals in robotics, semiconductors, and consumer electronics.

### Starter Code
Below is a basic framework to get you started. You will need to expand upon this code to complete the assignment.

```python
import requests
import pandas as pd

def fetch_chelsea_stats(api_url):
    # Step 1: Fetch data from the Premier League API
    response = requests.get(api_url)
    
    if response.status_code == 200:
        data = response.json()
        return data['players']  # Assuming 'players' is the key for player stats
    else:
        print("Error fetching data")
        return None

def analyze_player_stats(players):
    # Step 2: Convert the player data into a DataFrame
    df = pd.DataFrame(players)
    
    # Step 3: Calculate average goals, assists, and minutes played
    avg_goals = df['goals'].mean()
    avg_assists = df['assists'].mean()
    avg_minutes_played = df['minutes'].mean()
    
    return avg_goals, avg_assists, avg_minutes_played

# Test the function with a sample API URL (replace with actual URL)
api_url = 'https://api.football-data.org/v2/teams/61'  # Example for Chelsea F.C.
players_data = fetch_chelsea_stats(api_url)

if players_data:
    avg_goals, avg_assists, avg_minutes = analyze_player_stats(players_data)
    print(f"Average Goals: {avg_goals}")
    print(f"Average Assists: {avg_assists}")
    print(f"Average Minutes Played: {avg_minutes}")
```

### Detailed Instructions
1. **Modify the `fetch_chelsea_stats` Function**: Ensure that the function correctly handles different response statuses and extracts player statistics accurately. You may need to adjust the key used to access player data based on the actual structure of the API response.

2. **Enhance Data Analysis**:
   - Expand the `analyze_player_stats` function to include additional metrics such as total goals scored by all players and the player with the highest number of assists.
   - Use `df.groupby()` to analyze performance by position (e.g., forwards vs. defenders).

3. **Optimize Your Code**:
   - Consider using efficient data structures or methods to handle larger datasets.
   - Implement error handling for network issues and invalid data.

4. **Output Formatting**: 
   - Format your output to be more user-friendly. Consider using formatted strings or creating a summary report that includes all calculated metrics.

5. **Documentation**: Add comments and docstrings to your functions explaining their purpose and parameters.

### Criteria for Success and Evaluation
- **Functionality**: The script correctly fetches and analyzes Chelsea F.C. player statistics.
- **Performance**: Code optimization techniques are applied effectively, ensuring efficient handling of large datasets.
- **Code Quality**: The code is clean, well-documented, and follows best practices in Python programming.
- **Output**: The output is clear, user-friendly, and presents all required metrics in an organized manner.

### Submission
Submit your completed script along with a brief report (1-2 paragraphs) explaining your approach, any challenges you faced, and how you overcame them. This will help reinforce your learning and demonstrate your problem-solving skills in real-world applications.