# Weather Data ETL Pipeline

## Project Overview
This project is a simple ETL (Extract, Transform, Load) pipeline that pulls real-time weather data for multiple cities from the OpenWeather API, cleans and structures it using Pandas, and stores it in a CSV file for analysis. It was built as part of Week 7 of the AnalystLab Africa Data Analytics Internship (Batch B).

## Data Source
- **API:** [OpenWeather API](https://openweathermap.org/api)
- **Cities collected:** Lagos, London, New York
- **Fields retrieved:** City name, temperature, humidity, weather condition, wind speed, date and time of retrieval

## Tools Used
- Python
- Requests (API calls)
- Pandas (data cleaning and structuring)
- Jupyter Notebook

## ETL Process

### 1. Extract
Connected to the OpenWeather API using an API key and looped through a list of cities, sending a request for each and collecting the JSON response (temperature, humidity, condition, wind speed, and timestamp).

### 2. Transform
- Loaded the extracted data into a Pandas DataFrame
- Converted the `datetime` column from text to a proper datetime type
- Rounded temperature values to one decimal place
- Standardized weather condition text to title case (e.g. "overcast clouds" → "Overcast Clouds")

### 3. Load
Saved the cleaned dataset to a CSV file (`weather_data.csv`) for future analysis.

## Key Findings
- **Hottest city:** London at 28.3°C
- **Most humid city:** Lagos at 79%
- **Weather conditions:** Lagos was overcast, London had clear skies, and New York had scattered clouds

Even though London and New York had similar temperatures (28.3°C), humidity and cloud cover varied significantly across all three cities — showing that temperature alone doesn't tell the full weather story.

## What I Learned
Building this pipeline gave me hands-on experience with the full ETL cycle — connecting to a live API, handling real-world JSON responses, cleaning and structuring data with Pandas, and storing it for repeatable analysis. It reinforced how automation removes the manual, repetitive work of data collection so analysts can focus on insight generation.

## Files in This Repository
- `etl_pipeline.ipynb` — full ETL script (extract, transform, load, analysis)
- `weather_data.csv` — processed dataset
- `README.md` — project documentation
