📊 Los Angeles Crime Data Analysis

![ProjectOverview](../Images/la_crime.png)

📌 Objective

The goal of this project is to perform Exploratory Data Analysis (EDA) on crime data from Los Angeles to uncover patterns, trends, and insights related to crime occurrences over time, victim demographics, and weapon usage.

📂 Dataset Overview

The dataset contains records of reported crimes in Los Angeles, including:

Date reported and date occurred
Victim demographics (age, gender, etc.)
Crime type and description
Weapon used
Location details
🧹 Data Cleaning & Preprocessing
🔄 Date Conversion

Converted date columns from object type to datetime format for time-based analysis:

Date Rptd
DATE OCC
🕒 Feature Engineering

Extracted useful time-based features:

Year
(Optional: Month, Day for deeper analysis)
🧼 Handling Missing Values
Missing values in Weapon Desc replaced with "No Weapon"
Removed invalid entries where Vict Age <= 0
📈 Exploratory Data Analysis (EDA)
📅 Crimes Over Time

Analyzed crime trends by year to identify:

Growth or decline in crime rates
Any unusual spikes or drops

👉 Insight:

Crime trends generally show fluctuations across years, indicating possible seasonal or socio-economic influences.
👤 Victim Demographics

Examined victim-related data:

Age distribution
Gender-based patterns

👉 Insight:

Certain age groups are more frequently targeted
Potential patterns based on vulnerability or exposure
🔫 Weapon Usage Analysis

Studied how weapons are used in crimes:

Frequency of weapon types
Proportion of crimes involving weapons vs. no weapons

👉 Insight:

A significant number of crimes involve no weapon
Certain weapon types dominate violent crimes
🗺️ Crime Distribution

Analyzed how crimes vary across:

Locations
Crime categories

👉 Insight:

Some areas have consistently higher crime density
Certain crime types are location-specific
📊 Key Findings
Crime trends vary year by year, with noticeable fluctuations
Victim age plays a significant role in crime exposure
Many crimes occur without weapons, but weapon-related crimes are more severe
Geographic distribution highlights crime hotspots