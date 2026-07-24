# 🎬 Netflix Titles — Data Cleaning & Exploratory Analysis

Clean and analyze the Netflix Titles dataset to explore genres, countries, ratings, and release/addition trends — with 10 fully visualized insights.

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Pandas](https://img.shields.io/badge/Pandas-3.0-150458)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.10-11557c)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-4c72b0)

## 📌 Project Overview

This project performs an end-to-end exploratory data analysis (EDA) on the [Netflix Movies and TV Shows dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows) (8,807 titles). It covers data cleaning, feature engineering, and visualization to answer questions like:

- Does Netflix host more Movies or TV Shows?
- How has the catalog grown year over year?
- Which countries and genres dominate the catalog?
- What content ratings and durations are most common?
- Is there seasonality in when content is added?

## 🗂️ Repository Structure

```
├── netflix_titles.csv              # Raw dataset
├── netflix_titles_cleaned.csv      # Cleaned dataset (output of the notebook)
├── Netflix_Data_Analysis.ipynb     # Main analysis notebook (cleaning + EDA + visuals)
├── figs/                           # Exported chart images (PNG)
└── README.md
```

## 🧹 Data Cleaning Steps

- Filled missing `director`, `cast`, and `country` values with `"Unknown"` (missing at high rates, not safe to drop).
- Dropped the small number of rows missing `rating` or `date_added` (<0.2% of data).
- Parsed `date_added` into a proper datetime and removed duplicate title/director/country combinations.
- Engineered new features: `year_added`, `month_added`, `primary_country`, `duration_int` / `duration_unit`, and an exploded `genre_list`.

## 📊 Visualizations Included

1. Content type share (Movies vs. TV Shows)
2. Catalog growth over time (2008–2021)
3. Top 10 content-producing countries
4. Top 15 genres
5. Content rating distribution
6. Release year distribution
7. Movie duration distribution
8. TV show season counts
9. Content-addition heatmap (month × year)
10. Most prolific directors

## 🔑 Key Insights

- Movies make up ~70% of the catalog vs. ~30% TV Shows.
- Content additions grew rapidly 2015–2019, then dipped slightly in 2020–2021 (COVID-19 production slowdowns).
- The **U.S., India, and U.K.** are the top three content-producing countries.
- **International Movies, Dramas, and Comedies** are the most common genres.
- **TV-MA** and **TV-14** dominate — the catalog skews toward mature/teen audiences.
- Most TV shows have only **one season**, and most movies run **80–120 minutes**.

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Netflix_Data_Analysis.ipynb
```

## 📁 Dataset Source

[Netflix Movies and TV Shows — Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)

## 🛠️ Tools Used

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Jupyter Notebook`
