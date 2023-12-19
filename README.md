GIS-MCDA for Optimal Wind Farm Site Selection in Mendocino, California: A Fuzzy Logic and Analytical Hierarchy Process Integration in QGIS
A) Data Collection: The use of ArcGIS Hub for data collection is a sound choice, ensuring access to reliable and up-to-date datasets. The decision to employ Inverse Distance Weighting (IDW) for converting point datasets to continuous raster surfaces is appropriate for obtaining a smooth representation of land surface elevation and wind speed.

B) Slope Calculation: Utilizing the slope tool in QGIS to derive slope information from the digital elevation model (DEM) contributes to a better understanding of the terrain, a crucial factor in wind farm site selection.

C) Rasterization: The application of the Rasterize tool in QGIS to prepare raster layers for nature protection areas, transmission lines, and cities is essential for incorporating key environmental and infrastructural considerations into the analysis.

D) Proximity Analysis: Employing the Proximity tool in QGIS to generate distance raster layers for nature protection areas, transmission lines, and cities adds a valuable spatial dimension to your study, capturing the influence of nearby features on site suitability.

Fuzzy Logic and AHP Integration: The incorporation of fuzzy logic with a linear membership function in QGIS for preparing fuzzy standardized layers is a sophisticated approach, allowing for the representation of uncertainty and vagueness in the input data. The subsequent use of the Analytical Hierarchy Process (AHP) to determine the relative importance of parameters in wind farm site selection through weighting is a rigorous and well-established decision-making methodology.

Weighted Linear Combination (WLC): The application of WLC for data combination and the preparation of the final site suitability map is a logical step, consolidating the various factors considered in the analysis into a comprehensive output that reflects the overall suitability of potential wind farm sites.
