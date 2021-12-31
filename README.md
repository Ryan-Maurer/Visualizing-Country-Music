![image](./images/Spotify_banner.jpg)
# Visualizing Country Music Using Python, Power BI, and the Spotify API
This project aims to  identify changes withhin the country music genre through the utillizaiton of Spotify's API.

Tools and Processes:

* Python (Pandas, Matplotlib, Spotipy library)

* Power BI

* Excel

* PowerPoint

* Spotify API

* API Querying

* Data Cleaning, Exploatarion, Visualization, and Analysis


## "Country music is gone - and it's not coming back."- Alan Jackson

As someone who is relatively ignorant of country music and its history, I have many times been exposed to the notion that country music has evolved into something very different, if not contrary, from what it was during its "Golden Era".
[^1]
While some people making this observation are simply concerned about the incorporation of modern digital elements, I think that many people view country music's place in today's musical landscape as being very different from where it was during the mid-twentieth century.
A common complaint involves increasing overlap between it and pop music, even incorporating elements from rap and hip hop as well.  This growing trend is in opposition to Golden Era country music, where its place in the musical landscape was (presumably) more carved out and distinct.
While I have no wish to judge whether I agree with this sentiment, nor voice preference of one form of music over another, I thought that it would be interesting to investigate this claim visually using data analysis techniques.

<br />

# Table of Contents
1. [Data Questions](#data-questions)
2. [Methodology](#methodology)
3. [Data Sources](#data-sources)

## Data Questions
1. How has country music changed musically from decade to decade since the 1960's?
2. How has pop music changed musically from decade to decade since the 1960's?
3. How has pop and country music's trajectories correlated/diverted?

## Methodology 
In determining the best way of investigating the changes in country music, it's best to look at the source itself, the music of course! 
Whereas before it may have been difficult to objectively get qualitative attributes [^2]of songs besides length and tempo, today we have algorithms that can determine qualities of a song through processes such as machine learning.
One of the most phemonenol features that Spotify provides is their end-of-year "Wrapped" playlists, which utillizes these algorithms in no small part to make conclusions about their user's listening habits.
Does this user prefer happier up-tempo music, or do they prefer slower more somber music?  Based on how their preferred music rates in terms of valence[^3], energy, etc, Spotify can use that data to draw conclusions.
<br />
Another great thing about Spotify is that they provide access to this information for their entire catalogue through their API.  
Below is an example of an API query to get the audio features for the song "Achy Breaky Heart" by Billy Ray Cyrus:
<br />
![ScreenShot](https://github.com/Ryan-Maurer/Visualizing-Country-Music/blob/master/achy_breaky_console.jpg)
<br />
## Data Sources
qwerty

[^1]: "Golden Era" generally referring the period bewteen the 50's and 60's when the likes of Johnny Cash, Patsy Cline, and Merle Haggard dominated the charts
[^2]: A qualitative attribute in this case is a measure of the pressence of a certain element in a song, such as its perceived acousticness, energy, etc.
[^3]: The perceived positivity/negativity of a song.