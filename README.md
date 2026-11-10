# African Healthcare Indicators Analysis (2010–2023)

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Data Source](https://img.shields.io/badge/Data-World%20Bank%20WDI-orange)](https://data.worldbank.org/)

**Exploratory data analysis and visualization of key healthcare indicators across 10 African countries using Python (pandas, matplotlib, seaborn).**

This repository contains a complete, reproducible analysis of life expectancy, under-five mortality, immunization coverage, and health expenditure trends from 2010 to 2023.

---

## Abstract

This project examines healthcare performance indicators for ten selected African countries over a 14-year period. Using publicly available World Bank World Development Indicators data, the analysis computes descriptive statistics, tracks temporal changes, compares countries, and visualizes relationships between health outcomes and health system inputs. All calculations treat countries equally (unweighted). Five publication-ready charts support the interpretation of findings.

**Key observations include:**
- Substantial variation in under-five mortality, with Nigeria remaining a clear outlier in 2023.
- Measurable gains in life expectancy in several countries, most notably South Africa.
- Weak cross-sectional association between health expenditure per capita and life expectancy in this sample.
- Strong inverse relationship between life expectancy and under-five mortality.

---

## Dataset

| Attribute | Details |
|-----------|---------|
| **File** | `africa_healthcare.csv` |
| **Rows** | 140 (10 countries × 14 years) |
| **Period** | 2010–2023 |
| **Source** | World Bank World Development Indicators |
| **Retrieved** | 28 October 2026 |

### Countries included
Nigeria, Ghana, Kenya, South Africa, Egypt, Ethiopia, Rwanda, Uganda, Tanzania, Senegal.

### Variables

| Variable | Description |
|----------|-------------|
| `country` / `country_code` | Country name and ISO3 code |
| `year` | Calendar year |
| `life_expectancy_years` | Life expectancy at birth, total (years) |
| `under5_mortality_per_1000` | Under-five mortality rate (per 1,000 live births) |
| `dpt_immunization_pct` | DPT immunization coverage (% of children ages 12–23 months) |
| `health_expenditure_pct_gdp` | Current health expenditure (% of GDP) |
| `health_expenditure_per_capita_usd` | Current health expenditure per capita (current US$) |

> **Note:** Current US$ values are not adjusted for inflation or purchasing power. National statistics may include estimates and are subject to revision. This selected-country sample does not represent all of Africa.

### Data source citations
- Life expectancy: https://data.worldbank.org/indicator/SP.DYN.LE00.IN  
- Under-five mortality: https://data.worldbank.org/indicator/SH.DYN.MORT  
- DPT immunization: https://data.worldbank.org/indicator/SH.IMM.IDPT  
- Health expenditure (% of GDP): https://data.worldbank.org/indicator/SH.XPD.CHEX.GD.ZS  
- Health expenditure per capita: https://data.worldbank.org/indicator/SH.XPD.CHEX.PC.CD  

---

## Repository Contents

```
Africa_heathcare_indicator_solution/
├── African_Healthcare_Indicators_Solution.ipynb   # Full analysis notebook
├── africa_healthcare.csv                         # Dataset
├── requirements.txt                               # Python dependencies
├── LICENSE                                        # MIT License
└── README.md                                      # This file
```

---

## Analysis Overview

The Jupyter notebook covers ten structured questions:

1. Data loading, shape, data types, and coverage (countries & years)
2. Missing-value and duplicate-record audit
3. 2023 summary statistics (mean, median, min, max) for key indicators
4. Nigeria-specific change in life expectancy and under-five mortality (2010–2023)
5. Identification of countries with DPT immunization below 90% in 2023
6. **Bar chart** — Under-five mortality ranking (2023)
7. **Line chart** — Life expectancy trends for Nigeria, Ghana, Kenya, South Africa
8. **Horizontal bar chart** — DPT immunization coverage with 90% reference line
9. **Scatter plot** — Health expenditure per capita vs life expectancy + Pearson correlation
10. **Heatmap** — Pearson correlation matrix of five health indicators

All charts include titles, axis labels with units, and legends where appropriate.

---

## Requirements

- Python 3.10+
- pandas
- numpy
- matplotlib
- seaborn
- scipy

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/folasunkanmi/Africa_heathcare_indicator_solution.git
   cd Africa_heathcare_indicator_solution
   ```

2. (Optional) Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate        # Linux / macOS
   # or
   venv\Scripts\activate           # Windows
   ```

3. Install packages:
   ```bash
   pip install -r requirements.txt
   ```

4. Launch JupyterLab or Jupyter Notebook:
   ```bash
   jupyter lab
   ```

5. Open `African_Healthcare_Indicators_Solution.ipynb` and run all cells.

---

## Key Findings (Summary)

- **Under-five mortality (2023):** Highest in Nigeria (116.8), Ethiopia (51.5), and Uganda (49.4) per 1,000 live births.
- **Life expectancy gains (2010–2023):** South Africa recorded the largest absolute increase (+7.25 years), followed by Ghana (+4.20 years).
- **DPT immunization (2023):** Six of the ten countries met or exceeded the 90% classroom threshold.
- **Expenditure vs outcomes:** Pearson correlation between health expenditure per capita and life expectancy was near zero (r ≈ 0.05) in this cross-section, underscoring that spending level alone does not determine outcomes.
- **Strongest correlation:** Health expenditure (% of GDP) and health expenditure per capita (r ≈ 0.92); life expectancy and under-five mortality showed a strong inverse relationship (r ≈ −0.90).

---

## Citation

If you use this analysis, code, or derived figures in academic work, reports, or presentations, please cite as:

```
Folasunkanmi. (2026). African Healthcare Indicators Analysis (2010–2023) 
[Computer software]. GitHub. 
https://github.com/folasunkanmi/Africa_heathcare_indicator_solution
```

**BibTeX:**

```bibtex
@software{folasunkanmi_africa_healthcare_2026,
  author       = {Folasunkanmi},
  title        = {African Healthcare Indicators Analysis (2010--2023)},
  year         = {2026},
  publisher    = {GitHub},
  url          = {https://github.com/folasunkanmi/Africa_heathcare_indicator_solution},
  note         = {Python analysis using pandas, matplotlib, and seaborn. Data from World Bank World Development Indicators.}
}
```

**Data attribution:**  
World Bank. World Development Indicators. Retrieved 28 October 2026 from https://data.worldbank.org/

---

## License

This project is released under the [MIT License](LICENSE).

---

## Author

**Folasunkanmi**  
Data Analyst & Aspiring Data Scientist  
GitHub: [folasunkanmi](https://github.com/folasunkanmi)

---

*This repository is intended for educational and research purposes. Findings should be interpreted in the context of the limited country sample and the nature of secondary aggregate data.*
