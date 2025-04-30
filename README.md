# Ocean Routing Data Directory

This directory contains all the data files needed for the ocean routing system. Please place your data in the appropriate folders as described below.

## Directory Structure

### 1. `ocean_boundaries/`
Store ocean boundary data here, which defines where ships can travel.

**Recommended files to add:**
- `indian_ocean.geojson` - GeoJSON file with Indian Ocean boundaries
- `coastlines.shp` - Shapefile with coastline data (if using shapefiles)
- Any Natural Earth Data ocean boundary files

**Data sources:**
- [Natural Earth Data](https://www.naturalearthdata.com/downloads/10m-physical-vectors/10m-ocean/)
- [NOAA GSHHG](https://www.ngdc.noaa.gov/mgg/shorelines/data/gshhg/latest/)
- [OSM Water Polygons](https://osmdata.openstreetmap.de/data/water-polygons.html)

### 2. `weather/`
Store historical and forecast weather data for oceanic conditions.

**Recommended files to add:**
- `ocean_currents.nc` - NetCDF files with current data
- `wave_heights.csv` - CSV files with wave height data
- `wind_speeds.json` - JSON files with wind data

**Data sources:**
- [NOAA Ocean Data](https://www.ncei.noaa.gov/products/weather-climate-models/global-forecast)
- [Copernicus Marine Service](https://marine.copernicus.eu/)
- [INCOIS](https://incois.gov.in/portal/datainfo/insitu.jsp)

### 3. `ship_data/`
Store ship profiles and parameters here.

**Recommended files to add:**
- `ship_types.json` - JSON file with ship type specifications
- `fuel_consumption_rates.csv` - CSV file with fuel consumption at different speeds
- `historical_routes.csv` - CSV file with previously used routes (optional)

### 4. `api_keys/`
Store API configuration files and keys here. **Do not commit this directory to public repositories!**

**Recommended files to add:**
- `google_maps_key.txt` - Text file with Google Maps API key
- `weather_api_config.json` - JSON file with weather API credentials

## File Formats

- **GeoJSON** (.geojson): Preferred format for geographic data
- **Shapefile** (.shp, .dbf, .shx): Alternative format for geographic data
- **CSV** (.csv): For tabular data
- **JSON** (.json): For structured data
- **NetCDF** (.nc): For gridded weather/ocean data

## Example Usage

Place your data files in the appropriate folders, and the routing algorithms will automatically use them when calculating optimal routes. 