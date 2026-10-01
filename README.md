# WeatherWave

WeatherWave is a weather dashboard project developed using Java Swing and a web interface. The application uses the OpenWeatherMap API to display current weather information, forecasts, air conditions, and other weather details.

The project contains two versions:

* Java Swing desktop application
* Web-based weather dashboard

## Features

### Java Desktop Application

* Search weather information by city
* Display current temperature and weather condition
* Change temperature between Celsius and Fahrenheit
* Show hourly weather information
* Show a 5-day weather forecast
* Display air condition information
* Display pressure and dew point
* Show sunrise and sunset times
* Weather icons
* Simple dark-themed user interface

### Web Application

* Search for weather information by city
* City search suggestions
* Use browser location to get weather information
* Display current weather and forecast information
* Save recent searches in the browser
* Weather-based background changes
* Responsive design for desktop and mobile screens

## Technologies Used

### Desktop Application

* Java
* Java Swing
* OpenWeatherMap API
* JSON library

### Web Application

* HTML5
* CSS3
* JavaScript
* OpenWeatherMap API
* Browser Local Storage
* Browser Geolocation API

## Project Structure

```text
WeatherWave/
│
├── src/
│   └── weatherdashboard/
│       ├── Main.java
│       │
│       ├── config/
│       │   ├── ApiConfig.java
│       │   └── UITheme.java
│       │
│       ├── model/
│       │   ├── WeatherData.java
│       │   ├── HourlyForecast.java
│       │   ├── DailyForecast.java
│       │   └── AirConditions.java
│       │
│       ├── service/
│       │   ├── WeatherApiService.java
│       │   └── IconLoaderService.java
│       │
│       ├── ui/
│       │   ├── ModernCard.java
│       │   ├── WeatherDashboardFrame.java
│       │   └── components/
│       │       ├── HeaderPanel.java
│       │       ├── SearchPanel.java
│       │       ├── CurrentWeatherPanel.java
│       │       ├── HourlyForecastPanel.java
│       │       ├── AirConditionsPanel.java
│       │       └── FiveDayForecastPanel.java
│       │
│       └── util/
│           ├── DateTimeUtil.java
│           └── WeatherMathUtil.java
│
├── web/
│   ├── index.html
│   ├── app.js
│   └── styles.css
│
├── lib/
│   └── json-20240303.jar
│
├── package.json
└── README.md
```

## Requirements

Before running the project, make sure the following are installed:

* Java JDK
* A web browser
* Internet connection
* OpenWeatherMap API key

For the Java application, the JSON library included in the `lib` folder is also required.

## Running the Java Application

### Using Windows Batch File

The easiest way to run the desktop application on Windows is to double-click:

```text
run.bat
```

### Using PowerShell

You can also run:

```powershell
.\run.ps1
```

### Running Manually

Compile the Java source files:

```bash
javac -cp "lib/json-20240303.jar" -d out src/weatherdashboard/*.java src/weatherdashboard/*/*.java src/weatherdashboard/*/*/*.java
```

Then run the application:

```bash
java -cp "out;lib/json-20240303.jar" weatherdashboard.Main
```

## Running the Web Application

The web application is located inside the `web` folder.

You can open:

```text
web/index.html
```

directly in a browser.

Alternatively, if a local web server is configured, you can run:

```bash
npm start
```

or:

```bash
npx serve web
```

Then open the address shown by the server in your browser.

## API Configuration

WeatherWave uses the OpenWeatherMap API to get weather data.

If you want to use your own API key, update the API key in the following files:

### Java Application

```text
src/weatherdashboard/config/ApiConfig.java
```

### Web Application

```text
web/app.js
```

**Note:** API keys should not be uploaded to a public GitHub repository. If the project is going to be published on GitHub, it is better to keep the API key outside the source code and use environment variables or another secure configuration method.

## Main Parts of the Project

The Java application is divided into several parts to keep the code organized.

* **config** - Contains API and UI configuration.
* **model** - Contains classes used to store weather data.
* **service** - Handles API requests and weather icons.
* **ui** - Contains the Swing interface and its components.
* **util** - Contains utility methods for date, time, and weather calculations.
* **web** - Contains the HTML, CSS, and JavaScript version of the application.

## 👨‍💻 Author

**S.D Nuwan Tharanga**
---

## 📄 License


This project is intended for educational and academic use.
