# Module Title: Python Fundamentals and Optimization Techniques

## Example 1: Using Lists and Dictionaries for Data Storage

### 1. Introduction
In this section, we will explore the significance of using lists and dictionaries for data storage, particularly in the context of robotics, semiconductors, and consumer electronics. As discussed in Lecture 1, Python provides versatile data structures that can enhance data management and processing efficiency. For professionals in these industries, leveraging Python's capabilities can lead to improved automation, data analysis, and real-time decision-making.

### 2. Code Snippet
Below is a well-commented Python code snippet that demonstrates how to use lists and dictionaries for data storage:

```python
# Import necessary libraries
import json

# Sample data representing sensor readings in a robotics application
sensor_data = [
    {"sensor_id": 1, "temperature": 22.5, "humidity": 45},
    {"sensor_id": 2, "temperature": 23.0, "humidity": 50},
    {"sensor_id": 3, "temperature": 21.8, "humidity": 48}
]

# Function to calculate average temperature from sensor data
def calculate_average_temperature(data):
    total_temp = 0
    for entry in data:
        total_temp += entry['temperature']
    average_temp = total_temp / len(data)
    return average_temp

# Function to save sensor data to a JSON file for future reference
def save_sensor_data(data, filename='sensor_data.json'):
    try:
        with open(filename, 'w') as file:
            json.dump(data, file)
        print(f"Data saved successfully to {filename}.")
    except IOError as e:
        print(f"Error saving data: {e}")

# Calculate and print average temperature
avg_temp = calculate_average_temperature(sensor_data)
print(f"Average Temperature: {avg_temp:.2f}°C")

# Save the sensor data to a file
save_sensor_data(sensor_data)
```

### 3. Explanation
1. **Data Structure**: The `sensor_data` list contains dictionaries, each representing a sensor's readings (temperature and humidity). This structure allows easy access to each sensor's data using its unique `sensor_id`.

2. **Function Definitions**:
   - `calculate_average_temperature(data)`: This function iterates through the list of dictionaries, summing the temperatures and calculating the average. It implements best practices such as clear naming conventions and separation of concerns.
   - `save_sensor_data(data, filename)`: This function saves the sensor data to a JSON file. It includes error handling to manage potential file I/O issues.

3. **Execution**: The average temperature is calculated and printed. The sensor data is then saved to a JSON file for future analysis or reporting.

### 4. Application
In the context of robotics, using lists and dictionaries for data storage can significantly enhance the efficiency of monitoring systems. For example, in an automated greenhouse, sensors can collect temperature and humidity readings at regular intervals. By storing this data in a structured format (as shown above), engineers can analyze trends over time, optimize environmental conditions for plant growth, and automate irrigation systems based on real-time data.

In the semiconductor industry, similar techniques can be applied to monitor production equipment's performance metrics. By storing sensor readings in lists and dictionaries, engineers can quickly access relevant data to troubleshoot issues or improve manufacturing processes.

### Integration
This content is structured with clear headings and sections for easy parsing and integration into the learning platform. The use of markdown formatting enhances readability and organization, aligning with the user’s preference for project-based learning and practical applications of technology.

By mastering these concepts, you will be well-equipped to apply Python's powerful data structures to real-world problems in your field of interest, including robotics and consumer electronics.