# Music Mood Prediction Project 🎧

## Project Overview 🔎
For my project, I'm using the Spotify API to get my top tracks and analyze them to figure out their mood. Basically, I'm taking different audio features from these songs – like how fast they are, their beat, and other stuff – and using deep learning to sort them into mood categories. This way, I'm hoping to see if we can predict the vibe of a song just by its technical features. It's like making a smart playlist that understands how you feel!

## Motivation 🚀
The goal of this project is to explore the intricate relationship between my personal music preferences and my mood. Recognizing that many of us spend thousands of minutes each year immersed in music, I was inspired by my own Spotify Wrapped stats, which showed over 30,000 minutes of music consumption last year. This staggering amount led me to ponder: Does the music I listen to influence my mood, or does my mood dictate my music choices? To unravel this, I'm using classification models in deep learning to analyze the mood of the songs I listen to most frequently. By extracting various audio features from these tracks through the Spotify API, I aim to establish a correlation between the emotional tone of the music and my own emotional states. This project not only offers a personalized introspection into my musical journey but also contributes to the broader understanding of how music impacts our daily lives.

## Data Analysis 🧐
- **Data Collection:** Leveraged the Spotipy library to access Spotify's vast music database, meticulously gathering data on my top tracks. Due to API constraints, I segmented the data retrieval across different time frames to ensure comprehensive coverage.
- **Data Cleaning and Enrichment:** Undertook a rigorous data cleaning process to rectify format inconsistencies and enhance the dataset with additional relevant features. This step was crucial in preparing the data for detailed analysis.
- **Exploratory Data Analysis (EDA):** Conducted thorough exploratory data analysis to assess the quality and sufficiency of the collected data. This phase involved examining trends, patterns, and outliers, providing valuable insights and guiding the subsequent stages of the project.
- **Feature Engineering:** Implemented advanced feature engineering techniques to refine and transform the dataset, making it more conducive for machine learning algorithms. This process involved creating new features and modifying existing ones to capture the essence of the music more effectively.
- **Machine Learning Model Development:** Designed and trained a machine learning model tailored to predict the moods of songs based on the processed data. This model incorporated a blend of audio features and was fine-tuned to accurately classify tracks into specific mood categories.

## Findings 🔮

- I realized that overall mood of my songs were energetic, where sad musics are too small to take into the consideration. 
- I found out that energy and loudness has very high correlations hence, I will try to add more musics with high loudness to my playlists.

## Limitations and Future work. 📈
- **Overcoming API Limitations:** Due to the constraints within the Spotify Developer Program, I strategically collected my music data in CSV format. This approach allowed me to circumvent API limitations and gather the necessary information efficiently.
- **Future Expansion and Data Enhancement:** Looking ahead, I plan to establish a routine for data collection, continuously updating my dataset at regular intervals. This will not only enrich the dataset with a broader range of music preferences over time but also enhance the reliability and depth of the insights I can draw. 
- **Integration with Health Metrics:** An exciting dimension of my future work involves correlating my music listening habits with various health metrics. By doing this, I aim to develop a more holistic understanding of the interplay between the music I listen to and my mood. This integration promises to not only refine the mood predictions of songs but also explore the potential of music as a reflective tool for emotional and mental well-being.

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
