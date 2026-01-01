# NBA 3-Point Breakdown: Evolution of the Three-Point Revolution

An in-depth data analytics project exploring how 3-point shooting has transformed professional basketball over the past 25 years (1999-2023). This project combines exploratory data analysis, statistical visualization, and machine learning to understand one of the most significant strategic shifts in NBA history.

## 📊 Project Overview

The 3-point line, introduced to the NBA in 1976, has fundamentally altered how basketball is played. This project investigates:

1. **When and how did the NBA 3-Point boom arrive within the past 30 years?**
2. **What commonalities exist in shooting habits between today's players versus their counterparts in the late 1990s and early 2000s?**

Through comprehensive analysis of team statistics, player shooting patterns, and shot-level positional data, this project traces the evolution from the traditional inside-out game to today's perimeter-oriented offense.

## 🎯 Key Features

### Data Analysis Components
- **Temporal Trend Analysis**: Tracking 3-point shooting volume and efficiency across 24 seasons (1999-2023)
- **Position-Based Breakdown**: How shooting patterns differ across guards, forwards, and centers
- **Shot Mapping**: Geographic visualization of shot attempts and makes across different eras
- **Comparative Analysis**: Side-by-side comparisons of iconic players (e.g., Jokic vs. Shaq)
- **Team Success Correlation**: Relationship between 3-point shooting and overall team performance

### Machine Learning Models
- **Era Classification**: Predicting shot success using 5 different classifiers
  - Logistic Regression
  - Random Forest
  - K-Nearest Neighbors
  - Decision Tree
  - Gradient Boosting
- **Model Optimization**: Hyperparameter tuning via GridSearchCV and RandomizedSearchCV
- **Cross-Validation**: K-fold validation to ensure model robustness
- **Performance Metrics**: Comprehensive evaluation using accuracy, precision, recall, F1-score, and confusion matrices

## 📁 Project Structure

```
NBA-3-Point-Breakdown/
├── 3_Point_Shooting_Era_Breakdown (1).ipynb    # Main analysis notebook
├── 3_Point_Shooting_Era_Breakdown (1).pdf      # Generated report with visualizations
└── README.md                                    # Project documentation
```

## 🔧 Technologies Used

**Language**: Python 3.x (Jupyter Notebook/Google Colab)

**Core Libraries**:
- **Data Processing**: `pandas`, `numpy`
- **Visualization**: `matplotlib`, `seaborn`
- **Machine Learning**: `scikit-learn`
  - Classification algorithms
  - Model selection and hyperparameter tuning
  - Cross-validation frameworks
- **Statistical Analysis**: Standard Python data science stack

## 📦 Datasets

The project utilizes three comprehensive datasets covering different granularities of NBA shooting data:

### 1. Team-Level Data
- **Source**: "NBA Stats (1947-present)" by Sumitro Datta (Kaggle)
- **Coverage**: Seasons 1999-2023
- **Metrics**: Field goal percentages, 3-point percentages, team shooting efficiency

### 2. Player-Level Data
- **Coverage**: Seasons 1995-2024
- **Metrics**: Shooting rates from different court distances, per-player statistics
- **Quality**: Cleaned dataset with no missing values

### 3. Shot-Level Positional Data
Six season snapshots with granular shot location data:
- NBA_2004_Shots.csv
- NBA_2007_Shots.csv
- NBA_2011_Shots.csv
- NBA_2015_Shots.csv
- NBA_2019_Shots.csv
- NBA_2023_Shots.csv

Each dataset contains every shot attempted by every player with positional coordinates.

## 🔬 Analysis Methodology

The notebook is organized into five comprehensive sections:

### Section 0: Introduction
Sets the historical context for the 3-point revolution and its impact on modern basketball strategy.

### Section 1: Data Cleaning and Overview
- Imports and cleans team stats, player shooting, and positional datasets
- Removes missing values and standardizes position labels
- Provides statistical summaries and initial data exploration

