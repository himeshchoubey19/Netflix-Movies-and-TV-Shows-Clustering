# 🎬 Netflix Movies and TV Shows Clustering

This project performs unsupervised machine learning using **KMeans Clustering** to group Netflix titles (movies and TV shows) based on attributes like genre, duration, release year, rating, and country. The goal is to discover hidden patterns and similarities among content without using predefined labels.

---

## 📌 Objective

To analyze and group Netflix content into clusters using machine learning techniques, helping identify trends, similarities, and potential use cases for recommendations or market insights.

---

## 📂 Dataset

- **File:** `NETFLIX MOVIES AND TV SHOWS CLUSTERING.csv`
- **Source:** Contains metadata of Netflix Movies and TV Shows including:
  - Type (Movie/TV Show)
  - Title, Director, Cast, Country
  - Date Added, Release Year
  - Rating, Duration, Genres
  - Description

---

## 🧪 Workflow

### 1. Data Cleaning
- Dropped irrelevant columns: `title`, `director`, `cast`, `description`
- Removed rows with missing values in critical columns
- Reset the index for clean processing

### 2. Feature Engineering
- Converted `duration` into numeric values in minutes
- Extracted main genre from the `listed_in` column
- Applied Label Encoding on categorical variables: `type`, `country`, `rating`, and `main_genre`

### 3. Data Scaling
- Used `StandardScaler` to normalize all numeric features for fair clustering

### 4. Clustering
- Applied **KMeans** clustering with `n_clusters = 4`
- Assigned each record to one of the clusters based on features

### 5. Cluster Analysis
- Used `groupby()` to analyze and understand the average characteristics of each cluster

---

## 🛠️ Tech Stack

- Python
- Pandas
- Scikit-learn (LabelEncoder, StandardScaler, KMeans)
- Jupyter Notebook

---

## 📈 Sample Insights

After clustering, we observed:
- Clusters that group together long-duration movies vs short TV shows
- Genre and rating-based clusters
- Trends based on release years and countries

---
