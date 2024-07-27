### Real-Time Weather Analytics Project

#### Overview
![proj_5](https://github.com/user-attachments/assets/ba56e2fe-20eb-4b39-938e-435ff90f8830)

Welcome to my Real-Time Weather Analytics project! This project aims to provide real-time insights into weather patterns and conditions across various locations. Using SQL, I have structured a comprehensive database that allows for efficient querying and analysis of weather data. The project showcases my ability to work with real-time data, perform complex queries, and generate meaningful insights.

#### Project Description

The Real-Time Weather Analytics project consists of two main tables:

1. **Weather Data**
2. **Location**

##### Weather Data Table

The Weather Data table contains detailed information about weather conditions. Key columns include:

- `weather_id`: Unique identifier for each weather record.
- `location_id`: Foreign key referencing the Location table.
- `timestamp`: The date and time when the weather data was recorded.
- `temperature`: The temperature at the given time and location.
- `humidity`: The humidity percentage.
- `wind_speed`: The speed of the wind.
- `precipitation`: The amount of precipitation.
- `weather_condition`: A textual description of the weather (e.g., sunny, cloudy, rainy).

##### Location Table

The Location table holds information about the geographical locations where the weather data is collected. Key columns include:

- `location_id`: Unique identifier for each location.
- `city`: The name of the city.
- `state`: The name of the state.
- `country`: The name of the country.
- `latitude`: The latitude coordinate of the location.
- `longitude`: The longitude coordinate of the location.

#### Key Features

- **Real-Time Data Ingestion**: Continuously updated weather data to ensure real-time analysis.
- **Comprehensive Data Analysis**: Ability to query and analyze weather patterns, trends, and anomalies.
- **Geospatial Insights**: Integration of geographical data for location-based weather analysis.
- **Scalability**: Designed to handle large volumes of data efficiently.

#### SQL Queries

Here are some examples of SQL queries that can be performed on this dataset:

1. **Average Temperature by City**:
    ```sql
    SELECT l.city, AVG(w.temperature) as avg_temperature
    FROM Weather_Data w
    JOIN Location l ON w.location_id = l.location_id
    GROUP BY l.city;
    ```

2. **Weather Conditions Over Time**:
    ```sql
    SELECT timestamp, weather_condition, COUNT(*) as occurrences
    FROM Weather_Data
    GROUP BY timestamp, weather_condition
    ORDER BY timestamp;
    ```

3. **Top 5 Windiest Cities**:
    ```sql
    SELECT l.city, AVG(w.wind_speed) as avg_wind_speed
    FROM Weather_Data w
    JOIN Location l ON w.location_id = l.location_id
    GROUP BY l.city
    ORDER BY avg_wind_speed DESC
    LIMIT 5;
    ```

#### Conclusion

This Real-Time Weather Analytics project demonstrates my skills in SQL, data analysis, and handling real-time data. The project not only provides valuable insights into weather patterns but also serves as a robust foundation for future enhancements and integrations.

Feel free to explore the code, and I'm open to any feedback or suggestions for improvement!

---



Thank you for checking out my project!

---

**Narendra Singh**  
Data Analyst  
[LinkedIn](https://www.linkedin.com/in/narendra-singh)  
Email: narendra.1402@yahoo.com
