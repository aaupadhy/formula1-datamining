# F1 Data Mining Project

**CSCE 676 Data Mining | Spring 2026**

Aayush Upadhyay

## Overview

This project applies data mining techniques to the Formula 1 World Championship dataset (1950-2022), sourced from the Ergast Developer API. The goal is to uncover patterns in race outcomes, pit stop strategies, driver-constructor networks, and mechanical reliability using both course techniques and beyond-course methods.

## Techniques

**Course techniques:**
- Frequent itemset mining and association rules (pit stop strategy patterns)
- Graph mining with PageRank and community detection (driver-constructor networks)
- Large-scale ML with ensemble methods (race outcome prediction)
- Clustering with k-means and DBSCAN (identifying competitive eras)

**Beyond-course technique:**
- Survival analysis for DNF (did not finish) prediction using Cox proportional hazards modeling

## Dataset

The F1 World Championship dataset contains 14 relational CSV tables with ~515K lap time records, ~25K race results, ~8.9K pit stops, covering 1079 races across 73 seasons. Data sourced from the [Ergast Developer API](http://ergast.com/mrd/) under CC-BY-NC-SA 3.0 license.

## Setup

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook checkpoint1.ipynb
```

## Project Structure

```
├── checkpoint1.ipynb     # Checkpoint 1: Dataset selection and EDA
├── checkpoint2.ipynb     # Checkpoint 2: Research question formation
├── data/                 # F1 dataset CSV files
├── requirements.txt      # Python dependencies
└── README.md
```

## Checkpoints

- **Checkpoint 1:** Dataset comparison, selection, and exploratory data analysis
- **Checkpoint 2:** Research question definition, additional EDA, feasibility analysis, and initial method runs
