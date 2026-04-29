# NBA 3-Point Breakdown — Decoding Basketball's Analytics Revolution

End-to-end data science project quantifying how the 3-point shot reshaped the NBA across 25 seasons (1999–2023). Combines exploratory analysis, spatial visualization, and supervised machine learning to model how shot selection — and the league itself — has fundamentally changed.

![Python](https://img.shields.io/badge/Python-3.7%2B-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C)
![seaborn](https://img.shields.io/badge/seaborn-4C8CBF)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)

---

## TL;DR

- Analyzed **3 datasets** spanning **25 NBA seasons** and **6 full seasons of shot-level coordinates** (every shot, every player).
- Built and tuned **5 classification models** (Logistic Regression, KNN, Decision Tree, Random Forest, Gradient Boosting) to predict shot outcomes — with **GridSearchCV / RandomizedSearchCV** hyperparameter optimization and **k-fold cross-validation**.
- Identified **Gradient Boosted Trees** as the top performer on both eras after tuning, surfacing court-coordinate features (`LOC_X`, `LOC_Y`) as the dominant predictors.
- Produced spatial shot charts and KDE heatmaps that visually demonstrate the league's migration **away from the mid-range** and **toward the arc and the rim**.

---

## Why This Project

The 3-point line has driven the most consequential strategic shift in modern basketball. This project asks two questions a coach, GM, or analytics department would actually want answered:

1. **When did the 3-point boom inflect — and what does the data say drove it?**
2. **How do today's shooting habits differ from the late-1990s/early-2000s game, position by position and player by player?**

The answers are framed end-to-end: cleaning raw multi-source data → temporal trend analysis → spatial visualization → supervised ML scouting reports.

---

## Skills Demonstrated

| Area | Highlights |
|---|---|
| **Data Engineering** | Multi-source ingestion, schema reconciliation across team / player / shot-level grain, missing-value handling, position-label normalization |
| **EDA & Storytelling** | Time-series trend analysis, correlation studies (3PT volume vs. playoff appearances), comparative case studies (Jokić vs. Shaq, LeBron 2004 vs. LeBron 2023) |
| **Spatial Analytics** | Shot charts on a court overlay, KDE heatmaps of attempt density, distance-bucket distribution analysis |
| **Machine Learning** | Five classifiers benchmarked head-to-head, GridSearchCV + RandomizedSearchCV tuning, k-fold cross-validation, feature-importance interpretation |
| **Evaluation** | Accuracy, precision, recall, F1, confusion matrices — applied consistently across eras for apples-to-apples comparison |
| **Communication** | Annotated Jupyter notebook structured as a self-contained analyst report, exportable to PDF |

---

## Repository Contents

```
NBA-3-Point-Breakdown/
├── nba_shot_era_analysis.ipynb     # Primary notebook (analysis + ML)
├── nba_shot_era_analysis.pdf       # Rendered report with all visualizations
└── README.md
```

---

## Methodology

The notebook is organized as a five-section analyst report:

**0. Introduction** — Sets the historical and strategic context for the 3-point revolution.

**1. Data Cleaning & Overview** — Loads three datasets at three grains: team-level (1999–2023), player-level (1995–2024), and six season snapshots of shot-by-shot positional data (2004, 2007, 2011, 2015, 2019, 2023). Cleans, normalizes, and summarizes.

**2. Shooting Breakdown**
- 2.1 League-wide 3PT vs. 2PT volume trends
- 2.2 Did efficiency keep up with volume?
- 2.3 Position-level breakdown across all five positions (PG / SG / SF / PF / C)
- 2.4 Correlation between 3PT volume and playoff appearances

**3. Shot Mapping**
- 3.1 Shot-frequency heatmaps per era — visualizing the death of the mid-range
- 3.2 Distance-bucket distribution showing the 16-ft-to-arc shot nearly going extinct
- 3.3 Jokić vs. Shaq — same position, two opposite shot diets two decades apart

**4. Building a Scouting Report (Past vs. Present)** — A LeBron James case study using ML
- 4.1 Feature engineering on shot-coordinate data
- 4.2 Five classifiers trained on 2003–04 vs. 2022–23 seasons; default params → k-fold CV → hyperparameter tuning. Gradient Boosting wins both eras.
- 4.3 LeBron 2004: a paint-attacker with deadly baseline jumpers
- 4.4 LeBron 2023: same rim pressure, dramatically more 3PA — especially from his preferred top-right wing

**5. Conclusion** — Synthesizes findings on how analytics, rule changes, and pace-and-space offenses converged to reshape the league.

---

## Key Findings

- **The mid-range is endangered.** Shot volume from 16 ft to the 3-point line has collapsed to a fraction of its early-2000s share, replaced almost entirely by attempts at the rim and beyond the arc.
- **Every position adapted — including centers.** PFs and Cs caught up to guards in 3PT attempt and conversion rates, validating the "stretch big" archetype.
- **Volume and efficiency rose together.** Despite a higher proportion of 3PA, league-wide field-goal percentage trended upward — indicating better shot selection, not just more shots.
- **Playoff teams shoot more 3s.** Since the early 2000s, playoff teams have consistently attempted more 3-pointers than non-playoff teams.
- **Shot location dominates predictability.** Across both eras and all five models, court coordinates (`LOC_X`, `LOC_Y`) emerge as the most important features for predicting shot outcome.

---

## Tech Stack

**Language:** Python 3.7+

**Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

**Environment:** Jupyter Notebook / Google Colab

---

## Datasets

| Grain | Coverage | Notes |
|---|---|---|
| Team statistics | 1999–2023 | "NBA Stats (1947–present)" by Sumitro Datta (Kaggle) |
| Player shooting | 1995–2024 | Per-player rates by court distance |
| Shot-level positional | 6 seasons (2004, 2007, 2011, 2015, 2019, 2023) | Every shot, every player, with `LOC_X` / `LOC_Y` coordinates |

All datasets were cleaned to remove nulls and standardize position labels prior to analysis.

---

## Reproducing the Analysis

```bash
# 1. Clone
git clone https://github.com/ritvikv03/NBA-3-Point-Breakdown-.git
cd NBA-3-Point-Breakdown-

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# 3. Launch
jupyter notebook nba_shot_era_analysis.ipynb
```

Update the dataset paths in Section 1 if running outside the original Colab environment.

---

## Roadmap

- Interactive Plotly / Streamlit dashboard for shot-chart exploration
- Real-time data ingestion from the NBA Stats API
- Deep learning (CNN over shot-chart rasters) for shot-quality scoring
- Defensive-context features (closest defender distance, time on shot clock)
- Clutch-time and playoff-vs.-regular-season splits

---

## Acknowledgments

- **Data:** Kaggle NBA datasets, particularly Sumitro Datta's "NBA Stats (1947–present)"
- **Inspiration:** The Houston Rockets and Golden State Warriors organizations whose front offices popularized modern 3-point strategy

---

## Contact

I'm Ritvik — open to data science, ML engineering, and sports analytics opportunities. Feedback, questions, and collaboration are welcome.

> Built to understand how data has changed basketball forever.
