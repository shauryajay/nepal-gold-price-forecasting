# Forecasting Nepal's 24K Gold Prices Using Machine Learning

## 1. Project Overview

This project explores the use of machine learning to analyse and forecast 24-karat gold prices in Nepal.

The main objective is to investigate whether machine learning models can identify patterns in historical gold prices and use them to predict future prices.

This is my first machine learning project, and I am using it to develop practical skills in data analysis, machine learning, and model evaluation.

## 2. Research Question

**How accurately can machine learning models forecast 24K gold prices in Nepal using historical price data?**

## 3. Dataset

The project uses historical 24K gold price data from Nepal.

- Number of observations: 4,668
- Features: Published date and gold price
- Time period: June 2010 – November 2026
- Target variable: Gold price

The dataset is being explored and prepared using Python and Pandas.

## 4. Methodology

The project follows these main stages:

1. Data collection and exploration
2. Data cleaning and preprocessing
3. Feature engineering using previous gold prices
4. Chronological training and testing split
5. Training different machine learning models
6. Evaluating and comparing model performance

## 5. Models Tested

The following models have been explored:

- Decision Tree Regressor
- Random Forest Regressor
- Linear Regression
- ARIMA
- Feedforward Neural Network

Additional models may be explored as the project progresses.

## 6. Preliminary Results

The models are evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

| Model | MAE (NPR) |
|---|---:|
| Baseline | 1,647.16 |
| Linear Regression | 1,706.64 |
| Neural Network | 2,795.76 |
| ARIMA | 90,670.70 |
| Random Forest | 91,080.25 |
| Decision Tree | 91,137.51 |

The baseline currently performs best among the evaluated models.

## 7. Key Observations

- More complex models do not necessarily produce more accurate predictions.
- Decision Tree and Random Forest models struggled with the substantial increase in gold prices during the testing period.
- Linear Regression performed considerably better than the tree-based models.
- The simple baseline model currently outperforms the trained models.

## 8. Project Structure

```text
nepal-gold-price-forecasting/
│
├── data/
│   └── Dataset files
│
├── notebooks/
│   └── gold_price_forecasting.ipynb
│
├── docs/
│   └── experiment-log.md
│
├── .gitignore
├── requirements.txt
└── README.md
```

## 9. Project Files

- [View the Jupyter Notebook](notebooks/gold_price_forecasting.ipynb)
- [View the Experiment Log](docs/experiment-log.md)
- [View Project Dependencies](requirements.txt)

## 10. Future Work

- Experiment with LSTM neural networks.
- Explore additional features that may influence gold prices.
- Improve model performance.
- Investigate the effect of changing gold price trends.
- Compare different forecasting approaches.

## 11. Limitations

This project is exploratory and educational. Its predictions should not be treated as financial advice.

The dataset's reliability, forecasting assumptions, and model limitations will be examined further as the project develops.
