# Landslide_-Identifier
Landslides often interfere with the economic development of rural communities. Our target is to make a system for warning them before the hazard.

## Factors Considered

In here, we were considered six factors for this task. The research reports and geological references were used to select those factors.
Topographic parameters like slope, curvature and distance to stream maps were derived from Digital Elevation Model of Badulla District.
Landslide occurs more frequently on steeper slopes due to gravity stress. 
Curvature was classified into 3 classes of concave, convex and flat surfaces. In heavy rainfall, a convex or concave slope contains more water and retains this water for a longer period. So, more positive or negative values indicate the higher probability of landslide occurrence. In the flat curvature, the probability of landslide occurrence is very low. 
Distance to stream is an important factor that dictates the landscape evolution of the area and an indicator of the landslide and related erosional aspects. 
Landslides are greatly controlled by the lithology properties of the land surface. Since different lithological units have different landslide susceptibility values. They are very important for providing data for susceptibility and it displays approximate boundaries of geology. 

Rainfall is considered as an influencing factor to cause slope instability. Precipitation is a controlling factor that triggers landslides by providing water thereby increasing underground hydrostatic level and pore water pressure. 
Land-use change has been recognized throughout the world as one of the most important factor influencing the occurrence of rainfall-triggered landslides. Vegetation has a major contribution to resist slope movements.

## Landslide Inventory

The landslide inventory dataset in the current study consist a total of 25 landslides as right side map which were identified from NASA Map & App Gallery. In this study, the specific date of landslide occurrence is not well known. It was difficult to find polygon inventory map for badulla district. So, the inventory map was created using IDW interpolation method and you can see it in left side.

## Methodology

The methodology involved selection of factors, generation of data layers in GIS, numerical rating and weighting assignment to the factors, data integration in GIS, computation of the landslide potential index, suitable classification of landslide susceptibility and validation of the final resulting map using existing landslide inventory.

First, we gathered coordinates of the locations where landslides happened in Badulla area using NASA landslide viewer. Next, we created the inventory point map. After that, we created landslide distribution map using IDW method. We did so, because it was difficult to find a polygon map of relevant area. By the use of digital elevation modal of Badulla district, we created distance to stream, slope & curvature maps. Distance to stream map was developed from Euclidean distance buffering method in the spatial analyst tool of ArcGIS. Meteorological data was used to create the rainfall map. Inverse distance weight method was used to distribute the data over the region. Google earth images were used to create the land use map. Lithology map was created by referring data of ORR associates.Using elevation data, we created elevation map of badulla district. Land use & lithology maps were converted to raster. All the maps were resampled into 30m spatial resolution and projected into WGS 84 coordinate system. Weights were assigned accordingly using SDM Modelling and geological references as shown. Each classes of Curvature, land use, lithology, distance to stream maps' weights were assigned using spatial data module. Geological references were used to assign the weights for classes of slope, rainfall and elevation maps. Reclassification process was done using above assigned weights. Weights for each factor were assigned using geological references. Finally landslide susceptibility map was created using Landslide Susceptibility Index. Then it was converted to geojason file & used in mobile application.


## Landslide causative Factors

Assigning appropriate rates and weights for causative factors and their sub classes were the important parts of the study and it was leaded to the final Risk map.
In here, the weights for each classes of each factor were assigned. Geological references were used to reclassify classes of slope map, curvature map and elevation map. It was difficult to reclassify the classes of landuse map, Lithology map, distance to stream map and curvature map. So, a external tool box called “Spatial Data Modeller” was installed into Arcgis to assign the weights of each class of above factors. The land slide inventory map was used as the training layer for this task and we found how the factors effect to land slide occurrences. 


## Weights of Evidence

The landslide susceptibility map of the study area by WoE model was produced based on the weighted values from the seven causative factors and the landslide inventory. The table shows the factors and weights that we assigned. The final risk map was prepared by summing the weight of all that eight causative factors using a raster calculator in ArcGIS.

## Landslide Susceptibility Index(LSI)

In LSI model, reclassified factor maps were overlaid and weights ranging from 0% to 100% were assigned to each factor. For this study, the weight values were assigned based on the percentage of landslides in the highest ranked category of individual factors and geological references. This information was transferred in GIS database and Raster Calculator of the spatial analyst tool was used to calculate LSI as shown in the equation.

      LSI=  ((w1*x1)+(w2*x2)+(w3*x3)+(w4*x4)+(w5*x5)+(w6*x6)+(w7*x7))/7
                                                                   

After the analyzing, the LSI value ranged from 16 to 50 in this study. Finally, LSI map was reclassified into four susceptibility categories to prepare the landslide susceptibility map of the study area as follows, 

•	16 to 24 value range is as Very low risk area

•	24 to 31 value range is as low risk area

•	31 to 38 value range is as moderate risk area

•	38 to 50 value range is as high risk area


## Final Risk Map

Following table shows the areas of each category in square kilometers and the percentages of each risk category with corresponding to the total land area of badulla district.


High Risk Area = 159.767 km2 (6%)

Moderate Risk Area = 1060.939km2 (40%)

Low Risk Area = 987.539  km2   (34%) 

Very Low Risk Area = 451.913 km2 (17%) 


●	Above percentages and Landslide susceptibility Map was used for mobile application.

## Mobile Application Demo-https://www.youtube.com/watch?v=VsrYYLDj-0g

## Project Video-https://www.youtube.com/watch?v=6p9-90qIyhM
