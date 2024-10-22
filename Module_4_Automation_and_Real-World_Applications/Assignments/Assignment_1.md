# Assignment: End-to-End Automation Project for Chelsea F.C. Data Analysis

### Problem Statement:
Create an end-to-end automation project that collects, processes, and visualizes soccer match data for Chelsea F.C. This project will involve using APIs to fetch match data, utilizing Pandas for data manipulation, and employing Streamlit to create an interactive dashboard for visualizing the results. The goal is to automate the process of gathering and analyzing soccer data, which can be applied in various real-world scenarios, particularly in sports analytics and data-driven decision-making.

### Starter Code:
The following starter code provides a basic structure for your project. It includes functions to fetch data from an API, process it using Pandas, and set up a Streamlit app.

```python
import requests
import pandas as pd
import streamlit as st

# Function to fetch match data from the API
def fetch_match_data(api_url):
    response = requests.get(api_url)
    if response.status_code == 200:
        return response.json()
    else:
        st.error("Failed to fetch data from API")
        return None

# Function to process match data
def process_match_data(data):
    df = pd.DataFrame(data)
    # Add your data processing logic here (e.g., filtering, aggregating)
    return df

# Streamlit app setup
def main():
    st.title("Chelsea F.C. Match Data Analysis")
    
    # Step 1: Fetch match data
    api_url = 'https://api.soccerdata.com/chelsea/matches'  # Replace with a valid API URL
    match_data = fetch_match_data(api_url)

    if match_data:
        # Step 2: Process the match data
        df = process_match_data(match_data)
        
        # Step 3: Display the DataFrame in Streamlit
        st.dataframe(df)

        # Step 4: Add visualization (e.g., charts)
        st.line_chart(df['score'])  # Replace 'score' with relevant column names

if __name__ == "__main__":
    main()
```

### Detailed Instructions:
1. **Modify the `fetch_match_data` function**:
   - Ensure the API URL is correct and points to a valid endpoint that provides Chelsea F.C. match data.
   - Handle potential errors gracefully (e.g., by displaying an error message in Streamlit).

2. **Implement Data Processing Logic**:
   - In the `process_match_data` function, add code to clean and transform the fetched data. This may include:
     - Filtering out unnecessary columns.
     - Converting date strings to datetime objects.
     - Aggregating statistics (e.g., total goals, wins, losses).

3. **Enhance the Streamlit App**:
   - After displaying the DataFrame, add more visualizations that represent different aspects of the match data:
     - Use `st.bar_chart()` to show total goals per match.
     - Use `st.line_chart()` to visualize trends over time (e.g., performance over the season).
   - Include user input options (e.g., dropdowns or sliders) to filter the displayed data based on user selections (e.g., by date range or match type).

4. **Test Your Application**:
   - Run your Streamlit app locally using `streamlit run your_script.py`.
   - Ensure that all functionalities work as expected and that the visualizations correctly reflect the processed data.

### Criteria for Success and Evaluation:
- **Functionality**: The application successfully fetches, processes, and visualizes match data without errors.
- **Code Quality**: The code is well-structured, follows best practices, and includes comments explaining key sections.
- **User Experience**: The Streamlit app is user-friendly, with clear visualizations and intuitive navigation.
- **Data Accuracy**: The processed data accurately reflects the original dataset and any aggregations or transformations performed.

### Conclusion:
This assignment aims to apply the concepts learned in the lecture on automation in Python while focusing on a real-world application relevant to your interests in Premier League Soccer and data analysis. By completing this project, you will gain hands-on experience with APIs, data processing using Pandas, and building interactive applications with Streamlit, all of which are valuable skills in today's tech landscape.