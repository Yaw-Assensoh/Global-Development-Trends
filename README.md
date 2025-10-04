# Global-Development-Trends
📌 Project Overview

This project explores World Bank Development Indicators (WDI) to analyze global patterns across four key dimensions:

CO₂ emissions (environmental impact)
GDP (economic performance)
Internet usage (digital growth)
Life expectancy (social well-being)
The analysis combines time-series trends, geographical comparisons, and cross-indicator relationships to evaluate sustainable development progress from 2000-2025.

Key Research Questions

How have CO₂ emissions changed across countries from 2000–2025?
What is the relationship between GDP growth and internet usage?
How has life expectancy evolved across regions?
Which countries show the strongest progress in sustainable development?
Can we identify patterns linking economic performance and environmental impact?
🛠️ Setup Instructions

Data Requirements

Dataset Source: World Bank Development Indicators (WDI)
Size: ~2,660 rows × 22 columns
Geography: Countries & regions worldwide
Time Period: 2000–2025

Key Indicators:

CO₂ emissions (metric tons per capita)
GDP (current US$)
Internet users (per 100 people)
Life expectancy at birth (years)

Environment Setup
# Create and activate virtual environment
python -m venv wdi_analysis
source wdi_analysis/bin/activate  # On Windows: wdi_analysis\Scripts\activate

# Install dependencies
pip install -r requirements.txt

Required Dependencies (requirements)
pandas>=1.5.0
numpy>=1.21.0
matplotlib>=3.5.0
seaborn>=0.11.0
plotly>=5.0.0
geopandas>=0.10.0
jupyter>=1.0.0
notebook>=6.0.0

Run Commands
# Launch Jupyter Notebook
jupyter notebook

# Or run analysis directly
python scripts/main_analysis.py

# Generate specific visualizations
python scripts/visualization.py

# Run data preprocessing
python scripts/data_preprocessing.py

Project Structure
worldbank-wdi-analysis/
│
├── data/
│   ├── raw/
│   │   └── WDI_2000_2025.csv          # Original dataset
│   ├── processed/
│   │   ├── cleaned_data.csv           # Cleaned dataset
│   │   └── analysis_ready.csv         # Analysis-ready data
│   └── external/
│       └── world_countries.geojson    # GeoJSON for mapping
│
├── scripts
│   ├── 01_data_preparation.ipynb      # Initial data exploration
│   ├── 02_data_exploration.ipynb         # Data preprocessing
│   ├── 03_geospatial_analysis.ipynb   # choropleth maps
│   ├── 04_regression_analysis.ipynb  # trend analysis
│   ├── 05_clustering.ipynb            # cluster analysis
│   └── 06_time_series_analysis.ipynb  # trend analysis
│
├── outputs/
│   ├── figures/
│   │   ├── time_series/               # Trend plots
│   │   ├── maps/                      # Choropleth maps
│   │   ├── correlations/              # Relationship plots
│   │   └── regional/                  # Regional comparisons
│   ├── tables/
│   │   └── summary_statistics.csv     # Statistical summaries
│   └── reports/
│       └── analysis_report.html       # Interactive reports
│
├── Visualizations
│   └── config.yaml                    # Configuration parameters
│
├── requirements.txt                   # Python dependencies
├── README.md                          # Project documentation
└── .gitignore                         # Git ignore file


Implementation Details

Data Processing Steps

Data Loading & Inspection

Load WDI dataset
Check data types and missing values
Initial data quality assessment
Data Cleaning

Handle missing values using appropriate imputation
Reshape data from wide to long format
Standardize country names and codes
Filter relevant indicators and time period
Feature Engineering

Calculate growth rates
Create regional aggregates
Generate development classifications
Analytical Methods

Descriptive Statistics: Summary statistics for each indicator
Time-Series Analysis: Trend decomposition and smoothing
Geospatial Analysis: Choropleth maps using GeoPandas
Correlation Analysis: Relationship between indicators
Comparative Analysis: Regional and income group comparisons

Expected Outputs

Visualizations

Time-series plots showing trends for each indicator
Choropleth maps for geographical distribution
Scatter plots for correlation analysis
Bar charts for regional comparisons
Heatmaps for cross-country comparisons
Analytical Insights

Identification of top/bottom performing countries
Regional development patterns
Sustainable development trade-offs
Digital economy growth trajectories

Notes & Limitations

Some missing country/year data requires careful handling
Indicators rely on official national reporting with potential lags
Project is for educational purposes only
Analysis covers projected data up to 2025 (some estimates)
Regional comparisons may be affected by data availability