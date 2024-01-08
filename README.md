# Music Mood Prediction Project 🎧

## Project Overview 🔎
This project focuses on analyzing music data from Spotify to predict the mood of songs. Using the Spotify API, I retrieved my top tracks, extract various audio features, and employ deep learning techniques to classify these songs into different mood categories.

## Motivation 🚀
Aim of this project is gain insight about my taste of music since in our daily lifes most of us consume thousands of minutes of music every year. Last year when spotify wrapped approached, I found out that I listened more than 30000 thousand minutes of music. Hence, I wanted to find out that whether my music taste is affecting my mood or vice versa by using classification models to determine the mood of my most listened musics via deep learning.

## Data Analysis 🧐
- Data is collected from Spotify using spotipy Library
- Due to API limitations I collected the data between different time frames
- Cleaned the data, corrected the formats and enchanced with various features for further analysis
- Applied explarotary data analytics to gain insight about the sufficiency of collected data.
- Then applied feature engineering techniques to make my data sufficient for ml models. 
- Created ml model to predict moods of the songs based on my data.

## Findings 🔮

- I realized that overall mood of my songs were energetic, where sad musics are too small to take into the consideration. 
- I found out that energy and loudness has very high correlations hence, I will try to add more musics with high loudness to my playlists.

## Limitations and Future work. 📈
- There are API limitations in Spotify developer program. Hence, I collected my data as a csv file to avoid those limitations.
- For future work, I will collect my data on regular bases and enhance my dataset to gain more reliable insights and enhance my project with other health metrics in order to calculate and predict my mood as well as songs that I listen. 

## Key Features 🔑
- **Data Retrieval**: Fetch top tracks of my data between different time intervals from Spotify.
- **Data Analysis**: Perform Exploratory Data Analysis (EDA) on various audio features.
- **Mood Prediction**: Build a deep learning model to classify songs into moods like 'calm', 'energetic', 'happy', or 'sad'.

## Technologies Used 🧑🏻‍💻
- **Python**: Primary programming language.
- **Spotipy**: A lightweight Python library for the Spotify Web API.
- **Pandas**: For data manipulation and analysis.
- **PyTorch**: Deep learning library used
- **Scikit-Learn**: For additional machine learning functionality.

## Setup and Installation ⚙️
To run this project, you need to install the necessary Python libraries:

### For Apple Macs with Apple Silicon chips:
Setup virtual environment first for using pytorch:
```bash
python3 -m venv ~/venv-metal
source ~/venv-metal/bin/activate
python -m pip install -U pip
```
Then activate your virtual environment:
```bash
source 'your-venv-name'/bin/activate
```
After activating your python virtual environment, install necessary libraries:
```bash
pip3 install spotipy pandas scikit-learn torch
```

Signup for spotify developer program and create app [here](https://developer.spotify.com)

Change the credentials with yours in data collecting part.
```bash
sp = spotipy.Spotify(auth_manager=SpotifyOAuth(scope=scope, client_id='your-client-id', client_secret='your-client-secret', redirect_uri='http://localhost/'))
```
