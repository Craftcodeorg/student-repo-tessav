# Assignment: Create a Snowflake Instance for Music Preferences Analysis

## Problem Statement
You are tasked with creating a Snowflake instance to load and analyze data related to user interactions with music playlists or streaming services, specifically focusing on music preferences in genres such as EDM, R&B, and Jazz. This project aims to enhance your understanding of SQL commands (SELECT, INSERT, UPDATE, DELETE) while applying them to real-world data analysis scenarios relevant to consumer electronics and data processing.

## Starter Code
Below is a basic setup for connecting to a Snowflake instance and creating a table to store user music preferences. You will need to expand upon this starter code by adding the necessary SQL commands to insert, update, and analyze the data.

```python
import snowflake.connector

# Establish a connection to your Snowflake instance
def create_connection():
    conn = snowflake.connector.connect(
        user='YOUR_USERNAME',
        password='YOUR_PASSWORD',
        account='YOUR_ACCOUNT',
        warehouse='YOUR_WAREHOUSE',
        database='YOUR_DATABASE',
        schema='YOUR_SCHEMA'
    )
    return conn

# Create a table for storing music preferences
def create_music_preferences_table(conn):
    cursor = conn.cursor()
    try:
        cursor.execute("""
            CREATE TABLE IF NOT EXISTS music_preferences (
                user_id INT,
                genre VARCHAR,
                interaction_count INT,
                last_interaction TIMESTAMP
            );
        """)
        print("Table created successfully.")
    except Exception as e:
        print(f"Error creating table: {e}")
    finally:
        cursor.close()

# Connect to Snowflake and create the table
connection = create_connection()
create_music_preferences_table(connection)
connection.close()
```

## Detailed Instructions
### Step 1: Insert Data
Modify the starter code to include a function that allows you to insert new records into the `music_preferences` table. Use the INSERT SQL command to add data for at least three users with their respective music genre preferences.

### Step 2: Update Data
Create a function that updates the `interaction_count` for a specific user when they interact with a genre. This function should take `user_id`, `genre`, and the number of interactions as parameters. Use the UPDATE SQL command for this task.

### Step 3: Select Data
Implement a function that retrieves all records from the `music_preferences` table where the genre is either EDM, R&B, or Jazz. This function should use the SELECT SQL command and return the results in a user-friendly format.

### Step 4: Delete Data
Add functionality to delete a user’s record from the `music_preferences` table based on their `user_id`. Use the DELETE SQL command for this operation.

### Step 5: Analyze Data
Finally, write a function that analyzes the data and identifies which genre has the highest interaction count overall. This analysis will help you understand user preferences better.

## Criteria for Success and Evaluation
**Success Criteria:**
- The functions for inserting, updating, selecting, and deleting records are implemented correctly.
- The code is clean, well-documented, and follows best practices.
- The output of the analysis clearly indicates which genre has the highest interaction count.
- You can successfully connect to your Snowflake instance and manipulate data as required.

**Evaluation Rubric:**
- **Functionality (50%)**: Does the code perform all required operations correctly?
- **Code Quality (30%)**: Is the code clean, well-organized, and properly commented?
- **Output Clarity (20%)**: Are the results of the analysis presented in a clear and understandable manner?

This assignment will help you apply SQL concepts in a practical context while contributing to your learning goals in data analysis and processing within the consumer electronics industry.