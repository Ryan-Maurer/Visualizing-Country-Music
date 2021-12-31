![image](./images/Spotify_banner.jpg)
# Visualizing Country Music Using Python, Power BI, and the Spotify API
This project aims to  identify changes withhin the country music genre across decades through the utillizaiton of Spotify's API.

Tools and Procedures:

* Python (Pandas, Matplotlib, Seaborn, Spotipy library)

* Power BI

* Excel

* PowerPoint

* Spotify API

* API Querying

* Data Cleaning, Exploatarion, Visualization, and Analysis


## "Country music is gone - and it's not coming back."- Alan Jackson

As someone who is relatively ignorant of country music and its history, I have many times been exposed to the notion that country music has evolved into something very different, if not contrary, from what it was during its "Golden Era".
[^1]
While some people making this observation are simply concerned about the incorporation of digital elements into the genre, I think that many people view country music's place in today's musical landscape as being very different from where it was during the mid-twentieth century.
A common complaint involves an increasing overlap between it and pop music, even incorporating elements from rap and hip hop as well.  This growing trend is in opposition to Golden Era country music, where its place in the musical landscape was (presumably) more carved out and distinct.
While I have no wish to judge whether I agree with this sentiment, nor voice preference of one form of music over another, I thought that it would be interesting to investigate this claim visually using data analysis techniques.

<br />

# Table of Contents
1. [Data Questions](#data-questions)
2. [Methodology](#methodology)
3. [Data Sources](#data-sources)
4. [Cleaning and Exporting](#cleaning-and-exporting)
5. [Analysis](#analysis)

## Data Questions
1. How has country music changed musically from decade to decade since the 1960's?
2. How has pop music changed musically from decade to decade since the 1960's?
3. How have pop and country music's trajectories correlated/diverted?

## Methodology
In determining the best way of investigating the changes in country music, it's best to look at the source itself, the music of course!
Whereas before it may have been difficult to objectively get qualitative attributes [^2]of songs besides length and tempo, today we have algorithms that can determine qualities of a song through processes such as machine learning.
One of the most phemonenol features that Spotify provides is their end-of-year "Wrapped" playlists, which utillizes these types of algorithms in no small part to make conclusions about their user's listening habits.
Does this user prefer happier up-tempo music, or do they prefer slower more somber music?  Based on how their preferred music rates in terms of valence[^3], energy, etc, Spotify can use that data to draw conclusions.
Spotify provides access to this information for their entire catalogue through their API, which we can use to get all of the attributes we want for our songs.  
Below is an example of the results of an API query to get the audio features for the song "Achy Breaky Heart" by Billy Ray Cyrus:
<br />
![ScreenShot](./images/achy_breaky.JPG)
![ScreenShot](./images/spotify_features.png)
<br />
Each variable is listed with its rating, and a collection of these queries of releases from a particular time/genre can aid in making inferences about musical norms.
As stated, this project aims to collect country music and its attributes into a useable format in order to determine changes in musical preferences across decades.
In order to do so, lists of songs that are indicative of each decade is integral to the success of this project.
<br />
## Data Sources
The next step is to determine how to get the music to search for in the API.
Spotify's API allows for searching for tracks within a playlist, and the most straghtforward way I found to get music was by utillizing both pre-existing and self-created playlists.
Below is an example of one of the playlists I used to get a list of songs emblematic of country music in the 1960's[^4].
<br />
![image](./images/60s_playlist.JPG)
<br />
I primarily relied on Spotify-created playlists for country music, and for pop I inputted data from [davesmusicdatabase.blogspot.com](https://davesmusicdatabase.blogspot.com/p/best-of-lists.html#songs-era) into Spotify playlists[^5] .
I inputted data from the billboard hot 100 year-end charts for contemporary pop and country as well.
<br />
## Cleaning and Exporting
My preferred method of querying in the API was by using the [Spotipy](https://spotipy.readthedocs.io/en/2.19.0/) library for python.
The process was to get the data from JSON format into a Pandas DataFrame, and then exporting in csv format for dashboarding.  
![excel](./images/excel_screen.JPG)
<br />
## Analysis
I've found boxplots to be incredibly useful in visualizing changes across decades.  In this case, they give a high-level understanding of the distribution of the data for each variable, and when plotted by decade, paint an informative picture of how they change over time.
We can see, for instance, that acousticness overall has become predictably less and less prominant over time.  Due to the adoption of digital instruments and recording processes, it is no surprise to see this taking place and it outlines an effective way of interpretting this data, which is to compare what is being displayed to what we know about the progression of music and the adoption of technology over the last several decades.
To determine if there are issues with data one often performs a sanity check, where the comparison between the story being told by the data and what the analyst expects to see is not contradictory.
In this case, the increasingly smaller representation of accoustiness and the greater representation of energy and loudness was expected and I am happy to be capturing that with this visualization.
![box](./images/boxplots.JPG)
<br />

[^1]: "Golden Era" generally referring the period bewteen the 50's and 60's when the likes of Johnny Cash, Patsy Cline, and Merle Haggard dominated the charts
[^2]: A qualitative attribute in this case is a measure of the pressence of a certain element in a song, such as its perceived acousticness, energy, etc.
[^3]: The perceived positivity/negativity of a song.
[^4]: Obviously people's opinions on what the defining music of a decade is, and it was a challenge to find a process that worked with a sense of objectivity.  
For country music, Spotify has devoted playlists for each decade, which I determined effective in depicting the musical norms of the time.  
[^5]: An online database that creates lists of the most popular songs for each decade utillizing sales figures, chart data, radio airplay, and streaming figures.
