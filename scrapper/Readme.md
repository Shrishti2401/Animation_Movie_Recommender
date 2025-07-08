# 🛠️ TMDB Animation Movie Scraper

> **Notebook:** `01_movie_scrapper.ipynb`  
> **Source:** [TMDB - The Movie Database](https://www.themoviedb.org/)  
> **Status:** ✅ Completed  
> **Final Output File:** `animation_movies_featured.csv`

---

## 🎯 Objective

This notebook automates the scraping and enrichment of **animated movie metadata** from TMDB using their API. It serves as the **foundational dataset builder** for our project:  
**👉 Animation_Movie_Recommender (based on ethical values & life lessons).**

---

## 🌐 Data Source

> All movie data is sourced from **[TMDB - The Movie Database](https://www.themoviedb.org/)** using their official API.  
> This is for **educational and non-commercial use** in line with their guidelines.

---

## 📋 Table of Contents

- [1. Import Libraries](#1-import-libraries)
- [2. Configuration and Setup](#2-configuration-and-setup)
- [3. Batched Scraping Loop](#3-batched-scraping-loop)
- [4. Data Cleaning: Remove Duplicates](#4-data-cleaning-remove-duplicates)
- [5. Feature Engineering](#5-feature-engineering)
- [6. Preview Final Data](#6-preview-final-data)

---

## 🧪 Steps Performed

### ✅ 1. Scraping Logic:
- Used TMDB's `discover/movie` and `movie/{id}` endpoints.
- Total ~1600+ pages with `with_genres=16` (animation).
- Excluded **anime** using language + keyword filters.
- Scrapped till 500 pages , as pages after 500 do not contain Target data.
- Batches were saved with progress checkpointing.

### ✅ 2. Cleaning & Processing:
- Removed movies with duplicate `movie_id`
- Handled null values and missing titles
- Updated invalid or missing release dates
- Filtered short films (runtime < 40 mins)

### ✅ 3. Feature Engineering:
- `release_year`, `release_year_month`, `release_decade`
- `is_short_film` flag and `title (year)` formatting
- Cleaned runtime = 0 → converted to `Unknown`

---

## 📁 Output Summary

| File                          | Description                            |
|-------------------------------|----------------------------------------|
| `animation_movies_featured.csv` | Final cleaned and feature-engineered dataset |

- **Shape:** `9751 rows × 22 columns`
- **Columns include:** title, rating, genres, runtime, platform fields, value tags, and more

---

## 📌 Notes

- API key must be set manually (`API_KEY = '...'`) before use.
- Skipped pages and checkpointing help handle large-scale scraping.
- Rate-limiting (429 errors) handled with sleep intervals.

---

## 🚀 Next Step

→ Use this dataset to extract **ethical values** from user comments, reviews, or taglines. This will power a **value-driven recommendation engine** in the next phase.

---

## 📢 Disclaimer

This project and dataset are created solely for **educational, personal, and non-commercial** use.  
All data belongs to **TMDB and its contributors.**

---
