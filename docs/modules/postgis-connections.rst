PostGIS Connections
===================

Aurora provides direct integration with PostGIS databases through two connection modes:

- Import — ingest PostGIS data into Aurora datasets
- Remote — use PostGIS data live without ingestion

These options allow Aurora to support both managed datasets and live database sources.

Overview
--------

PostGIS connections allow Aurora to access spatial tables from external PostgreSQL/PostGIS databases.

Users can choose between:

- Copying data into Aurora (Import)
- Referencing data in place (Remote)

This enables flexible integration with enterprise GIS databases.

Connection Modes
----------------

Aurora supports two PostGIS connection modes.

PostGIS Import
^^^^^^^^^^^^^^

Import copies spatial tables from PostGIS into Aurora datasets.

Imported datasets behave like native Aurora data and can be used in:

- Maps
- Dashboards
- Pipelines
- Analysis
- Apps

Import supports:

- One-time import
- Scheduled refresh

This is equivalent to pipeline ingestion from PostGIS.

Remote PostGIS
^^^^^^^^^^^^^^

Remote connections allow Aurora to use PostGIS tables directly without copying data.

Remote datasets remain in the source database and are accessed live.

Remote connections support two storage models:

- View (live query)
- Materialized View (local cached)

Remote data can be used in maps, dashboards, and analysis.

Import Mode
-----------

PostGIS Import retrieves spatial tables and stores them as Aurora datasets.

Import configuration includes:

- Host
- Port
- Database
- Schema
- Table
- Geometry column
- ID column (optional)

Imports can be:

- One-off — single ingestion
- Scheduled — recurring updates

Scheduled imports keep Aurora datasets synchronized with PostGIS.

Remote Mode
-----------

Remote PostGIS uses database tables directly without ingestion.

Remote configuration includes:

- Host
- Port
- Database
- Schema
- Table
- Geometry column
- ID column (optional)

Aurora creates a spatial data reference pointing to the external table.

Remote Storage Options
----------------------

Remote connections provide two execution models.

View (Live)
^^^^^^^^^^^

Aurora queries the PostGIS table directly at runtime.

Characteristics:

- No local storage
- Always current
- Depends on remote database performance
- No Aurora indexing

Best for:

- Frequently updated data
- Operational databases
- Live analysis
- Large tables

Materialized View
^^^^^^^^^^^^^^^^^

Aurora creates a locally stored materialized view of the remote table.

Characteristics:

- Local copy in Aurora database
- Local spatial indexes
- Faster rendering and analysis
- Refresh scheduling available

Materialized views balance live data with performance.

Normalization
-------------

Remote tables can be normalized for Aurora use.

Normalization defines:

- Geometry column
- ID column
- Spatial data identifier

This ensures compatibility with maps, dashboards, and analysis.

Scheduling
----------

Both Import and Materialized View modes support scheduling.

Scheduling enables:

- Automatic refresh
- Database synchronization
- Live dashboard updates
- Pipeline-like behavior

Import refreshes Aurora datasets.

Materialized View refreshes cached remote data.

Relationship to Live Analysis
-----------------------------

Remote PostGIS connections are commonly used with Live Analysis.

Live Analysis tools operate directly on PostGIS data without ingestion.

See :doc:`live-analysis`.

Relationship to Pipelines
-------------------------

PostGIS Import uses the Aurora Pipeline framework.

Pipelines ingest PostGIS tables into Aurora datasets.

See :doc:`pipelines`.

Typical Uses
------------

PostGIS Import:

- Stable datasets
- Analytical layers
- Map publishing
- Dashboards
- Data transformation

Remote View:

- Operational GIS databases
- Frequently updated tables
- Monitoring dashboards
- Live spatial data

Materialized View:

- Large datasets
- Performance-critical maps
- Cached enterprise data
- Hybrid live/local workflows

