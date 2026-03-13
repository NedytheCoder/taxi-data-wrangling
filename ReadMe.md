# Taxi Trip Analysis Pipeline

## Overview

This CA data wrangling project analyzes NYC taxi trip data, joins it with daily weather data, detects anomalous trips using a robust z-score method, and generates a deterministic dataset fingerprint.

I carried out this analysis using **Python >=3.12,<3.13**, **Jupyter Notebook** and managed with the **uv Python package manager**.

---

## Environment Setup

Install dependencies:

```bash
uv sync
```

If uv is not installed:

```bash
pip install uv
```

---

## Dataset Files

I placed the following datasets in the project root directory:

* `yellow_tripdata_2022-07.parquet`
* `nycentral_city_weather_data.csv`
* `taxi_zone_lookup.csv`

---

## Weather Station ID

Station ID used for weather data: `USW00094728`

---

## Running the Notebook

Navigate to the analysis.ipynb file and open it.

Then select a python kernel with a version >=3.12,<3.13.

Proceed to run all cells from top to bottom (or if available, click the "Run All" button) to reproduce the analysis and generate the outputs.

---

## Outputs Generated

Running the notebook produces the following files inside the `outputs/` directory:

```
outputs/task1_hourly_volume.png
outputs/task1_speed_hist.png
outputs/task1_summary.csv
outputs/task2_hhi.png
outputs/task2_top_routes.csv
outputs/task3_join_quality.csv
outputs/task3_rain_amount.png
outputs/task3_rain_duration.png
outputs/task4_anomalies.csv
outputs/task4_anomaly_scatter.png
outputs/task5_fingerprint.txt
```

---

## Reproducibility

The fingerprint generation is deterministic. A seed is derived from the student ID and a salt using SHA256. Because the seed is fixed, the same dataset and code will always produce identical outputs when the notebook is executed.
