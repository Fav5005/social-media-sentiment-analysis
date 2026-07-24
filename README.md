# 📊 Social Media Sentiment Analysis

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)

> An end-to-end data analytics project exploring user sentiment, engagement metrics, and interaction trends across social media platforms built entirely in Python within Jupyter Notebook.

---

## 📑 Table of Contents
- [Project Overview](#-project-overview)
- [Data Sources](#-data-sources)
- [Tools Used](#%EF%B8%8F-tools-used)
- [Data Cleaning & Preparation](#-data-cleaning--preparation)
- [Exploratory Data Analysis](#-exploratory-data-analysis-eda)
- [Data Visualizations](#-data-visualizations)
- [Key Insights](#-key-insights)
- [References](#-references)

---

## 📌 Project Overview
This project examines social media performance and user sentiment using a structured Python data pipeline. By processing raw engagement metrics and sentiment scores directly within Jupyter Notebook, it identifies top-performing content categories, analyzes user sentiment distribution (Positive, Neutral, Negative), and surfaces actionable engagement patterns across time and platforms.

---

## 📁 Data Sources
The primary dataset used for this analysis is a structured CSV file containing social media engagement metrics and sentiment scores:

| Field Name | Type | Description |
| :--- | :--- | :--- |
| `Post_ID` | String | Unique identifier for each post |
| `Platform` | Categorical | Social media channel (Twitter, Instagram, etc.) |
| `Sentiment` | Categorical | Sentiment flag (`Positive`, `Neutral`, `Negative`) |
| `Sentiment_Score` | Numeric | Calculated polarity score |
| `Likes` | Integer | Total like counter |
| `Retweets/Shares` | Integer | Total share/repost counter |
| `Comments` | Integer | Total comment counter |
| `Timestamp` | Datetime | Date and time of post publication |

---

## 🛠️ Tools Used
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Environment & Version Control:** Jupyter Notebook, Git, GitHub

---

## 🧹 Data Cleaning & Preparation
Raw data was processed using Python and Pandas through a structured cleaning pipeline before analysis:

1. **Handling Missing Values:** Imputed missing numerical engagement values using median strategies and dropped unrecoverable text fields.
2. **Deduplication:** Filtered out duplicate post entries based on unique identifiers.
3. **Data Type Standardization:** Parsed timestamp strings into `datetime` objects and standardized categorical text formatting.
4. **Log Transformations:** Applied logarithmic scaling ($\log(x + 1)$) to heavily skewed engagement metrics using `numpy.log1p()` to handle extreme outliers and address overplotting.

---

## 📊 Exploratory Data Analysis (EDA)
Key analyses conducted using Pandas and Matplotlib/Seaborn:

* **Sentiment Distribution:** Evaluated overall ratios of Positive, Neutral, and Negative posts.
* **Engagement vs. Sentiment:** Correlated high engagement (likes, shares) with specific sentiment polarities using scatter plots and box plots.
* **Time-Series Trends:** Mapped engagement volume and sentiment fluctuations over time using Pandas resampling and line plots.
* **Category Performance:** Aggregated top content categories using bar charts to measure overall audience interaction.

---

## 📉 Data Visualizations
All charts and plots were rendered directly in the Jupyter Notebook using Matplotlib and Seaborn:

* **Distribution Plots:** Histograms and KDE plots showing post engagement spreads before and after log transformations.
* **Sentiment Comparison:** Seaborn categorical plots (boxplots and bar charts) displaying median likes and comments by sentiment group.
* **Correlation Heatmaps:** Correlation matrix identifying relationships between likes, shares, comments, and sentiment scores.
* **Time Trends:** Resampled line plots charting sentiment shifts across days and peak activity hours.


## 💡 Key Insights
* **Positive Content Virality:** Posts with positive sentiment achieved a noticeably higher median engagement rate compared to neutral or negative content.
* **Optimal Posting Window:** Peak user engagement consistently concentrated in late afternoon and early evening hours.
* **Platform Dynamics:** Visual platforms yielded significantly higher comment-to-like ratios than text-first networks.

---

## 🔗 References
* [Python Documentation](https://docs.python.org/3/)
* [Pandas Documentation](https://pandas.pydata.org/docs/)
* [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
* [Seaborn Documentation](https://seaborn.pydata.org/)
