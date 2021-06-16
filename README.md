# Project title 

Copernicus Land And Atmospheric Monitoring For Estimating Groundwater Recharge

# Project description

Accurate estimation of the spatial and temporal distribution of recharge are important for groundwater flow and contaminant transport prediction and data interpretation (Westenbroek 2009). Jyrkama and Syke (2007) has found that the use of physically based, spatially variable recharge boundary condition in transient groundwater modeling problems improves the model performance.

The objective of the project is to realize a methodology that uses data from earth observation to estimate the groundwater recharge. The project areas correspond to the Po basin area in northern Italy; the 71.000 km2 area will include a variety of land characteristic, uses and elevations.  The methodology will include preprocessing of existing data and will rely of existing code that will be adapted to estimate the Groundwater recharge.
The United States Geological Survey (USGS) has developed the Soil Water Balance (SWB) computer code to calculate the spatial and temporal variation in groundwater recharge. This program evaluate the recharge rate separately  for each grid cell in the model domain. To obtain an accurate estimate of the SWB recharge rate the software uses climate data and landscape characteristics information.

rehcarge=(precipitation+snowmelt+inflow)−(interception+outflow+evotranspiration)−∆soil moisture 

Required input data includes tabular and  gridded data files: 

	• Land used (integer Grid). The idea is to use CORINE Land Cover (Copernicus) data to generate a grid with the required information on land uses. 
	
	• Hydrologic soil Group (integer grid).
	The hydrological Group is based on the potential runoff estimation. The soil is associated to one of the 4 hydrological group A,B,C or D from the highest infiltration soil to the lowest. The main parameter used to evaluate the hydrological group is the saturated soil permeability (Ksat) which can be estimated relying on available Pedo-transfer functions (PTF). There exist many PTF in literature which can be divided in two main categories: data driven PTF and Physical based PTF. The idea is to choose appropriate PTFs based on the required input data and by looking at similar studies. The selected PTFs will be calibrated, validated, and compared using some local in-situ information provided by local authorities (i.e., APRAV and ARPAE).
	
	• Surface water Flow direction (integer grid).
	The surface water flow direction is toward the neighboring grid cell that has lower elevation and will be evaluated using the Digital Elevation Model.
	
	• Available soil-water capacity (real number grid).
	The information used to assess Ksat includes at least the soil type. It can be also used to calculate the available soil water capacity (Dripps 2003). 
	
	• Land use (Lookup Table) and Soil moisture retention table.
	For the land use and soil moisture retention table, information will be taken from similar data used in other studies or from information provided by regional and local authorities.
	
	• Climate data (tabular or gridded data)
It is planned to use the Copernicus Atmospheric Monitoring Service to implement gridded climate input data.

The project is uploaded to allow the community to integrate input with a possible long-term goal of a European-wide implementation.


# References 

Westenbroek, S.M., Kelson, V.A., Dripps, W.R., Hunt, R.J., and Bradbury,  K.R. 2009 SWB-A modified Thornthwaite-Mather Soil-Water-Balance code for estimating groundwater recharge, Techniques and Methods 6-A31, Groundwater Resources Program.

Jyrkma, M.I., and Sykes, J.F. 2007, The impact of climate change on spatially varying groindwater recharge in the GradnRiver watershed (Ontario) Journal of Hydrology , v.338, no. 3-4, p.273-250. 

Dripps, W.R., 2003, The spatial and temporal variability  of groundwater recharge within the Troit lake basin of northern Wisconsin 
