# Simulation of an ETL process and Data Modelling for song analysis

## Sparkify
The (fictional) start-up sparkify wants to know more about the usage of their music app and extracted song data and recorded user data.

### Goal
Their goal is to run queries on song play analysis. This will allow them to analyze the popularity of songs, even based on the locations of the users.


### ETL Pipeline
Both the song datasets and the user log datasets are read in "json" format. The song dataset is a subset of the [Million Song Dataset](http://millionsongdataset.com/) and the log datasets have been created by [this event simulator](https://github.com/Interana/eventsim).
The "json" files are read using pandas and saved to a postgreSQL database.


### Database Schema
The database schema follows the star schema with the songplays table being the fact table having four associated dimension tables ("users", "songs", "artists" and "time"). This allows simple queries on the songplays.


### Conda Environment
The anaconda environment used for this project is documented in "environment.yml". 
