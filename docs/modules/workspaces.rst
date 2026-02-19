Workspaces
==========

Workspaces provide logical separation of data, maps, dashboards, and analysis within Aurora.

Each workspace contains its own datasets and content, allowing organizations to organize projects, departments, or clients independently.

Overview
--------

Aurora operates within a selected workspace context.

When a workspace is active, all actions apply only to that workspace:

- Datasets
- Maps
- Dashboards
- Views
- Analysis
- Pipelines
- Connections

Switching workspace changes the visible data and content scope.

Selecting a Workspace
---------------------

Users select a workspace when entering Aurora or from the workspace selector in the header.

The selector lists available workspaces and dataset counts.

Choosing a workspace activates it as the current working context.

Workspace Isolation
-------------------

Workspaces isolate content from one another.

Each workspace has:

- Independent datasets
- Independent maps
- Independent dashboards
- Independent views
- Independent pipelines
- Independent PostGIS connections

Content in one workspace is not visible in others unless shared or duplicated.

Typical Uses
------------

Workspaces are commonly used for:

- Departments (Planning, Utilities, Public Safety)
- Organizations (Clients, Agencies)
- Projects (Studies, Initiatives)
- Environments (Production, Staging)
- Teams or business units

This enables clean separation of spatial content.

Dataset Scope
-------------

Datasets belong to a single workspace.

All dataset operations occur within that workspace:

- Import
- Pipelines
- Views
- Clip / Dissolve
- Analysis outputs

Maps and dashboards in the workspace reference its datasets.

Maps and Dashboards
-------------------

Maps and dashboards are workspace-specific.

When a workspace is active:

- Only its maps appear
- Only its dashboards appear
- Only its datasets are selectable

Switching workspace changes available content instantly.

Pipelines and Connections
-------------------------

Pipelines and PostGIS connections are also scoped to a workspace.

This allows:

- Different databases per workspace
- Different refresh schedules
- Client-specific sources
- Project-specific ingestion

Workspace context controls data integration.

Workspace Switching
-------------------

Users can switch workspaces at any time using the header selector.

Switching workspace:

- Changes dataset catalog
- Changes maps and dashboards
- Changes analysis context
- Changes pipelines and connections

No data is moved; only context changes.

Relationship to Aurora Architecture
-----------------------------------

Workspaces provide the top-level organizational layer in Aurora.

Hierarchy:

- Workspace
- Dataset
- Map / Dashboard / View
- Analysis / Pipelines / Apps

All spatial content exists within a workspace.

Summary
-------

Workspaces provide:

- Content isolation
- Organizational structure
- Multi-project support
- Multi-client separation
- Context switching

They define the active data and content scope within Aurora.

