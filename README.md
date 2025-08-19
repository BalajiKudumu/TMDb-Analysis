# TMDB Movies Data Analysis

## Project Overview
This project analyzes the TMDB Movies dataset to uncover trends, relationships, and insights regarding movie popularity, budget, revenue, runtime, genres, and other features. The goal is to understand which factors contribute to a movie's success in terms of popularity and revenue.

The analysis includes data wrangling, visualization, and exploration of relationships between different features.

---

## Dataset
The dataset contains information about 10,866 movies with 21 attributes, including:

- `popularity`
- `budget` & `budget_adj`
- `revenue` & `revenue_adj`
- `original_title`
- `cast`, `director`, `genres`, `production_companies`
- `runtime`, `vote_count`, `vote_average`, `release_year`
- Other metadata like `tagline`, `keywords`, `homepage`

Missing values were handled as follows:

- Object type columns (`cast`, `director`, `tagline`, `keywords`, `genres`, `production_companies`) filled with `"missing"`
- Numeric columns (`budget`) replaced 0 values with `NaN`

Non-useful columns like `id`, `imdb_id`, `homepage`, and `overview` were dropped.

---

## Key Questions and Findings

### 1. Does higher budget mean higher popularity?
- Scatter plot and grouped analysis indicate that high-budget movies tend to have higher popularity.
- High-budget movies show ~55% higher average popularity than low-budget movies.
- **Conclusion:** Higher budget increases the likelihood of higher popularity, but it is not a strict guarantee.

### 2. Does runtime affect popularity?
- Movies were grouped as short (<100 mins), medium (100–200 mins), and long (>200 mins).
- Popularity is highest for medium-length movies (around 120–150 mins).
- **Conclusion:** Extremely long movies (>200 mins) do not necessarily gain high popularity.

### 3. Does higher popularity mean higher profits?
- Created a new column `profit = revenue - budget`.
- Movies with higher popularity generate significantly higher average profits.
- **Conclusion:** Popularity is a strong indicator of profitability.

### 4. Features of Top 10 Revenue Movies
- Top 10 revenue movies have:
  - Runtime: 100–200 mins
  - Release year: 1995–2015
- High budgets, high popularity, and medium runtimes are common among these top earners.

### 5. Most popular genres over the years
- Drama, Comedy, Action, Horror, and Adventure dominate the dataset.
- Over time, both the quantity and diversity of movies increased.
- Heatmaps of budget and revenue by genre and year show high-budget movies do not always yield high revenue.

---

## Visualizations
- Scatter plots for budget vs. popularity and runtime vs. popularity
- Bar charts for average popularity by budget and runtime
- Histograms for top 10 revenue movies
- Heatmaps for revenue and budget across genres and years
- Bar plots for genre occurrence frequency

---

## Conclusions
- High-budget movies generally achieve higher popularity (~55% increase), but budget alone is not sufficient for success.
- Medium-length movies (120–150 mins) tend to be more popular.
- Popularity is strongly correlated with profit.
- Drama, Comedy, and Action are consistently the most popular genres.
- Movie production and audience choice diversity increased over the years.

---

## Limitations
- Missing and zero values may impact analysis.
- Popularity and vote counts metrics are not fully transparent.
- Currency and inflation adjustments were not fully accounted for.
- Foreign movie financial data may not be consistent.

---

## References
- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Kaggle TMDB Movies Dataset](https://www.kaggle.com)



## 📬 Contact

Maintained by **Balaji Kudumu**  
If you use this project in your research, please give appropriate credit.

---

## 📄 License

MIT License - see `LICENSE` file for details.
