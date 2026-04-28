# Formula 1 Data Mining Project

**CSCE 676 Data Mining | Spring 2026**  
**Aayush Upadhyay**

Start here: [`main_notebook.ipynb`](main_notebook.ipynb)

Project video: [https://youtu.be/0XYKSPZVZ-8](https://youtu.be/0XYKSPZVZ-8)

Repository URL: [https://github.com/aaupadhy/formula1-datamining](https://github.com/aaupadhy/formula1-datamining)

## Overview

This project uses historical Formula 1 race data from 1950 through 2022 to study how race outcomes, pit stop strategies, and reliability patterns have changed across eras. I use clustering and ensemble models to study competitive eras, association rule mining to find pit stop strategy patterns, and survival analysis to model DNF risk.

## Research Questions

1. Can Formula 1 seasons be clustered into distinct competitive eras, and does adding era information improve race outcome prediction?
2. What frequent pit stop strategy patterns are associated with top finishes, and do those patterns differ between street and permanent circuits?
3. What risk factors are associated with not finishing a race, and how has the survival landscape changed across Formula 1 eras?

## Data

The data comes from the Formula 1 World Championship dataset, originally sourced from the [Ergast Developer API](http://ergast.com/mrd/). The checked-in `data/` folder contains 13 CSV tables covering races, results, drivers, constructors, circuits, pit stops, qualifying, standings, sprint results, seasons, and status codes.

The main notebook loads the raw CSV files directly from `data/` and creates the modeling tables inside the notebook. No separate preprocessing script is required.

## Results Summary

The strongest finding is that Formula 1 is highly era-dependent. Modern seasons have much lower DNF risk than early and middle eras, and the survival curves are statistically different by log-rank test. Pit stop association rules mostly connect successful one-stop races with later first stops, especially for top-ten finishes. Era clustering is meaningful, but adding the cluster label only changes top-five prediction slightly because year, grid position, driver, constructor, and circuit already capture much of that signal.

## Reproducing the Project

This was prepared and verified with Python 3.12. The notebook should also run in Colab after installing the packages in `requirements.txt`.

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook main_notebook.ipynb
```

Run the notebook cells from top to bottom. The checkpoint notebooks are included for project history, but the final deliverable is `main_notebook.ipynb`.

## Key Dependencies

- Python 3.12
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- lifelines
- mlxtend
- jupyter

See `requirements.txt` for the install list.

## Repo Structure

```text
.
├── main_notebook.ipynb   # Final curated deliverable notebook
├── checkpoint1.ipynb     # Project Checkpoint 1
├── checkpoint2.ipynb     # Project Checkpoint 2
├── data/                 # Formula 1 CSV tables
├── requirements.txt      # Python dependencies
└── README.md             # Project overview and reproduction guide
```
