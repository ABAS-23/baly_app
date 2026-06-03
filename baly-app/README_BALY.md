# 🚗 Baly User Experience Analysis

A data-driven sentiment analysis of **Baly** — Iraq's leading ride-sharing and food delivery platform — examining the gap between **user expectations** and **driver realities**.


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

