# Mexican Real Estate Market Analysis

Part of the **Applied Data Science Lab** by **[WorldQuant University (WQU)](https://www.wqu.edu/)**.

---

## 🎯 Research Question
> **"Are property prices in Mexico more influenced by property size or by location?"**

An exploratory and statistical analysis investigating the primary drivers of residential real estate valuation across Mexican states.

---

## 📂 Project Structure

```text
├── 1.1 Getting to Know the Data.ipynb                   # Data auditing, cleaning, and wrangling
├── 1.2 Visualizing Housing Data.ipynb                   # Distributions, boxplots, and scatterplots
├── 1.3 Correlation and Variable Relationships.ipynb     # Correlation, heatmaps, and Simpson's Paradox
├── 1.4 Price per Square Meter and Location Effects.ipynb# Normalized metrics, variance decomposition & location effects
├── README.md                                            # Project documentation
└── data/                                                # Raw and cleaned CSV datasets
```

---

## 📑 Module Breakdown

### 📘 [1.1 Getting to Know the Data](./1.1%20Getting%20to%20Know%20the%20Data.ipynb)
* **Wrangling Pipelines**: Used method chaining to clean, handle missing data, convert currencies (`price_mxn` to `price_usd`), and parse coordinate strings (`lat`, `lon`).
* **Unified Dataset**: Merged three regional sources into a clean, tidy dataset (`mexico-real-estate-combined-clean.csv`).

### 📊 [1.2 Visualizing Housing Data](./1.2%20Visualizing%20Housing%20Data.ipynb)
* **Distribution Skewness**: Demonstrated why the median is more reliable than the mean for right-skewed real estate prices.
* **Bivariate Explorations**: Used boxplots and trimmed scatterplots (1st–99th percentiles) to reveal state-level price premiums (e.g., Distrito Federal).

### 📈 [1.3 Correlation and Variable Relationships](./1.3%20Correlation%20and%20Variable%20Relationships.ipynb)
* **Correlation ($r \approx 0.59$)**: Quantified national area-price correlation, finding size is more predictive for houses ($r \approx 0.72$) than apartments ($r \approx 0.52$).
* **Simpson's Paradox**: Showed that aggregate national statistics mask extreme state-level divergence.
* **Diminishing Returns**: Highlighted non-linear value compression—larger properties cost less per square meter.

### 🏙️ [1.4 Price per Square Meter and Location Effects](./1.4%20Price%20per%20Square%20Meter%20and%20Location%20Effects.ipynb)
* **Feature Engineering**: Created `price_per_m2` to control for size and isolate pure location premiums.
* **Grouped Aggregations**: Ranked states by median space cost (Distrito Federal highest at ~$959/m²) and identified high within-state inequality.
* **Property Type Dynamics**: Confirmed apartments command higher per-m² rates than houses due to urban land scarcity.
* **Variance Decomposition**: Quantified that between-state location differences substantially drive price variance.

---

## 💡 Key Takeaways
1. **Location Trumps Size**: While total price scales with area, location is the dominant determinant of value density (`price_per_m2`).
2. **Type Matters**: Apartments hold higher per-m² value than houses due to urban concentration and shared amenities.
3. **National Figures Mislead**: Extreme state-level variance makes local, segmented analysis essential for real estate appraisal.

