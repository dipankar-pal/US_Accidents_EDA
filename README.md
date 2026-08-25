# US Accidents Exploratory Data Analysis (2016–2023)


An end-to-end Exploratory Data Analysis (EDA) project on the US Accidents dataset. This project cleans a large accident dataset and explores patterns in accident severity, time, weather, road features, and geographic hotspots.

# Project Objective

The goal is to find useful traffic-safety patterns that can support better monitoring, prevention planning, and a future Power BI dashboard.

Key questions answered:

. Which accident severity level is most common?

. When do accidents happen most often?

. Which weather conditions are associated with higher-severity accidents?

. Which road features are present during accidents?

. Which cities and locations are accident hotspots?

# Dataset

Dataset: US Accidents (2016–2023) 

Source: Kaggle

Size: 3 GB (7.7 million)

Country: United States

Main date column: Start_Time

Unique accident identifier: ID

The original dataset file is not included in this repository because of its large size. Download it from Kaggle and place it in the project folder before running the notebook.

Tools and Libraries

Python

Pandas

NumPy

Matplotlib

Seaborn

Jupyter Notebook

# Project Files

├── EDA_US_Accidents.ipynb                 # Complete data-cleaning and EDA notebook
├── US_Accidents_EDA_Presentation.pptx     # Presentation of key findings
├── README.md                               # Project documentation
└── US_Accidents_March23_Cleaned.csv        # Generated after running the notebook (not uploaded)

# Data Cleaning Steps

The notebook performs the following preparation steps:

Converts Start_Time and End_Time into datetime format.

Removes columns with a high amount of missing data:

Wind_Chill(F)

Precipitation(in)

End_Lat

End_Lng

Fills missing numeric values using the column mean:

Wind_Speed(mph)

Visibility(mi)

Humidity(%)

Temperature(F)

Pressure(in)

Fills categorical and time-related values using forward fill or Unknown.

Removes the Description column.

Saves the cleaned dataset as US_Accidents_March23_Cleaned.csv.

Exploratory Analysis

# 1. Severity Analysis

Severity

Accident Count

1

67,366

2

6,156,981

3

1,299,337

4

204,710

Insight: Severity 2 is the most common accident level, representing approximately 79.7% of the dataset.

# 2. Time Analysis

Accident counts are analyzed by:

Year

Month

Day of week

Hour of day

This analysis helps identify long-term trends, seasonal patterns, weekday variation, and peak accident hours.

# 3. Weather and Severity Analysis

The notebook analyzes:

High-severity accident rate by weather condition

Severity distribution by weather condition

High-severity rate by wind direction

Spearman correlation between weather variables and severity

High severity is defined as Severity 3 or Severity 4.

# 4. Road Feature Analysis

Road features analyzed include:

Traffic Signal

Crossing

Junction

Stop

Station

Railway

Give Way

No Exit

Traffic Calming

Bump

Roundabout

Key insights:

Traffic signals are present in 14.8% of accident records.

Crossings are present in 11.3% of accident records.

Junctions are present in 7.4% of accident records.

Junctions show a high-severity accident rate of approximately 26.8%.

# 5. Location and Hotspot Analysis

The project identifies:

Top accident-prone states

Top accident-prone cities

Latitude/longitude accident heatmaps

Overall accident hotspots vs. high-severity accident hotspots

Top city in the notebook output: Miami, Florida — 186,923 accidents.

Key Findings

Most records are Severity 2 accidents.

Major metropolitan areas contain a large share of reported accidents.

Accident patterns vary across year, month, weekday, and hour.

Weather should be interpreted alongside road, traffic, and location factors; correlation does not prove causation.

Junctions deserve particular attention because of their relatively high high-severity accident rate.

Comparing total hotspots with high-severity hotspots helps prioritize safety interventions.

How to Run the Project

Clone this repository:



Install the required libraries:

pip install pandas numpy matplotlib seaborn jupyter

Download the US Accidents dataset from Kaggle.

Place the dataset in the project folder and make sure the file name matches the notebook:

US_Accidents_March23.csv

Open and run the notebook:

jupyter notebook EDA_US_Accidents.ipynb

Future Improvements

Build an interactive Power BI dashboard from the cleaned dataset.

Add state- and city-level filters.

Compare accident duration using End_Time - Start_Time.

Add machine learning to predict accident severity.

Use external traffic-volume data for deeper causal analysis.

# Author

Dipankar Pal
Aspiring Data Analyst | Power BI Developer
Skills: Power BI, SQL Server, Python, Pandas, DAX, Power Query and Data Visualization

If you found this project useful, please consider giving the repository a star.
