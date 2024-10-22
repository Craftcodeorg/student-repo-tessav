### Module Title: Automation and Real-World Applications

### Exercise Requirements

1. **Problem Statement**: 
   You are tasked with creating an interactive dashboard that displays pizza order trends over time. To achieve this, you will automate the data collection process using a simulated API that provides pizza order data. This exercise will help you apply the concepts learned in the lecture about automating data collection from APIs, specifically focusing on the techniques discussed regarding the Premier League API.

   Imagine you are working for a pizza chain that wants to analyze its sales data over the past year to identify trends and improve its marketing strategies. Your goal is to retrieve the data from a mock API and visualize it using a dashboard.

2. **Fill-in-the-Blank Starter Code**: 
   Below is a starter code that you need to complete. The code includes comments and guidance to help you understand what to fill in.

   ```python
   import requests
   import matplotlib.pyplot as plt
   import pandas as pd

   # Function to fetch pizza order data from a mock API
   def fetch_pizza_order_data(api_key):
       url = "https://api.mockpizza.com/v1/orders"  # Mock API URL
       headers = {
           "Authorization": f"Bearer {api_key}"
       }
       
       response = requests.get(url, headers=headers)
       if response.status_code == 200:
           return response.json()  # Return JSON data if request is successful
       else:
           print("Failed to retrieve data")
           return None

   # Function to visualize pizza order trends
   def visualize_order_trends(data):
       # Convert JSON data into a DataFrame
       df = pd.DataFrame(data)  # Fill in this line to create DataFrame from data

       # Group by date and sum the orders
       order_trends = df.groupby('date')['orders'].sum().reset_index()  # Fill in this line

       # Plotting the trends
       plt.figure(figsize=(10, 5))
       plt.plot(order_trends['date'], order_trends['orders'], marker='o')  # Fill in this line
       plt.title('Pizza Order Trends Over Time')
       plt.xlabel('Date')
       plt.ylabel('Number of Orders')
       plt.xticks(rotation=45)
       plt.tight_layout()
       plt.show()

   # Main execution
   if __name__ == "__main__":
       api_key = "your_api_key_here"  # Replace with your actual API key
       pizza_data = fetch_pizza_order_data(api_key)
       
       if pizza_data:  # Ensure data is retrieved successfully
           visualize_order_trends(pizza_data)
   ```

3. **Hints**: 
   - When creating the DataFrame, ensure you are passing the correct structure of the JSON data returned from the API.
   - Remember to group the data by date; you may need to use the correct column names from your DataFrame.
   - For plotting, ensure you are accessing the correct columns for dates and order counts.

4. **Expected Outcome**: 
   After completing the exercise, you should have a functional Python script that:
   - Retrieves pizza order data from a mock API.
   - Processes and visualizes this data in a clear and informative manner using a line graph.
   - Demonstrates your understanding of API interaction, data processing, and visualization techniques as discussed in the lecture.

### Integration
- Ensure that all code is well-structured and commented for clarity.
- Use markdown for formatting, making it easy to read and follow.
- Include any necessary files or resources as links if applicable.

This exercise aligns with your background in Python programming and your interest in practical applications of technology, particularly in data analysis and automation.