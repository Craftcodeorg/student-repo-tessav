### Assignment: Build a SQL Database for Managing Game Statistics

#### Problem Statement
Create a SQL database to manage and analyze game statistics for multiple sports, including basketball, soccer, and video games. The database should allow you to perform complex queries that involve joins and aggregations to derive insights from the data. This assignment is particularly relevant for applications in robotics, semiconductors, and consumer electronics, where data analysis plays a crucial role in performance optimization and decision-making.

#### Starter Code
Below is a basic SQL schema to get you started. You will need to expand upon this by adding sample data and writing queries to extract meaningful insights.

```sql
-- Create table for basketball players
CREATE TABLE basketball_players (
    player_id INT PRIMARY KEY,
    name VARCHAR(100),
    team VARCHAR(100),
    points INT,
    assists INT,
    rebounds INT
);

-- Create table for soccer players
CREATE TABLE soccer_players (
    player_id INT PRIMARY KEY,
    name VARCHAR(100),
    team VARCHAR(100),
    goals INT,
    assists INT,
    matches_played INT
);

-- Create table for video game players
CREATE TABLE video_game_players (
    player_id INT PRIMARY KEY,
    name VARCHAR(100),
    game VARCHAR(100),
    score INT,
    matches_played INT
);
```

#### Detailed Instructions

1. **Create the Database**: 
   - Use the starter SQL code to create the three tables: `basketball_players`, `soccer_players`, and `video_game_players`. Ensure that each table has relevant fields for storing player statistics.

2. **Insert Sample Data**:
   - Populate each table with at least five records of sample data. For example:
   ```sql
   INSERT INTO basketball_players (player_id, name, team, points, assists, rebounds) VALUES
   (1, 'LeBron James', 'Lakers', 25, 7, 8),
   (2, 'Stephen Curry', 'Warriors', 30, 6, 5);
   ```

3. **Write Queries**:
   - Write SQL queries that utilize complex joins and aggregations. Here are some examples of what you might implement:
     - Query to find the average points scored by basketball players in each team.
     - Query to join soccer players with their teams and find the total goals scored by each team.
     - Query to find video game players who have played more than a certain number of matches and their average score.

4. **Use Aggregation Functions**:
   - Implement aggregation functions such as `SUM()`, `AVG()`, and `COUNT()` in your queries to provide insights into the data. For example:
   ```sql
   SELECT team, AVG(points) AS average_points
   FROM basketball_players
   GROUP BY team;
   ```

5. **Document Your Work**:
   - Ensure your SQL code is well-documented with comments explaining the purpose of each table, the sample data inserted, and the logic behind your queries.

#### Criteria for Success and Evaluation

- **Database Structure**: 
  - The database must be correctly structured with appropriate tables and relationships.
  
- **Data Insertion**: 
  - At least five records should be inserted into each table.

- **Query Complexity**: 
  - Queries must demonstrate the use of joins and aggregation functions effectively.

- **Code Quality**: 
  - The SQL code should be clean, well-organized, and properly commented.

- **Insights Derived**: 
  - The queries should provide meaningful insights relevant to the sports being analyzed.

- **Documentation**: 
  - Clear documentation should accompany your SQL scripts, explaining your thought process and any assumptions made.

By completing this assignment, you will reinforce your understanding of SQL fundamentals while applying them to a practical scenario that aligns with your interests in sports analytics and data processing in robotics and consumer electronics.