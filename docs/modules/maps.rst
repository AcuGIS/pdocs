Maps
====

The Maps module provides Aurora’s Map Builder for creating interactive spatial views from Aurora datasets.

Aurora maps combine spatial layers, styling, popups, charts, and analysis into a unified view that can be used in dashboards, apps, and shared visualizations.

Overview
--------

Aurora maps are composed of dataset-driven layers configured in Map Builder.

Each map:

- References Aurora datasets
- Stores layer styling and behavior
- Supports interactive exploration and filtering
- Links spatial features to charts and analysis
- Updates automatically when datasets change

Maps are used across Aurora in dashboards, apps, and reports.

Map Builder
-----------

Maps are created and edited in the Map Builder.

Map Builder allows you to:

- Add datasets as layers
- Configure layer styling
- Define popups and charts
- Enable time and clustering behavior
- Control legends and visibility
- Arrange layer order

Layer Configuration
-------------------

Each dataset layer in a map supports the following configuration options.

Layer Order
^^^^^^^^^^^

- Move layer up
- Move layer down

These control drawing order and visual stacking.

Styling
^^^^^^^

Layer symbology can be customized using fill and stroke styles.

Options:

- Fill color
- Stroke color
- Stroke width
- Opacity

Styles can be reset to the dataset default.

Popup Configuration
^^^^^^^^^^^^^^^^^^^

Popups display feature information on click.

Popup settings include:

- Select attributes to display
- Custom popup formatting
- Enable chart popup
- Configure popup chart type and fields
- Toggle custom popup content

Popups connect spatial features to data context.

Layer Charts
^^^^^^^^^^^^

Layers can expose charts linked to their features.

Layer chart configuration allows:

- Selecting chart type
- Selecting fields
- Linking chart to map selection
- Displaying charts in dashboards or popups

Charts update dynamically as map filters or selections change.

Legend
^^^^^^

Each layer can define its legend representation.

Legend settings control:

- Symbol display
- Label formatting
- Visibility in map and dashboards

Time Slider
^^^^^^^^^^^

Temporal datasets can enable a time slider.

Time configuration includes:

- Time field selection
- Playback range
- Animation behavior

The time slider filters features by time and supports animated exploration.

Clustering
^^^^^^^^^^

Point layers can enable clustering.

Clustering groups nearby features at lower zoom levels to improve readability and performance.

Clusters expand automatically when zooming.

Pyramid Chart
^^^^^^^^^^^^^

Layers can generate pyramid charts from their attributes.

Pyramid charts visualize distributions or hierarchical comparisons derived from spatial features.

They can be displayed in dashboards or linked views.

Map Behavior
------------

Aurora maps support interactive exploration:

- Zoom and pan
- Feature selection
- Popup inspection
- Layer toggling
- Time filtering
- Cluster expansion
- Linked chart filtering

Selections and filters propagate to connected charts and dashboards.

Relationship to Datasets
------------------------

Maps reference Aurora datasets rather than external services.

This provides:

- Consistent styling
- Stable identifiers
- Fast rendering
- Integration with pipelines and GeoSync
- Automatic updates when datasets refresh

When a dataset is updated, all maps using it reflect the changes.

Use in Dashboards and Apps
--------------------------

Maps are core components of Aurora dashboards and apps.

They can:

- Drive charts via selection
- Respond to dashboard filters
- Display popup charts
- Participate in analysis views
- Synchronize with timelines and presentations

Maps act as the spatial anchor for analytical content.

Relationship to Other Modules
-----------------------------

Maps integrate closely with:

- :doc:`dashboards` — charts linked to map layers
- :doc:`pipelines` — datasets feeding maps
- :doc:`geosync` — field-collected data in maps
- :doc:`reporting` — map views in reports
- :doc:`apps` — published map experiences

