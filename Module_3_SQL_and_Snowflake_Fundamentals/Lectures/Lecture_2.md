# Lecture: 2. Basic SQL Queries: SELECT, INSERT, UPDATE, DELETE

### 1. Learning Objectives:
By the end of this lecture, learners will be able to:
- Understand and execute basic SQL queries: SELECT, INSERT, UPDATE, and DELETE.
- Identify the appropriate use cases for each type of query in database management.
- Apply these queries in practical scenarios, particularly in contexts related to sports analytics or game data management.

### 2. Introduction:
In this lecture, we will explore the foundational SQL commands essential for interacting with databases. Understanding these basic queries is crucial for anyone looking to master Data Structures and Algorithms (DSA), optimize Python code, and deepen their knowledge of databases and AI technologies.

SQL (Structured Query Language) is the standard language for managing and manipulating relational databases. As a fan of Chelsea F.C. and a gamer, you can appreciate how data drives decision-making in sports and gaming industries. For instance, analyzing player statistics or game performance data can significantly enhance strategies both on the field and in video games like Valorant or Minecraft.

### 3. Core Concepts:

#### **3.1 SELECT Statement**
- **Definition**: The SELECT statement retrieves data from one or more tables.
- **Syntax**: 
  ```sql
  SELECT column1, column2 FROM table_name WHERE condition;
  ```
- **Example**: To fetch player names and goals scored from a "players" table:
  ```sql
  SELECT player_name, goals_scored FROM players WHERE team = 'Chelsea F.C.';
  ```

#### **3.2 INSERT Statement**
- **Definition**: The INSERT statement adds new records to a table.
- **Syntax**: 
  ```sql
  INSERT INTO table_name (column1, column2) VALUES (value1, value2);
  ```
- **Example**: Adding a new player to the "players" table:
  ```sql
  INSERT INTO players (player_name, goals_scored) VALUES ('New Player', 0);
  ```

#### **3.3 UPDATE Statement**
- **Definition**: The UPDATE statement modifies existing records in a table.
- **Syntax**: 
  ```sql
  UPDATE table_name SET column1 = value1 WHERE condition;
  ```
- **Example**: Updating a player's goals scored:
  ```sql
  UPDATE players SET goals_scored = goals_scored + 1 WHERE player_name = 'Player X';
  ```

#### **3.4 DELETE Statement**
- **Definition**: The DELETE statement removes records from a table.
- **Syntax**: 
  ```sql
  DELETE FROM table_name WHERE condition;
  ```
- **Example**: Removing a player from the "players" table:
  ```sql
  DELETE FROM players WHERE player_name = 'Retired Player';
  ```

### 4. Practical Application:
In the context of Premier League Soccer, these SQL commands can be used to manage player statistics effectively. For instance, a sports analyst might use the SELECT statement to gather data on player performance across matches. 

**Scenario**: Imagine you’re managing a database for Chelsea F.C. You want to track how many goals each player has scored throughout the season. Using the SELECT query allows you to extract this vital information efficiently.

### 5. Summary:
In this lecture, we covered the four basic SQL commands: SELECT, INSERT, UPDATE, and DELETE. These commands are fundamental for database interaction and management. Remember that mastering these queries will not only aid your understanding of databases but will also support your broader career goals in technology and data analysis.

### 6. Next Steps:
In our next lecture, we will delve into more advanced SQL concepts such as JOINs and aggregations, which will enable you to analyze data across multiple tables effectively. To prepare, consider reviewing the previous lecture on database fundamentals and think about how you might combine data from different sources in your future projects.