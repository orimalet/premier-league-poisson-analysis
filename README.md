# Premier League - Results, Shots & Poisson Score Model

Small–mid scale project: download EPL match data from **football-data.co.uk**, build a quick league table and rolling form, and use a **Poisson model** to estimate team attacking/defensive strengths and match outcome probabilities.

## Features
- Auto-download season CSV (default **2024–25**; change `SEASON_START` to switch seasons).
- League table from raw results; home/away form.
- Rolling 5-match form and shots/SOT rates per team.
- Poisson score model → scoreline matrix, win/draw/loss probabilities, and Monte Carlo simulation.

## Stack
- Python 3.9+
- numpy, pandas, matplotlib, requests, jupyter

## Getting started
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
source .venv/bin/activate

pip install -r requirements.txt
jupyter notebook Premier_League_Poisson_Notebook.ipynb
```

## Repository structure
```
.
├── Premier_League_Poisson_Notebook.ipynb   # End to end analysis
├── requirements.txt
└── README.md
```

## Notes
- The Poisson model is intentionally simple (no Dixon–Coles time weighting or correlation adjustment). Good for pedagogy & quick insights.
- Some seasons may have slightly different CSV schemas; the notebook selects available columns safely.
