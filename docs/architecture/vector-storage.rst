
This consistent schema allows Aurora to support maps, dashboards, analysis, pipelines, and views using a unified spatial storage model.

Table Structure
---------------

Each vector dataset table follows the same structure.

Example:

.. code-block:: sql

   \d spatial_data_11231

Columns:

- id — internal Aurora row identifier
- feature_id — original feature identifier (optional)
- geometry_type — geometry type label
- properties — feature attributes (JSONB)
- geometry — geometry in GeoJSON form (JSONB)
- geom — PostGIS geometry column
- harvested_at — ingestion timestamp
- created_at — record creation time
- updated_at — last modification time
- deleted_at — soft delete marker

This structure separates geometry storage from attribute storage while maintaining full PostGIS compatibility.

Column Details
--------------

id
^^

Primary key for the Aurora record.

This is the internal feature identifier used by Aurora.

feature_id
^^^^^^^^^^

Original feature identifier from the source dataset, if available.

Examples:

- ESRI OBJECTID
- QGIS feature ID
- External database ID

geometry_type
^^^^^^^^^^^^^

Geometry type label such as:

- Point
- LineString
- Polygon
- MultiPolygon

Used for styling and rendering logic.

properties
^^^^^^^^^^

All non-spatial attributes stored as JSONB.

This flexible schema allows Aurora to store heterogeneous datasets without altering table structure.

Examples:

.. code-block:: json

   {
     "name": "Chicago",
     "population": 2696555,
     "region": "Cook"
   }

geometry
^^^^^^^^

Geometry stored in GeoJSON form (JSONB).

Used for:

- API output
- serialization
- client rendering
- interoperability

geom
^^^^

Native PostGIS geometry column:

- Type: geometry(Geometry, 4326)
- Spatially indexed
- Used for spatial queries and analysis

All Aurora spatial operations use this column.

Timestamps
^^^^^^^^^^

harvested_at
   Time the feature was ingested from source.

created_at
   Aurora record creation time.

updated_at
   Last modification time.

deleted_at
   Soft delete marker for removed features.

Indexes
-------

Each dataset table includes a primary key index on ``id``.

Additional spatial indexes are created on ``geom`` for efficient spatial queries.

Dataset Isolation
-----------------

Each dataset is stored in its own table rather than sharing a global feature table.

Advantages:

- Isolation between datasets
- Independent lifecycle
- Faster queries
- Simplified deletion
- Parallel ingestion
- Independent indexing
- Dataset-level permissions

Aurora maps and dashboards reference dataset tables directly.

Relationship to Maps
--------------------

Map layers read geometry from the ``geom`` column and attributes from ``properties``.

Styling, popups, and analysis operate on this unified structure.

Relationship to Pipelines
-------------------------

Pipelines populate ``spatial_data_<id>`` tables during ingestion.

Sources may include:

- PostGIS
- ESRI
- QGIS
- GeoPackage
- CSV with geometry
- Raster vectorization

All sources are normalized into the same schema.

Relationship to Views and Derived Datasets
------------------------------------------

Derived datasets such as:

- Views
- Clip results
- Dissolve results
- Analysis outputs

are also stored as ``spatial_data_<id>`` tables.

This ensures all Aurora vector data behaves consistently regardless of origin.

Geometry Model
--------------

Aurora stores geometry in two representations:

- ``geom`` — native PostGIS geometry
- ``geometry`` — GeoJSON representation

This dual storage allows:

- Fast spatial computation
- Direct API serialization
- Map rendering without conversion
- Cross-system interoperability

Soft Deletion
-------------

Records are not immediately removed.

If a feature is deleted:

- ``deleted_at`` is set
- Feature excluded from queries
- History preserved

This supports lineage and audit workflows.

Summary
-------

Aurora vector datasets use a standardized PostGIS schema:

- One table per dataset
- JSONB attributes
- Native PostGIS geometry
- GeoJSON geometry
- Consistent timestamps
- Spatial indexing

This architecture enables Aurora’s unified mapping, analysis, and dashboard capabilities.

