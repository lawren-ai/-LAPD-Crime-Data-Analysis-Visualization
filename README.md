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
  peak_crime_hour = 14  # 2:00 PM
  ```

This suggests that crimes tend to peak during the afternoon, likely due to high human activity during this time.

### 📈 Visualization



---

## 🌆 2. Area with Highest Night Crime Frequency

We defined night crimes as those occurring between **10:00 PM and 3:59 AM**. Filtering the dataset for those hours, we analyzed which areas were hotspots.

### 🔍 Result

- The **area with the most night crimes**:
  ```python
  peak_night_crime_location = "77th Street"
  ```

This implies a need for increased night-time patrolling in this area.

### 📈 Visualization



---

## 🧑‍🏫 3. Victim Age Group Distribution

We categorized victims into age groups: `0-17`, `18-25`, `26-34`, `35-44`, `45-54`, `55-64`, and `65+`, then counted crime occurrences per group.

### 🔍 Result

```python
victim_ages =
0-17      8573
18-25    20345
26-34    19221
35-44    16012
45-54    12320
55-64     7520
65+       3890
Name: age_group, dtype: int64
```

Young adults (18-25) and adults (26-34) are the most targeted, perhaps due to lifestyle exposure.

### 📈 Visualization



---

## 🌀 4. Deeper Exploratory Insights

### ✨ a. Top 10 Most Common Crime Types

```python
['BATTERY - SIMPLE ASSAULT', 'VEHICLE - STOLEN', 'BURGLARY FROM VEHICLE', ...]
```



### 👩👨 b. Crimes by Gender

Males and females are almost equally targeted, with slightly more male victims.&#x20;

### ⚔️ c. Violent vs Non-Violent Crimes

We classified crimes using keywords like `ASSAULT`, `ROBBERY`, `HOMICIDE`, etc.&#x20;

### 🌟 d. Crime Trends by Month

Some months show spikes — possibly due to seasonal events or holidays.&#x20;

### 🌍 e. Heatmap by Hour & Day of Week

This heatmap reveals that weekdays, especially **Friday afternoons**, experience heightened crime.&#x20;

---

## 📆 Tools & Libraries Used

- Python (pandas, matplotlib, seaborn)
- Jupyter Notebook for interactive development

---

## 🚀 Conclusion & Recommendations

Based on our analysis, we offer the following insights to support LAPD operations:

- Increase patrols in **high-crime hours (2PM - 4PM)**.
- Deploy night units to areas like **77th Street**, which experiences significant late-night activity.
- Launch awareness campaigns and community engagement for **youths and young adults**, the most targeted age groups.
- Monitor **weekend trends and holiday spikes** using ongoing crime feeds.

---

## 💼 Future Work

- Geospatial analysis with mapping (using `folium` or `geopandas`)
- Real-time crime prediction models
- Integrating weather, events, or socioeconomic indicators

---

## 🙏 Acknowledgements

Huge thanks to the **Los Angeles Police Department** for providing the data and their continued efforts in keeping the city safe.

> Data analysis by [Your Name]. Visual storytelling powered by Python.

---

## 🌐 License

MIT License. For educational and civic use.

