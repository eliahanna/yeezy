# yeezy
Analyze the music and lyrics of Kanye West and related hip-hop artists using the Spotify and Genius Lyrics APIs.

# About
This project is an extension of work originally completed for the U.C. Berkeley MIDS course, w209: Data Visualization.
Kanye West is one of the most popular and controversial artists of his generation. Given his prominent place in the hip-hop scene, I am interested in quantifying attributes of his music and lyrics in order to understand how Kanye differs from his peers and where they are similar. To quantify his music and lyrics, I leverage the Spotify and Genius Lyrics APIs. I will also use Spotify to identify ‘related’ artists as the comparison group.

# High Level Plan
* Obtain and Prepare Data 
  * Pull track data from Spotify for Kanye and related artists
  * Clean the track data to remove duplicates (live and special editions)
  * Pull lyrics for all the tracks from Genius Lyrics
* Validate Data  
  * Check for songs that are missing lyrics
* Create New Features
  * Total Word Count
  * Unique Word Count
  * Unique Word Percentage
  * Number of Verses
  * Total Drug References
  * Drug References by Drug
  * Total Swear Words
  * Swear Words by Word
  * Total Syllables
  * References to God
  * Repetitiveness
* Analysis
  * Compare Spotify and Lyrical Metrics Against Popularity
  * Can we predict artist through Spotify and lyrical metrics?
* Possible next steps
  * Sentiment Analysis

# Repo Contents
* getData.py - Pulls track and album data from Spotify for Kanye West and related artists, removes duplicates (ex: live and special editions). Pulls lyrics from Genius Lyrics for each track and combines the data sets. Writes the result to data_with_lyrics.csv for easy retrieval. 

# Requirements
To run getData.py, you will need developer tokens for the Spotify and Genius Lyrics APIs stored in a file called creds.py. The format should be:
```
spotify_username = "your_spotify_username_token"
spotify_password = "your_spotify_password_token"
genius_token = "your_genius_token"
  
