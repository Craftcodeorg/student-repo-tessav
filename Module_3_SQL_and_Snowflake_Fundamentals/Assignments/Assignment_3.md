### Assignment: Analyzing Chelsea F.C. Performance Data with SQL and Python

#### Problem Statement:
Create a Python application that integrates SQL queries with Snowflake to analyze Chelsea F.C.'s performance data over the season. The application should fetch player statistics and match results from a Snowflake database, allowing you to visualize trends in player performance, such as goals scored, assists, and overall contributions during various matches. This task will help you apply the concepts of SQL joins learned in the lecture, specifically focusing on INNER and LEFT joins.

#### Starter Code:
Below is a basic framework for your application. It includes a function to connect to the Snowflake database and a placeholder for your SQL query. You'll need to expand upon this code to implement the necessary functionality.

```python
import snowflake.connector
import pandas as pd
import matplotlib.pyplot as plt

# Function to connect to Snowflake
def connect_to_snowflake(user, password, account):
    conn = snowflake.connector.connect(
        user=user,
        password=password,
        account=account
    )
    return conn

# Function to fetch Chelsea F.C. performance data
def fetch_performance_data(conn):
    # Placeholder for your SQL query
    query = """
    SELECT Players.name, SUM(Matches.goals) AS total_goals, SUM(Matches.assists) AS total_assists
    FROM Players
    LEFT JOIN Matches ON Players.id = Matches.player_id
    WHERE Players.team = 'Chelsea F.C.'
    GROUP BY Players.name
    ORDER BY total_goals DESC;
    """
    
    # Execute the query and fetch data into a DataFrame
    df = pd.read_sql(query, conn)
    return df

# Main function to run the analysis
def main():
    # Connect to Snowflake (replace with your credentials)
    conn = connect_to_snowflake('your_username', 'your_password', 'your_account')
    
    # Fetch performance data
    performance_data = fetch_performance_data(conn)
    
    # Visualize the data
    plt.bar(performance_data['name'], performance_data['total_goals'])
    plt.xlabel('Players')
    plt.ylabel('Total Goals')
    plt.title('Chelsea F.C. Player Goals Analysis')
    plt.xticks(rotation=45)
    plt.show()

# Run the application
if __name__ == "__main__":
    main()
```

#### Detailed Instructions:
1. **Database Connection**: Modify the `connect_to_snowflake` function with your actual Snowflake credentials. Ensure you handle any exceptions that may arise during the connection process.

2. **SQL Query**: Update the SQL query in the `fetch_performance_data` function to include any additional statistics you want to analyze (e.g., total assists, yellow cards). Make sure to use appropriate JOINs based on your database schema.

3. **Data Visualization**: Enhance the visualization section by adding more plots (e.g., assists vs. goals) or using different types of visualizations (like pie charts for contributions). Ensure your plots are well-labeled for clarity.

4. **Output Formatting**: Consider formatting the output of your analysis neatly in the console before visualizing it. For instance, print the DataFrame before plotting.

5. **Documentation**: Add comments throughout your code explaining each section's purpose and any assumptions you've made regarding the data structure.

#### Criteria for Success and Evaluation:
- **Functionality**: The application correctly connects to Snowflake, retrieves data using SQL joins, and visualizes player statistics.
- **Code Quality**: The code is clean, well-structured, and follows best practices, including proper error handling.
- **Documentation**: The code is adequately commented, making it easy to understand the flow and logic.
- **Visual Output**: The visualizations are clear, informative, and effectively communicate the insights derived from the data.

This assignment encourages hands-on practice with real-world relevance in sports analytics while reinforcing your understanding of SQL joins and Python programming. Good luck!