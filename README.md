# Smart-Itinerary-Generator
End-to-end geospatial framework for customized pedestrian tours in the Seattle metropolitan area

Workflow Overview:

Data Acquisition: Download OSM layers via OSMnx; ingest POIs.
Network Preparation: Clean and simplify graph; load into PostGIS.
Preference Parsing: Convert user text to OSM tags via LLM.
Routing: Snap points, split network, run pgr_dijkstra, and assemble itinerary.
Feature Engineering: Compute segment length and turn count.
Model Training: Train and validate XGBoost regressor on OSRM-derived times.

Together, these blocks automated the entire workflow, from raw user input through spatial querying, network preparation, vertex snapping, and Dijkstra‐based routing, entirely within Python and PostGIS, making the personalized walking tour both data‐driven and reproducible.
