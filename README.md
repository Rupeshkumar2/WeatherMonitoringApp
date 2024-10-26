# Real-Time Weather Monitoring System

This real-time data processing application monitors weather conditions in major Indian metro cities and provides summarized insights using rollups and aggregates. Built using **Python** and **SQLite3**, this system retrieves data from the **OpenWeatherMap API**, processes it to generate daily summaries, and triggers alerts based on configurable thresholds. The application also includes visualizations to display historical weather trends and alerts.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup & Installation](#setup--installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Testing](#testing)
- [Additional Features](#additional-features)
- [Project Standards](#project-standards)

## Features
1. **Continuous Weather Data Retrieval**: Fetches real-time weather data from the OpenWeatherMap API at configurable intervals.
![image](https://github.com/user-attachments/assets/650d95e8-d344-428f-8734-9bb1939bb747)
2. **Daily Weather Summary Rollup**: Summarizes daily weather data, including average, maximum, minimum temperatures, and dominant weather conditions.
![image](https://github.com/user-attachments/assets/f6ce0ea3-9032-4818-82ac-b9b4420e8bcc)
3. **Alert Thresholds**: Allows users to set thresholds for temperature or specific weather conditions. Alerts are triggered if these thresholds are breached.
4. **Visualization**: Displays daily summaries, historical weather trends, and alerts for easy monitoring.
![image](https://github.com/user-attachments/assets/bed354ec-b507-4b20-aa61-ba3470f174c5)


## Technologies Used
- **Python**: Chosen for its versatility and extensive libraries for data processing and API handling.
- **SQLite3**: A lightweight database, ideal for local storage of daily weather summaries and alerts.
- **Matplotlib**: For creating visualizations of weather trends and triggered alerts.
- **Requests**: For API calls to OpenWeatherMap to retrieve live weather data.

## Setup & Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Rupeshkumar2/WeatherMonitoringApp
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

## Additional Features
- **Extended Weather Parameters**: Supports additional data points (humidity, wind speed).
- **Multi-City Support**: Extended to other cities or allow user-defined cities.
- **Email Notifications**: Email alert functionality.

## Project Standards
* **System Functionality**: Completeness and accuracy in monitoring weather conditions, processing data in real-time, and reliably triggering alerts.
* **Data Handling Precision**: Correctness in parsing API data, converting temperature units, and computing daily rollups and aggregates.
* **Performance Efficiency**: Effective data retrieval and processing within designated time intervals to maintain responsiveness.
* **Test Coverage**: Inclusion of comprehensive test cases that validate functionality across diverse weather conditions and user-defined configurations.
* **Code Quality and Documentation**: Clarity, modularity, and maintainability of the codebase, with thorough documentation for setup and usage instructions.
