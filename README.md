Here's the README with enhanced formatting for GitHub:

---

# Real-Time Weather Monitoring System

This real-time data processing application monitors weather conditions in major Indian metro cities and provides summarized insights using rollups and aggregates. Built using **Python** and **SQLite3**, this system retrieves data from the **OpenWeatherMap API**, processes it to generate daily summaries, and triggers alerts based on configurable thresholds. The application also includes visualizations to display historical weather trends and alerts.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup & Installation](#setup--installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Testing](#testing)
- [Future Enhancements](#future-enhancements)

## Features
1. **Continuous Weather Data Retrieval**: Fetches real-time weather data from the OpenWeatherMap API at configurable intervals.
2. **Daily Weather Summary Rollup**: Summarizes daily weather data, including average, maximum, minimum temperatures, and dominant weather conditions.
3. **Alert Thresholds**: Allows users to set thresholds for temperature or specific weather conditions. Alerts are triggered if these thresholds are breached.
4. **Visualization**: Displays daily summaries, historical weather trends, and alerts for easy monitoring.

## Technologies Used
- **Python**: Chosen for its versatility and extensive libraries for data processing and API handling.
- **SQLite3**: A lightweight database, ideal for local storage of daily weather summaries and alerts.
- **Matplotlib** / **Seaborn**: For creating visualizations of weather trends and triggered alerts.
- **Requests**: For API calls to OpenWeatherMap to retrieve live weather data.

## Setup & Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/Real-Time-Weather-Monitoring.git
   cd Real-Time-Weather-Monitoring
   ```

2. **Install Requirements**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Get an OpenWeatherMap API Key**:
   - Sign up at [OpenWeatherMap](https://openweathermap.org/) and get your free API key.

4. **Set up Environment Variables**:
   - Create a `.env` file in the project root and add your API key:
     ```plaintext
     API_KEY=your_openweather_api_key
     ```

## Usage
1. **Run the Application**:
   ```bash
   python main.py
   ```

2. **Access Summaries & Alerts**:
   - Daily summaries and triggered alerts can be viewed in the database or in the console, based on configurations.

3. **View Visualizations**:
   - Graphical representations of daily weather summaries, trends, and alerts are available within the app.

## Configuration
- **Polling Interval**: Set the frequency of API calls in seconds (default is 300 seconds, or 5 minutes).
- **Alert Thresholds**: Define custom thresholds for temperature or weather conditions (e.g., alert if the temperature exceeds 35°C for two consecutive updates).
  
Configuration is managed in `config.json`:
```json
{
  "interval_seconds": 300,
  "temperature_threshold": 35
}
```

## Testing
1. **System Setup**:
   - Verify the system connects to OpenWeatherMap using a valid API key.

2. **Data Retrieval Simulation**:
   - Simulate API calls at different intervals and verify correct data parsing.

3. **Temperature Conversion**:
   - Ensure Kelvin to Celsius (or Fahrenheit) conversions work as expected.

4. **Daily Weather Summary Rollup**:
   - Verify daily summaries for correctness in averages, max/min temperatures, and dominant weather conditions.

5. **Alert Thresholds**:
   - Test threshold configuration and simulate weather data to confirm alerts trigger when expected.

## Future Enhancements
- **Extended Weather Parameters**: Support additional data points (humidity, wind speed).
- **Multi-City Support**: Extend to other cities or allow user-defined cities.
- **Email Notifications**: Implement email alert functionality.

## Why These Technologies?
- **Python**: Efficient for real-time data processing and well-supported libraries for API interaction and data handling.
- **SQLite3**: Lightweight, portable database suitable for managing persistent weather data and alert history.
- **Matplotlib/Seaborn**: Provides powerful visualization capabilities to track weather trends visually.

---

Feel free to adjust configurations and contribute to the project!
