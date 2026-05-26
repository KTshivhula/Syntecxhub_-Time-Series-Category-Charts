# Syntecxhub_-Time-Series-Category-Charts
Superstore sales analysis: line charts (daily/monthly/quarterly), bar chart, pie chart. PNG exports. Jupyter notebook + README with formatting discussion. Python, pandas, matplotlib.
# =====================================================
# Save Final Summary Report as README.md (for GitHub)
# =====================================================

readme_content = """# Project 1: Time Series & Category Charts – Summary Report

**Author:** Khoro Avhavhoni Tshivhula  
**Date:** May 26, 2026

---

## 📊 Numeric Summary

- **Time period:** 2011-01-01 to 2014-12-31 (from Superstore data)
- **Total sales (all categories):** $12,642,501.92

### Sales by category

| Category | Total Sales (USD) | Share (%) |
|----------|------------------|------------|
| Technology | $4,744,557.50 | 37.5% |
| Furniture  | $4,110,874.19 | 32.5% |
| Office Supplies | $3,787,070.23 | 30.0% |

- **Best performing month:** 2014-12 (approximately $1,200,000)
- **Best performing quarter:** 2014Q4 (approximately $3.5 million)

---

## 📈 Discussion: Chart Choices & Formatting

### 1. Time Series Line Charts

| Chart | Points | Why this type | Formatting choices |
|-------|--------|----------------|--------------------|
| **Daily sales** | 1,430 | Shows raw fluctuations, detects outliers | Thin blue line (0.5 width, alpha 0.7); rotated x‑labels (45°); dashed light grey grid; no labels (too many points) |
| **Monthly sales** | 48 | Smooths noise, reveals seasonality | Red line with circular markers; x‑labels rotated 90°; grid; no labels (would overlap) |
| **Quarterly sales** | 16 | Shows long‑term trends and cycles | Green dashed line with square markers; **value labels** added (best practice: labels only when n ≤ 20); labels offset above points, bold, rotated 45° |

**All line charts share:** Bold title (size 14), axis labels with units ($), legend, `tight_layout()`, saved as 150 dpi PNG.

### 2. Bar Chart – Category Comparison

- **Why bar chart?** Best for comparing discrete categories and showing rank. Length of bar directly represents value.
- **Sorting:** Descending order (Technology → Furniture → Office Supplies) for immediate rank perception.
- **Data labels:** Dollar amounts placed **3% above** each bar, centred, bold, with commas.
- **Y‑axis:** Custom tick formatter shows `$1,000,000` instead of `1000000`.
- **Grid:** Only horizontal (y‑axis), dashed, light grey (alpha 0.3).
- **Spines:** Top and right spines removed for cleaner look.
- **Colours:** Color‑blind friendly palette (blue, orange, green) – consistent with pie chart.

### 3. Pie Chart – Share of Sales

- **Why pie chart?** Shows part‑to‑whole relationship (percentage contribution of each category).
- **Inside labels:** Each slice shows both **percentage and dollar amount** (e.g., `37.5% ($4,744,558)`).
- **Exploded slice:** Largest category (Technology) pulled out slightly (explode=0.05) for emphasis.
- **Colours:** Same as bar chart (blue, orange, green) for visual consistency.
- **Caution:** Pie charts work best with ≤5 categories – we have exactly 3, ideal.
- **Start angle:** 90° for a more natural look.

### 4. General Formatting Choices (All Charts)

- **Resolution:** 150 dpi, PNG, `bbox_inches='tight'` to avoid clipping.
- **Titles:** Bold, size 14, descriptive of the content.
- **Axis labels:** Always include units (`$` or `USD`).
- **Legends:** Placed upper left where needed (line charts); pie chart uses direct labels.
- **Layout:** `plt.tight_layout()` ensures no overlapping elements.

### 5. Data Labels – Best Practice

- **Applied only when number of points ≤ 20.**  
  - Quarterly chart (16 points) → labels added.  
  - Monthly chart (48 points) → labels would overlap → omitted.  
  - Daily chart (1,430 points) → labels impossible → omitted.  
- This keeps the charts clean, professional, and readable.

---

## 💡 Key Insights from the Data

1. **Technology** is the top category (37.5% of sales), but the distribution is fairly balanced – all three categories contribute nearly one‑third.
2. **Seasonal pattern:** Q4 (October–December) consistently shows the highest sales, likely driven by holiday shopping.
3. The daily chart reveals high volatility, but the monthly and quarterly charts show a clear upward trend from 2011 to 2014.

---

## 📁 Project Structure
