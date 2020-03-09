# Spotify Manipulation with Python; can a Data Scientist Replace a DJ?

## Introduction
Data Science is vast and continuously expands into new industries, offering a multitude of valuable (corporate mainly) applications. The music industry is one of them. Should we treat any of those applications like a "black box", we would observe an input (data) and an output (product).

## Scope
This project aims to manipulate the Spotify music data with Python, having a twofold scope:

✔️ proving that the existence of an API (Application Programming Interface) is of high importance, in terms of feeding algorithms with extra fine data.

✔️ demonstrating how plain statistics (when properly applied) can encode daily actions, break them down into their fundamental elements and on top of them build valuable products.

## Scenario

Lately, the Data Corp I work for as a data scientist, records remarkable profits from their Youth Marketing segment and in reward for this, it rewards its young customers with a party. In the absence of a DJ, my supervisor asked me to take care of the music and make the party last until the morning! She gave to me a number of Spotify playlists, the PR department had already created, in order to check them out and create the final one. My blindness to the modern music generally, leads me to a tricky alternative:

*How about accessing all the playlists using Python, extracting every single audio feature of each track, reason about them statistically and wrapping  the most suitable (to our party) tracks to a final playlist? Given of course a technicality: I am not going to hear a single beat of any of them!*

## Roadmap

We make requests to the Spotify API for data collection, using the free Python libraries, Spotipy and Requests. We access the user playlists, tracks and perform EDA on their audio features, using Numpy, Pandas & Matplotlib. A number of data visualizations are depicted, to better communicate the results. Finally, we create the final playlist of tracks.

## Authorization Flow Guide

1. Sign up at Spotify for Developers at https://developer.spotify.com/ and select "Create an app". Write down your 'Client ID' and 'Client Secret'. While in the "Dashboard", select the "Edit settings" menu and in the "Redirect URIs" field fill the: http://localhost:7777/callback.
2. Open Spotify_Data_Manipulation_Python.ipynb and in the Authorization Flow code block, insert your Spotify username, Client ID, Client Secret and Redirect URI as `cid`, `secret`, `redirect_uri` and `username`, respectively.
3. Execute it. The first time Spotipy will need user authentication and will open a webpage, asking you to log in with your Spotify account and accept the permissions. After doing so, it will redirect you to a link. Copy the 'Redirect URI' and paste in the field that will appear in the Notebook. Hit 'enter'.
4. Now, you are connected to the Spotify API and capable to get your playlists ID, song IDs and use them to extract the features.

## Additional Analysis
There is quite a number of additional analyses to be performed, expanding this one. You are welcome to extend and shape yours in any direction you may prefer. For instance, you can additionally try and remove the tracks that have significantly low `danceability` and `valence` audio features, and boost even more the playlist's `score`. Furthemore, you can apply each approach sequentially (on the dataframe that is produced each time).

[*It stands as an independent analysis in an effort to enhance my ability to communicate results, reason about data statistically and stay motivated to continuously implement newly aquired skills & capabilities, so as to enrich my portfolio of data science-oriented projects*]