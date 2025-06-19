# 📊 IMF Economic Data Analysis (2010–2024)

This Python project automates the retrieval, processing, and visualization of key international economic indicators from the **IMF World Economic Outlook (WEO)

The solution generates a professional Excel report, including:
- Cleaned and normalized economic data
- Summary statistics and year-over-year changes
- Visualizations (line chart, bar chart, correlation heatmap)
- Automatically generated textual insights

---

## Features

- Fetches data for:
  - **GDP Growth (% change)**
  - **Inflation (Consumer Prices, % change)**
  - **Unemployment (% of labor force)**
- Covers 7 countries:
  - United States, Germany, Brazil, India, South Africa, United Kingdom, Japan
- Time Range: **2010–2024**
- Data Processing:
  - Cleans missing data
  - Z-score normalization
  - Computes year-over-year changes
- Visuals:
  - Multi-line chart (GDP growth over time)
  - Grouped bar chart (Inflation & Unemployment latest year)
  - Heatmap (correlation between indicators)
- Reporting:
  - Exports everything to `IMF_Economic_Report_From_API.xlsx`
  - Auto-written narrative summary of insights

---

## How to Run

### 1. Install dependencies

```bash
pip install pandas matplotlib seaborn requests xlsxwriter
```

### 2. Save the script

Save the script file as:

```bash
IMF iData API Intg and Adv Analysis.py
```

### 3. Run the script

```bash
python IMF iData API Intg and Adv Analysis.py
```

### 4. Output

A full Excel report will be created:

```
IMF_Economic_Report_From_API.xlsx
```

---

## Customizing the Script

### Change Countries

Edit this list inside the script:

```python
countries = ["US", "DE", "BR", "IN", "ZA", "GB", "JP"]
```

### Adjust Time Period

Modify the `start_year` and `end_year` values in the `fetch_imf_data()` function.

### Change Indicators

You can customize or extend the indicators by modifying:

```python
indicators = {
    "NGDP_RPCH": "GDP, constant prices (% change)",
    "PCPIPCH": "Inflation, average consumer prices (% change)",
    "LUR": "Unemployment rate (% of labor force)"
}
```

---

## Troubleshooting

| Problem                           | Solution                                                                 |
|----------------------------------|--------------------------------------------------------------------------|
| `KeyError: 'Series'`             | That indicator or country may not have available data.                   |
| Empty or missing Excel charts    | Ensure `matplotlib`, `seaborn`, and `xlsxwriter` are installed properly. |
| Blank report                     | Confirm API returned data (add `print(df.head())` to debug).             |

---

## Output Structure

- **Raw_Data** – Cleaned API data
- **Summary_Averages** – Mean values per country/indicator
- **Summary_Pivot** – Cross-tab for quick comparison
- **GDP Chart** – Line chart (2010–2024)
- **Bar Chart** – Latest year bar chart
- **Heatmap** – Correlation matrix (India)
- **Summary_Text** – Natural language insights

---

##  About This Project

This project demonstrates:
- Real-time data integration from a public API
- Advanced data wrangling with pandas
- Analytical thinking with clear insight generation
- High-quality Excel-based deliverables for economists and decision-makers

It is designed to support both **technical analysts** and **non-technical users**.
