# Spotify Songs Database Setup

## Overview

This script is designed to create a MySQL database using a Spotify Songs dataset. The database is normalized into tables representing tracks, playlists, albums, and genres, adhering to the principles of database normalization.

# Database Structure
The normalized database consists of the following tables:

## Track:

Columns: track_id, track_name, track_artist, track_popularity, danceability, energy, key, loudness, mode, speechiness, acousticness, instrumentalness, liveness, valence, tempo, duration_ms, playlist_uid, track_album_id

## Playlist:

Columns: playlist_id, playlist_name, playlist_uid

## Album:

Columns: track_album_id, track_album_name, track_album_release_date

## Genre:

Columns: playlist_genre, playlist_subgenre


![image](https://github.com/Redgerd/Spotify-Database/assets/117646793/783df12e-9dea-4cba-be2d-c549f38f1ecd)

