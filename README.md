# The Perfect-Spotify-Playlist
*Pegah Mirghafari*
___
## Problem Statement

generating a playlist, based on a song, from your liked songs only! 
**“After that communism was the only answer for me, I thought. And if you can’t be a communist and make money you have to be a rock n roll star, at least in Hoboken. “ -Lou Reed**

My dream job would be working for Spotify as a data scientist since their product is the only product I can 100% get behind, **"and if I can't be a rock 'n' roll star and make money, then Spotify is the only answer for me, I thought; at least in Brooklyn."**
I knew right from the start that I will dedicate my most crucial project to rock n roll and Spotify. 
I was lost, however,  as to what I wanted to do. What is not done yet?. One day when for the 100th time someone asked me for my Spotify playlist, I found myself having to explain once again why I do not have any playlists. 
The truth of the matter is that liking a song is straightforward on Spotify. I can do it in less than a second, but making a playlist is an art or a dire project on its own, one that I was dreading to tackle. Where should I start? There are MANY ways I could categorize my liked songs and make a playlist based on a song's mood, similarity amongst artists, their genres, language, decade, story, and thousands of other ways that I cannot even imagine. Too many options always crippled my decision-making abilities, and now I was left with more than two thousand songs in my playlist that I played on shuffle. They would change my mood from a hopeless romantic to just mindlessly dancing, and that was only half of it.  
Then, I remembered the time I was listening to "Going to California" by Led Zeppelin while driving home. I was lost in the lyrics and the tempo of the song and had turned my volume very high. The song came to an end, and the red lights turned green, all while the next song played on HIGH VOLUME , John Bon Jovi, screaming: 
**"SHOT THROUGH THE HEART, AND YOU'RE TO BLAME, DARLING, YOU GIVE LOVE A BAD NAME".**
If one listens to "you give love a bad name," on its own, on high volume, one might enjoy it. But when you're lost in the dreams of "going to California, the last thing you want is Bon Jovi accusing you of giving love a bad name. It could give you a heart attack! 
That was it! This is my destiny! This is why it was brought here on earth!!! I need to automate Spotify to make various playlists on my liked songs, and like songs alone, and do it fast, because while I like to pretend that I am an open-minded person, I have to admit I'm close-minded when it comes to music! I only listen to the 2000 songs I've liked, occasionally adding one or two to the collection. Besides, creating a playlist seems like such a daunting task. Either I would get too distracted and end up with a five-song playlist, or I would lay in my bed static upon waking up, dedicating 10 hours to the task. Either way, I would wind up frustrated. 
### So here it is, an app that takes YOUR liked songs and creates a 20-song playlist for you, based on any song you choose! The first ten are in ascending order of tempo, and the next then in descending order, because WHAT GOSE UP MUST COME DOWN -Isaac Newton(probably).  


___
## Contents:
- [Data Dictionary](#Data-Dictionary)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Preprocessing](#Preprocessing)
- [Recommender Summary](#Recommender-Summary)
- [Limitations](#Limitations)
- [Next Steps](#Next-Steps)
  
      
<br/>
<br/>  

___

## Data Dictionary:
The data scraped for this project was from my own personal spotify liked songs.  

|Feature|Type|Description|
|---|---|---|
|danceability|float|Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.|
|energy|float|Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.|
|key|float|The key music is written in. Integers map to pitches using standard [Pitch Class Notation](https://en.wikipedia.org/wiki/Pitch_class) . E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on.|
|loudness|float|The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typical range between -60 and 0 db.|
|mode|int|Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.|
|speechiness|float|Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.|
|acousticness|float|A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.|
|instrumentalness|float|Predicts whether a track contains no vocals. “Ooh” and “aah” sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly “vocal”. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.|
|liveness|float|Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.|
|valence|float|A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).|
|tempo|float|The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.|
|duration_ms|int|Duration of song in milliseconds.|
|time_signature|int|An estimated overall time signature of a track. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure).|


<br/> 

Descriptions were taken from the official documentation at Spotify's Developer website [here](https://developer.spotify.com/documentation/web-api/reference/tracks/get-several-audio-features/). They desplay the distribution of the metrics.
