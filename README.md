# IMDB Movie Analysis – Excel Project 

## 1. Project Overview

This project analyzes IMDB movie data to identify factors that influence movie success, defined by **IMDB ratings**. The insights from this analysis can help movie producers, directors, and investors make informed decisions when planning future projects.

**Objective:** Determine which factors – genre, duration, language, director, and budget – contribute to higher IMDB ratings and overall movie success.

---

## 2. Data Cleaning

Before analysis, the dataset was preprocessed with the following steps:

1. **Handling Missing Values:** Removed rows with missing IMDB ratings or budget/gross figures.
2. **Removing Duplicates:** Ensured each movie is unique based on title and release year.
3. **Data Type Conversion:**  
   - Budget and gross earnings converted to numeric format.  
   - Duration converted to minutes.  
   - Genres separated into individual entries for multi-genre movies.
4. **Feature Engineering:**  
   - Calculated **Profit Margin** = Gross Earnings − Budget.  
   - Extracted **Primary Genre** for simplified analysis.

---

## 3. Data Analysis

### A. Movie Genre Analysis
**Goal:** Determine the impact of genre on IMDB ratings.  

**Steps:**  
- Counted movies per genre using `COUNTIF`.  
- Calculated descriptive statistics for IMDB scores per genre: Mean, Median, Mode, Range, Variance, and Standard Deviation.

**Insights:**  
- Most common genres: Drama, Comedy, Action.  
- Highest mean IMDB ratings observed in Drama and Biography.  
- Genre influences ratings: viewers prefer content-driven genres over purely action-packed ones.

---

### B. Movie Duration Analysis
**Goal:** Examine how movie duration impacts IMDB ratings.  

**Steps:**  
- Calculated mean, median, and standard deviation of movie durations.  
- Created scatter plot of **Duration vs IMDB Rating** and added a trendline.

**Insights:**  
- Average movie duration: ~120 minutes.  
- Positive but weak correlation between longer movies and higher ratings.  
- Extremely short (<80 mins) or very long (>180 mins) movies often had lower ratings.

---

### C. Language Analysis
**Goal:** Explore the impact of language on movie ratings.  

**Steps:**  
- Counted movies per language using `COUNTIF`.  
- Calculated mean, median, and standard deviation of IMDB scores per language.

**Insights:**  
- Most common languages: English, Hindi, French.  
- English-language movies have slightly higher mean ratings.  
- Language alone is not a strong predictor of success.

---

### D. Director Analysis
**Goal:** Identify directors with the most successful movies.  

**Steps:**  
- Calculated average IMDB score per director.  
- Used `PERCENTILE` to determine top-performing directors.

**Insights:**  
- Top directors consistently have movies above the 90th percentile in ratings.  
- Notable directors: Christopher Nolan, Steven Spielberg, Quentin Tarantino.  
- Experienced directors significantly influence movie success.

---

### E. Budget Analysis
**Goal:** Assess the impact of movie budgets on financial success.  

**Steps:**  
- Calculated correlation between **Budget** and **Gross Earnings** using `CORREL`.  
- Calculated **Profit Margin** = Gross − Budget.  
- Identified movies with the highest profit margin using `MAX`.

**Insights:**  
- Positive correlation (~0.7) between budget and gross earnings.  
- Some low-budget movies achieved exceptional profit margins due to high audience reception.  
- Budget is a strong factor in financial success but does not guarantee high ratings.

---

## 4. Five Whys Analysis Example
**Problem:** Movies with higher budgets tend to have higher ratings.  

1. **Why?** Higher budgets allow better production quality.  
2. **Why?** Better production quality improves viewer experience.  
3. **Why?** Enhanced viewer experience leads to higher ratings.  
4. **Why?** Positive experiences lead to positive reviews.  
5. **Why?** Positive reviews influence others to watch the movie, increasing popularity and success.

---

## 5. Conclusion & Recommendations

- **Genre:** Drama and biography films consistently receive higher ratings.  
- **Duration:** Optimal movie length is 90–150 minutes for better audience reception.  
- **Language:** English movies dominate ratings and reach, but high-quality movies in other languages can also succeed.  
- **Directors:** Experienced directors significantly influence movie ratings and success.  
- **Budget:** Higher budgets correlate with higher revenue, but creative content ensures high ratings.

**Actionable Insights:**  
1. Focus on compelling storytelling within genres favored by audiences.  
2. Maintain an optimal movie duration to maximize ratings.  
3. Invest in skilled directors to enhance quality and reception.  
4. Budget wisely: a high budget improves revenue potential but creative content ensures high ratings.

---
