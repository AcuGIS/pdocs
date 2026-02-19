Live Analysis
=============

Live Analysis provides real-time spatial pattern analysis directly from PostGIS data sources.

Unlike standard Aurora analysis, which operates on Aurora datasets within maps, Live Analysis connects directly to a PostGIS database and computes results dynamically on page load.

Overview
--------

Live Analysis enables continuously updated spatial pattern detection without data ingestion.

It supports:

- Hot Spot analysis
- Outlier detection
- Kernel Density (KDE)

Results are computed directly from the connected PostGIS source each time the page or report loads.

This allows dashboards and reports to reflect the latest database state without pipelines or dataset refresh.

Architecture
------------

Live Analysis operates as:

- Direct PostGIS connection
- Query-time spatial computation
- Map and dashboard rendering
- Optional snapshot storage

Data is never copied into Aurora datasets unless snapshots are created.

Live Spatial Pattern Tools
--------------------------

Aurora provides three Live Spatial Pattern tools.

Hot Spot Analysis
^^^^^^^^^^^^^^^^^

Identifies statistically significant spatial clusters of high and low values.

Hot Spot analysis:

- Computes Gi* z-scores and p-values
- Classifies hotspot intensity levels
- Uses current spatial extent and filters
- Supports snapshot storage
- Integrates with map and dashboard styling

Hot Spot outputs can be viewed live or stored for later use.

Outlier Analysis
^^^^^^^^^^^^^^^^

Detects spatial anomalies such as high values surrounded by low values.

Outlier analysis:

- Identifies spatial outliers and clusters
- Computes local spatial statistics
- Generates live maps and summaries
- Supports dashboard reports
- Compatible with map styling

Outlier results update automatically from PostGIS.

Kernel Density (KDE)
^^^^^^^^^^^^^^^^^^^^

Generates a continuous density surface representing spatial intensity.

KDE:

- Computes density from point events
- Uses configurable bandwidth
- Uses current filters and extent
- Produces live raster surfaces
- Supports dashboard reports

Density surfaces reflect current database state.

Live Execution Model
--------------------

Live Analysis runs automatically on page load or refresh.

Execution uses:

- Current PostGIS data
- Active filters
- Map extent (if applicable)
- Analysis parameters

No Aurora dataset creation or pipeline execution is required.

Snapshots and Reports
---------------------

Live Analysis results can optionally be saved as snapshots.

Snapshots allow:

- Historical comparison
- Stable reporting
- Dashboard reuse
- Map styling persistence

Snapshots convert live results into stored Aurora content.

Relationship to Maps
--------------------

Live Analysis integrates with Aurora maps for visualization.

Maps provide:

- Spatial context
- Extent filtering
- Styling
- Layer display

However, analysis computation occurs in PostGIS, not the map engine.

Relationship to Dashboards
--------------------------

Live Analysis supports dashboards with continuously updated spatial statistics.

Dashboards can display:

- Live hotspot maps
- Outlier summaries
- KDE surfaces
- Pattern reports

This enables real-time spatial monitoring.

Relationship to Pipelines
-------------------------

Live Analysis does not use Pipelines.

Pipelines ingest data into Aurora datasets.

Live Analysis reads directly from PostGIS and computes results dynamically.

Typical Uses
------------

Live Analysis is suited for:

- Real-time incident data
- Monitoring systems
- Operational dashboards
- Streaming or frequently updated data
- Event density tracking
- Dynamic risk analysis

Examples:

- Crime incidents
- Sensor events
- Service calls
- Asset failures
- Traffic events
- Field reports

