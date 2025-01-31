### Project Overview:
This project involves analyzing Spotify usage data to gain insights into listening behavior, music preferences, and patterns in playback over time. The data includes information on individual song plays, artist names, album names, play timestamps, and whether the song was skipped or played on shuffle. The analysis is performed using a variety of techniques such as data cleaning, feature engineering, statistical analysis, visualization, and machine learning.

### Key Sections of the Project:
1. **Data Preprocessing and Cleaning**: 
   - The dataset is loaded and checked for missing values. 
   - Missing values in certain columns are filled using forward-fill.
   - Data is cleaned and irrelevant rows are removed.
   - The timestamp is converted into a readable format, and new features (e.g., date, hour, day of the week, month, year) are created.

2. **Exploratory Data Analysis (EDA)**: 
   - Summary statistics and visualizations are created to explore trends in playback data. 
   - Key insights are drawn, including:
     - The most-played tracks, artists, and albums.
     - Playback trends over time (daily, monthly, quarterly).
     - Analysis of shuffle and skip behavior.
     - Insights into when people tend to listen to music (hourly and weekly patterns).
     - The diversity of tracks and artists played over time.
   
3. **Modeling**:
   - A logistic regression model is built to predict whether a track will be skipped based on features like playback time, shuffle status, and quarter of the year.
   - Model performance is evaluated using accuracy and classification metrics.
   
4. **Clustering**:
   - A K-Means clustering algorithm is applied to segment listening behavior based on features like playback time, shuffle status, and skip behavior.
   - Clusters are visualized to understand different types of listeners or listening habits.

5. **Sentiment Analysis**:
   - Sentiment analysis is performed on track names to determine the sentiment polarity of each track. This provides insights into whether the names of the tracks tend to have positive or negative sentiment.

### Visualizations:
1. **Daily Playback Trend**: A line plot showing the total playback time (in milliseconds) per day, highlighting daily trends.
2. **Top 10 Most Played Tracks**: A bar plot visualizing the tracks with the most total playback time.
3. **Top 10 Most Played Artists**: A bar plot displaying the artists with the highest total playback time.
4. **Playback Time Distribution by Quarter**: A boxplot to understand how playback times vary across different quarters.
5. **Shuffle and Skipped Analysis**: A stacked bar chart showing the number of plays when shuffle is on/off and whether the track was skipped.
6. **Hourly and Daily Listening Activity**: A heatmap showing hourly listening patterns across different days of the week.
7. **Monthly Diversity**: A line plot comparing the number of unique tracks and unique artists listened to each month.
8. **Top Skipped Artists**: A bar plot showing artists with the highest skip rate.
9. **Clustering of Playback Data**: A pair plot visualizing clusters of playback behavior.

### Machine Learning Model:
- **Logistic Regression**: The logistic regression model is used to predict whether a song is likely to be skipped based on features like `ms_played`, `shuffle`, and `quarter`.
- **Model Evaluation**: The model's performance is evaluated using classification metrics such as accuracy, precision, recall, and F1-score.

### Requirements:
To run this project, you will need the following Python libraries:
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `plotly`
- `sklearn`
- `textblob`

### README File for GitHub:

```markdown
# Spotify Data Analysis Project

This project analyzes Spotify listening data to explore user behavior, music preferences, and playback trends. The analysis covers data preprocessing, exploratory data analysis (EDA), clustering, machine learning, and sentiment analysis to gain actionable insights into listening habits.

## Key Insights
- **Most Played Tracks and Artists**: The project identifies the top 5 tracks, artists, and albums based on total playback time.
- **Playback Trends**: Trends in daily and hourly listening activity are visualized to uncover when people listen to music the most.
- **Shuffle and Skip Behavior**: Analysis of whether users skip tracks more often when shuffle is enabled.
- **Clustering of Listening Behavior**: Using K-Means clustering to segment listeners based on playback time, shuffle status, and skip behavior.
- **Sentiment of Track Names**: An analysis of the sentiment polarity of track names using TextBlob.

## Project Structure

- `spotify_history.csv`: Raw Spotify usage data
- `spotify_data_analysis.ipynb`: Jupyter Notebook with the analysis and visualizations
- `README.md`: This file

## Installation

1. Clone this repository:

```bash
git clone https://github.com/yourusername/spotify-data-analysis.git
```

2. Install the required libraries:

```bash
pip install -r requirements.txt
```

Or manually install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn plotly scikit-learn textblob
```

## Usage

1. Upload your own `spotify_history.csv` file by running the code in the Jupyter Notebook.
2. Run the notebook step by step to see various visualizations, clustering results, and machine learning model evaluations.

## Data Description

The dataset (`spotify_history.csv`) contains the following columns:
- `ts`: Timestamp of the track play
- `track_name`: Name of the track
- `artist_name`: Name of the artist
- `album_name`: Name of the album
- `ms_played`: Total playback time in milliseconds
- `skipped`: Whether the track was skipped (0 = No, 1 = Yes)
- `shuffle`: Whether shuffle mode was enabled (0 = No, 1 = Yes)
- `reason_start`: Reason for playback start
- `reason_end`: Reason for playback end

## Visualizations
1. **Daily Playback Trend**: A line plot showing the total playback time per day.
2. **Top 10 Most Played Tracks**: A bar plot displaying the tracks with the highest total playback time.
3. **Top 10 Most Played Artists**: A bar plot of the most-played artists.
4. **Playback Time Distribution by Quarter**: A boxplot showing playback time distribution across different quarters of the year.
5. **Shuffle and Skip Behavior**: A bar chart showing the relationship between shuffle mode and skipping tracks.
6. **Hourly Listening Activity**: A heatmap of listening activity by hour and day of the week.

## Machine Learning Model

### Logistic Regression
- A logistic regression model is trained to predict whether a song is skipped based on features like playback time (`ms_played`), shuffle status, and quarter of the year.
- The model's accuracy and other classification metrics are evaluated.

## Clustering
- **K-Means Clustering** is used to group listeners into clusters based on their listening behavior.
- The clusters are visualized to understand distinct patterns in playback.

## Sentiment Analysis
- Sentiment analysis is performed on track names using TextBlob to determine the sentiment polarity.

## Conclusion

This project provides insights into listening behaviors and helps understand music consumption patterns. The analysis can be expanded by incorporating additional features or using more advanced models for prediction and classification.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
'''
