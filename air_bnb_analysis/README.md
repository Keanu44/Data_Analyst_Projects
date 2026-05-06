# Airbnb Paris Listings Analysis

![Project Overview](../Images/Airbnb-Logo.png)

A data analysis project exploring Airbnb listing trends in Paris, with a focus on neighbourhood pricing, accommodation capacity, and the impact of 2015 short-term rental regulations on host growth and pricing.

## Overview

This notebook analyzes a multi-city Airbnb dataset (`Listings.csv`) and narrows its focus to **Paris** — examining how prices vary across neighbourhoods, how accommodation capacity affects nightly rates, and how the number of new hosts and average prices have shifted over time.

## Dataset

- **File:** `Listings.csv`
- **Encoding:** ISO-8859-1
- **Total rows (full dataset):** ~279,712 listings across multiple cities
- **Paris subset:** ~64,690 listings

### Key Columns Used

| Column | Description |
|---|---|
| `host_since` | Date the host joined Airbnb |
| `neighbourhood` | Neighbourhood of the listing |
| `city` | City of the listing |
| `accommodates` | Number of guests the listing can accommodate |
| `price` | Nightly price in Euros |

The full dataset contains 33 columns including host details, review scores, room type, and booking settings.

## Requirements

Install the required Python libraries before running the notebook:

```bash
pip install pandas numpy matplotlib seaborn
```

| Library | Version (recommended) |
|---|---|
| `pandas` | ≥ 1.3 |
| `numpy` | ≥ 1.21 |
| `matplotlib` | ≥ 3.4 |
| `seaborn` | ≥ 0.11 |

## Project Structure

```
.
├── AirBnb.ipynb       # Main analysis notebook
├── Listings.csv       # Source dataset (required)
└── README.md
```

## Analysis Steps

### 1. Data Loading & Cleaning
- Load `Listings.csv` with `ISO-8859-1` encoding
- Parse `host_since` as a datetime column
- Inspect null values and column data types

### 2. Filtering for Paris
- Subset the dataset to Paris listings only
- Retain the five most relevant columns: `host_since`, `neighbourhood`, `city`, `accommodates`, `price`
- Inspect and handle edge cases (listings with 0 accommodates and 0 price)

### 3. Aggregations
Three aggregated views are computed to drive the visualizations:

- **`paris_neighbourhood`** — Mean price per night grouped by neighbourhood, sorted ascending
- **`paris_listings_accommodates`** — Mean price grouped by number of guests for the Elysée neighbourhood
- **`paris_listings_over_time`** — Annual resampling of new host count and average price, indexed by `host_since`

### 4. Visualizations

| Chart | Description |
|---|---|
| Horizontal bar chart | Average listing price by Paris neighbourhood |
| Horizontal bar chart | Average listing price by accommodation capacity (Elysée) |
| Line chart | Number of new Airbnb hosts in Paris over time |
| Line chart | Average nightly price in Paris over time |
| Dual-axis line chart | New hosts vs. average price overlaid — highlights the effect of 2015 regulations |

## Key Findings

- **Neighbourhood pricing varies significantly** across Paris arrondissements, with some areas commanding notably higher nightly rates.
- **Larger accommodations cost more**, as expected — the Elysée neighbourhood shows a clear positive correlation between guest capacity and price.
- **2015 French regulations** appear to have caused a measurable decline in the number of new hosts joining the platform, while average prices trended upward — consistent with reduced supply driving up costs.

## Usage

1. Place `Listings.csv` in the same directory as `AirBnb.ipynb`.
2. Open the notebook in Jupyter:
   ```bash
   jupyter notebook AirBnb.ipynb
   ```
3. Run all cells in order (`Kernel > Restart & Run All`).

## Notes

- Some listings have `accommodates = 0` and `price = 0`; these appear to be data quality issues and should be filtered out for any pricing analysis.
- The dataset uses `ISO-8859-1` encoding due to French special characters in listing names and neighbourhoods.
