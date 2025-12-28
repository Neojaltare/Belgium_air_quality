# Belgium Air Quality Monitor 🌍

Real-time air quality monitoring dashboard for Belgian cities using OpenAQ data.

## Overview

This project processes live air quality measurements from OpenAQ and displays 3-hour rolling averages across Belgian cities on an interactive map.

## Features

- 📊 Real-time data processing from OpenAQ via SQS
- 🗺️ Interactive map visualization with color-coded air quality levels
- 📍 City-level aggregation across multiple monitoring stations
- ⏱️ 3-hour rolling averages for all pollutants (PM2.5, PM10, NO2, O3, CO, SO2)
- 🔄 Auto-refresh every 5 minutes

## Architecture
```
OpenAQ → SNS → SQS → Lambda (Processor) → DynamoDB → Lambda (API) → Web Dashboard
```

## Tech Stack

- **Backend**: AWS Lambda (Python), DynamoDB, SQS
- **Frontend**: Leaflet.js, vanilla JavaScript
- **Data Source**: OpenAQ

## Live Demo

🔗 [View Dashboard](https://neojaltare.github.io/belgium-air-quality/)

## Air Quality Index

- 🟢 **Good** (0-12 µg/m³)
- 🟡 **Moderate** (12-35 µg/m³)
- 🟠 **Unhealthy for Sensitive Groups** (35-55 µg/m³)
- 🔴 **Unhealthy** (55-150 µg/m³)
- 🟣 **Very Unhealthy** (150+ µg/m³)

## Local Development

1. Update the API URL in `index.html` (line 258)
2. Open `index.html` in a browser

## License

MIT