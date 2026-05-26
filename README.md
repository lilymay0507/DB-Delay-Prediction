# DB Delay Prediction Dataset

Dataset for wild benchmarking ML engineering agents on realistic train delay prediction tasks, collected via Deutsche Bahn API and DWD weather API.

## Data Sources
- **Deutsche Bahn Timetables and StaDa API** - (https://data.deutschebahn.com/opendata)
- **DWD (Deutscher Wetterdienst)** - (https://wetterdienst.readthedocs.io/en/latest/)

## Dataset Structure
```
dataset/
├── DB/
│   ├── berlin_station_schema.json     # OpenAPI schema for station data
│   ├── timetables_schema.json         # OpenAPI schema for timetables
│   ├── stations/
│   │   └── berlin_stations.json       # Metadata for 133 Berlin train stations
│   ├── timetable_changes/             # Real-time changes, collected every 10 minutes
│   │   └── YYYYMMDD_HHMMSS/
│   │       └── {evaNo}.xml
│   └── timetable_plan/                # Planned timetables, collected once per hour
│       └── YYYYMMDD_HHMMSS/
│           └── {evaNo}.xml
└── weather/
    ├── weather_stations_metadata.csv  # Metadata for 64 DWD weather stations
    └── {stationId}_{name}.csv         # Hourly weather data per station
```
## Key Features
- 133 Berlin train stations with EVA numbers and geographic coordinates
- Train planned timetables + real-time changes (delays, cancellations, disruptions)
- Weather data: temperature, precipitation, wind speed/direction
- 64 DWD weather stations within 30km of Berlin center

## Collection Period
- Start: 2026-05-26
- Ongoing
