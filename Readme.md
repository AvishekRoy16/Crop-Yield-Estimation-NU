# Crop Price Forecasting Dashboard — Archived Academic Prototype

This repository preserves a 2021 university-era prototype that combines historical commodity-price tables, rainfall values, decision-tree regression and a Flask dashboard.

> **Status:** archival learning project. Despite the repository name, the application forecasts crop-price indicators; it does not estimate crop yield. It is not maintained, validated for current use or suitable for agricultural or financial decisions.

## What the prototype demonstrates

- exploratory notebooks for crop, rainfall and temperature data;
- per-commodity CSV processing;
- a Flask application with commodity pages and chart views;
- a simple decision-tree workflow driven by month, year and rainfall;
- a dashboard concept for comparing projected price movement.

## Application flow

```text
Historical commodity CSVs
          +
Hard-coded monthly rainfall
          |
          v
Per-crop decision trees
          |
          v
Price-index projection
          |
          v
Flask dashboard and commodity pages
```

## Why this is not presented as a validated model

The current implementation has material methodological limitations:

- each tree is trained on the complete available table, with no held-out or time-based evaluation;
- tree depth is randomly selected at application start, so output is not reproducible;
- the application extrapolates the calendar year beyond the historical range;
- rainfall is a fixed 12-value array rather than a versioned observation or forecast source;
- data origin, collection dates and redistribution terms are not documented;
- model error, temporal stability and regional coverage are not measured;
- the interface's third-party image licences are not recorded.

Because of those gaps, no accuracy claim, performance chart or current-price claim is made here.

## Provenance boundary

The repository was committed as a university-era project, but its core crop-price implementation substantially overlaps code and descriptions that also appear in public crop-price projects and publications. The original source lineage, licence and individual-versus-team contribution have not yet been established. Until they are, this repository should be treated as a preserved study copy, not evidence of independent authorship and not a profile pin.

## Repository map

```text
.
|-- app.py                         # Flask routes and forecasting workflow
|-- crops.py                       # crop metadata used by the interface
|-- templates/                     # historical dashboard templates
|-- static/                        # commodity tables and UI assets
|-- ML-Research/                   # exploratory notebooks
|-- Research-Report-1.pdf          # historical project documentation
|-- Research-Report-2.pdf
`-- IOT  Final Presentation.pptx
```

## What a credible rebuild would require

1. Confirm the original code, dataset and asset licences, plus the personal contribution boundary.
2. Replace static and undocumented inputs with permitted, versioned data sources.
3. Define the target precisely—price, price index or yield—and rename the project accordingly.
4. Use chronological backtesting with naive seasonal baselines and fixed model parameters.
5. Report MAE by crop and forecast horizon, including uncertainty and failure cases.
6. Rebuild the interface with licensed or original assets and label all dates and units.

The reports and presentation are retained for chronology only; their claims are not independently verified by this README.
