# Investigate a Dataset — TMDb Movies

Udacity Data Analyst project. I used the TMDb movies dataset to clean data and answer two simple questions.

## What I Answered
1) What movies did **George Miller** direct and how were they rated?
2) In **2015**, which **3 genres** had the highest average popularity?

## Dataset
- Source: TMDb (Kaggle)
- File used: `Database_TMDb_movie_data/tmdb-movies.csv`
- Key columns: `popularity, budget, revenue, original_title, director, runtime, genres, release_date, vote_average`

## Steps (Very Short)
- Removed duplicates.
- Dropped high-null, non-essential columns (`homepage`, `tagline`, `keywords`, `production_companies`).
- Dropped rows missing: `imdb_id`, `cast`, `genres`, `director`, `overview`.
- Converted `release_date` to datetime and fixed future-year typos (e.g., 2066 → 1966).
- Filtered out rows with `runtime == 0` or `budget == 0` or `revenue == 0`.

## Results (Quick)
- **George Miller** top-rated in this dataset: *Mad Max: Fury Road (2015)* and *Mad Max 2 (1981)*.
- **2015 Top Genres by Popularity:** **Science Fiction**, **Western**, **Adventure**.

## How to Run
```bash
pip install -r requirements.txt  # optional
jupyter notebook Investigate_a_Dataset.ipynb
# or export:
python -m nbconvert --to html Investigate_a_Dataset.ipynb
