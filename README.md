# 🚕 Chicago Taxi Market Analysis | SQL, Python & Statistical Insights

### Exploring Taxi Market Competition, Popular Destinations, and Weather-Related Travel Patterns

**Python • Pandas • Matplotlib • SciPy • Exploratory Data Analysis • Hypothesis Testing**

## 📌 Project Overview

Understanding transportation patterns is essential for evaluating market competition, identifying high-demand locations, and improving urban mobility services.

This project analyzes taxi trip data from Chicago to investigate the distribution of rides among taxi companies, identify popular drop-off locations, and evaluate whether weather conditions are associated with differences in trip duration.

The analysis combines exploratory data analysis, visualizations, and statistical hypothesis testing to generate insights from transportation data.

## 🎯 Project Objectives

- Identify the leading taxi companies in Chicago.
- Analyze the distribution of rides across taxi operators.
- Determine the 10 neighborhoods with the highest average number of drop-offs.
- Explore the concentration of taxi activity across different areas.
- Compare trip durations under different weather conditions.
- Test whether rainy weather is associated with statistically significant differences in trip duration.

## 🛠️ Technologies Used

| Technology | Application |
|---|---|
| Python | Data processing and analysis |
| Pandas | Data exploration and transformation |
| Matplotlib | Data visualization |
| SciPy | Statistical hypothesis testing |
| Jupyter Notebook | Analysis and documentation |

The project belongs to a learning module involving SQL-based data extraction. The provided notebook focuses on analyzing the resulting CSV datasets using Python.

## 📂 Dataset Description

Three datasets were used in the analysis.

### 1. Taxi Companies — `project_sql_result_01.csv`

Contains taxi company names and their corresponding number of trips.

- `company_name` — Taxi company name
- `trips_amount` — Number of rides

### 2. Drop-off Locations — `project_sql_result_04.csv`

Contains average taxi trips by destination neighborhood.

- `dropoff_location_name` — Destination neighborhood
- `average_trips` — Average number of trips

### 3. Trip Duration and Weather — `project_sql_result_07.csv`

Contains information about Saturday trips between the Loop and O'Hare International Airport.

- `start_ts` — Trip start date and time
- `weather_conditions` — Weather classification
- `duration_seconds` — Trip duration in seconds

## 🔍 Data Preparation

The preparation process included:

1. Loading the CSV datasets with Pandas.
2. Inspecting dataset dimensions and data types.
3. Checking for missing values.
4. Identifying duplicate records.
5. Converting trip timestamps to datetime format.
6. Sorting taxi companies and neighborhoods by ride volume.
7. Separating trip durations by weather conditions for statistical testing.

The inspection identified 197 duplicate rows in the trip-duration dataset. These were reported during data exploration.

## 📊 Exploratory Data Analysis

### Taxi Company Performance

The analysis revealed that taxi activity was concentrated among a relatively small number of operators.

**Top companies by trip volume:**

| Taxi Company | Number of Trips |
|---|---:|
| Flash Cab | 19,558 |
| Taxi Affiliation Services | 11,422 |
| Medallion Leasing | 10,367 |
| Yellow Cab | 9,888 |
| Taxi Affiliation Service Yellow | 9,299 |

**Key Insight:** Flash Cab recorded the highest number of trips in the analyzed data, suggesting a strong market presence.

### Most Popular Drop-off Locations

The analysis identified the neighborhoods with the highest average number of taxi drop-offs.

| Neighborhood | Average Trips |
|---|---:|
| Loop | 10,727.47 |
| River North | 9,523.67 |
| Streeterville | 6,664.67 |
| West Loop | 5,163.67 |
| O'Hare | 2,546.90 |

**Key Insight:** The Loop and River North were among the busiest destinations, reflecting a concentration of taxi activity in important urban areas.

## 🧪 Statistical Hypothesis Testing

### Research Question

**Does the average duration of Saturday taxi trips from the Loop to O'Hare International Airport differ between rainy and non-rainy weather conditions?**

### Hypotheses

**Null Hypothesis (H₀):** Average trip durations are equal under rainy and non-rainy conditions.

**Alternative Hypothesis (H₁):** Average trip durations differ between the two weather conditions.

### Methodology

An independent two-sample t-test was performed.

The analysis included:

- Separating trips into `Bad` and `Good` weather groups.
- Calculating sample variances.
- Using a t-test with unequal variances (Welch's t-test).
- Evaluating statistical significance at α = 0.05.

### Results

| Metric | Result |
|---|---|
| Significance level | 0.05 |
| Rainy-weather variance | 520,294.09 |
| Good-weather variance | 576,382.01 |
| p-value | 6.74 × 10⁻¹² |
| Statistical decision | Reject H₀ |

### Interpretation

The p-value was substantially below the significance threshold of 0.05.

Therefore, the analysis found a **statistically significant difference in average trip duration** between the two weather groups.

This result establishes an association in the analyzed sample, but does not independently demonstrate that weather conditions caused the difference.

## 💡 Key Findings

- Taxi activity was concentrated among a limited number of companies.
- Flash Cab recorded the highest trip volume in the analyzed dataset.
- The Loop and River North were among the most frequent drop-off destinations.
- Trip durations differed significantly between the two weather groups.
- Exploratory analysis and statistical testing provided complementary insights into Chicago's taxi market.

## ⚠️ Limitations

- The analysis relies on aggregated taxi-company and neighborhood datasets.
- The weather comparison focuses on a specific route and day of the week.
- Duplicate records were identified in the trip dataset and may require additional investigation.
- Other factors, such as traffic congestion and departure time, may affect trip duration.
- Statistical significance does not establish causation.

## 🚀 How to Run the Project

1. Clone or download the repository.
2. Install the required Python libraries.
3. Place the three CSV datasets in a local `data/` directory.
4. Update the dataset paths in the notebook.
5. Open the notebook in Jupyter Notebook or JupyterLab.
6. Execute the cells sequentially.

Install the dependencies:

```bash
pip install pandas matplotlib scipy notebook
```

## 📈 Conclusion

This project demonstrates how exploratory data analysis and statistical hypothesis testing can be used to understand transportation market dynamics.

The findings highlight market concentration among taxi companies, the importance of major urban destinations, and statistically significant differences in trip durations across weather conditions.

The project showcases practical skills in Python, data visualization, data validation, and statistical reasoning.

## 👩‍💻 Author

**Andressa Cruz Miranda**

Computer Science | Data Analytics | Python | Statistical Analysis

[GitHub Profile](https://github.com/Andressa202)

*Developed as part of the TripleTen Data Science program.*
