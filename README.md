# NYC Yellow Taxi Data Analysis (2023) 

## Project Overview

This project performs a comprehensive **Exploratory Data Analysis (EDA)** on New York City Yellow Taxi trip records from 2023. The goal is to uncover patterns in urban mobility, revenue generation, and operational bottlenecks to provide data-driven recommendations for a new taxi operator entering the market.

The analysis focuses on optimizing fleet operations, pricing strategies, and customer experience by leveraging temporal, financial, and geospatial data.

## Objectives

* **Operational Efficiency:** Identify high-demand time windows and "slow routes" caused by congestion.
* **Revenue Maximization:** Analyze fare components, tipping behaviors, and high-value pickup zones.
* **Strategic Planning:** Recommend fleet positioning strategies based on weekday/weekend and seasonal trends.

## Dataset

* **Source:** [NYC Taxi & Limousine Commission (TLC) Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page).
* **Year:** 2023
* **Format:** Parquet files (monthly).
* **Auxiliary Data:** NYC Taxi Zones Shapefiles (for geospatial mapping).

> **Note:** Due to the massive size of the raw dataset, a stratified sampling technique (5% of data per hour per day) was implemented to create a representative dataset of ~300,000 trips for analysis.

## Tech Stack

* **Python:** Core programming language.
* **Pandas & NumPy:** Data manipulation and cleaning.
* **Matplotlib & Seaborn:** Static visualizations (heatmaps, bar charts, scatter plots).
* **GeoPandas:** Geospatial analysis and mapping of taxi zones.

## Key Insights & Findings

### 1. Temporal Patterns

* **Peak Demand:** The system experiences extreme pressure during weekday evenings (**18:00 – 19:00**), particularly on Thursdays and Fridays.
* **Lowest Activity:** Demand is lowest between 3:00 AM and 5:00 AM.
* **Seasonality:** A dip in activity is observed in Jan/Feb, with recovery in Q2 and peaks in Q4.

### 2. Geographical Hotspots

* **Manhattan Dominance:** 90%+ of trips are concentrated in Manhattan, specifically **Upper East Side**, **Midtown Center**, and **Times Square**.
* **Airport Trips:** JFK and LaGuardia offer high-value fares but lower trip frequency compared to short city hops.

### 3. Financial & Operational Bottlenecks

* **Slow Routes:** Routes within Midtown Center during rush hour have average speeds <10 mph, reducing fleet turnover.
* **Tipping Behavior:** Credit card payments correlate with significantly higher tip percentages compared to cash.

## Visualizations

*The notebook includes the following visualizations:*

* Choropleth maps of Pickup/Dropoff densities.
* Heatmaps of correlation between trip distance, duration, and fare.
* Hourly and Weekly demand curves.

## How to Run

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/NYC-Taxi-Analysis.git

```

2. **Install Dependencies**
```bash
pip install pandas numpy matplotlib seaborn geopandas pyarrow

```

3. **Data Setup**
* Download 2023 Yellow Taxi Parquet files from the TLC website into a `data/` folder.
* Ensure `taxi_zones` shapefiles are in the `taxi_zones/` directory.

4. **Run the Notebook**
Open `EDA_NYC_Taxi_Analysis_Rakshith_G.ipynb` in Jupyter Notebook or Google Colab.

## Recommendations

Based on the analysis, the following strategies were proposed:

1. **Dynamic Dispatching:** Pre-allocate drivers to commercial hubs 30 minutes before the 6 PM rush.
2. **Nightlife Deployment:** Shift fleet focus from Financial District to East Village/Meatpacking District after 9 PM on weekends.
3. **Congestion Pricing:** Implement time-based surcharges for trips originating in Midtown zones with average speeds <5 mph.

## Author

**Rakshith G**

* [LinkedIn](https://www.linkedin.com/in/rakshith-g-553507214/)
* [GitHub](https://github.com/rkshthg)

---

*This project was completed as part of a Data Science curriculum focusing on EDA and Big Data handling.*
