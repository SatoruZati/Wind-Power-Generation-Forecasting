# Wind Power Generation Forecasting

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Datasets](#datasets)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Results](#results)
- [File Structure](#file-structure)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## Project Overview
Wind Power Generation Forecasting is an internship project aimed at developing a robust machine learning pipeline to predict short-term wind power output based on meteorological and temporal features. Accurate forecasts help grid operators balance supply and demand, facilitating greater integration of renewable energy.

**Key Objectives:**
- Merge and preprocess multi-location time-series data.
- Perform exploratory data analysis to identify key patterns.
- Build, evaluate, and compare regression and deep learning models.
- Optimize models via hyperparameter tuning and ensemble methods.

---

## Features
- Data ingestion from multiple CSV sources with location tagging.
- Comprehensive data cleaning and feature engineering (timestamp parsing, handling missing values).
- Exploratory Data Analysis (univariate, bivariate, correlation heatmaps).
- Baseline and advanced regression models (Linear Regression, Random Forest, XGBoost).
- Neural network forecasting with TensorFlow/Keras.
- Model evaluation metrics: MSE, RMSE, MAE, R².
- Hyperparameter tuning using `GridSearchCV`.
- Stacked ensemble to boost predictive performance.

---

## Datasets
The project uses four CSV files corresponding to different wind farm locations:
- `Location1.csv`
- `Location2.csv`
- `Location3.csv`
- `Location4.csv`

Each file contains:
- `Timestamp` (date and time of measurement)
- `Power` (wind power output)
- `WindSpeed`, `WindDirection`, `Temperature`, _etc._
- A new `Location` column is added during preprocessing for identification.

---

## Installation
1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/wind-power-forecasting.git
   cd wind-power-forecasting
   ```

2. **Create a virtual environment (optional but recommended)**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage
1. **Prepare the data**
   - Place `Location1.csv` through `Location4.csv` into the `data/` folder.

2. **Run the notebook**
   ```bash
   jupyter notebook main.ipynb
   ```

3. **Follow the steps** in the notebook:
   - Data merging & preprocessing
   - Exploratory Data Analysis
   - Model training & evaluation
   - Hyperparameter tuning & ensembling

4. **Export results**
   - Performance metrics table
   - Actual vs. Predicted plots

---

## Methodology
1. **Data Collection & Merging**
   - Load and concatenate data from all locations.
2. **Data Cleaning & Feature Engineering**
   - Parse timestamps, remove unnecessary columns, impute missing values.
   - Create time-based features (hour, day, month).
3. **Exploratory Data Analysis**
   - Univariate distributions of power and features.
   - Correlation heatmap and scatterplots.
4. **Model Development**
   - Baseline: Linear Regression
   - Tree-based: Random Forest, XGBoost
   - Deep Learning: Sequential Keras model
5. **Model Evaluation & Optimization**
   - Use MSE, RMSE, MAE, R² for comparison.
   - Grid search for hyperparameters.
   - Stack top models into an ensemble.

---

## Results
| Model                   | MSE      | RMSE     | MAE      | R² Score |
|-------------------------|----------|----------|----------|----------|
| Stacked Ensemble        | 0.359717 | 0.599764 | 0.439174 | 0.643399 |
| Optimized Random Forest | 0.360299 | 0.600249 | 0.439799 | 0.642823 |
| Optimized XGBoost       | 0.376748 | 0.613798 | 0.449729 | 0.626516 |


**Best Performing Model:** Stacked Ensemble with RMSE = 0.599764 and R² = 0.643399.

---

## File Structure
```bash
├── data/                  # Raw CSV files (Location1.csv–Location4.csv)
├── notebooks/
│   └── main.ipynb         # Jupyter notebook with full pipeline
├── scripts/
│   └── preprocess.py      # Data cleaning and feature engineering script
│   └── train_models.py    # Model training and evaluation script
├── reports/
│   └── figures/           # Plots and visualizations
├── requirements.txt       # Python dependencies
├── README.md              # This file
└── LICENSE
```

---

## Dependencies
- Python ≥3.8
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost
- tensorflow

Install via:
```bash
pip install -r requirements.txt
```

---

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch: `git checkout -b feature/YourFeature`
3. Commit your changes: `git commit -m 'Add new feature'`
4. Push to the branch: `git push origin feature/YourFeature`
5. Open a Pull Request.

Please ensure code style consistency and update documentation as needed.

---

## License
This project is licensed under the [MIT License](LICENSE).

---

## Contact
**Your Name**  
Email: 50.satadrujati.11sc1@gmail.com 
GitHub: SatoruZati

---

_Powered by Python_

