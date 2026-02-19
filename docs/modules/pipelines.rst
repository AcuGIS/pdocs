Pipelines
=========

Aurora Pipelines provide automated workflows for ingesting, transforming, and updating spatial and tabular data from external sources into Aurora datasets.

They enable continuous data integration from GIS systems, databases, files, and web services, ensuring maps and dashboards always reflect current data.

Overview
--------

A Pipeline defines:

- **Source** — where data originates
- **Processing** — optional transformations
- **Target** — Aurora dataset destination
- **Schedule** — when updates run

Pipelines can run on demand or automatically on a defined schedule.

Supported Sources
-----------------

Aurora Pipelines can ingest data from a wide range of geospatial and enterprise sources, including:

- ESRI (Feature Services, File Geodatabases, Shapefiles)
- QGIS projects and layers
- PostGIS and PostgreSQL
- GeoServer / OGC services (WFS, WMS where applicable)
- CSV and tabular files
- GeoPackage
- Raster sources (GeoTIFF, COG, tiles)

Processing
----------

Pipelines can optionally transform data during ingestion.

Typical processing steps include:

- Field mapping and renaming
- Geometry reprojection
- Attribute filtering
- Spatial filtering
- Schema normalization
- Raster conversion or tiling
- Data merging or replacement

Targets
-------

Pipeline outputs are stored as Aurora datasets, which can be used in:

- Maps
- Dashboards
- Reports
- Apps
- Analysis workflows

A Pipeline can create a new dataset or update an existing one.

Scheduling
----------

Pipelines support automated execution using schedules such as:

- Manual (run on demand)
- Hourly
- Daily
- Weekly
- Custom intervals

Scheduled pipelines ensure Aurora content stays synchronized with external systems.

Typical Uses
------------

Common Pipeline scenarios include:

- Synchronizing enterprise GIS layers into Aurora
- Importing ESRI or QGIS data for web publishing
- Updating dashboards from operational databases
- Converting raster data for visualization
- Maintaining live datasets from OGC services
- Aggregating multiple sources into a unified layer

Workflow
--------

The basic Pipeline workflow is:

1. Select data source
2. Configure connection or upload
3. Define processing options
4. Choose target dataset
5. Set schedule
6. Run or activate

Architecture
------------

Pipelines operate as server-side ingestion jobs within Aurora.

They:

- Connect to external sources
- Retrieve data
- Apply transformations
- Store results in Aurora storage
- Trigger dataset updates

Updated datasets immediately propagate to dependent maps, dashboards, and apps.

Relationship to Other Modules
-----------------------------

Pipelines integrate with several Aurora components:

- :doc:`maps` — publish pipeline datasets
- :doc:`dashboards` — analyze pipeline data
- :doc:`geosync` — field synchronization pipelines
- :doc:`reporting` — reports from pipeline outputs

See Also
--------

- :doc:`../workflows/import-esri-qgis`
- :doc:`../workflows/sync-field-data`
