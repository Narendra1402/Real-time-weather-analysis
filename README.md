# ⛅ Real-Time Weather Analytics – SQL Project

A robust SQL-based project to analyze and monitor real-time weather patterns across geographies, highlighting skills in data modeling, complex querying, and insight generation.

![proj_5](https://github.com/user-attachments/assets/ba56e2fe-20eb-4b39-938e-435ff90f8830)

## 🧠 Project Overview

Weather impacts nearly every aspect of daily life, from transportation and energy usage to agriculture and public safety. This project addresses the need for real-time insights into weather conditions across multiple cities and countries. It leverages structured SQL tables to support scalable querying and analytics on key climate metrics like temperature, wind speed, humidity, and more.



## 🛠️ Tools & Technologies

- **SQL** (MySQL/PostgreSQL/SQL Server – depending on environment)
- **Relational Database Design**
- **Real-Time Data Handling (Simulated or via API)**



## 🧱 Database Schema

The project consists of two main tables:

### 🌦️ Weather\_Data Table

Captures all real-time weather metrics.

| Column              | Description                                |
| ------------------- | ------------------------------------------ |
| `weather_id`        | Unique identifier for each weather record  |
| `location_id`       | Foreign key referencing `Location` table   |
| `timestamp`         | Date and time of observation               |
| `temperature`       | Temperature reading in Celsius             |
| `humidity`          | Humidity percentage                        |
| `wind_speed`        | Wind speed (km/h or m/s)                   |
| `precipitation`     | Rain/snowfall amount                       |
| `weather_condition` | Textual label (e.g., Sunny, Cloudy, Rainy) |

### 📍 Location Table

Stores geospatial details for each city.

| Column        | Description    |
| ------------- | -------------- |
| `location_id` | Primary key    |
| `city`        | City name      |
| `state`       | State/province |
| `country`     | Country        |
| `latitude`    | Geo latitude   |
| `longitude`   | Geo longitude  |



## 🧩 Key Features

- 📡 **Real-Time Data Capture**\
  Supports continuous ingestion of weather metrics (simulated/API-based).

- 📈 **Advanced Querying**\
  Identify city-level patterns, extremes, and anomalies in climate.

- 🌍 **Geospatial Integration**\
  Analyze data by geography using latitude and longitude.

- ⚙️ **Scalable Design**\
  Ready for expansion to thousands of global locations.



## 📊 Sample SQL Queries

### 1. 🔥 Average Temperature by City

```sql
SELECT l.city, AVG(w.temperature) AS avg_temperature
FROM Weather_Data w
JOIN Location l ON w.location_id = l.location_id
GROUP BY l.city;
```

### 2. 🌦️ Weather Conditions Over Time

```sql
SELECT timestamp, weather_condition, COUNT(*) AS occurrences
FROM Weather_Data
GROUP BY timestamp, weather_condition
ORDER BY timestamp;
```

### 3. 💨 Top 5 Windiest Cities

```sql
SELECT l.city, AVG(w.wind_speed) AS avg_wind_speed
FROM Weather_Data w
JOIN Location l ON w.location_id = l.location_id
GROUP BY l.city
ORDER BY avg_wind_speed DESC
LIMIT 5;
```



## 📁 Folder Structure

```
├── README.md
├── schema/
│   └── weather_schema.sql
├── scripts/
│   └── sample_queries.sql
├── images/
│   └── weather_dashboard.png
```



## 📌 Future Enhancements

- API integration with live sources like OpenWeatherMap
- Power BI/Tableau dashboard integration
- Predictive analytics using historical trends

## 🤝 Let’s Connect

📧 [your.email@example.com](mailto\:your.email@example.com)\
🔗 [LinkedIn](https://linkedin.com/in/yourprofile)\
🌐 [Portfolio](https://yourportfolio.com)



> 🌐 Turning climate data into actionable insights — one query at a time.




## 🔗 Connect With Me  
Feel free to explore more of my projects and reach out:  
- [LinkedIn](https://www.linkedin.com/in/narendrasingh1402)
- [YouTube](https://www.youtube.com/@Analyst_Hive)  
- [Portfolio](https://narendra1402.github.io/)

