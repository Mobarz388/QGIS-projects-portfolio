Wind farm site selection with QGIS
Steps for wind farm site selection using GIS-MCDA in Mendocino, California
1. Data collection from ArcGIS Hub (https://hub.arcgis.com/search?collection=Dataset)
2. A) Data quantification of land surface elevation and wind speed dataset by using Inverse Distance Weighting (IDW) to convert point dataset to a continuous raster surface
2. B) Use slope tool in QGIS to prepare slope from digital elevation model (DEM)
2. C) Use Rasterize tool in QGIS to prepare raster layers for nature protection areas, transmission lines, and cities
2. D) using Proximity tool in QGIS to prepare Distance raster layers for nature protection areas, transmission lines, and cities
3. Apply fuzzy logic linear membership function in QGIS to prepare fuzzy standardized layers
4. Employ analytical hierarchy process (AHP) to determine the contribution (relative) importance of parameters in wind farm site selection based on the weighting of parameter
5. Use weighted linear combination (WLC) for data combination and prepare final site suitability map
