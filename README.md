# Billboard to Spotify Playlist Creator

This Python script allows users to generate a private Spotify playlist based on Billboard's Hot 100 chart for a specific date. It scrapes the Billboard website for the top 100 songs of a chosen date and then searches for those songs on Spotify to create a custom playlist.

## Features

- **Date-based song retrieval:** Input any date in the format `YYYY-MM-DD`, and the script will scrape the Billboard Hot 100 chart for that specific date.
- **Spotify playlist creation:** After retrieving the song list, the script searches Spotify for the corresponding tracks and creates a private playlist with those songs.
- **Error handling:** If a song isn't found on Spotify, it skips that track and informs the user.

## Requirements

- Python 3.x
- [Spotipy](https://spotipy.readthedocs.io/en/2.19.0/#) (Spotify Web API wrapper)
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) (HTML/XML parser)
- [Requests](https://docs.python-requests.org/en/latest/)

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/billboard-spotify-playlist.git

2. **Install the required Python libraries:**
   ```pip install spotipy requests beautifulsoup4```
   
3. **Spotify Developer Account:**

    - Register at Spotify Developer to get your client_id and client_secret.
    - Set up a new Spotify app and add a redirect URI (e.g., http://example.com).

4. **Edit your script:**

   - Replace the client_id, client_secret, and redirect_uri in the script with the values from your Spotify Developer account.
   - Update the cache_path and username with your own details.

## Usage

  1. **Run the script:**

    bash

```python billboard_spotify.py```

2. **Input a date:**

- `When prompted, enter a date in the format YYYY-MM-DD (e.g., 2023-10-01) to retrieve the Billboard Hot 100 chart for that day.

3. **Playlist Creation:**

  - The script will scrape the song names from Billboard's chart.
  - It will then search Spotify for each song and add them to a new playlist.
  - The playlist will be created in your Spotify account as a private playlist.

4. **Error Handling:**

  - If a song isn't found on Spotify, it will be skipped, and you'll receive a message indicating the song's absence.

## Example

bash

```Which year do you want to travel to? Type the date in this format YYYY-MM-DD: 2022-05-15```

The script will output the following:

bash

```Creating a playlist for 2022-05-15 Billboard 100...
Song 1 added...
Song 2 added...
Some Song doesn't exist in Spotify. Skipped.
```

## Notes

  - Make sure to log in to Spotify and authorize the script through the URL displayed when you run it.
  - The playlist will be created as private by default.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
