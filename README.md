# 📊 OTT Content Performance Analysis

An end-to-end **Data Analytics project** focused on analyzing OTT platform content using **SQLite, SQL, Excel, and Power BI**.  
This project provides insights into content distribution, ratings, genres, countries, and release trends through interactive dashboards.

---

## 🧩 Project Overview

OTT platforms generate massive content data.  
This project analyzes OTT content to answer key business questions such as:
- Which genres are most popular?
- Which countries produce the most content?
- How do ratings and duration vary by genre?
- What are the year-wise content release trends?

---

## 🛠️ Tools & Technologies Used

- **SQLite** – Data storage and querying  
- **SQL** – Data extraction & aggregation  
- **Microsoft Excel** – Initial analysis & pivot insights  
- **Power BI** – Interactive dashboards & visual storytelling  

---

## 📂 Dataset Details

**Source:** Sample OTT content dataset  


**Key Columns:**
- `title`
- `type` (Movie / TV Show)
- `genre`
- `country`
- `release_year`
- `rating`
- `duration_minutes`

---

## 🧮 SQL Queries Used

```sql
-- Total Titles
SELECT COUNT(*) AS total_titles FROM ott_content;

-- Average Rating
SELECT ROUND(AVG(rating), 2) AS avg_rating FROM ott_content;

-- Highest Rating
SELECT MAX(rating) AS highest_rating FROM ott_content;

-- Titles by Genre
SELECT genre, COUNT(*) AS total_titles
FROM ott_content
GROUP BY genre
ORDER BY total_titles DESC;

-- Titles by Country
SELECT country, COUNT(*) AS total_titles
FROM ott_content
GROUP BY country
ORDER BY total_titles DESC;

-- Year-wise Trend
SELECT release_year, COUNT(*) AS total_titles
FROM ott_content
GROUP BY release_year
ORDER BY release_year;
---


