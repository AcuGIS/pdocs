Analysis
========

Aurora provides spatial and statistical analysis tools directly within the Map Builder.

All analysis is initiated from a map and operates on the map’s active layers and current spatial context.

Analysis results can be visualized immediately in the map and used in dashboards and datasets.

Overview
--------

Analysis in Aurora is map-driven.

Users select an analysis category and tool from the Map Builder, then configure parameters using the map’s datasets and spatial extent.

Analysis can:

- Generate new layers
- Produce summary statistics
- Highlight spatial patterns
- Create derived datasets
- Feed dashboards and charts

Analysis Categories
-------------------

Aurora provides several analysis categories within Maps.

Proximity & Distance
^^^^^^^^^^^^^^^^^^^^

Tools for distance-based spatial relationships.

Includes:

- Buffer — create distance zones around features
- Nearest — find nearest features
- Proximity — analyze distance relationships
- Center & Dispersion — spatial central tendency
- Outliers — distance-based outlier detection

Overlay & Join (Vector)
^^^^^^^^^^^^^^^^^^^^^^^

Vector overlay and spatial relationship tools.

Includes:

- Intersect — geometric intersection of layers
- Overlay Layers — combine spatial layers
- Join — spatial attribute join
- Join Features (Aggregated) — aggregated spatial join
- Summarize Within — summarize features inside areas
- Summarize Nearby — summarize nearby features
- Erase — remove overlapping geometry

Spatial Pattern Analysis
^^^^^^^^^^^^^^^^^^^^^^^^

Pattern detection and density visualization tools.

Includes:

- Clustering — group spatial clusters
- Heatmap — density surface visualization
- Hot Spots — statistically significant clusters
- Outliers — spatial anomaly detection

Routing
^^^^^^^

Network-based spatial analysis.

Routing tools operate on network datasets to compute paths and connectivity.

Raster Analysis
^^^^^^^^^^^^^^^

Analysis of raster datasets.

Raster tools compute statistics and spatial relationships based on raster cell values within the map extent or selected areas.

Feature Tools
^^^^^^^^^^^^^

Geometry and feature-level operations applied to map layers.

These tools modify or derive features directly within the map context.

Time Analysis
^^^^^^^^^^^^^

Temporal analysis tools for time-enabled datasets.

Includes:

- Time Cube — spatiotemporal aggregation
- Forecast / Rolling Average — temporal trend analysis

Map-Driven Execution
--------------------

All analysis operates within the current map context.

This means analysis uses:

- Active layers
- Visible features
- Map extent
- Spatial selection
- Radius / proximity settings
- Time slider (if enabled)

This ensures analysis reflects what the user is viewing.

Results
-------

Analysis results may:

- Create new map layers
- Highlight features
- Generate statistics
- Produce derived datasets
- Feed dashboard widgets

Results appear immediately in the map.

Relationship to Maps
--------------------

Analysis is a core capability of the Maps module.

Maps provide:

- Spatial context
- Layer selection
- Interaction tools
- Visualization
- Filtering
- Time controls

Analysis extends map exploration into spatial computation.

Relationship to Dashboards
--------------------------

Analysis outputs can be used in dashboards.

Examples:

- Hotspot layers in maps
- Outlier summaries in widgets
- Proximity results in charts
- Raster statistics in analysis panels

Dashboards visualize results produced in maps.

Typical Uses
------------

Aurora map analysis supports:

- Proximity studies
- Coverage analysis
- Spatial clustering
- Density mapping
- Overlay comparisons
- Network routing
- Temporal trends
- Raster statistics
- Spatial aggregation

Examples:

- Schools within 1 km of hospitals
- Crime hotspots
- Population density
- Service coverage
- Nearest facilities
- Time-series trends
- Raster suitability

