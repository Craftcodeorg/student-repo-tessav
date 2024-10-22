### Assignment: Create a Comprehensive Automation Script for Video Game Player Statistics

#### Problem Statement:
In this assignment, you will create an automation script that pulls player statistics from two popular video games: Valorant and Minecraft. The script will generate performance reports based on the retrieved data. This task is directly related to the concepts taught in the lecture on using Selenium, Requests, and Beautiful Soup for web automation and data scraping. This project will help you understand how to gather and analyze data relevant to your interests in gaming and enhance your skills in Python automation.

#### Starter Code:
Below is a basic framework for your automation script. You will need to build upon this code by adding functionality to fetch and parse player statistics from the respective game websites.

```python
import requests
from bs4 import BeautifulSoup

def fetch_valorant_stats(player_name):
    # Step 1: Construct the URL for Valorant player stats
    url = f'https://example.com/valorant/stats/{player_name}'
    
    # Step 2: Send a GET request to fetch the webpage
    response = requests.get(url)
    
    # Step 3: Check if the request was successful
    if response.status_code == 200:
        # Step 4: Parse the HTML content using Beautiful Soup
        soup = BeautifulSoup(response.text, 'html.parser')
        
        # Step 5: Extract relevant player statistics (modify selectors as needed)
        stats = {
            'kills': soup.find('div', class_='kills').text,
            'deaths': soup.find('div', class_='deaths').text,
            'assists': soup.find('div', class_='assists').text,
        }
        return stats
    else:
        print("Failed to retrieve data for Valorant player.")
        return None

def fetch_minecraft_stats(player_name):
    # Step 1: Construct the URL for Minecraft player stats
    url = f'https://example.com/minecraft/stats/{player_name}'
    
    # Step 2: Send a GET request to fetch the webpage
    response = requests.get(url)
    
    # Step 3: Check if the request was successful
    if response.status_code == 200:
        # Step 4: Parse the HTML content using Beautiful Soup
        soup = BeautifulSoup(response.text, 'html.parser')
        
        # Step 5: Extract relevant player statistics (modify selectors as needed)
        stats = {
            'blocks_broken': soup.find('div', class_='blocks-broken').text,
            'deaths': soup.find('div', class_='deaths').text,
            'time_played': soup.find('div', class_='time-played').text,
        }
        return stats
    else:
        print("Failed to retrieve data for Minecraft player.")
        return None

# Example usage
valorant_player = 'example_player'
minecraft_player = 'example_player'

valorant_stats = fetch_valorant_stats(valorant_player)
minecraft_stats = fetch_minecraft_stats(minecraft_player)

print("Valorant Stats:", valorant_stats)
print("Minecraft Stats:", minecraft_stats)
```

#### Detailed Instructions:
1. **Modify the URL**: Replace `https://example.com/valorant/stats/{player_name}` and `https://example.com/minecraft/stats/{player_name}` with actual URLs that provide player statistics for Valorant and Minecraft.

2. **Update HTML Selectors**: Inspect the HTML structure of the target websites to find the correct CSS selectors or tags that contain the statistics you want to extract. Update the `soup.find()` calls accordingly.

3. **Enhance Data Reporting**: Create a function that takes the fetched statistics and formats them into a readable report. This report should clearly present the player's performance across both games.

4. **Error Handling**: Implement error handling to manage potential issues such as network errors or unexpected HTML structure changes.

5. **Testing**: Test your script with different player names to ensure it works correctly across various scenarios.

#### Criteria for Success and Evaluation:
- **Functionality**: The script should successfully fetch and display player statistics from both games.
- **Code Quality**: The code should be clean, well-organized, and follow best practices in Python programming.
- **Documentation**: Include comments explaining each part of your code for clarity.
- **Output Format**: The performance report should be clear and user-friendly, presenting data in an organized manner.

By completing this assignment, you will gain hands-on experience with web automation and data scraping, reinforcing your understanding of the concepts discussed in the lecture while also aligning with your interests in video games and data analysis.