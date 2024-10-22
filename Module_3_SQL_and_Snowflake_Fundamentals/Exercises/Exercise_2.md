### Module Title: SQL and Snowflake Fundamentals

### Exercise Requirements

1. **Problem Statement**: 
   You are tasked with analyzing the performance metrics of players from two different games: Valorant and Premier League Soccer (Chelsea F.C.). Your goal is to create a report that shows how player performance in Valorant correlates with their performance in soccer. You will need to use SQL JOINs to combine data from two tables: `valorant_players` and `soccer_players`. 

   The `valorant_players` table contains the following columns:
   - `player_id`
   - `player_name`
   - `kills`
   - `deaths`
   - `assists`

   The `soccer_players` table contains:
   - `player_id`
   - `player_name`
   - `goals_scored`
   - `assists`
   - `matches_played`

   Your task is to write an SQL query that retrieves the player names, total kills, total goals scored, and assists from both games for players who have participated in both Valorant and soccer. 

2. **Fill-in-the-Blank Starter Code**: 
   Below is the starter SQL code with blanks for you to fill in:

   ```sql
   -- SQL query to analyze player performance across games
   SELECT 
       v.player_name AS valorant_player,
       v.kills AS total_kills,
       s.goals_scored AS total_goals,
       v.assists + s.assists AS total_assists
   FROM 
       valorant_players v
   JOIN 
       soccer_players s ON v.player_id = s.player_id
   WHERE 
       _______  -- Add condition to filter players based on specific criteria if needed
   ORDER BY 
       total_goals DESC;  -- Order by total goals scored
   ```

3. **Hints**: 
   - Remember that the JOIN operation combines rows from two or more tables based on a related column between them. In this case, you will use the `player_id` as the linking key.
   - Think about whether you want to include all players or only those who have a certain level of performance in either game. You might want to add a WHERE clause to filter results based on performance metrics.
   - Consider using aggregate functions if you need to summarize data further, although this specific task does not require it.

4. **Expected Outcome**: 
   Upon completing the SQL query, you should be able to retrieve a list of players who play both Valorant and soccer, showing their total kills in Valorant, goals scored in soccer, and combined assists from both games. The final output should be well-structured, making it easy to analyze how performance metrics in one game relate to another.

### Integration
- Ensure that the exercise content is well-structured with clear headings and sections for easy parsing and integration into the learning platform. Use markdown for formatting, and include any necessary files or resources as links. 

This exercise not only reinforces your understanding of SQL JOINs but also applies your interest in sports analytics, making it relevant to your career goals in data analysis and technology.