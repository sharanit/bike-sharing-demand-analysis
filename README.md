# 🚴 Bike Sharing Demand Analysis & Hypothesis Testing

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Complete-success)

A comprehensive statistical analysis of bike-sharing demand patterns using hypothesis testing and exploratory data analysis. This project identifies key factors influencing rental demand and provides actionable insights for operational optimization.

## 📊 Project Overview

This project analyzes bike-sharing rental data to understand demand patterns and identify significant predictors of rental volumes. Using rigorous statistical methods, we test hypotheses about the impact of temporal, seasonal, and weather factors on bike-sharing demand.

### Business Context

Bike-sharing services face revenue fluctuations driven by various external factors. This analysis helps answer critical business questions:
- Which variables significantly predict demand?
- How do different factors influence rental patterns?
- What operational strategies can optimize revenue?

## 🎯 Key Objectives

1. **Identify Significant Predictors**: Determine which variables have statistically significant impact on bike rental demand
2. **Quantify Relationships**: Measure the strength and nature of relationships between predictors and demand
3. **Statistical Validation**: Use hypothesis testing to validate business assumptions
4. **Actionable Insights**: Translate statistical findings into business recommendations

## 📁 Project Structure

```
bike-sharing-demand-analysis/
│
├── README.md                          # Project documentation
├── requirements.txt                   # Python dependencies
├── LICENSE                           # MIT License
│
├── notebooks/
│   └── bike_sharing_analysis.ipynb   # Main analysis notebook
│
├── data/
│   └── README.md                     # Data source information
│
├── reports/
│   ├── ANALYSIS_REPORT.md           # Detailed findings
│   └── EXECUTIVE_SUMMARY.md         # Executive summary
│
└── images/                           # Visualizations and plots
    └── .gitkeep
```

## 🔍 Analysis Methodology

### Statistical Tests Performed

1. **Two-Sample T-Test**
   - Objective: Test if working days affect rental demand
   - Null Hypothesis: No difference in mean rentals between working and non-working days
   
2. **ANOVA (Analysis of Variance)**
   - Objective: Compare rental demand across multiple seasons and weather conditions
   - Tests: Season impact and weather impact on demand
   
3. **Chi-Square Test**
   - Objective: Test independence between weather and season
   - Determines if weather patterns depend on seasonal changes

### Data Analysis Steps

1. **Data Profiling & Cleaning**
   - Shape analysis and data type verification
   - Missing value detection and handling
   - Outlier identification

2. **Exploratory Data Analysis**
   - Univariate analysis of all variables
   - Bivariate relationship exploration
   - Distribution analysis and visualization

3. **Hypothesis Testing**
   - Assumption checking (normality, equal variance)
   - Test statistic calculation
   - P-value interpretation and conclusion

4. **Insight Generation**
   - Pattern identification
   - Business translation of statistical findings

## 📈 Key Findings

### Major Insights

- **Seasonal Impact**: Fall season shows significantly higher demand (2.1x Spring)
- **Weather Dependency**: Clear weather drives 1.65x more rentals than rainy conditions
- **User Composition**: Registered users account for 81% of total demand
- **Working Day Effect**: Statistically insignificant difference (p > 0.05)

### Statistical Results

| Test | Variable | p-value | Result | Effect Size |
|------|----------|---------|---------|-------------|
| T-Test | Working Day | 0.642 | No significant difference | Small |
| ANOVA | Season | < 0.001 | Highly significant | Large |
| ANOVA | Weather | < 0.001 | Highly significant | Large |
| Chi-Square | Weather × Season | < 0.001 | Dependent | Medium |

## 💡 Business Recommendations

### Immediate Actions

1. **Dynamic Fleet Management**: Adjust bike availability based on seasonal forecasts
2. **Weather-Responsive Operations**: Implement daily weather-based operational adjustments
3. **Targeted Marketing**: Concentrate marketing spend during high-demand seasons

### Strategic Initiatives

1. **Predictive Demand Modeling**: Build forecasting models using season + weather
2. **User Conversion Programs**: Focus on converting casual users to registered members
3. **Dynamic Pricing**: Implement weather and season-based pricing strategies
4. **Geographic Diversification**: Expand to regions with complementary seasonal patterns

## 🛠️ Technologies Used

- **Python 3.8+**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib & Seaborn**: Data visualization
- **SciPy**: Statistical testing and analysis
- **Jupyter Notebook**: Interactive development environment

## 📊 Dataset Information

**Source**: Bike sharing rental data (2011-2012)  
**Size**: 10,886 hourly records  
**Features**: 12 variables including temporal, weather, and demand metrics

### Key Variables

- **Temporal**: datetime, season, holiday, workingday
- **Weather**: weather condition, temperature, humidity, windspeed
- **Demand**: casual users, registered users, total count

*See `data/README.md` for detailed variable descriptions*

## 🚀 Getting Started

### Prerequisites

```bash
Python 3.8 or higher
pip (Python package manager)
```

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/bike-sharing-demand-analysis.git
cd bike-sharing-demand-analysis
```

2. **Create virtual environment** (recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Launch Jupyter Notebook**
```bash
jupyter notebook notebooks/bike_sharing_analysis.ipynb
```

## 📖 Usage

1. Open the Jupyter notebook in the `notebooks/` directory
2. Run cells sequentially to reproduce the analysis
3. Modify parameters or add custom analyses as needed
4. Refer to `reports/` directory for detailed findings

## 📝 Documentation

- **[Analysis Report](reports/ANALYSIS_REPORT.md)**: Comprehensive technical analysis
- **[Executive Summary](reports/EXECUTIVE_SUMMARY.md)**: High-level business insights
- **[Data Documentation](data/README.md)**: Dataset details and variable descriptions

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE]file for details.

## 👤 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/sharanit)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/sharanvora)

## 🙏 Acknowledgments

- Dataset provided by bike-sharing service for research purposes
- Statistical methodology based on standard hypothesis testing frameworks
- Visualization inspired by best practices in data science communication

## 📧 Contact

For questions or feedback, please open an issue or contact [sharanvoracareers@gmail.com]

---

⭐ If you found this project helpful, please consider giving it a star!
