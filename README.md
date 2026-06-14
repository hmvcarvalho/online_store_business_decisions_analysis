# online_store_business_decisions_analysis

Analysis of business decision-making for an online store, including hypothesis prioritization using ICE and RICE frameworks, and A/B test results analysis.

## Project Structure

```
online_store_business_decisions_analysis/
├── data/
│   ├── hypotheses_us.csv       # Hypotheses with ICE/RICE scoring inputs
│   ├── orders_us.csv           # Orders data for A/B test analysis
│   └── visits_us.csv           # Visits data for A/B test analysis
├── notebooks/
│   ├── 01_hypotheses_prioritization.ipynb  # ICE and RICE framework scoring
│   └── 02_AB_test_analysis.ipynb           # A/B test results and conclusions
├── .gitignore
├── README.md
└── requirements.txt
```

## Results & Conclusions

### Hypothesis prioritization (ICE vs RICE)
- ICE ranks hypotheses by Impact and Confidence only, while RICE also accounts for Reach.
- Adding Reach reshuffled the rankings significantly: **H8** ("Show banners with current offers and sales on the main page") rose from 3rd (ICE) to 1st (RICE), while **H9** dropped from 1st to 5th once its low Reach was considered.
- RICE is the recommended framework, as it better reflects real-world business impact by factoring in how many users a hypothesis affects.

### A/B test analysis
- **Conversion rate**: Group B has a statistically significant higher conversion rate than Group A (Mann-Whitney U test, p = 0.011 raw data, p = 0.008 with outliers removed — both reject H0).
- **Average ticket**: No statistically significant difference between groups (Mann-Whitney U test, p = 0.862 raw data, p = 0.974 with outliers removed — both fail to reject H0). Group B's apparent revenue lead was driven mainly by a few large outlier orders.
- **Decision**: Stop the test and roll out Group B. Since revenue per visitor = conversion rate × average ticket, a higher conversion rate with no change in average ticket means Group B should generate more overall revenue.

## Key Dependencies

| Library | Version | Purpose |
|---|---|---|
| pandas | 3.0.3 | Data manipulation and analysis |
| numpy | 2.4.6 | Numerical computing |
| matplotlib | 3.10.9 | Data visualization |
| seaborn | 0.13.2 | Statistical data visualization |
| scipy | 1.17.1 | Statistical tests |
| jupyter / notebook | 1.1.1 / 7.5.7 | Interactive notebooks |
| jupyterlab | 4.5.8 | Notebook IDE |

> Full pinned dependencies are listed in `requirements.txt`.

## Setup

### 1. Create and activate the virtual environment

**Windows (PowerShell):**
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS / Linux:**
```bash
python -m venv .venv
source .venv/bin/activate
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Then open the notebooks inside the `notebooks/` folder in the order indicated by their prefix numbers.
