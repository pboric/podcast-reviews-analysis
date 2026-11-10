# Podcast Reviews Analysis

An analysis of podcast reviews from a SQLite database (podcasts, categories and reviews) with SQL, pandas, sentiment
analysis and hypothesis tests: which podcasts and categories get the most and the best reviews, and does review
activity go together with more positive reviews?

## Key findings

- Ratings are very positive overall: average ratings per category are mostly between 4.4 and 4.8 out of 5.
- **Review frequency and sentiment:** the correlation between how often a podcast is reviewed and how positive its
  reviews are is practically zero (r = −0.02). It is statistically significant only because the dataset is very
  large.
- **Newer podcasts:** there is no evidence that newer podcasts receive higher initial ratings (slope p = 0.47).
- **Popular categories:** categories with more reviews have slightly *less* positive sentiment (r = −0.20,
  p = 0.04), the opposite of the hypothesis.

## What the notebook covers

1. Exploring the database schema and joining the tables with SQL (including a CTE that aggregates categories)
2. Cleaning: consolidating similar categories, missing values and duplicates
3. EDA: rating distribution, reviews over time, top podcasts and categories by review count and average rating
4. Sentiment of review texts with TextBlob, and word clouds
5. Three hypothesis tests (Pearson correlation and linear regression)

## Repository

| File | Content |
|---|---|
| [`podcast_reviews_analysis.ipynb`](podcast_reviews_analysis.ipynb) | The full analysis |
| `Podcasts_Reviews_Analysis.pdf` | A short summary with the main charts |

## Data

[Podcast Reviews](https://www.kaggle.com/datasets/thoughtvector/podcastreviews) by Thoughtvector on Kaggle (SQLite
database, not included; licence CC BY-NC-SA 4.0). Download `database.sqlite` and put it next to the notebook.

## Run it

```bash
pip install -r requirements.txt
jupyter notebook podcast_reviews_analysis.ipynb
```

## License

MIT (code). The data has its own licence, see above.
