# 🌪️ LAPD Crime Data Analysis & Visualization

Welcome to a detailed breakdown and exploratory data analysis (EDA) of crime data in **Los Angeles, California** — also known as the City of Angels. This project aims to extract insights from reported crime records to support the **Los Angeles Police Department (LAPD)** in understanding patterns of criminal activity and improving strategic decision-making.

---

## 📊 Dataset Overview

The dataset used in this analysis is `crimes.csv`, which includes detailed records of crimes reported in the city. Each record contains information such as:

- Date and time of occurrence (`DATE OCC`, `TIME OCC`)
- Location (`AREA NAME`)
- Victim demographics (`Vict Age`, `Vict Sex`)
- Crime description (`Crm Cd Desc`)
- Crime identifier (`DR_NO`)

---

## 🔢 Project Objectives

The LAPD has enlisted our help to address the following key questions:

1. **Which hour of the day has the highest frequency of crimes?**
2. **Which area experiences the most night crimes (between 10PM and 3:59AM)?**
3. **What is the frequency of crimes against different victim age groups?**
4. **Can we uncover deeper trends by filtering and visualizing crime by type, time, day of week, and demographic factors?**

---

## 🕒 1. Peak Crime Hour

To understand criminal behavior in relation to time, we extracted the hour from the `TIME OCC` field and plotted the number of crimes across each hour of the day.

### 🔍 Result

- The hour with the **highest number of reported crimes** is stored as:
  ```python
  peak_crime_hour = 12  # 12:00 PM
  ```

This suggests that crimes tend to peak at noon, likely due to high human activity during this time.

### 📈 Visualization
![Peak Crime Hour](https://github.com/lawren-ai/-LAPD-Crime-Data-Analysis-Visualization/blob/main/CrimeFrequenceByHourOfday.PNG)


---

## 🌆 2. Area with Highest Night Crime Frequency

We defined night crimes as those occurring between **10:00 PM and 3:59 AM**. Filtering the dataset for those hours, we analyzed which areas were hotspots.

### 🔍 Result

- The **area with the most night crimes**:
  ```python
  peak_night_crime_area = "Central"
  ```

This implies a need for increased night-time patrolling in this area.

### 📈 Visualization
![Peak Night_crime area](https://github.com/lawren-ai/-LAPD-Crime-Data-Analysis-Visualization/blob/main/Top10AreasWithMostCrimes.PNG)


---

## 🧑‍🏫 3. Victim Age Group Distribution

We categorized victims into age groups: `0-17`, `18-25`, `26-34`, `35-44`, `45-54`, `55-64`, and `65+`, then counted crime occurrences per group.

### 🔍 Result

```python
Victim Age Group Distribution:
age_group
0-17      4528
18-25    28291
26-34    47470
35-44    42157
45-54    28353
55-64    20169
65+      14747
```

Adults (26-34) and early middle-aged adults (35-44) are the most targeted, perhaps due to lifestyle exposure.

### 📈 Visualization
![Victim age group distribution]


---

## 🌀 4. Deeper Exploratory Insights

### ✨ a. Top 10 Most Common Crime Types

```python
['BATTERY - SIMPLE ASSAULT', 'BURGLARY FROM VEHICLE', 'ASSAULT WITH DEADLY WEAPON, AGGRAVATED ASSAULT', 'INTIMATE PARTNER - SIMPLE ASSAULT', 'THEFT FROM MOTOR VEHICLE - GRAND ($950.01 AND OVER)', 'VANDALISM - FELONY ($400 & OVER, ALL CHURCH VANDALISMS)', 'THEFT PLAIN - PETTY ($950 & UNDER)', 'BURGLARY', 'THEFT-GRAND ($950.01 & OVER)EXCPT,GUNS,FOWL,LIVESTK,PROD']
```
### 📈 Visualization
![Top 10 most common crimes]



### ⚔️ b. Violent vs Non-Violent Crimes

I classified crimes using keywords like `ASSAULT`, `ROBBERY`, `HOMICIDE`, etc.&#x20;

### 📈 Visualization
![Victim age group distribution]


### 🌟 c. Crime Trends by Month

Some months show spikes (e.g June) — possibly due to seasonal events or holidays.&#x20;

### 📈 Visualization
![Crime Trends by Month]


### 🌍 d. Heatmap by Hour & Day of Week

This heatmap reveals that weekdays, especially **Friday and Wednesday Afternoons**, experience heightened crime.&#x20;

### 📈 Visualization
![Heatmap by Hour & Day of Week]
---

## 📆 Tools & Libraries Used

- Python (pandas, matplotlib, seaborn)
- Jupyter Notebook for interactive development

---

## 🚀 Conclusion & Recommendations

Based on my analysis, I offer the following insights to support LAPD operations:

- Increase patrols in **high-crime hours (12PM - 1PM)**.
- Deploy night units to areas like **Central**, which experiences significant late-night activity.
- Launch awareness campaigns and community engagement for **young adults and early middle-aged adults**, the most targeted age groups.
- Monitor **weekend trends and holiday spikes** using ongoing crime feeds.

---

## 💼 Future Work

- Geospatial analysis with mapping (using `folium` or `geopandas`)
- Real-time crime prediction models
- Integrating weather, events, or socioeconomic indicators

---

## 🙏 Acknowledgements

Huge thanks to the **Los Angeles Police Department** for providing the data and their continued efforts in keeping the city safe.

> Data analysis by [Ayotunde Akinboade]. Visual storytelling powered by Python.

---

## 🌐 License

MIT License. For educational and civic use.

