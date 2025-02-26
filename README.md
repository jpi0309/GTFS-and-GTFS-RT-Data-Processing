# GTFS-and-GTFS-RT-Data-Processing
Processing raw GTFS and GTFS-RT data for Gdańsk to support further analysis. We determine the bus position along the route, calculate the accumulated distance, identify potential delays, and detect the stop where the vehicle is currently located.

## Project Description
This project focuses on processing and analyzing public transport data to improve efficiency and visualization of bus routes. It integrates static GTFS data with real-time GPS readings to track vehicle movements, estimate arrival times, and analyze delays.

The workflow consists of:
1. **GTFS Data Processing**: Extracting and modifying stop locations, travel distances, and route segmentation.
2. **GPS Data Processing**: Matching GPS readings to routes, estimating delays, and predicting arrival times.
3. **Route Segmentation**: Splitting the network into segments to improve analysis and visualization.
4. **Visualization**: Generating interactive maps to represent bus movement and delays dynamically.

## Overview
This project processes GTFS (General Transit Feed Specification) and GPS data to analyze public transport efficiency. It includes segmentation of bus routes, real-time GPS data processing, and visualization tools to assess bus movement and delays.

## Features

### Example Visualizations
Below, you can see divided bus network into segments and  visualization of processed gps points:
- **Segmented Bus Network:**
  ![Segmented Network](path/to/your/image1.png)

- **Processed GPS Data Visualization:**
  ![GPS Data](path/to/your/image2.png)

- **GTFS Data Processing**: Parses stops and shape data, adds distance tracking, and structures trip data.
- **GPS Data Processing**: Reads GPS records, maps them to segments, estimates accumulated distances and delays.
- **Visualization**: Generates interactive maps for route segmentation and real-time tracking.
- **Efficiency Analysis**: Tracks bus movement over time to identify bottlenecks and scheduling issues.

## Requirements
- Python 3.8+
- Pandas
- NumPy
- Folium
- Matplotlib
- Shapely
- Joblib
- Jupyter Notebook (optional for running notebooks)

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repository.git
   cd your-repository
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Data Preparation
### 1. GTFS Data Processing
- Parses GTFS stops and shape data.
- Adds `shape_distance_traveled` and `stop_dist_traveled` for trip mapping.
- Segments routes into manageable units.
- Generates a k-d tree for fast nearest-neighbor lookup.

### 2. GPS Data Processing
- Reads GPS records from CSV.
- Matches GPS points to the nearest route segment.
- Estimates accumulated travel distance.
- Calculates expected arrival times and delays.
- Saves processed results for visualization.

## Usage
### GTFS Processing
Run the GTFS processing notebook to segment routes and create supporting files:
```sh
jupyter notebook "GTFS processing.ipynb"
```
This generates segmented routes and a k-d tree used for GPS processing.

### GPS Processing
Run the GPS processing notebook to estimate bus positions and delays:
```sh
jupyter notebook "gps processing algorithm.ipynb"
```
This processes live GPS readings and produces results stored in `results/processed_gps.csv`.

### Visualization
After running the processing scripts, interactive maps can be accessed in:
- `results/segments_map.html` (segmented routes visualization)
- `results/processed_gps.html` (GPS tracking visualization)

## Example Outputs
Below, you can insert images showcasing the results:
- **Segmented Bus Network:**
  ![Segmented Network](path/to/your/image1.png)

- **Processed GPS Data Visualization:**
  ![GPS Data](path/to/your/image2.png)

## Notes
- The project assumes GTFS data for Gdańsk, Poland (November 2024 dataset), but can be adapted to other cities.
- Time adjustments consider local time shifts due to daylight savings.

## Author
- Developed as part of a public transportation analysis project.

## License
MIT License

