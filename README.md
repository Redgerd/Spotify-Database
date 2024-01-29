# Spotify Songs Database Setup

## Overview

This script facilitates the creation of a MySQL database using a Spotify Songs dataset. The process involves several stages to ensure data accuracy, integrity, and adherence to database normalization principles.
[https://essay.utwente.nl/75422/1/NIJKAMP_BA_IBA.pdf] was used as reference

### Stage 1: Historical Layer (db_stg0)

The entire Spotify Songs dataset is initially loaded into a database named `db_stg0`, serving as the Historical Layer. This layer stores raw data without any transformations, preserving the complete historical record.

### Stage 2: Integration Layer (db_stg1)

Data is then migrated to the Integration Layer (`db_stg1`) with the implementation of triggers. These triggers identify and separate records with incorrect formats or inconsistencies into designated tables. This ensures that data integrity is maintained, and any anomalies are properly handled.

### Stage 3: Access Layer (db_stg2)

Finally, the database is normalized into tables within the Access Layer (`db_stg2`). This layer is designed to enhance user accessibility and analytical capabilities by representing tracks, playlists, albums, and genres in a structured format. The normalization adheres to best practices, ensuring efficient storage and retrieval of data.

# Database Structure

The normalized database comprises the following tables:

## Track Table:

Columns:
- track_id
- track_name
- track_artist
- track_popularity
- danceability
- energy
- key
- loudness
- mode
- speechiness
- acousticness
- instrumentalness
- liveness
- valence
- tempo
- duration_ms
- playlist_uid
- track_album_id

## Playlist Table:

Columns:
- playlist_id
- playlist_name
- playlist_uid

## Album Table:

Columns:
- track_album_id
- track_album_name
- track_album_release_date

## Genre Table:

Columns:
- playlist_genre
- playlist_subgenre

  ![image](https://github.com/Redgerd/Spotify-Database/assets/117646793/df56e477-c9dd-40dd-93e3-c4852b4623ca)
