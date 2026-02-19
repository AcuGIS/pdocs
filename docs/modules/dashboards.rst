Dashboards
==========

The Dashboards module provides Aurora’s Dashboard Builder for creating interactive analytical views that combine maps, charts, tables, metrics, and spatial analysis.

Dashboards link datasets, maps, and analytics into a unified workspace for exploration and decision support.

Overview
--------

An Aurora dashboard is composed of configurable widgets arranged in a grid layout.

Widgets connect to Aurora datasets and maps and update dynamically in response to filters, selections, and spatial interactions.

Dashboards enable:

- Data exploration
- Spatial analysis
- Statistical summaries
- Map-chart interaction
- Comparative views
- Monitoring and reporting

Dashboard Builder
-----------------

Dashboards are created and edited in the Dashboard Builder.

The Builder provides:

- Widget palette
- Drag-and-drop layout
- Dataset selection
- Configuration panels
- Interactive filtering
- Save and publish controls

Widgets can be resized and arranged to create analytical layouts.

Widget Types
------------

Aurora dashboards support multiple widget types.

Map
^^^

Embeds an interactive Aurora map.

Maps in dashboards:

- Display dataset layers
- Respond to filters
- Drive linked charts
- Support selection and zoom
- Provide spatial context

Chart
^^^^^

Displays dataset charts such as:

- Bar
- Line
- Pie

Charts update based on filters and map selections.

Table
^^^^^

Displays dataset attributes in tabular form.

Tables support:

- Sorting
- Filtering
- Selection
- Group summaries

Counter
^^^^^^^

Displays aggregated metrics from a dataset.

Examples:

- Count
- Sum
- Average
- Min / Max

Counters provide quick KPI-style indicators.

Filters
^^^^^^^

Adds dataset filter controls to the dashboard.

Filters allow users to:

- Select attribute values
- Restrict features
- Drive all linked widgets

Filters synchronize maps, charts, and tables.

Vector Analysis
^^^^^^^^^^^^^^^

Provides statistical summaries for vector datasets.

Vector analysis includes:

- Count
- Nulls
- Min / Max
- Sum
- Mean
- Median
- Standard deviation
- Distinct values

These summaries update with filters and selections.

Raster Analysis
^^^^^^^^^^^^^^^

Provides statistical summaries for raster datasets.

Raster analysis widgets calculate statistics for raster values within the current map or selection.

Hot Spot
^^^^^^^^

Displays hotspot analysis summary statistics derived from spatial clustering analysis.

Outlier
^^^^^^^

Displays outlier analysis summary statistics identifying anomalous spatial features.

HTML
^^^^

Adds formatted HTML content to dashboards.

HTML widgets support:

- Text
- Images
- Links
- Descriptive panels
- Instructions

Interactions
------------

Aurora dashboards support linked interactions across widgets.

Interactions include:

- Filter ? updates all widgets
- Map selection ? updates charts and tables
- Chart selection ? filters map
- Widget selection ? updates summaries
- Spatial radius / selection ? updates analysis

This enables coordinated spatial and statistical exploration.

Layout
------

Dashboards use a flexible grid layout.

Widgets can be:

- Added
- Moved
- Resized
- Removed

This allows custom analytical arrangements.

Relationship to Maps
--------------------

Maps act as spatial anchors within dashboards.

Maps can:

- Drive filters
- Provide selection context
- Define analysis extent
- Synchronize with charts
- Highlight features

Dashboards reference Aurora maps and datasets directly.

Relationship to Datasets
------------------------

All dashboard widgets connect to Aurora datasets.

Datasets may originate from:

- Imports
- Pipelines
- Views
- Clip / Dissolve operations
- GeoSync

Dataset updates automatically propagate to dashboards.

Typical Uses
------------

Aurora dashboards are used for:

- Spatial data analysis
- Monitoring indicators
- Comparing groups
- Exploring distributions
- Identifying hotspots and outliers
- Reporting spatial statistics
- Operational monitoring

Examples:

- Enrollment by district
- Assets by region
- Population by category
- Service coverage
- Infrastructure metrics

Publishing
----------

Dashboards can be saved and shared within Aurora.

They can be:

- Embedded in apps
- Linked from maps
- Used in reports
- Shared with users

Relationship to Other Modules
-----------------------------

Dashboards integrate with:

- :doc:`maps` — spatial context and selection
- :doc:`views` — filtered datasets
- :doc:`pipelines` — updated data sources
- :doc:`geosync` — field data dashboards
- :doc:`reporting` — analytical outputs

