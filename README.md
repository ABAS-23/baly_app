# 🚗 Baly User Experience Analysis

A data-driven sentiment analysis of **Baly** — Iraq's leading ride-sharing and food delivery platform — examining the gap between **user expectations** and **driver realities**.

---

## 📊 Interactive Dashboard

[![Open Interactive Dashboard](https://cool-entremet-6c340a.netlify.app/)

---

## 🔍 What We Did

### 1. Manual Data Collection
- **280 real user reviews** from Google Play (Baly User App)
- **100 real driver reviews** from Google Play (Baly Captain App)
- Collected over **one week** by reading and categorizing each review individually
- **No datasets, no shortcuts** — real data from a real app

### 2. Manual Categorization & Labeling
Each review was tagged with:
- **Category** — What is the complaint about?
- **Rating** — Star rating (1-5)
- **Helpful_Count** — How many users found it helpful
- **Date** — When was it posted
- **Gender** — User/Driver gender (M/F)

### 3. Deep Analysis & Insights
Discovered hidden patterns by comparing the two datasets side-by-side.

---

## 💡 Key Findings

### Finding #1: The Wage Crisis
```
Driver Reviews Analysis:
99% of complaints → "Wages are too low"
Only 1% → App bugs, support issues

Implication:
The platform is technically sound for drivers,
but economically unsustainable.
```

### Finding #2: The Rating Contradiction
```
Same app, different ratings:

Mobile (Google Play - Iraq only)  → 4.2 ⭐
Web (Google Play - Global)        → 3.6 ⭐

Why? Geographic filtering + limited reviews inflate mobile score.
```

### Finding #3: The Two-Sided Gap
```
USERS complain about:
├─ Price (25%)
├─ App bugs (22%)
├─ Driver behavior (14%)
└─ Other (39%)

DRIVERS complain about:
├─ Low wages (99%)
└─ Other (1%)

Same platform = completely different pain points
```

### Finding #4: The Silent Majority
```
Users who write reviews are angry.
Users who stay silent are neutral or happy.

The 4.2 rating on mobile hides a silent approval gap.
Real sentiment may be lower than displayed.
```

---

## 📁 Dataset

### Users Dataset (`baly_users.xlsx`)
- 280 reviews
- Categories: Price_Issue, App_Technical, Support_Service, Positive
- Date Range: 2022–2026
- Manual verification: 100%

### Drivers Dataset (`captain_baly.xlsx`)
- 100 reviews
- Categories: Payment_Issue, App_Technical, Trip_Cancellation, Support_Service, Positive
- Date Range: 2022–2026
- Manual verification: 100%

---

## 📊 Dashboard Overview

The interactive dashboard reveals:
- Timeline visualization of reviews over time
- Rating distribution comparison (Users vs Drivers)
- Category breakdown with donut charts
- Trend analysis showing if app improved over time
- Key statistics and insights cards

**Open the dashboard above to explore the data!**

---

## 🎯 Why This Matters

### For Baly (Internal)
- Users expect service quality; drivers expect fair pay
- The app isn't broken for drivers — the business model is
- Low ratings don't reflect app quality; they reflect wage concerns

### For Data Science Community
- Rare example of **multi-stakeholder sentiment analysis**
- Manual data collection from live platform (not Kaggle)
- Local dataset — addresses gap in Middle Eastern app analysis

### For Job Seekers / Portfolio
- Demonstrates ability to **collect real data manually**
- Shows **comparative analysis skills**
- Reveals **business insights** from raw reviews
- Proves **attention to data quality and context**

---

## 🚀 How to Use

### 1. View the Dashboard
Click the button above — no installation needed.

### 2. Analyze the Data
```python
import pandas as pd

users = pd.read_excel("baly_users.xlsx")
drivers = pd.read_excel("captain_baly.xlsx")

# Compare wage complaints between drivers
wage_complaints = drivers[drivers['Category'] == 'Payment_Issue']
print(f"Wage complaints: {len(wage_complaints) / len(drivers) * 100:.1f}%")
```

### 3. Extend the Analysis
Add your own visualizations, NLP sentiment analysis, or predictive models.

---

## 📊 Key Statistics

```
Total Reviews          : 380
Users                  : 280 reviews
Drivers                : 100 reviews
Coverage               : 4 years (2022–2026)
Data Quality           : 100% manual verification
Geographic Coverage    : Iraq (Baghdad-focused)
```

---

## ⚠️ Data Limitations

### Strengths ✅
- **Real data** from active Google Play reviews
- **Manual categorization** ensures accuracy
- **Complete dataset** — no missing values
- **Verified sources** — all from official Baly apps

### Limitations ⚠️
- **Sample size for drivers** — only 100 reviews (limited generalization)
- **Geographic bias** — mostly Baghdad-based users
- **Recency bias** — most reviews from 2025–2026
- **Selection bias** — only people motivated to review (usually angry or very happy)
- **Language** — Arabic reviews; translations may vary
- **Platform limitation** — doesn't capture in-app feedback or customer support tickets

---

## 👤 Author

**Abbas Hussein**  
Data Analyst | Python | Business Intelligence  
[LinkedIn](https://www.linkedin.com/in/abbas-hussein) · [GitHub](https://github.com/ABAS-23)

---

## 🔮 Future Work

Potential expansions:
- **NLP Sentiment Analysis** — Beyond manual categorization
- **Topic Modeling** — Discover hidden complaint patterns
- **Time Series Forecasting** — Will complaints improve?
- **Predictive Models** — What drives users to leave reviews?

---

*Last Updated: June 2026*  
*Real data. Real insights. No shortcuts.*
