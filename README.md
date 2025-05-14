# IMDB Horror Movie Data Analysis (2020–2024)

This project analyzes new horror movies from **2020 to 2024**, with a focus on **quality, runtime, and sub-genre trends** using data from **TMDb** and **OMDb** APIs.

---

# Objectives

- Retrieve and clean a dataset of horror feature films (2020–2024)
- Merge **TMDb** genre/year filtering with **OMDb** IMDb rating and runtime data
- Analyze trends in:
- IMDb rating quality (ratio of movies rated > 7.0)
- Runtime trends (percentage of movies over 100 minutes in length)
- Most viewed sub-genres through highest-rated titles
- Highest-rated 10 horror films of the period under consideration

---


# Sources of Data

- **TMDb (The Movie Database)** — Used to gather horror films by sub-genre and year
- **OMDb (Open Movie Database)** — Used to append TMDb titles with:
- IMDb rating
- Runtime
- Complete genre string

APIs were requested with Python's `requests` library and combined into a single cleaned DataFrame with ~220 entries.


# Preprocessing

- Dropped rows with missing or invalid (`N/A`) data
- Converted year, runtime, and ratings to numeric types
- Removed "Horror" from genre breakdown to split sub-genres
- Saved entire dataset to CSV for reproducibility


# Key Findings

- The percentage of horror movies with **IMDb ratings > 7.0** fluctuated from year to year, with occasional banner years.
- Movies longer than **100 minutes** appeared more regularly but were not necessarily associated with higher ratings.
- Top-rated sub-genres were **Thriller, Mystery, and Drama**, indicating a trend towards psychological storytelling.
- The **Top 10 highest-rated movies** reflected global diversity and strong critical support.


# Files

| horror_movies_2020_2024_tmdb_omdb.csv - Cleaned final dataset 
| `IMDb Horror Scraper Final.ipynb - Central Jupyter notebook (data collection, analysis, plots) 
|  README.md This document 

---

# Requirements

- Python 3
- VSCode
- Libraries: `requests`, `pandas`, `seaborn`, `matplotlib`
- API keys: OMDb and TMDb

---

# Future Work

- Add box office/budget information
- Include Rotten Tomatoes or Metacritic ratings

