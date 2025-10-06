# 📊 Financial Analysis Tool

A professional Python tool for stock price analysis using **Monte Carlo Simulation** and **Linear Regression** with automated PDF report generation.

![Python Version](https://img.shields.io/badge/python-3.7%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-Google%20Colab-orange)

---

## 🎯 Features

### 📈 Monte Carlo Simulation
- **1,000 simulations** using Geometric Brownian Motion
- **Dual time horizons**: 5-year and 10-year forecasts
- **90% confidence intervals** for probabilistic price paths
- Expected returns and risk metrics

### 📉 Linear Regression Analysis
- **Trend identification** with daily and annualized rates
- **Standard deviation bands** (±1σ and ±2σ)
- **Visual confidence zones** showing 68% and 95% probability ranges
- Historical price pattern analysis

### 📄 Automated PDF Reports
- **Professional PDF output** with all visualizations
- **Comprehensive statistics** and analysis summary
- **Automatic download** upon completion
- Dark theme design for modern presentation

### 🎨 Professional Visualizations
- **Dark theme** with GitHub-inspired color palette
- **Enhanced grids** (major and minor) for precise reading
- **High-resolution charts** (18x10 inches)
- **Color-coded elements** for clarity

---

## 🚀 Quick Start

### Prerequisites

- Python 3.7 or higher
- Google Colab account (recommended) or local Python environment

### Required Libraries

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
```

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/financial-analysis-tool.git
cd financial-analysis-tool
```

2. **Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. **Upload to Google Colab** (recommended)
   - Open [Google Colab](https://colab.research.google.com/)
   - Upload the Python script
   - Run all cells

---

## 📖 Usage

### Step 1: Prepare Your Data

Your CSV or Excel file must contain:
- A `Date` column (any date format)
- A `Close` or `Clôture` column (closing prices)

**Example CSV format:**
```
Date,Close
2020-01-01,100.50
2020-01-02,101.25
2020-01-03,99.80
...
```

### Step 2: Run the Analysis

1. Execute the script in Google Colab or your Python environment
2. Upload your data file when prompted
3. Wait for the analysis to complete (typically 30-60 seconds)
4. Download the automatically generated PDF report

### Step 3: Interpret Results

**Monte Carlo Simulation Output:**
- Blue line: Historical prices
- Orange paths: 1,000 simulated future scenarios
- Green dashed line: Expected price path
- Shaded area: 90% confidence interval

**Linear Regression Output:**
- Blue line: Actual historical prices
- Red dashed line: Linear trend
- Orange bands: ±1σ (68% confidence)
- Purple bands: ±2σ (95% confidence)

---

## 📊 Output Examples

### Monte Carlo Simulation (5-Year Forecast)
The tool generates probabilistic price forecasts showing:
- Expected final price
- Standard deviation
- 95% confidence interval
- Potential return percentage

### Linear Regression with Bands
Visual representation of:
- Long-term price trend
- Price volatility zones
- Over/undervalued periods
- Support and resistance levels

### PDF Report Contents
1. **Cover Page**: Ticker, analysis date, data summary
2. **Statistics Page**: All numerical results
3. **Visualizations**: All generated charts

---

## 🛠️ Technical Details

### Monte Carlo Methodology

The simulation uses **Geometric Brownian Motion (GBM)**:

```
dS = μ * S * dt + σ * S * dW
```

Where:
- `S` = Stock price
- `μ` = Drift (mean return)
- `σ` = Volatility (standard deviation)
- `dW` = Wiener process (random component)

**Parameters calculated from historical data:**
- Daily returns: `log(P_t / P_{t-1})`
- Mean (μ): Average of log returns
- Volatility (σ): Standard deviation of log returns

### Linear Regression Methodology

**Model:** `Price = β₀ + β₁ × Days + ε`

**Confidence Bands:**
- ±1σ band: Contains ~68% of price observations
- ±2σ band: Contains ~95% of price observations

---

## 📁 Project Structure

```
financial-analysis-tool/
│
├── financial_analysis.py    # Main script
├── README.md                 # This file
├── requirements.txt          # Python dependencies
├── LICENSE                   # MIT License
│
└── examples/
    ├── sample_data.csv       # Example dataset
    └── sample_report.pdf     # Example output
```

---

## ⚙️ Configuration

You can customize the analysis by modifying these parameters in the code:

```python
# Monte Carlo settings
num_simulations = 1000              # Number of simulations
trading_days_per_year = 252         # Trading days

# Forecast horizons
forecast_periods = {
    '5 Years': 5 * 252,
    '10 Years': 10 * 252
}

# Visual settings
COLORS = {
    'primary': '#58a6ff',
    'historical': '#58a6ff',
    'simulation': '#f78166',
    # ... customize colors
}
```

---

## 📝 Data Requirements

### Supported File Formats
- ✅ CSV (`.csv`)
- ✅ Excel (`.xls`, `.xlsx`)

### Required Columns
- `Date`: Trading date (any standard format)
- `Close` or `Clôture`: Closing price

### Data Quality Tips
- Ensure continuous daily data (no large gaps)
- Remove or handle missing values
- Use adjusted closing prices for accuracy
- Minimum recommended: 252 data points (1 year)

---

## 🎨 Customization

### Changing Colors
Modify the `COLORS` dictionary to match your brand:

```python
COLORS = {
    'historical': '#YOUR_COLOR',
    'simulation': '#YOUR_COLOR',
    'mean': '#YOUR_COLOR',
    # ...
}
```

### Adjusting Time Horizons
Add or modify forecast periods:

```python
forecast_periods = {
    '3 Years': 3 * 252,
    '5 Years': 5 * 252,
    '15 Years': 15 * 252
}
```

### Grid Customization
Adjust grid appearance in the configuration section:

```python
plt.rcParams['grid.alpha'] = 0.5        # Transparency
plt.rcParams['grid.linewidth'] = 0.8    # Line thickness
```

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Scikit-learn** for machine learning tools
- **Matplotlib & Seaborn** for beautiful visualizations
- **Pandas & NumPy** for efficient data processing
- **Google Colab** for free cloud computing

---

## 📧 Contact

For questions, suggestions, or issues:

- 📧 Email: noelarquemin@yahoo.fr
- 🐛 Issues: [GitHub Issues](https://github.com/yourusername/financial-analysis-tool/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/yourusername/financial-analysis-tool/discussions)

---

## ⚠️ Disclaimer

**This tool is for educational and research purposes only.**

- Not financial advice
- Past performance does not guarantee future results
- Monte Carlo simulations are probabilistic models with inherent uncertainty
- Always consult with a qualified financial advisor before making investment decisions

---

## 🔮 Future Enhancements

- [ ] Add ARIMA/GARCH models
- [ ] Support for multiple assets portfolio analysis
- [ ] Interactive dashboard with Plotly
- [ ] Real-time data fetching from APIs (Yahoo Finance, Alpha Vantage)
- [ ] Backtesting framework
- [ ] Risk metrics (VaR, Sharpe Ratio, etc.)
- [ ] Export to Excel with detailed tables

---

<div align="center">

**⭐ Star this repository if you find it useful!**

Made with ❤️ and Python

</div>
