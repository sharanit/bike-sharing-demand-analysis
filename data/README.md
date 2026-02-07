# Dataset Documentation

## Overview

This dataset contains hourly bike-sharing rental data from a bike-sharing system, spanning two years (2011-2012). The data includes information about temporal factors, weather conditions, and rental counts.

## Data Source

**Original Source**: Bike Sharing Dataset  
**URL**: https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/428/original/bike_sharing.csv  
**Collection Period**: 2011-2012  
**Granularity**: Hourly records  
**Total Records**: 10,886 observations

## Dataset Characteristics

- **Size**: 10,886 rows × 12 columns
- **File Format**: CSV (Comma-Separated Values)
- **Missing Values**: None
- **Data Quality**: Clean, ready for analysis

## Variable Descriptions

### Temporal Variables

| Variable | Type | Description | Values/Range |
|----------|------|-------------|--------------|
| `datetime` | DateTime | Date and hour of the record | 2011-01-01 to 2012-12-31 |
| `season` | Categorical | Season of the year | 1: Spring<br>2: Summer<br>3: Fall<br>4: Winter |
| `holiday` | Binary | Whether the day is a holiday | 0: No<br>1: Yes |
| `workingday` | Binary | Whether the day is a working day | 0: Weekend/Holiday<br>1: Working day |

### Weather Variables

| Variable | Type | Description | Values/Range |
|----------|------|-------------|--------------|
| `weather` | Categorical | Weather condition | 1: Clear/Partly Cloudy<br>2: Mist/Cloudy<br>3: Light Rain/Snow<br>4: Heavy Rain/Snow |
| `temp` | Continuous | Actual temperature in Celsius | Min: -8°C<br>Max: 39°C |
| `atemp` | Continuous | "Feels like" temperature in Celsius | Min: -16°C<br>Max: 50°C |
| `humidity` | Continuous | Relative humidity percentage | 0-100% |
| `windspeed` | Continuous | Wind speed | 0-67 km/h |

### Demand Variables

| Variable | Type | Description | Range |
|----------|------|-------------|-------|
| `casual` | Integer | Count of casual (non-registered) users | 0-367 |
| `registered` | Integer | Count of registered users | 0-886 |
| `count` | Integer | **Total rental count** (casual + registered) | 1-977 |

## Target Variable

**Primary Target**: `count` - Total number of bike rentals per hour

This is the dependent variable for all predictive and inferential analyses.

## Data Quality Notes

### Completeness
- ✅ No missing values in any column
- ✅ All records have complete information

### Consistency
- ✅ Date range is continuous without gaps
- ✅ Count = Casual + Registered (validated)
- ✅ Categorical variables use consistent encoding

### Outliers
- Temperature: Some extreme values during winter and summer months (expected)
- Windspeed: Few high values during storm conditions (valid)
- Rentals: High-demand periods show elevated counts (valid business patterns)

## Usage Notes

### Loading the Data

```python
import pandas as pd

# Load from URL
url = "https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/428/original/bike_sharing.csv"
df = pd.read_csv(url)

# Convert datetime
df['datetime'] = pd.to_datetime(df['datetime'])

# Convert categorical variables
categorical_cols = ['season', 'holiday', 'workingday', 'weather']
df[categorical_cols] = df[categorical_cols].astype('category')
```

### Recommended Transformations

1. **DateTime Parsing**: Convert `datetime` to proper datetime type for time-based analysis
2. **Category Encoding**: Convert categorical variables (season, weather, etc.) to category type
3. **Feature Engineering**: Extract hour, day of week, month from datetime for richer analysis

## Statistical Properties

### Distribution Characteristics

- **Count (Target)**: Right-skewed distribution with median ~142, mean ~189
- **Temperature**: Approximately normal distribution
- **Humidity**: Slight left-skew, most values between 40-80%
- **User Types**: Registered users dominate (81% of total rentals)

### Seasonal Patterns

- **Fall**: Highest average demand (~236 rentals/hour)
- **Summer**: Second highest (~208 rentals/hour)  
- **Winter**: Moderate demand (~186 rentals/hour)
- **Spring**: Lowest demand (~111 rentals/hour)

### Weather Impact

- **Clear Weather**: Highest rental rates
- **Misty/Cloudy**: Moderate reduction in rentals
- **Light Rain/Snow**: Significant reduction
- **Heavy Rain/Snow**: Severe reduction (rare occurrence)

## Citation

If you use this dataset, please cite:

```
Bike Sharing Demand Dataset
Source: Bike Sharing System Analysis
Period: 2011-2012
Accessed: [Your Access Date]
```

## Data License

This dataset is provided for educational and research purposes. Please verify the original data source for specific licensing terms.

## Additional Resources

- **Analysis Notebook**: `notebooks/bike_sharing_analysis.ipynb`
- **Full Analysis Report**: `reports/ANALYSIS_REPORT.md`
- **Executive Summary**: `reports/EXECUTIVE_SUMMARY.md`

---

For questions about the data or its usage in this project, please refer to the main README or open an issue.
