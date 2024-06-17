# QGIS-projects-portfolio

Methodology for Wind Farm Site Selection Using QGIS in Mendocino, California
Step 1: Data Collection and Preparation
Data Sources:

Wind Speed: Global Wind Atlas Data.
Elevation: Digital Terrain Model (DTM) from Global Wind Atlas.
Cities, Power Transmission Lines, Nature Protection Areas: ArcGIS HUB.
Data Processing in QGIS:

Interpolate Wind Speed Data:

Convert point data to raster using Inverse Distance Weighting (IDW) in QGIS.
Use the "IDW Interpolation" tool: Select the point layer for wind speed, specify the Z-value field (wind speed), set the output raster size and coordinate system, then run the tool.
Calculate Slope from DTM:

Use the "Slope" tool in QGIS: Input the DTM raster from Global Wind Atlas and generate the slope raster.
Rasterize Vector Layers (Cities, Power Transmission Lines, Nature Protection Areas):

Use the "Rasterize (Vector to Raster)" tool: Select the input vector layer and set the attribute field to rasterize. Define the output raster resolution and coordinate system, then run the tool.
Calculate Distance Rasters:

Use the "Proximity (Raster Distance)" tool: Input the rasterized layer (e.g., cities) and generate the distance raster. Repeat for power transmission lines and nature protection areas.
Step 2: Data Standardization Using Fuzzy Logic
Import Data into QGIS:

Load all prepared raster datasets (wind speed, slope, distance to cities, distance to power transmission lines, distance to nature protection areas) into QGIS.
Fuzzy Standardization:

Apply fuzzy membership functions to standardize each raster layer.

Wind Speed:

Standardize wind speed values from 0 (least suitable) to 1 (most suitable) using a linear transformation.
Slope:

Apply a decreasing function as gentler slopes are more suitable.
Distance to Cities:

Apply an increasing function, as greater distances from cities are more suitable.
Distance to Nature Protection Areas:

Apply an increasing function, as greater distances from protected areas are more suitable.
Distance to Power Transmission Lines:

Apply a decreasing function, as closer proximity to transmission lines is more suitable.
Step 3: Assign Weights Using AHP
Define Criteria and Weights:

Criteria: Wind speed, slope, distance to cities, distance to power transmission lines, distance to nature protection areas.
Use AHP to assign weights to each criterion based on their importance.
Pairwise Comparison Matrix:

Construct a matrix and obtain weights from the comparison.
Ensure consistency ratio (CR) ≤ 0.1.
Assign Weights in QGIS:

Use the "Raster Calculator" to multiply each standardized raster by its respective weight.
Step 4: Combine Weighted Layers Using WLC
Weighted Linear Combination (WLC):
Sum the weighted standardized layers to create the final suitability map.
Step 5: Final Suitability Map and Analysis
Generate Suitability Map:

The WLC calculation results in a raster map indicating the suitability of each area for wind farm development.
Reclassify Suitability Map:

Use the "Reclassify" tool to categorize the suitability map (e.g., very low, low, moderate, high, very high).
Visualize and Interpret Results:

Analyze the suitability map to identify the best locations for wind farms.
Validation:

Validate results with field data or additional expert input to ensure practical feasibility.
Results and Analysis
Integration of Tools and Uncertainty Reduction
The integration of GIS, multi-criteria decision analysis (MCDA) using AHP, fuzzy logic, and the weighted linear combination (WLC) method in QGIS has demonstrated significant advantages in the wind farm site selection process. By combining these tools, we have effectively reduced the uncertainty inherent in the decision-making process. Each tool contributes to different aspects of the analysis:

GIS provides a robust spatial analysis platform that allows for precise mapping and analysis of various environmental and socio-economic factors.
AHP helps in assigning relative weights to each criterion based on expert judgment, ensuring that the importance of each factor is appropriately considered.
Fuzzy Logic standardizes the criteria into a common scale (0-1), accommodating the inherent vagueness and uncertainty of spatial data.
WLC combines the weighted criteria into a single suitability map, facilitating an integrated assessment of all factors.
Suitability Map and Key Findings
The final suitability map generated through the WLC approach highlights areas with varying degrees of suitability for wind farm development in Mendocino, California. The map was categorized into five classes: very low, low, moderate, high, and very high suitability. Here are the key findings from the analysis:

Coastal Proximity:

Locations close to the coast exhibit higher suitability for wind farm development. This is primarily due to higher wind speeds and relatively flat terrain, making these areas ideal for harnessing wind energy.
Environmental and Socio-Economic Factors:

Areas farther from nature protection zones, urban centers, and major infrastructure such as power transmission lines are also identified as highly suitable. These factors help minimize environmental impacts and reduce costs associated with grid connection and infrastructure development.
Wind Speed:

High wind speed areas, particularly those identified using data from the Global Wind Atlas and interpolated through IDW in QGIS, show strong potential for wind farm sites. Wind speeds between 6-7 m/s are deemed optimal for wind energy generation.
Slope:

Gentle slopes (3-5%) are preferred as they facilitate easier construction and maintenance of wind turbines.
Conclusion
The integration of GIS, AHP, fuzzy logic, and WLC in QGIS provides a comprehensive and effective methodology for wind farm site selection. This approach not only reduces uncertainty but also ensures that all relevant factors are considered in a systematic and weighted manner. The suitability map clearly indicates that coastal areas and regions with high wind speeds, gentle slopes, and favorable proximity to infrastructure are the most suitable for wind farm development in Mendocino, California. This integrated methodology can be applied to other regions and renewable energy projects to enhance decision-making and site selection processes.






