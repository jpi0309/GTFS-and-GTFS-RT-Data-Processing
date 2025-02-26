# GTFS & GPS Data Processing for Public Transport

## Overview
This project processes GTFS (General Transit Feed Specification) and GPS data to analyze public transport efficiency. It includes segmentation of bus routes, real-time GPS data processing, and visualization tools to assess bus movement and delays.

The project is divided into two main components:
1. **GTFS Data Processing** - Constructs a structured transit network by processing bus stops, route shapes, and segmenting routes for efficient pathfinding.
2. **GPS Data Processing** - Matches real-time GPS data to the GTFS-based network to track vehicle positions, estimate arrival times, and analyze delays.

## Features
- Generates a grid-based segmentation of the transit network.
- Processes public transportation data, including bus stops, arrivals, and schedules.
- Constructs a graph-based representation of the transportation network for efficient routing.
- Implements a real-time GPS tracking system that estimates bus positions and delays.
- Provides an interactive visualization of routes and GPS-tracked vehicles.
- Allows integration of updated data to maintain an accurate transit model.
  
Below, visualization of the division of the bus network into common segments (left) and processed GPS readings with obtained information characterizing the trip (right):
 <p align="center">
    <img src="segmentation.png" alt="Shortest Path" width="400"/>
    <img src="processed_gps.png" alt="Another Image" width="400"/>
</p>


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
3. Run the Jupyter Notebook:
   ```sh
   jupyter notebook "GTFS processing.ipynb"
   jupyter notebook "gps processing algorithm.ipynb"
   ```

## Usage
- Open and execute the GTFS processing notebook to segment and preprocess transit data.
- Run the GPS processing notebook to estimate real-time bus positions and delays.
- The computed results are stored in the `results/` directory and can be visualized as an interactive map.

## Dependencies
The project requires the following Python libraries:
- pandas
- numpy
- folium
- matplotlib
- shapely
- joblib
- networkx (for potential route optimization)

Ensure that all dependencies are installed before running the notebooks.

## Data
The dataset includes:
- GTFS data for bus stops, trips, and route shapes.
- Real-time GPS records of bus positions and timestamps.
- Processed outputs stored as CSV and interactive HTML maps.

## Future Improvements
- Integrating real-time data streaming.
- Enhancing GPS tracking accuracy and delay estimation.
- Expanding the approach to other cities beyond Gdańsk.

## License
This project is licensed under the MIT License.

## Author
Developed as part of a public transportation analysis project. Contributions are welcome!



