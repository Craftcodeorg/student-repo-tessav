### Module Title: SQL and Snowflake Fundamentals

---

### Exercise Requirements

#### 1. Problem Statement:
As a data analyst for Chelsea F.C., your task is to extract player statistics from the club's database to assist in performance analysis for the upcoming season. You need to write SQL queries that will help the coaching staff identify key players based on various performance metrics. Specifically, you will need to find:

- Players who scored more than 10 goals last season.
- Players who provided more than 5 assists last season.
- The average number of minutes played by players in the last season.

Use the following SQL structure to complete the tasks:

```sql
-- Query to find players who scored more than 10 goals
SELECT name FROM players WHERE goals > 10;

-- Query to find players who provided more than 5 assists
SELECT name FROM players WHERE assists > 5;

-- Query to calculate the average minutes played by all players
SELECT AVG(minutes_played) FROM players;
```

Make sure to consider how this data can influence coaching decisions and player training focus.

---

#### 2. Fill-in-the-Blank Starter Code:
Below is a starter code snippet that you will need to complete. This code is designed to help you understand how to calculate player performance metrics programmatically using Python.

```python
# Starter code for implementing lecture concepts
def get_player_performance(database_connection):
    """
    This function retrieves player performance statistics from the Chelsea F.C. database.
    
    Parameters:
    database_connection (object): The connection object to the database.
    
    Returns:
    dict: A dictionary containing player names and their respective statistics.
    """
    
    # Initialize an empty dictionary to store player statistics
    player_stats = {}
    
    # SQL query to select player names and their goals
    query = "SELECT name, goals, assists, minutes_played FROM players;"
    
    # Execute the query and fetch results
    cursor = database_connection.cursor()
    cursor.execute(query)
    
    # Fetch all rows from the executed query
    results = cursor.fetchall()
    
    # Loop through the results and populate the player_stats dictionary
    for row in results:
        name = row[0]  # Player's name
        goals = row[1]  # Goals scored
        assists = row[2]  # Assists made
        minutes_played = row[3]  # Minutes played
        
        # Fill in the player_stats dictionary
        player_stats[name] = {
            'goals': goals,
            'assists': assists,
            'minutes_played': minutes_played
        }
    
    return player_stats

# Example usage (assuming a valid database connection)
# db_connection = _______  # Establish a connection to your database here
# performance_data = get_player_performance(db_connection)
# print(performance_data)
```

---

#### 3. Hints:
- **Hint 1**: Think about how you can use the `SELECT` command to filter results based on specific criteria such as goals and assists.
- **Hint 2**: Remember that aggregate functions like `AVG()` can help you calculate averages, which is useful for analyzing overall player performance.
- **Hint 3**: Ensure that your SQL queries are structured correctly and test them in a safe environment before integrating them into your application.

---

#### 4. Expected Outcome:
By completing this exercise, you should be able to:
- Write SQL queries that accurately extract player statistics from a Chelsea F.C. database.
- Understand how to connect to a database using Python and execute SQL commands.
- Demonstrate an understanding of how these statistics can impact coaching strategies and player development.
- Ensure that your code is well-commented, follows best practices, and includes error handling for potential database connection issues.

---

### Integration
This exercise is designed to provide practical experience in SQL and data manipulation, aligning with your interests in data analysis and your career goals in technology. Please ensure that your submissions are organized clearly, with proper documentation of your thought process and code functionality.