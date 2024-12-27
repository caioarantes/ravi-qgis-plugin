# Ravi QGIS Plugin

# RAVI Plugin

RAVI is a QGIS plugin designed for seamless integration with Google Earth Engine (GEE) to process and visualize geospatial data, with a particular focus on Sentinel-2 imagery. The plugin supports vegetation index calculations, time series analysis, and interactive visualization, making it a valuable tool for researchers, farmers, and GIS enthusiasts working in agriculture, land monitoring, or environmental studies.

## Features

### 1. Earth Engine Integration
- **Authentication and Initialization**: Easily authenticate and initialize GEE for geospatial operations.
- **Imagery Processing**: Download, clip, and analyze Sentinel-2 imagery directly within QGIS.


### 2. Vegetation Index Calculations
- Supports popular indices like NDVI, EVI, SAVI, GNDVI, and GCI.
- Customizable metric-based compositing: mean, max, min, median, or amplitude.

### 3. Time Series Analysis
- Generate time series for vegetation indices over a selected Area of Interest (AOI).
- Filter and smooth data using Savitzky-Golay filtering.
- Compare time series with precipitation data from NASA POWER.

### 4. AOI and Date Filtering
- Load AOI from shapefiles or GeoJSON files.
- Filter imagery by date ranges and cloud coverage thresholds.

### 5. Custom Cloud Filtering
- **Cloud Ratio Threshold**: Set a custom threshold to filter out images based on cloud cover ratio.
- **Masking**: Remove pixels based on cloud, snow, and shadow masks to utilize partially cloudy imagery.

### 6. Visualization
- Interactive charts using Plotly for time series.
- Custom raster styling with predefined color ramps for NDVI and other indices.


## Installation

To install the Ravi QGIS Plugin, follow these steps:

1. Open QGIS and navigate to the Plugins menu.
2. Select "Manage and Install Plugins".
3. Check the box for "Show also experimental plugins" to enable experimental plugins.
4. Search for "Ravi QGIS Plugin" in the plugin repository.
5. Click "Install" to add the plugin to your QGIS installation.
6. Enable the plugin in the Installed tab.
7. Restart QGIS to complete the installation process.


## Usage

### Step 1: Authentication
- Open the plugin dialog.
- Authenticate with Google Earth Engine using your credentials.

### Step 2: Load AOI
- Select an AOI by loading a shapefile or GeoJSON file.
- Ensure the geometry is valid (Polygon or MultiPolygon).

### Step 3: Configure Parameters
- Set the desired vegetation index, metric, date range, and cloud coverage thresholds.
- Optionally, configure filtering and smoothing parameters for time series.

### Step 4: Process and Visualize
- Click on the respective buttons to download imagery, calculate indices, or generate time series.
- Visualize results in the interactive Plotly charts or add styled raster layers to QGIS.

## Requirements

- QGIS 3.x
- Google Earth Engine API (`earthengine-api==1.3.1`)
- Python libraries:
  - PyQt5
  - pandas
  - numpy
  - scipy
  - geopandas
  - requests
  - Plotly

## Troubleshooting

- **Earth Engine Authentication Failed**: Ensure you have installed the Earth Engine API and authenticated correctly.
- **AOI Errors**: Verify the AOI file is valid and has the correct CRS (EPSG:4326 preferred).
- **Visualization Issues**: Ensure all required Python libraries are installed.

## Contributing

Contributions are welcome! Feel free to fork the repository and submit pull requests for bug fixes, new features, or documentation improvements.

## License

This plugin is licensed under the GNU General Public License v2.0 or later. See the LICENSE file for details.

## Contact

For questions or support, please contact [Caio Arantes](mailto:github.com/caioarantes).