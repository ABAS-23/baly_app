# 🚗 Baly User Experience Analysis

A data-driven sentiment analysis of **Baly** — Iraq's leading ride-sharing and food delivery platform — examining the gap between **user expectations** and **driver realities**.

---

## 📊 Interactive Dashboard

[![Open Dashboard](https://img.shields.io/badge/📊%20Open%20Interactive%20Dashboard-%F0%9F%93%�%20Live%20Preview-9D174D?style=for-the-badge&labelColor=0A0C0F)](baly_dashboard_enhanced.html)

The dashboard reveals **contradictory truths** about the same platform:
- Users complain about **multiple issues** (prices, app bugs, service)
- Drivers complain about **one issue** — low wages (99%)

---

## 🔍 What We Did

### 1. Manual Data Collection
- **280 real user reviews** from Google Play (Baly User App)
- **100 real driver reviews** from Google Play (Baly Captain App)
- Collected over **one week** by reading and categorizing each review individually
- **No datasets, no shortcuts** — real data from a real app

### 2. Manual Categorization & Labeling
Each review was tagged with:
```
Category      → What is the complaint about?
Rating        → Star rating (1-5)
Helpful_Count → How many users found it helpful
Date          → When was it posted
Gender        → User/Driver gender (M/F)
```

**Categories included:**
- **Users:** Price_Issue, App_Technical, Support_Service, Positive
- **Drivers:** Payment_Issue, App_Technical, Trip_Cancellation, Support_Service, Positive

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

Mobile (Google Play - Iraq only)  → 4.2 ⭐ (40 reviews)
Web (Google Play - Global)        → 3.6 ⭐ (thousands)

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

## 📁 Dataset Structure

### Users Dataset (`baly_users.csv`)
| Field | Description |
|-------|-------------|
| ID | Unique review ID |
| Category | Type of complaint (Price, App_Technical, Support_Service, Positive) |
| Rating | Star rating 1-5 |
| Review | Review text |
| Helpful_Count | Users who found this helpful |
| Date | Date posted |
| Gender | M (Male) or F (Female) |

**Size:** 280 reviews | **Date Range:** 2022–2026

### Drivers Dataset (`baly_captain.csv`)
| Field | Description |
|-------|-------------|
| ID | Unique review ID |
| Category | Type of complaint (Payment_Issue, App_Technical, Trip_Cancellation, Support_Service, Positive) |
| Rating | Star rating 1-5 |
| Review | Review text |
| Helpful_Count | Drivers who found this helpful |
| Date | Date posted |

**Size:** 100 reviews | **Date Range:** 2022–2026

---

## 🛠️ What We Built

**Interactive Dashboard (`baly_dashboard_enhanced.html`)**
- Timeline visualization of reviews over time
- Rating distribution comparison (Users vs Drivers)
- Category breakdown (Donut charts)
- Trend analysis showing if app improved over time
- Key statistics and insights cards

**No code libraries used except:**
- Chart.js (for data visualization)
- Google Fonts (for typography)
- Vanilla CSS & JavaScript

---

## 📈 Insights at a Glance

```
Dataset Size          : 380 total reviews
Users                 : 280 reviews across 4 categories
Drivers               : 100 reviews across 5 categories
Coverage              : 4 years (2022–2026)
Data Quality          : 100% manual verification
Geographic Coverage   : Iraq (Baghdad-focused)
```

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
Simply open `baly_dashboard_enhanced.html` in any web browser — no installation needed.

### 2. Analyze the Data
```python
import pandas as pd

users = pd.read_csv("baly_users.csv")
drivers = pd.read_csv("baly_captain.csv")

# Compare wage complaints between drivers
wage_complaints = drivers[drivers['Category'] == 'Payment_Issue']
print(f"Wage complaints: {len(wage_complaints) / len(drivers) * 100:.1f}%")
```

### 3. Extend the Analysis
Add your own visualizations, NLP sentiment analysis, or predictive models.

---

## 📊 Data Quality & Limitations

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

## 🔗 Data Sources

| Source | Type | Coverage |
|--------|------|----------|
| Google Play - Baly User App | Official App Store | 280 user reviews |
| Google Play - Baly Captain App | Official App Store | 100 driver reviews |
| Manual Collection | Data Engineer | Over 1 week |

---

## 👤 Author

**Abbas Hussein**  
Data Analyst | Python | Business Intelligence  
[LinkedIn](https://www.linkedin.com/in/abbas-hussein) · [GitHub](https://github.com/ABAS-23)

---

## 📝 License

This project uses real reviews from Baly's public Google Play listings. All data was collected from publicly available sources for educational and analytical purposes.

---

## 🔮 Future Work

Potential expansions:
- **NLP Sentiment Analysis** — Beyond manual categorization
- **Topic Modeling** — Discover hidden complaint patterns
- **Time Series Forecasting** — Will complaints improve?
- **Network Analysis** — How do reviews influence each other?
- **Multi-language Comparison** — Arabic vs English reviews

---

*Last Updated: May 2026*  
*Real data. Real insights. No shortcuts.*
