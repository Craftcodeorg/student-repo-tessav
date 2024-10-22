### Assignment: Design an Automated Music Preference Tracker

#### Problem Statement:
Create an automated system that tracks music preferences over time and generates insights into popular genres (EDM, R&B, Jazz) through data analysis. This system will utilize APIs to collect data from a music streaming service (e.g., Spotify API) and analyze the listening patterns of users. This project is relevant to the fields of data analysis and automation in consumer electronics, aligning with your career goals in robotics and semiconductors.

#### Starter Code:
Below is a basic framework to get you started. You will need to build upon this code to complete the assignment.

```python
import requests
import json

# Replace 'your_api_key' with your actual Spotify API key
SPOTIFY_API_URL = "https://api.spotify.com/v1/me/top/artists"
HEADERS = {
    "Authorization": "Bearer your_api_key"
}

def fetch_music_data():
    """Fetches the user's top artists from Spotify."""
    response = requests.get(SPOTIFY_API_URL, headers=HEADERS)
    
    if response.status_code == 200:
        return response.json()
    else:
        print("Failed to retrieve data")
        return None

def analyze_music_preferences(data):
    """Analyzes the music preferences from the fetched data."""
    genre_count = {'EDM': 0, 'R&B': 0, 'Jazz': 0}
    
    # Process the data to count genres
    for artist in data['items']:
        genre = artist['genres']  # Assuming genres is a list
        for g in genre:
            if g in genre_count:
                genre_count[g] += 1
                
    return genre_count

# Main execution
music_data = fetch_music_data()
if music_data:
    preferences = analyze_music_preferences(music_data)
    print(f"Music Preferences: {preferences}")
```

#### Detailed Instructions:
1. **Set Up Your Environment**:
   - Ensure you have the `requests` library installed. You can install it using `pip install requests`.

2. **Fetch Data**:
   - Modify the `fetch_music_data()` function to include error handling and ensure it retrieves a user's top artists effectively.
   - Update the URL and headers as necessary to match your API key and any required parameters.

3. **Analyze Music Preferences**:
   - In the `analyze_music_preferences(data)` function, enhance the logic to categorize artists into their respective genres more effectively.
   - Consider adding more genres if you wish to expand beyond EDM, R&B, and Jazz.

4. **Data Storage**:
   - Implement a way to store the analyzed data over time (e.g., using a CSV file or a database). This will allow you to track changes in music preferences over time.

5. **Insights Generation**:
   - Create additional functions to generate insights from the collected data, such as trends over time, most listened genres, etc.

6. **Testing**:
   - Write unit tests to verify that your functions behave as expected. Test cases should include various scenarios, such as empty data responses or unexpected API changes.

#### Criteria for Success and Evaluation:
- **Functionality**: The program should successfully fetch data from the Spotify API and analyze music preferences accurately.
- **Code Quality**: The code should be clean, well-structured, and documented with comments explaining each part.
- **Data Handling**: The ability to store and manage data effectively over time will be crucial.
- **Insights Generation**: The program should provide meaningful insights based on the collected data.

**Success Criteria**:
- The system correctly retrieves and analyzes music preferences.
- The code follows best practices for readability and maintainability.
- The output is clear and provides valuable insights into music trends.

By completing this assignment, you will gain practical experience in API automation, data analysis, and real-world applications relevant to your interests in technology and music. Good luck!