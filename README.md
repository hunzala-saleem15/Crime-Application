# Crime Hotspot Predictor & Safety Analytics – São Paulo, Brazil

A data-driven crime analysis and prediction project focused on identifying crime hotspots, understanding crime patterns, and enhancing public safety. This phase emphasizes data cleaning and exploratory data analysis (EDA) using the Brazil Crime Dataset from São Paulo.

---

## Project Overview

Crime rates are increasing in many metropolitan areas, including São Paulo. This project leverages historical crime data to:

- Clean and structure inconsistent raw crime reports
- Explore crime patterns through visual and statistical analysis
- Identify high-risk locations and time periods
- Provide insights into demographic vulnerabilities
- Lay the foundation for predictive models and city safety rankings

---

## Data Cleaning

The raw dataset presented several challenges:

- Inconsistent formats (dates, text fields)
- Missing values across multiple municipalities
- Redundant or irrelevant fields
- Duplicates and spatial outliers

### Cleaning Steps

- Parsed and standardized `DATA_OCORRENCIA_BO` and `HORA_OCORRENCIA_BO` into proper datetime objects
- Removed rows with null `LATITUDE` or `LONGITUDE` for location-based analysis
- Cleaned categorical values: normalized strings in `CIDADE`, `RUBRICA`, `DESCR_TIPO_BO`
- Filtered inconsistent reports (e.g. entries without `NUM_BO`)
- Handled and documented missing demographic data (`SEXO_PESSOA`, `IDADE_PESSOA`, `COR_CUTIS`)

**Libraries used:** Pandas, NumPy, Regex

---

## Exploratory Data Analysis (EDA)

EDA provided insights into crime frequency, geographic distribution, time trends, and demographic effects.

### Key Findings

1. **Top Cities by Crime Count**
   - São Paulo city had the highest number of reports
   - Outskirts showed underreporting due to data collection delays

2. **Crime Over Time**
   - Crimes peaked during late evenings and weekends
   - December recorded a noticeable increase in crime incidents

3. **Crime by Type**
   - Most frequent: Theft, Assault, and Domestic Violence
   - Less frequent but severe: Armed Robbery, Homicide

4. **Location Risk Analysis**
   - High-risk zones included major transit and commercial areas
   - Residential zones showed moderate but consistent activity

5. **Demographic Impact**
   - Males were more commonly recorded as victims and suspects
   - Young adults (18–29) were the most affected
   - Ethnicity data had gaps, limiting conclusive analysis

**Libraries used:** Seaborn, Matplotlib, GeoPandas, Plotly

---

## Dataset Summary

**Source:** [Kaggle - Crime Data in Brazil](https://www.kaggle.com/datasets/inquisitivecrow/crime-data-in-brazil)

- Format: CSV
- Records: 800,000+
- Region: Greater São Paulo
- Key columns:
  - `DATA_OCORRENCIA_BO`, `HORA_OCORRENCIA_BO`
  - `CIDADE`, `LATITUDE`, `LONGITUDE`
  - `DESCR_TIPO_BO`, `FLAG_STATUS`
  - `SEXO_PESSOA`, `IDADE_PESSOA`, `COR_CUTIS`

---

## Future Directions

Although this phase focused on data preparation and EDA, future extensions of this project include:

- Hotspot Detection using K-Means Clustering
- Time-Series Forecasting (ARIMA, LSTM)
- Crime Prediction with Logistic Regression
- Safety Scoring and City Rankings
- Mobile App integration for public safety alerts and recommendations

---

## Tech Stack

**Programming Language:** Python

**Libraries & Tools:**
- Data Manipulation: Pandas, NumPy
- Visualization: Matplotlib, Seaborn, Plotly, GeoPandas, Folium
- Mapping APIs: Google Maps, OpenStreetMap
- Machine Learning (for future use): Scikit-learn, TensorFlow, Statsmodels

---

## Project Zip File

You can download the project zip file from OneDrive using the following link:

[Download Project.zip from OneDrive](https://drive.google.com/drive/folders/1a0VObBuMwgq9BtDAiAT28Eu3ven_Dbl0?usp=sharing)

---

## References

- Dataset: [Crime Data in Brazil – Kaggle](https://www.kaggle.com/datasets/inquisitivecrow/crime-data-in-brazil)
- Mapping tools: Google Maps API, OpenStreetMap

---
