Dataset Operations
==================

Aurora provides dataset-level operations for creating maps, charts, dashboards, views, and derived datasets directly from an existing dataset.

These actions are available from the **More Actions** menu on a dataset.

Overview
--------

Dataset operations allow you to quickly create new analytical or spatial outputs without leaving the dataset context.

Available operations include:

- Create Map
- Create Chart
- Create Dashboard
- Create View
- Clip Dataset
- Dissolve

These operations either create new Aurora content or generate new datasets derived from the original data.

Create Map
----------

Creates a new Aurora map using the selected dataset as a layer.

The map opens in Map Builder with the dataset already added.

Typical uses:

- Visualizing a newly imported dataset
- Starting spatial analysis
- Styling and publishing data
- Adding the dataset to dashboards or apps

Create Chart
------------

Creates a chart based on dataset attributes.

You can configure:

- Chart type
- Fields
- Aggregation
- Grouping

Charts created from datasets can be used in dashboards and map-linked analysis.

Create Dashboard
----------------

Creates a new dashboard with the dataset available for widgets.

The dataset can be used to:

- Drive charts
- Filter maps
- Display metrics
- Build analytical views

This is the fastest way to begin dashboard creation from data.

Create View
-----------

Creates a filtered or derived view of the dataset.

Views allow you to:

- Apply attribute filters
- Restrict features
- Focus on subsets
- Prepare analysis inputs

Views reference the original dataset and update automatically when the source changes.

Clip Dataset
------------

Creates a new dataset by clipping features to a selected spatial area.

Clipping:

- Restricts features to a boundary
- Removes outside geometry
- Produces a new Aurora dataset

Typical uses:

- Extracting regional subsets
- Preparing localized analysis data
- Reducing dataset size
- Creating study-area datasets

Dissolve
--------

Creates a new dataset by dissolving geometries based on an attribute or merging all features.

Dissolve operations:

- Merge features sharing an attribute value
- Aggregate boundaries
- Combine all geometry into one feature (optional)

Typical uses:

- Creating administrative regions
- Aggregating parcels or zones
- Generating summary geometries
- Preparing analysis units

Resulting Datasets
------------------

Clip and Dissolve operations create new Aurora datasets.

These derived datasets:

- Appear in the dataset catalog
- Can be mapped or charted
- Can feed dashboards and pipelines
- Retain lineage to the source dataset

Relationship to Maps and Dashboards
-----------------------------------

Dataset operations are entry points into Aurora workflows.

From a dataset you can immediately create:

- Maps
- Charts
- Dashboards
- Views
- Derived datasets

This enables rapid transition from data ingestion to visualization and analysis.

