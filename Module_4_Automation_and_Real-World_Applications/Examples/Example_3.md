# Module Title: Automation and Real-World Applications

## Example 3: Building a Simple Dashboard with Streamlit

### 1. Introduction
In this section, we will explore the significance of building a simple dashboard using Streamlit as covered in the lecture on automating data collection from APIs, specifically the Premier League API. This example is crucial for professionals in the fields of Robotics, semiconductors, and consumer electronics as it demonstrates how to visualize and interact with real-time data effectively.

Streamlit allows developers to create web applications for data visualization with minimal effort. By integrating data from APIs like the Premier League API, professionals can create dashboards that display relevant metrics, automate reporting processes, and provide insights into performance metrics. This aligns with your career goals of mastering data processing and automation while enhancing your skills in Python optimization and database management.

### 2. Code Snippet
Here’s a well-commented code snippet that illustrates how to build a simple dashboard with Streamlit to display soccer match data retrieved from the Premier League API:

```python
import streamlit as st
import requests

# Function to fetch match data from the Premier League API
def fetch_match_data(api_key):
    url = "https://api.premierleague.com/v1/matches"
    headers = {
        "Authorization": f"Bearer {api_key}"
    }
    
    try:
        response = requests.get(url, headers=headers)
        response.raise_for_status()  # Raise an error for bad responses
        return response.json()['matches']
    except requests.exceptions.RequestException as e:
        st.error(f"Error fetching data: {e}")
        return []

# Streamlit app layout
st.title("Premier League Match Dashboard")
api_key = st.text_input("Enter your API Key:", type="password")

if api_key:
    matches = fetch_match_data(api_key)
    
    if matches:
        st.subheader("Current Matches")
        for match in matches:
            home_team = match['homeTeam']['name']
            away_team = match['awayTeam']['name']
            match_status = match['status']
            st.write(f"{home_team} vs {away_team} - Status: {match_status}")
    else:
        st.write("No matches available.")
else:
    st.write("Please enter your API key to fetch match data.")
```

### 3. Explanation
- **Importing Libraries**: The code begins by importing the necessary libraries, `streamlit` for creating the web app and `requests` for making API calls.
  
- **Function Definition**: The `fetch_match_data` function is defined to handle API requests. It takes an API key as an argument, constructs the request, and handles potential errors using a try-except block. This ensures that any issues with the request do not crash the application.

- **Streamlit App Layout**: The Streamlit app layout is established using `st.title` and `st.text_input` to create a user-friendly interface where users can input their API key.

- **Data Display**: Once the API key is provided, the app fetches match data. If matches are found, it displays each match's home and away teams along with their current status. If no matches are available or if there’s an error, appropriate messages are displayed.

This code implements key concepts from the lecture by demonstrating how to access an API, handle JSON data, and present it in a user-friendly format. 

### 4. Application
A real-world application of this concept within Robotics, semiconductors, and consumer electronics could be in creating dashboards for monitoring equipment performance or analyzing operational data. For instance, in semiconductor manufacturing, engineers can use similar dashboards to visualize machine performance metrics in real-time, automate alerts for maintenance needs, and optimize production schedules based on current output data.

By leveraging automated data collection through APIs and presenting it via interactive dashboards like Streamlit, organizations can enhance their decision-making processes, improve operational efficiency, and reduce downtime—all critical factors in competitive industries like robotics and electronics.

### Integration
This content is structured to facilitate easy integration into your learning platform. Each section is clearly defined with headings for better readability and understanding. Utilizing markdown formatting ensures that the content is visually appealing and accessible for learners seeking to enhance their skills in automation and real-world applications.