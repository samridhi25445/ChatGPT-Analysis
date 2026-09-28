# ChatGPT-Analysis
Analysis of 196k+ ChatGPT mobile app reviews (Jul 2023–Aug 2024). Explores user sentiment (88% positive), tracks monthly rating trends, and identifies key friction points—such as server errors, login issues, and post-update crashes—to provide actionable UX/stability improvements.

# 🤖 ChatGPT User Review Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo/blob/main/chatgpt_analysis.ipynb)

A comprehensive data analysis of 196k+ user reviews for the ChatGPT mobile application to uncover sentiment distribution, technical friction points, and usage trends over time.

---

## 📌 Project Overview
This project analyzes user feedback for the ChatGPT mobile application using a dataset of **196,727 user reviews** collected between **July 2023 and August 2024**. By evaluating rating distributions, text sentiments, and longitudinal patterns, this study aims to understand user satisfaction, isolate key friction points, and provide data-backed recommendations to enhance product reliability and user experience.

---

## 🎯 Problem Statement & Objectives
User feedback provides direct insights into application performance, user expectations, and functional bugs. The primary objective is to dissect user sentiment, trace temporal shifts in review volume and satisfaction, and categorize recurring issues causing negative ratings.

### Key Objectives
* **Sentiment Analysis:** Classify user feedback into positive, neutral, and negative sentiment tiers using numerical ratings and textual indicators.
* **Issue Identification:** Isolate specific technical, functional, and user-experience issues driving 1-star and 2-star reviews.
* **Time-Series Analysis:** Evaluate review trends, average ratings, and monthly volume fluctuations over the 14-month dataset span.

---

## 📊 Dataset Summary & High-Level Metrics
The dataset (`chatgpt_reviews.csv`) contains 196,727 entries across four main attributes: `Review Id`, `Review`, `Ratings` (1 to 5 stars), and `Review Date`.

| Metric / Category | Count / Value | Percentage / Range |
| :--- | :--- | :--- |
| **Total Reviews** | 196,727 | 100% |
| **Date Range** | July 25, 2023 – August 23, 2024 | ~14 Months |
| **5-Star Reviews (Positive)** | 150,215 | 76.36% |
| **4-Star Reviews (Positive)** | 22,897 | 11.64% |
| **3-Star Reviews (Neutral)** | 8,157 | 4.15% |
| **2-Star Reviews (Negative)** | 3,375 | 1.72% |
| **1-Star Reviews (Negative)** | 12,083 | 6.14% |

> **Overall Summary:** **88.0% of reviews are positive** (4–5 stars), indicating high core user satisfaction, while **7.86% are negative** (1–2 stars) and **4.15% are neutral** (3 stars).

---

## 🔍 Analytical Findings

### 1. Sentiment Analysis
* **Positive Sentiment (88.0%):** Users frequently highlight accuracy, assistance with coding/studies/writing, convenience, and model capability (especially GPT-4o enhancements).
* **Neutral Sentiment (4.15%):** Focuses on minor bug reports mixed with praise, feature requests (e.g., custom themes, offline mode), or requests for higher free-tier limits.
* **Negative Sentiment (7.86%):** Primarily driven by system downtime, authorization failures, and sudden unexpected changes after app updates.

### 2. Issue Identification (Negative Review Drivers)
Analysis of keywords across 1-star and 2-star reviews reveals five major failure modes:
1. **Server & System Errors:** "Error", "network failure", and "server glitch" appear in over **850+ negative reviews**, indicating server capacity during peak hours.
2. **Authentication & Login Issues:** Login loops, session dropouts, and Google account verification failures (**640+ instances**).
3. **Update Regression & App Instability:** Crashes and lag introduced immediately following app updates (**730+ instances**).
4. **Inaccurate Output & Hallucinations:** Incorrect answers, outdated factual responses, or repetitive loops (**580+ instances**).
5. **Usage Caps & Free Tier Restrictions:** Frustration surrounding daily message limits, premium paywalls, and GPT-4 model restrictions (**340+ instances**).

### 3. Time-Series Analysis
* **Volume Growth:** Review volume expanded significantly from ~8,200 reviews/month in mid-2023 to peak volumes exceeding **28,000 reviews/month in May 2024** (coinciding with major model releases like GPT-4o).
* **Rating Stability:** Monthly mean ratings remained consistently strong between **4.32 and 4.54 out of 5.0**, demonstrating resilient user baseline satisfaction across rapid user growth.

---

## 💡 Strategic Recommendations
* 🛠️ **Improve System Reliability:** Enhance server redundancy to minimize runtime connection and response generation errors during high-traffic windows.
* 🔐 **Streamline Authentication:** Fix session persistence bugs and simplify login flows to reduce account lockout complaints.
* 🧪 **Pre-Release QA Testing:** Strengthen regression testing before releasing mobile app updates to prevent post-update crash spikes.
* ⏱️ **Transparent Rate Limiting:** Provide clearer UI indicators for model usage thresholds so users understand rate limits before encountering sudden lockouts.
