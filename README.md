# Apify-Tiktok-Scraper-Using-Python

---

# 📊 TikTok Video Performance Analysis

## 📌 Project Overview

This project analyzes TikTok video performance using scraped data from Apify TikTok Scraper. The goal is to understand which factors influence engagement rate and to explore both statistical and predictive modeling approaches.

The dataset contains 50 TikTok videos with metadata such as:

* Posting time
* Video duration
* Music information
* Caption text
* Engagement metrics (likes, comments, shares, saves, views)

---

## 🎯 Business Questions

1. What is the best posting time?
2. Does weekend posting improve engagement?
3. Does video duration affect engagement?
4. Does original music perform better?
5. Do hashtags influence engagement?
6. Can we predict engagement rate?
7. Can we segment video performance into clusters?

---

## 📂 Dataset Features

Key columns used:

* `diggCount` (likes)
* `commentCount`
* `shareCount`
* `collectCount`
* `playCount`
* `videoMeta.duration`
* `musicMeta.musicOriginal`
* `createTimeISO`
* `text` (caption)

Derived features:

* Engagement = likes + comments + shares + saves
* Engagement Rate = engagement / playCount
* Posting hour
* Time category (morning, afternoon, evening, late night)
* Hashtag count
* Log-transformed engagement rate

---

# 🔎 Exploratory Data Analysis

EDA revealed:

* Engagement distribution is right-skewed.
* Posting time varies but is not evenly distributed.
* Hashtag usage varies significantly across videos.
* Some videos show high engagement despite low view count, indicating niche audience behavior.

---

# 📈 Regression Analysis

A multiple linear regression model was built to test:

* Posting time
* Video duration
* Music originality
* Hashtag count

### Key Findings:

* The overall model was not statistically significant (p > 0.05).
* Most predictors were not individually significant.
* Posting at 5 AM showed a negative significant effect.
* R-squared suggested moderate variance explanation but low adjusted R-squared due to small sample size.

### Interpretation:

Engagement performance may be driven by more complex or non-linear factors rather than simple structural variables like time or duration.

---

# 🤖 Predictive Modeling (Random Forest)

A Random Forest Regressor was implemented to capture non-linear relationships.

* Data split into train/test sets
* Feature importance was extracted
* Model evaluated using R² score

Random Forest showed stronger predictive signals compared to linear regression, suggesting engagement patterns are likely non-linear.

---

# 📊 Clustering Analysis

K-Means clustering was used to segment videos into performance groups based on:

* Engagement rate
* Play count

This resulted in 3 clusters:

* Low-performing videos
* Medium-performing videos
* High-performing / viral videos

This segmentation helps identify content performance tiers.

---

# 🧠 Key Insights

* Posting day (weekday vs weekend) does not significantly affect engagement.
* Video duration and music originality are not strong drivers in this dataset.
* Hashtag usage may play a more important role.
* Engagement appears to be influenced by complex, potentially non-linear factors.
* Content quality and relevance likely play a larger role than structural variables.

---

# ⚠️ Limitations

* Small dataset (n = 50)
* Uneven distribution across posting hours
* External algorithm factors not observable
* No follower count variable available

Future improvements:

* Larger dataset (500+ videos)
* Sentiment analysis on captions
* Topic modeling on hashtags
* Advanced models (XGBoost, SHAP analysis)

---

# 🚀 Conclusion

This project demonstrates:

* Feature engineering
* Statistical regression analysis
* Hypothesis testing
* Machine learning modeling
* Performance clustering
* Insight storytelling

The results suggest that TikTok engagement is complex and may not be fully explained by simple structural variables. Non-linear modeling provides stronger predictive power, indicating the importance of advanced modeling approaches in social media analytics.

---

Kalau kamu mau, aku bisa:

* Buat versi lebih ringkas
* Buat versi lebih formal untuk recruiter
* Tambahkan visualisasi section
* Tambahkan project architecture diagram
* Atau bikin LinkedIn post summary 🔥
