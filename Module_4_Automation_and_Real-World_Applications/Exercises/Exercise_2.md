### Module Title: Automation and Real-World Applications

### Exercise Requirements

1. **Problem Statement**: 
   Build an automated data processing pipeline that analyzes basketball game statistics, specifically focusing on the Miami Heat's performance. Your task is to scrape the latest game statistics from a sports website, process the data to calculate the average points scored by the team over the last five games, and display the results. This exercise will require you to apply the concepts covered in the lecture about using Selenium, Requests, and Beautiful Soup.

2. **Fill-in-the-Blank Starter Code**:
   Below is a starter code template. Fill in the blanks to complete the functionality of the program. Make sure to include error handling and comments to explain your reasoning.

   ```python
   import requests
   from bs4 import BeautifulSoup

   def fetch_miami_heat_stats(url):
       # Step 1: Fetch the webpage
       response = requests.get(url)
       if response.status_code != 200:
           print("Failed to retrieve data")
           return None

       # Step 2: Parse the HTML
       soup = BeautifulSoup(response.text, 'html.parser')

       # Step 3: Extract game statistics
       games = soup.find_all('div', class_='game-statistics')  # Update class name as per actual website
       points = []
       
       for game in games[:5]:  # Limit to last 5 games
           score = game.find('span', class_='points').text  # Update class name as per actual website
           points.append(int(score))

       # Step 4: Calculate average points
       average_points = sum(points) / len(points) if points else 0
       return average_points

   # Test the function with an example URL for Miami Heat's game stats
   url = 'https://example.com/miami-heat/stats'  # Replace with actual URL
   print("Average Points Scored by Miami Heat in Last 5 Games:", fetch_miami_heat_stats(url))
   ```

3. **Hints**:
   - **Hint 1**: Ensure that you check the HTTP response status to handle any potential errors when fetching data from the website.
   - **Hint 2**: When extracting game statistics, make sure to inspect the HTML structure of the webpage to find the correct class names for points and game statistics.
   - **Hint 3**: Remember to convert the extracted points from strings to integers before performing calculations.
   - **Hint 4**: Use list comprehension for concise and efficient data processing when calculating averages.

4. **Expected Outcome**:
   The student should be able to fill in the blanks correctly, demonstrating an understanding of how to scrape web data, process it, and calculate averages. The final solution should adhere to best practices, include error handling, and be well-commented to explain the reasoning behind each step. Upon completion, students will have a working script that automates data collection and analysis for basketball game statistics, aligning with their interests in sports analytics and their career goals in data processing and automation.

### Integration
- Ensure that the exercise content is well-structured with clear headings and sections for easy parsing and integration into the learning platform. Use markdown for formatting and include any necessary files or resources as links.