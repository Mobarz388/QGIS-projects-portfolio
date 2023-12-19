GIS-MCDA for Optimal Wind Farm Site Selection in Mendocino, California: A Fuzzy Logic and Analytical Hierarchy Process Integration in QGIS

Steps for wind farm site selection:

A) Data Collection: Wind speed and elevation data were sourced from the Global Wind Atlas, a recognized provider of wind resource information. Inverse Distance Weighting (IDW) was employed to convert point datasets to continuous raster surfaces, ensuring a smooth representation of land surface elevation and wind speed. Additionally, for comprehensive spatial analysis, key parameters such as cities, nature protection areas, and power transmission lines were sourced through ArcGIS Hub.

B) Slope Calculation: Utilizing the slope tool in QGIS to derive slope information from the digital elevation model (DEM) contributes to a better understanding of the terrain, a crucial factor in wind farm site selection.

C) Rasterization: The application of the Rasterize tool in QGIS to prepare raster layers for nature protection areas, transmission lines, and cities is essential for incorporating key environmental and infrastructural considerations into the analysis.

D) Proximity Analysis: Employing the Proximity tool in QGIS to generate distance raster layers for nature protection areas, transmission lines, and cities adds a valuable spatial dimension to our study, capturing the influence of nearby features on site suitability.

E) Fuzzy Logic and AHP Integration: The incorporation of fuzzy logic with a linear membership function in QGIS for preparing fuzzy standardized layers is a sophisticated approach, allowing for the representation of uncertainty and vagueness in the input data. The subsequent use of the Analytical Hierarchy Process (AHP) to determine the relative importance of parameters in wind farm site selection through weighting is a rigorous and well-established decision-making methodology.

F) Weighted Linear Combination (WLC): The application of WLC for data combination and the preparation of the final site suitability map is a logical step, consolidating the various factors considered in the analysis into a comprehensive output that reflects the overall suitability of potential wind farm sites.
