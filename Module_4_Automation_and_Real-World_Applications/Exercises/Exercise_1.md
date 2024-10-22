# Module Title: Automation and Real-World Applications

## Exercise Requirements

### 1. Problem Statement
As an aspiring automation specialist interested in Premier League Soccer, your task is to create a Python script that automates the process of fetching live scores from the Premier League website. This exercise will help you apply the concepts discussed in Lecture 1, focusing on automation using Python and real-world applications in sports analytics.

**Scenario:** You are working for a sports analytics company that needs real-time data on Chelsea F.C. matches. Your goal is to build a script that retrieves live match scores and outputs them in a user-friendly format. This will not only streamline the data collection process but also provide insights for performance analysis.

### 2. Fill-in-the-Blank Starter Code
Below is the starter code that you will need to complete. Fill in the blanks to complete the functionality of the script.

```python
import requests
from bs4 import BeautifulSoup

def fetch_live_scores(url):
    # Make an HTTP request to fetch the content of the page
    response = requests.get(url)
    
    # Check if the request was successful
    if response.status_code == 200:
        # Parse the content using BeautifulSoup
        soup = BeautifulSoup(response.content, 'html.parser')
        
        # Find the live score element (replace 'score-class' with the actual class name)
        live_scores = soup.find_all(class_='score-class')
        
        # Extract and return the scores
        scores = [score.get_text() for score in live_scores]
        return scores
    else:
        return "Error fetching data: " + str(response.status_code)

# URL for the Premier League live scores (replace with actual URL)
url = "https://www.premierleague.com/live"
print(fetch_live_scores(url))
```

### 3. Hints
- **HTTP Requests:** Remember to use the `requests` library to fetch data from the web. Check the status code to ensure your request was successful.
- **Parsing HTML:** Use `BeautifulSoup` to parse HTML content. Familiarize yourself with methods like `find()` and `find_all()` to locate specific elements.
- **Class Names:** Inspect the Premier League website to find out the actual class names used for live scores. This is crucial for extracting the correct data.
- **Error Handling:** Implement basic error handling to manage potential issues, such as network errors or changes in the website structure.

### 4. Expected Outcome
Upon completing this exercise, you should be able to:
- Successfully fill in the blanks in the starter code.
- Fetch live scores from the Premier League website for Chelsea F.C.
- Output the scores in a clear format.
- Demonstrate an understanding of web scraping techniques, including making HTTP requests and parsing HTML content.
- Implement error handling to manage any issues encountered during data retrieval.

The final solution should adhere to best practices, including proper commenting to explain each step of your code, as emphasized in Lecture 1.

### Integration
Ensure that you follow the structure outlined above for clarity and ease of understanding. Use markdown formatting for headings and sections, and include any necessary links or resources that may assist in completing this exercise.