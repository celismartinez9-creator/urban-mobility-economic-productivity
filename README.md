# Urban Mobility & Economic Productivity in Latin America

## 📌 Context
As a data analyst, the goal is to evaluate how urban mobility (traffic congestion, delays) relates to economic productivity (GDP per capita) across major Latin American cities, in order to identify where investment in transport infrastructure could have the biggest impact.

## 🎯 Objective
- Identify cities with high congestion and low economic productivity
- Identify cities with the best combined indicators (efficient mobility + strong economy)
- Determine which variables show the strongest relationship with urban development

## 🗂️ Data
- **TomTom Traffic Index** — real-time and historical traffic congestion data
- **OECD Cities** — GDP per capita, unemployment, and population data
- **Coverage:** 15 cities across 7 Latin American countries, year 2024

## 🛠️ Tools
Python · Pandas · NumPy · Seaborn · Matplotlib · Jupyter Notebook

## 🔍 Methodology
1. Data cleaning: standardized column names to snake_case, converted date and numeric fields (handling European-style decimal separators)
2. Filtered records to year 2024 using explicit `.copy()` to avoid modifying source data
3. Aggregated traffic metrics by city-year (mean values)
4. Merged traffic and economic datasets using an inner join on city and year
5. Visual validation: boxplot (outlier detection), histogram (GDP distribution), and comparative bar charts

## 📊 Key Findings
- **No direct correlation** between GDP per capita and traffic congestion across the region
- **Montevideo** has the highest GDP per capita but exceptionally low congestion
- **Mexico City** shows the highest congestion in the dataset, despite having the second-highest GDP per capita
- **Bogotá and Santiago de Chile** show high congestion combined with lower GDP — a distinct pattern worth investigating
- Population size correlates more consistently with congestion than GDP does
- An outlier was flagged in Mexico City (delay value of 2833.05), noted as requiring data validation

## 💡 Recommendations
- **Invest in road infrastructure in Bogotá and Santiago de Chile** — both are highly populated with growth potential tied to improved mobility
- **Study Buenos Aires as a benchmark** — high population, strong GDP, and moderate congestion suggest effective infrastructure management
- **Validate the Mexico City outlier** before using it in further analysis, to rule out data collection errors

## 📁 Repository Structure
```
├── data/
│   └── ladb_mobility_economy_2024_clean.csv
├── notebooks/
│   └── mobility_economy_analysis.ipynb
├── files/
│   ├── boxplot_jams_delay.png
│   ├── histogram_gdp_capita.png
│   ├── population_by_city.png
│   └── congestion_vs_gdp_by_city.png
└── README.md
```
