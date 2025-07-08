# 🛠️ Animated Movie Scraper — TMDB Source

> **Part of the `Animation_Movie_Recommender` Project**  
> **Notebook Name:** `01_movie_scraper.ipynb`  
> **Status:** ✅ Completed  
> **Source:** [The Movie Database (TMDB)](https://www.themoviedb.org/)

---

## 🎯 Objective

This notebook is dedicated to scraping **animated movie metadata** from TMDB (The Movie Database) using their public API. The goal was to collect a **comprehensive and high-quality dataset** of animated films to power the upcoming **ethical value-based recommender system**.

---

## 🌐 Data Source

All movie metadata in this dataset was sourced from:

> **📌 [TMDB – The Movie Database](https://www.themoviedb.org/)**  
> TMDB is a popular open-source and community-driven movie database used by many apps and platforms. Data was collected **only for learning and personal research purposes** in compliance with TMDB API usage guidelines.

---

## 🔍 Features Collected

For each animation movie, the following key fields were collected:

- Movie Title
- Description (Overview)
- Genre Tags
- Original Language
- Release Date
- Runtime
- Popularity
- Vote Average
- Vote Count
- Poster URL
- Platform Availability (when available)

---

## ⚙️ Process Overview

| Step | Description |
|------|-------------|
| 1️⃣ | Registered and authenticated via TMDB API |
| 2️⃣ | Automated scraping across **1,600+ pages** (~30,000+ animation movies) |
| 3️⃣ | Filtered for valid and relevant movie records |
| 4️⃣ | Cleaned missing/invalid values (e.g., null runtimes, empty overviews) |
| 5️⃣ | Removed duplicate titles and standardized naming |
| 6️⃣ | Feature engineered additional columns:`release_year`,`release_year_month`, `release_decade`, `is_short_film` (runtime < 40 min) , `formatted_title` = Title (Year) |
| 7️⃣ | Saved as final cleaned CSV: `animation_movies_scrapper.csv` |

---

## 📁 Output File

- **File Name:** `(animation_movies_featured.csv)[]`  
- **Shape:** `9751 rows × 22 columns`  
- ✔️ Cleaned, deduplicated, and feature-rich dataset  
- ✔️ Ready for NLP analysis, tagging, and recommendation logic

---

## 📌 Notes

- Only animation genre movies were fetched using `with_genres=16` parameter in TMDB.
- TMDB API rate limits were respected by adding strategic pauses in the loop.
- This notebook is the **foundation step** of the recommender system project.

---

## 📢 Disclaimer

> This dataset is collected solely for **educational and non-commercial** purposes.  
> All rights to the original data belong to TMDB and their content contributors.

---

## 🚀 Next Step

→ Move to **NLP-based keyword extraction** and **value tagging** from user reviews/comments.

---
