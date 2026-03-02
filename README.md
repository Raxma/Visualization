# Visualization Portfolio — Crime Data Analytics (2020–Present)

This repository is a visualization-first analytics project built in Python to explore incident-level records over time and communicate patterns through clear, stakeholder-friendly visuals. The work focuses on making a messy real-world dataset analysis-ready (date parsing, categorical normalization, missing-value policy), then producing time-series trends, category comparisons, and spatial visuals.

Why this matters (KTP relevance): this is the same workflow you’d use in a digital transformation project—turn raw operational data into a reliable analytics layer, then surface actionable insights via repeatable visual pipelines.

## What I built
1) Data cleaning + governance-style decisions

Standardized column handling (strip whitespace, consistent dtypes)

Parsed dates (e.g., DATE OCC, Date Rptd) with robust coercion and null handling

Applied explicit missing-value and “unknown code” policies (kept code columns numeric; filled text fields with readable labels)

Added derived time features (Year, Month) from DATE OCC for trend analysis

2) Time-series analysis (daily / weekly / monthly)

Resampled incident counts across time granularities

Monthly aggregation uses modern pandas offsets (ME for month-end) for compatibility

Trend plots formatted for readability (sensible tick spacing and labels)

3) Category-level trends (interactive and static)

Monthly trends by crime category with dropdown selection (Plotly)

Clear separation of “data prep” vs “visualization” steps to keep notebook readable

4) Pattern discovery (association rules) + network visualization

Built transaction-style records from multi-crime code fields and ran Apriori + association rules

Visualized relationships using networkx (graph representation of frequent co-occurrence)

## Repository structure
notebooks/
  Visualization.ipynb
output/                     # exported charts/maps for review (recommended to commit)
data/                        # local only (dataset is private; ignored by git)
  README.md                  # explains private dataset policy
.env                         # local only (ignored)
.env.example                 # committed template
README.md
requirements.txt
.gitignore


## Dataset note (private data)

The dataset used for this analysis is private and not included in the public repository.

If you have the dataset locally, you can run the notebook end-to-end using the setup below.

### How to run locally (optional)
#### 1) Create and activate a virtual environment

Windows (PowerShell)

py -m venv .venv
.\.venv\Scripts\Activate.ps1
#### 2) Install dependencies
pip install -r requirements.txt
#### 3) Configure dataset path via .env

Create a file named .env in the repo root:

DATA_PATH=C:\path\to\Crime_Data_from_2020_to_Present.csv

A template is provided in .env.example.

#### 4) Run the notebook

Open:

notebooks/Visualization.ipynb

What to look at (for reviewers)

If you’re reviewing this as a portfolio project without the dataset:

Open notebooks/Visualization.ipynb and scan:

cleaning + feature preparation

time-series trend visuals

category breakdowns

association rule mining + network visualization

Review exported artifacts in /output (if committed):

trend plots (monthly + smoothed)

category trend dashboard

map/heatmap screenshot or exported HTML

### Skills evidenced (mapped to KTP criteria)

Data-driven projects: end-to-end workflow from raw records → cleaned dataset → analysis → visuals
Data integration & preparation: robust datetime handling, missing-value policy, derived features
Predictive / advanced analytics foundations: association rules + graph representation
Process discipline: reproducible config via .env, clear run order, structured outputs
Stakeholder communication: visuals designed to communicate patterns and trade-offs clearly

### Notes / limitations

Dataset is not included (privacy). Results are shown via saved notebook outputs and/or exported plots in /output.

Time aggregation uses ME instead of deprecated pandas M offset for compatibility with newer pandas versions.

Contact

Rasman Khurshid — Nottingham, UK
rasmakhan37@gmail.com
 | +44 7459 079848

