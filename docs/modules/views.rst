Views
=====

Aurora Views are derived datasets created by filtering an existing dataset using attribute conditions.

A View contains only the features that match the defined criteria and is stored as a new Aurora dataset.

Overview
--------

A View is created from:

- Source dataset
- Attribute filter conditions
- Logical operators (AND / OR)

The result is a new dataset representing a subset of the original data.

Views are used to isolate, analyze, and visualize specific portions of a dataset without modifying the source.

Creating a View
---------------

Views are created from the dataset **More Actions ? Create View** operation.

The Create View dialog allows you to:

- Select source dataset
- Name the new dataset
- Define filter conditions
- Combine conditions with AND / OR
- Create the derived dataset

Filter Conditions
-----------------

Each condition includes:

- Field
- Data type
- Operator
- Value

Examples:

- population = 10000
- land_use = Residential
- shape_area = 500000
- zoning IN Commercial

Multiple conditions can be combined.

Logical Operators
-----------------

Conditions can be combined using:

- AND — feature must satisfy all conditions
- OR — feature may satisfy any condition

This allows complex subset definitions.

Resulting Dataset
-----------------

When a View is created:

- A new Aurora dataset is generated
- Only matching features are included
- Geometry and attributes are preserved
- Dataset appears in catalog
- Lineage to source dataset is retained

The View behaves like any other Aurora dataset.

Typical Uses
------------

Views are commonly used for:

- Filtering by attribute ranges
- Selecting thematic subsets
- Creating analysis inputs
- Preparing dashboard datasets
- Defining study populations
- Segmenting large datasets
- Building category-specific layers

Examples:

- Parcels > 1 acre
- Cities with population > 50k
- Commercial zoning areas
- Roads by classification
- Buildings by height range

Relationship to Source Dataset
------------------------------

Views do not modify the original dataset.

The source dataset remains unchanged.

The View represents a filtered copy that can be independently:

- Mapped
- Charted
- Analyzed
- Used in dashboards
- Used in pipelines

Relationship to Dataset Operations
----------------------------------

Views are one of the core dataset derivation tools in Aurora.

See also:

- :doc:`../workflows/dataset-operations`
- :doc:`../modules/maps`
- :doc:`../modules/dashboards`

