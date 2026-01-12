# Bus Stop Location Optimization Using Genetic Algorithms in ArcGIS Pro

BusStopAllocation is a spatial decision-support project that identifies and allocates optimal bus stop locations using a Genetic Algorithm (GA) integrated directly with ArcGIS Pro. The project combines evolutionary optimization techniques with GIS-based spatial analysis to support evidence-based public transport planning.

The workflow is developed entirely within the **ArcGIS Pro** ecosystem, leveraging ArcPy for geoprocessing, spatial analysis, and feature class management, while using Python-based genetic algorithm logic to iteratively evolve candidate bus stop solutions.


## 🔍 Project Overview

Urban bus stop placement involves balancing multiple, often conflicting objectives such as:
- Accessibility for surrounding populations
- Minimum walking distance to stops
- Adequate spacing between stops
- Compatibility with surrounding land use
- Network coverage efficiency

This project addresses these challenges by formulating bus stop placement as a multi-objective optimization problem, solved using a Genetic Algorithm. Candidate bus stop locations are generated from road centerlines and evaluated iteratively until near-optimal spatial configurations are produced.


## 🛠 How the Project Was Built

The project follows a GIS-first optimization workflow:

1. Preprocessing in ArcGIS Pro
   - Road centerlines are processed to generate potential bus stop candidate points.
   - Spatial filters are applied (e.g. minimum distance from intersections, spacing constraints).
   - Supporting datasets such as population, land-use parcels, and service areas are prepared.
   - All preprocessing steps rely on ArcGIS Pro geoprocessing tools, some of which require licensed extensions.

2. Genetic Algorithm Implementation
   - A Genetic Algorithm is implemented in Python using evolutionary principles such as:
       - Selection
       - Crossover
       - Mutation
   - Each individual represents a potential configuration of bus stop locations.
   - Fitness functions evaluate each solution based on multiple spatial criteria derived from GIS analysis.

3. Integration with ArcPy
   - ArcPy is used to:
       - Read and write feature classes
       - Perform distance calculations
       - Assign surrounding parcels or population to nearest bus stops
       - Export results back into geodatabases for visualization
   - Each generation of the algorithm can be visualized directly in ArcGIS Pro, allowing planners to inspect spatial evolution over time.

4. Output & Analysis
   - Final optimized bus stop locations are written to feature classes.
   - Results can be further analyzed, mapped, or published using ArcGIS Pro tools and dashboards.


## 🧩 ArcGIS Pro Dependency & Licensing
This project requires ArcGIS Pro to run successfully.
- The preprocessing and spatial evaluation stages depend on ArcGIS Pro geoprocessing tools.
- Some workflows may require licensed ArcGIS extensions (e.g. Network Analyst or Spatial Analyst, depending on the dataset and configuration).
- The repository does not include geodatabases or proprietary datasets; instead, scripts are provided to regenerate outputs within a licensed ArcGIS Pro environment.


## 🎯 Intended Use
This project is intended for:
- Transport and urban planners
- GIS analysts
- Researchers exploring spatial optimization
- Decision-support applications in public transport planning

<br/>
 It is designed to be adaptable to different cities, datasets, and planning constraints by modifying input layers and fitness functions.
