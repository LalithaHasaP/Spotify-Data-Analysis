Predicting the Next Most Streamed Song: A Data-Driven Music Analysis

## Overview:

Music is a powerful force that influences emotions, concentration, motivation, and memory. In this project, we explore the patterns and properties of top-charting songs over the past decade to answer a fascinating question:

**Can we predict the properties of the next most streamed song?**

Using the Spotify Top 100 Songs dataset (2010–2019) from Kaggle, we analyze trends in artist types, genres, and technical features like energy, loudness, and acousticness to identify what makes a song a chart-topper.


## Project Goals:

* Investigate common trends in popular songs from 2010 to 2019.
* Identify which song properties (e.g., energy, acousticness, loudness) are most strongly correlated.
* Use data visualizations to uncover patterns.
* Predict properties of future top songs.


## Dataset

**Source:** Kaggle
**Title:** Spotify Top 100 Songs of 2010-2019
**Rows:** 1000
**Columns:** 18

### Key Features Used:

* `bpm`: Beats Per Minute (tempo)
* `nrgy`: Energy
* `dnce`: Danceability
* `dB`: Loudness
* `acous`: Acousticness
* `pop`: Popularity
* `artist`, `top genre`, `artist type`, `position`


## Methodology

### 1. Data Cleaning & Preparation

* Loaded CSV data and removed any `NaN` rows.
* Focused on numerical columns for correlation analysis.
* Used visualizations to explore categorical variables like artist type and genre.

### 2. Exploratory Data Analysis (EDA)

* Pie charts for `artist type` distribution.
* Bar plots for top 10 genres and top 10 artists.
* Heatmap of correlation between numerical features.

### 3. Statistical Modeling

* Focused on songs in **Position 1** (top-charting).
* Built curve fitting models to examine:

  * Energy vs Loudness
  * Energy vs Acousticness
  * Acousticness vs Loudness


## Key Insights

* **Solo artists** dominate the charts.
* **Dance pop** is the most prevalent genre.
* Strong **positive correlation** between **energy** and **loudness**.
* Moderate **negative correlation** between **energy** and **acousticness**.
* Slight **negative correlation** between **acousticness** and **loudness**.


## Conclusion

The top song of the future is likely to be:

* A **pop** song
* By a **solo artist**
* With **high energy** and **high loudness**

This is supported by recent top hits:

| Year | Song               | Artist         | Loudness | Energy | Acousticness |
| ---- | ------------------ | -------------- | -------- | ------ | ------------ |
| 2020 | *Blinding Lights*  | The Weeknd     | -6       | 73     | 0            |
| 2021 | *Driver's License* | Olivia Rodrigo | -9       | 43     | 77           |
| 2022 | *As It Was*        | Harry Styles   | -5       | 73     | 34           |


## Technologies Used

* Python
* Pandas
* Matplotlib & Seaborn
* Plotly Express
* SciPy (`curve_fit`)


## How to Run

1. Clone the repo or download the notebook.
2. Make sure to install dependencies:

   ```bash
   pip install pandas matplotlib seaborn plotly scipy
   ```
3. Run the Jupyter Notebook to view all charts and analysis.

---

## Visual Outputs

* Pie charts of artist types
* Bar charts of top genres and artists
* Correlation heatmap
* Sunburst chart of top 5 artists and their genres
* Line plots from curve fitting (energy vs loudness, etc.)


## License

This project is for educational purposes. Dataset copyright belongs to original Kaggle contributors.
