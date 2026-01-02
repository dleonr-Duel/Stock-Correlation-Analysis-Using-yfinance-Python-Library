# Stock Correlation and Diversification Analysis

## Overview
This project is a command-line Python tool for analyzing correlation and diversification across financial assets using real historical market data. It demonstrates practical FinTech and quantitative skills including time-series analysis, return-based statistics, data visualization, and reproducible research workflows.

The tool allows users to select assets, download adjusted close prices, compute daily returns, evaluate correlations, and generate publication-ready visualizations that support portfolio diversification analysis.

---

## Core Objectives
- Analyze how financial assets move relative to one another
- Quantify diversification using return correlations
- Visualize market relationships in a clear, interpretable way
- Build a reusable, well-documented analysis tool

---

## Skills Demonstrated
- Financial time-series analysis
- pandas and NumPy for data manipulation
- Return and correlation-based statistics
- Data visualization with matplotlib and seaborn
- Command-line interface (CLI) design with argparse
- Reproducible, timestamped outputs
- Clean project structure suitable for technical review

---

## How the Program Works
1. Downloads adjusted close price data using Yahoo Finance
2. Cleans and aligns time-series data
3. Computes daily percentage returns
4. Builds a correlation matrix across assets
5. Normalizes prices for relative performance comparison
6. Generates and saves visual outputs
7. Identifies the most highly correlated asset pairs

---

## Default Asset Set
If no tickers are specified, the program analyzes a diversified ETF portfolio:
- SPY – S&P 500
- QQQ – Nasdaq 100
- IWM – Russell 2000
- XLK – Technology sector
- XLF – Financial sector
- TLT – U.S. Treasury bonds

This mix highlights equity co-movement and the diversification role of fixed income.

---

## Installation

Install required packages:
```bash
pip install pandas numpy matplotlib seaborn yfinance
```

---

## Usage

Run interactively:
```bash
python StockCorrelationAnalysis_TS_Final.py
```

Run with custom tickers and date range:
```bash
python StockCorrelationAnalysis_TS_Final.py -t SPY,QQQ,IWM,XLK,XLF,TLT -s 2021-01-01
```

Optional flags:
- `--save-csv`  Save adjusted close prices to CSV
- `-o outputs`  Specify a custom output directory

---

## Outputs

The program generates timestamped files for reproducibility:

- **Normalized Price Chart**  
  Compares relative asset performance by normalizing all prices to a common starting value

- **Correlation Heatmap**  
  Visualizes the strength and structure of return correlations across assets

- **Optional CSV File**  
  Adjusted close prices for extended analysis

---

## Interpretation
- Assets with correlations close to 1.0 tend to move together and reduce diversification
- Lower or negative correlations improve diversification potential
- Fixed-income assets typically exhibit lower correlation with equities

These results mirror real-world portfolio construction principles.

---

## Why This Project Matters
This project reflects how quantitative concepts are applied in real financial analysis. It shows the ability to work with real market data, apply statistical reasoning, and communicate results clearly through code and visualizations.

The design and structure intentionally resemble entry-level FinTech and quantitative research workflows.

---

## Future Extensions
- Rolling and regime-based correlation analysis
- Volatility and risk metrics
- Portfolio-weighted correlation measures
- Support for additional asset classes

---

## Disclaimer
This project is for educational purposes only and does not constitute financial advice.

