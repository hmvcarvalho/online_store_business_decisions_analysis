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
│   ├── 01_hypothesis_prioritization.ipynb  # ICE and RICE framework scoring
│   └── 02_AB_test_analysis.ipynb           # A/B test results and conclusions
├── .gitignore
├── README.md
└── requirements.txt
```

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
