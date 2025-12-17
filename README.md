#  Diamond Price Prediction - Linear Regression

##  Project Overview

Machine learning project that predicts diamond prices based on physical properties. Built as part of a Data Science course to demonstrate linear regression techniques, data cleaning, and exploratory data analysis.

##  Business Problem

A jewelry store needs to automate diamond valuation due to high customer volume. This model predicts diamond prices based on physical measurements, enabling quick and accurate pricing.

##  Dataset

- **Source:** Classic diamonds dataset (53,940 diamonds)
- **After cleaning:** 53,917 diamonds
- **Target variable:** Price (USD)

##  Features Used

| Feature | Description |
|---------|-------------|
| carat | Weight of diamond (1 carat = 0.20 grams) |
| x | Length in mm |
| y | Width in mm |
| z | Depth in mm |

**Removed features:** cut, color, clarity, depth, table (correlation < 0.3 with price)

##  Model Performance

| Metric | Score |
|--------|-------|
| R² Score | 0.8633 |
| RMSE | $1,505.77 |
| MAE | $896.55 |

**Key insight:** Model explains 86.3% of price variance. Carat is the strongest predictor (+$10,826 per carat).

## Tech Stack

- Python 3.11
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Docker

##  How to Run with Docker
```bash
docker-compose build
docker-compose up
```

Then open http://localhost:8888 in your browser.

##  Project Structure
```
├── Linear Regresion diamonds.ipynb  # Main notebook
├── diamonds.csv                      # Original dataset
├── diamonds_cleaned.csv              # Cleaned dataset
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── README.md
```

##  Key Findings

1. **Carat dominates pricing** - strongest correlation with price (0.92)
2. **Simpson's Paradox** - quality features (cut, color, clarity) show weak correlation due to confounding with carat
3. **Multicollinearity** - x, y, z dimensions are highly correlated with carat (>0.95)

## Future Improvements

- Log transformation of price for better predictions
- Try advanced models (Random Forest, XGBoost)
- Feature engineering (volume = x × y × z)

##  Author

Milica Antić

---