### Section 2: Shooting Breakdown
- **2.1** Overall 3-point trends across multiple time periods
- **2.2** Analysis of 3-point shooting success rates
- **2.3** Position-specific shooting pattern analysis
- **2.4** Correlation between 3-point efficiency and team success metrics

### Section 3: Shot Mapping
- **3.1** Visual heat maps of shot attempts and successful shots
- **3.2** Shot distance distribution analysis across eras
- **3.3** Player-by-player comparative analysis (modern vs. classic playstyles)

### Section 4: Building a Scouting Report (Past vs Present)
- **4.1** Feature engineering for machine learning models
- **4.2** Model training and evaluation:
  - Training separate classifiers on 2003-2004 data (early era)
  - Training same classifiers on 2022-2023 data (modern era)
  - Hyperparameter optimization using grid search
  - Comprehensive evaluation with multiple performance metrics
  - Visual comparison through confusion matrices
  - Analysis of how shooting predictability has changed between eras

### Section 5: Conclusion
Synthesizes findings about the 3-point revolution and its implications for modern basketball.

## 📈 Key Insights

This project generates:
- **Time-series visualizations** showing the acceleration of 3-point shooting adoption
- **Position-based analysis** revealing how every position (even centers) has adapted to perimeter shooting
- **Correlation studies** linking 3-point volume/efficiency to team success
- **Machine learning models** that demonstrate how shot selection patterns differ dramatically between eras
- **Visual shot charts** comparing shooting patterns across 20+ years of NBA evolution

## 🚀 Getting Started

### Prerequisites
```bash
Python 3.7+
Jupyter Notebook or Google Colab
```

### Required Libraries
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Running the Analysis
1. Clone this repository
2. Open `3_Point_Shooting_Era_Breakdown (1).ipynb` in Jupyter Notebook or Google Colab
3. Ensure datasets are accessible (update file paths if necessary)
4. Run cells sequentially to reproduce the analysis

## 📊 Sample Visualizations

The notebook generates numerous visualizations including:
- 3-point attempt trends over time (line charts)
- Position-specific shooting heat maps
- Shot location scatter plots with court overlay
- Model performance confusion matrices
- Correlation matrices for shooting metrics and team success

## 🔍 Research Questions Answered

1. **The 3-Point Boom Timeline**: Data reveals the inflection point where teams dramatically increased 3-point volume, correlating with rule changes, analytics adoption, and the success of pace-and-space offenses.

2. **Modern vs. Classic Shooting Habits**: Machine learning models demonstrate significant differences in shot selection, with modern players taking substantially more 3-pointers across all positions while maintaining or improving efficiency.

## 🤝 Contributing

Feedback, suggestions, and contributions are welcome! Areas for potential expansion:
- Additional seasons and real-time data integration
- Defensive impact analysis on 3-point shooting
- Playoff vs. regular season shooting pattern differences
- Individual player trajectory analysis
- Advanced shot quality metrics

## 📝 Future Enhancements

Potential areas for further exploration:
- Deep learning models for shot prediction
- Real-time API integration for current season data
- Interactive dashboards using Plotly or Streamlit
- Advanced spatial analysis using court coordinate data
- Clutch-time shooting pattern analysis

## 📄 License

This project is open source and available for educational and research purposes.

## 🙏 Acknowledgments

- **Data Sources**: Kaggle NBA statistics datasets by Sumitro Datta and other contributors
- **Inspiration**: The NBA's analytical revolution and teams like the Houston Rockets and Golden State Warriors who popularized modern 3-point strategies
- **Tools**: Python data science ecosystem and Jupyter/Google Colab for interactive analysis

## 📧 Contact

Open to feedback, collaboration opportunities, and discussions about basketball analytics! Feel free to reach out with suggestions or questions.

---

**Built with** 🏀 **and** 📊 **to understand how data has changed basketball forever.**
