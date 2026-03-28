# 🎮 Steam Market Analytics Dashboard — Power BI

**Author:** Nikhil Upadhyay | MSc Business Analytics @ Dublin Business School  
**Tools:** Power BI Desktop · DAX · Steam Spy API · Azure Maps  
**Live Dashboard:** [View on Power BI](https://app.powerbi.com/groups/me/reports/d9c8e26f-e7f0-47f1-9c12-68fbf30589bd/259097848d74bc50b8b5?experience=power-bi)  
**GitHub:** [github.com/TrazeMaG](https://github.com/TrazeMaG)

---

## 🎯 The Problem This Solves

If you're a game publisher, investor, or product manager trying to enter the Steam market — where do you start?

With **80,000+ games** on Steam and pricing ranging from free to €60+, the market is overwhelming. Most dashboards show you raw numbers. This one tells you **where to publish, what to charge, and which genres actually make money**.

---

## 💡 What Makes This Unique — The 3-Mode System

Inspired by **gaming graphics settings (Low / Medium / Ultra)**, this dashboard has three completely different modes for three different types of users:

```
┌─────────────────────────────────────────────────────┐
│  🔵 PROFESSIONAL MODE  — Blue corporate theme       │
│     For: Executives, investors, board presentations │
│     Shows: Market overview, geographic intel, KPIs  │
├─────────────────────────────────────────────────────┤
│  🟡 GAMING MODE        — Dark + gold cinematic      │
│     For: Product managers, creative teams           │
│     Shows: Player engagement, sentiment, funnel     │
├─────────────────────────────────────────────────────┤
│  🟢 PERFORMANCE / ECO  — Green efficiency theme     │
│     For: Pricing analysts, revenue strategists      │
│     Shows: Pricing sweet spots, RPI, cost analysis  │
└─────────────────────────────────────────────────────┘
```

Most dashboards force everyone to look at the same view. This one adapts to the person using it — **just like a game adapts its graphics to your hardware**.

---

## 📊 Dataset

| Attribute | Value |
|-----------|-------|
| Source | Steam Spy API (steamspy.com) |
| Original dataset | 10,000 games |
| Filtered dataset | **1,293 actively played games** |
| Data attributes | 26 fields |
| Geographic coverage | 28 countries |
| Time period | Steam catalogue (Nov–Dec 2024) |

**Why 1,293 and not 10,000?**  
77% of the original games had zero engagement — no playtime, no reviews. Keeping them would've created misleading dashboards. Professional BI practice prioritises data quality over volume. The filtered set is statistically valid (6–12× minimum sample size) and far more useful for publishing decisions.

---

## 🔑 Key Metrics & Custom DAX

### Revenue Potential Index (RPI) — custom metric
```dax
RPI = Price × LOG10(total_reviews + 1)
```
This balances pricing against review volume using logarithmic scaling — preventing free viral games from dominating while still recognising their reach.

### Engagement Tier Classification
```dax
Engagement Tier = 
  SWITCH(TRUE(),
    [avg_playtime] > 500, "High",
    [avg_playtime] > 100, "Medium",
    "Low"
  )
```

### Sentiment Score
```dax
Sentiment Score = 
  DIVIDE([Positive Reviews], [Total Reviews], 0) * 100
```

---

## 📈 Key Insights from the Data

### 1. 💰 The Pricing Sweet Spot Nobody's Using
The **€5–€15 price range** contains 43% of all games AND shows the highest engagement (324 high-engagement titles). Most publishers overprice or underprice. This range is underutilised.

### 2. 🌍 Geographic Concentration
**US, Europe, and China** account for 60% of all published games. Yet mid-tier markets (Australia, Canada, South Korea) show disproportionately high RPI — an untapped opportunity.

### 3. 🎮 Genre vs Engagement Reality Check
Action leads in volume (94 games) but **RPG and Strategy have higher average playtime per user**. Volume ≠ engagement. Publishers chasing Action are fighting the most crowded market for average returns.

### 4. 📉 The Free-to-Play Trap
Free games have the highest ownership numbers but the **lowest average playtime and worst sentiment scores**. Paid games in the €10–€20 range show 3× better engagement per user.

### 5. ⭐ Review Count vs Sentiment Disconnect
The scatter analysis reveals games with **medium review counts (500–5,000) often have better sentiment** than viral blockbusters. Niche, well-crafted games outperform mass-market titles on player satisfaction.

---

## 🛠️ Technical Implementation

### Power BI Features Used
- **Bookmarks** — for 3-mode switching with a single button click
- **DAX measures** — 8 custom calculated measures including RPI
- **Azure Maps** — geographic publisher distribution across 28 countries
- **Dynamic slicers** — filter by Name, Tags, Genres, Categories simultaneously
- **Heatmap matrix** — Genre × Engagement tier cross-analysis
- **Scatter plot** — Price vs Sentiment with RPI bubble sizing
- **Funnel chart** — Player engagement conversion analysis
- **KPI cards** — 5 core market metrics with trend indicators

### Data Pipeline
```
Steam Spy API
    ↓
Python script (API calls, pagination, rate limiting)
    ↓
Raw CSV (10,000 games, 26 fields)
    ↓
Power BI data model (filtering, relationships, type detection)
    ↓
DAX layer (RPI, Engagement Tier, Sentiment Score, custom measures)
    ↓
3-mode dashboard (Professional / Gaming / Eco)
```

### Python API Script (Steam Spy)
```python
import requests, time, pandas as pd

def fetch_steam_data():
    url = "https://steamspy.com/api.php"
    games = []
    
    for page in range(0, 100):  # paginated calls
        params = {"request": "all", "page": page}
        r = requests.get(url, params=params)
        data = r.json()
        games.extend(data.values())
        time.sleep(1.5)  # respect rate limits
        
    return pd.DataFrame(games)
```

---

## 📁 Files in This Repo

| File | Description |
|------|-------------|
| `Steam Dashboard Analysis Complete.pbix` | Full Power BI dashboard file |
| `Steam-Market-Analysis-Dashboard.pdf` | PDF export of all 3 modes |
| `Steam-Market-Analysis-Dashboard.pptx` | Presentation slides (4-min pitch deck) |
| `Py Script for steam api.txt` | Python script used for data collection |
| `README.md` | This file |

---

## 🚀 How to Run

1. Download `Steam Dashboard Analysis Complete.pbix`
2. Open in **Power BI Desktop** (free download from Microsoft)
3. Click the mode buttons at the top to switch between Professional / Gaming / Eco views
4. Use slicers on the left to filter by genre, tag, publisher country
5. Hover any visual for detailed tooltips

**Or view live:** [Power BI Published Link](https://app.powerbi.com/groups/me/reports/d9c8e26f-e7f0-47f1-9c12-68fbf30589bd/259097848d74bc50b8b5?experience=power-bi)

---

## 🎓 Academic Context

This dashboard was built as part of the **Business Intelligence & Visualisation** module at Dublin Business School (MSc Business Analytics, 2025). It received recognition for its innovative multi-mode design and custom RPI metric.

---

## 👤 About Me

**Nikhil Upadhyay** — Business Analyst | Dublin, Ireland  
Passionate about data, gaming, and making complex information actually useful.

📧 nikhil25000@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/nikhil-upadhyay-72353a143)  
🐙 [GitHub](https://github.com/TrazeMaG)

---

*"O Captain, my Captain" — a thinker navigating the age of AI 🧭*
