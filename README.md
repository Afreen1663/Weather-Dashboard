# Simple Weather App

A simple weather application built using HTML, CSS, and JavaScript. The app uses the OpenWeather API to fetch real-time weather data based on the city entered by the user.

<img width="784" alt="Image" src="https://github.com/user-attachments/assets/4d909d45-e9e7-4163-a5a6-bbaa72b1fb8f" />

## Live Demo
Website Link: https://afreen1663.github.io/Weather-Dashboard/
## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [API Integration](#api-integration)
- [How It Works](#how-it-works)
- [Results](#results)

## Overview

The Simple Weather App provides users with real-time weather information by entering the name of a city. It displays the current temperature, weather conditions, and temperature range (high/low) for the day.  

## Features

- Real-time weather information using the OpenWeather API
- Dynamic display of city name, temperature, weather conditions, and date
- Clean and responsive user interface

## Technologies Used

- HTML
- CSS
- JavaScript
- OpenWeather API

## API Integration
You can get your API by signing up with OpenWeather.
The app uses the OpenWeather API with the following API endpoint:

```bash
https://api.openweathermap.org/data/2.5/weather?q={city_name}&units=metric&APPID={API_key}
```

- **API Key**: The app uses an API key from OpenWeather.
- **Units**: Data is fetched in metric units (°C).

## How It Works

1. The user types the city name in the search box and presses `Enter`.
2. The app sends a request to the OpenWeather API using `fetch()`.
3. The API returns the weather data in JSON format.
4. The app dynamically updates the DOM to display the city, temperature, weather conditions, and high/low temperatures.

### Code for API Call:
```javascript
fetch(`${api.base}weather?q=${query}&units=metric&APPID=${api.key}`)
  .then(weather => weather.json())
  .then(displayResults);
```

## Results

The app displays:

- **City and Country**: Displays the name of the city and its corresponding country.
- **Date**: The current date in a formatted style.
- **Temperature**: Displays the current temperature in Celsius.
- **Weather Condition**: General description of the weather (e.g., Clear, Rain, Clouds).
- **High/Low Temperature**: Displays the minimum and maximum temperatures for the day.

This Simple Weather App is a great starting point for learning how to integrate APIs into web applications using JavaScript.
