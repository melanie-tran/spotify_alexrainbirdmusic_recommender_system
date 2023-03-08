# spotify_alexrainbirdmusic_recommender_system
The goal of this project is to build a content based filtering recommender system that recommends song similar to songs found on user: alexrainbirdMusic's playlist.

Knowing what song to incorporate onto alexrainbirdMusic's playlists is extremely important since his profitability is tied to the number of views he has on his playlist videos on YouTube. alexrainbirdMusic has over 1.2M subscribers on YouTube and over 116k followers on Spotify. The more playlists he creates that ties to his goal of bringing the "finest independent pop, folk and rock music" to his followers, the more views and money he will get. 

Currently, alexrainbirdMusic has artists submit their songs on his website and he reviews the song to determine if it should be added to a playlist. This is a much more manual and tedius process for selecting songs. 

alexrainbirdMusic links: 
- **Youtube**: https://www.youtube.com/user/alexrainbird
- **Spotify**: https://open.spotify.com/user/alxrnbrdmusic?si=10a9c1d81a764e18

## Project Details: 
The data retrieved for this project was gathered using Spotify's Web Developer API and Spotipy. 

This project is structured in three notebooks: 
1. Get Data
2. Exploratory Data Analysis
3. Build Recommender System

## Results: 

### EDA Summary
- **Audio Features Distribution**
    - Objective: Explore the distribution of the audio features for the track data. 
        - Across all playlists, most playlist had tracks that:
            - Are not acoustic
            - Are both danceable and not danceable
            - Have higher energy
            - Have vocals
            - Are not performed live
            - Are loud
            - Have both slow and fast tempo
            - Do not have high presence of spoken word
            - Are both sad and happy  
- **Audio Features Correlation**
    - Objective: Analyze the correlation between audio features.
        - Positive Correlation: 
            - Energy & Loudness
            - Valence & Energy
            - Valence & Danceability
            - Valence & Loudness
        - Negative Correlation: 
            - Acousticness & Energy
            - Acousticness & Loudness
            - Acousticness & Valence 
- **Over Time (2016 to 2022)**
    - Objective: Analyze how audio features fluctuate over time based on the month and year data of the compilation playlists.
        - There was not a signficant difference in average audio features across the months and years. 
- **Comparison by Genres**
    - Objective: Compare the audio features across the genres.
        - Alt & Rock had the highest Energy and Valence scores
        - Folk, Pop, & Indie had higher scores for acoustic songs
        - Instrumentalness, Liveness, Speechiness were similiar across all genres 
- **Comparison by Seasons**
    - Objective: Compare the audio features across the seasons. 
        - There was not a signficant difference in average audio features across the seasons.


### Modeling Summary
A recommender system using content-based filtering and cosine similarity was created to successfully recommend Alternative, Indie, Pop, Folk, and Rock songs that alexrainbirdMusic can incorporate into his playlists. While the main challenge with recommender systems is that the user cannot quantify the accuracy, this is a much faster option to find similar songs than listening to submitted songs and making a judgement. 

In addition to the recommender system, alexrainbirdMusic can leverage A/B testing where he can determine which songs are more popular and relevant to be included in his playlists.  

## Credits: 
Credits to Eric Chang as the notebook is built on top of his previous code: https://github.com/enjuichang/PracticalDataScience-ENCA/tree/main/notebooks. 



