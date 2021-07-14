# Project title 

Copernicus Land And Atmospheric Monitoring For Estimating Groundwater Recharge

# Project description

Accurate estimation of the spatial and temporal distribution of recharge are important for groundwater flow and contaminant transport prediction and data interpretation (Westenbroek 2009). Jyrkama and Syke (2007) has found that the use of physically based, spatially variable recharge boundary condition in transient groundwater modeling problems improves the model performance.

The objective of the project is to realize a methodology that uses data from earth observation to estimate the groundwater recharge. The project areas correspond to the Po basin area in northern Italy; the 71.000 km2 area include a variety of land characteristic, uses and elevations.  The methodology include preprocessing of existing data and rely of existing code to estimate the Groundwater recharge.
The United States Geological Survey (USGS) has developed the Soil Water Balance (SWB) computer code to calculate the spatial and temporal variation in groundwater recharge. This program evaluate the recharge rate separately  for each grid cell in the model domain. To obtain an accurate estimate of the SWB recharge rate the software uses climate data and landscape characteristics information.

rehcarge=(precipitation+snowmelt+inflow)−(interception+outflow+evotranspiration)−∆soil moisture 

Required input data includes tabular and  gridded data files: 

	• Land used (integer Grid). The idea is to use CORINE Land Cover (Copernicus) data to generate a grid with the required information on land uses. 
	
	• Hydrologic soil Group (integer grid).
	The hydrological Group is based on the potential runoff estimation. The soil is associated to one of the 4 hydrological group A,B,C or D from the highest infiltration soil to the lowest. The main parameter used to evaluate the hydrological group is the saturated soil permeability (Ksat) which can be estimated relying on available Pedo-transfer functions (PTF). There exist many PTF in literature which can be divided in two main categories: data driven PTF and Physical based PTF. The idea is to choose appropriate PTFs based on the required input data and by looking at similar studies. The selected PTFs are calibrated, validated, and compared using some local in-situ information provided by local authorities (i.e., APRAV and ARPAE).
	
	• Surface water Flow direction (integer grid).
	The surface water flow direction is toward the neighboring grid cell that has lower elevation and is evaluated using the Digital Elevation Model.
	
	• Available soil-water capacity (real number grid).
	The information used to assess Ksat includes at least the soil type. It can be also used to calculate the available soil water capacity (Dripps 2003). 
	
	• Land use (Lookup Table) and Soil moisture retention table.
	For the land use and soil moisture retention table, information is taken from similar data used in other studies or from information provided by regional and local authorities.
	
	• Climate data (tabular or gridded data)
It is planned to use the Copernicus Atmospheric Monitoring Service to implement gridded climate input data.

The project is uploaded to allow the community to integrate input with a possible long-term goal of a European-wide implementation.

# Instructions:
The Demo_and_swb_executable folder contains the code to evaluate the recharge. The code is the one available on the USGS website (https://www.usgs.gov/software/swb-modified-thornthwaite-mather-soil-water-balance-code-estimating-groundwater-recharge).

The folder contains a .zip file. The zipped folder contains SWB.exe and all the folder placed correctly to allow the code to access to the input and set up files. The files to run a demonstration case for the Po river basin are already placed in the correct folders (except for the climate data).
To execute the code and prepare the input please follow the README.txt contained in the folder.

For more details on the models implemented in SWB and input requirements please refer to the User Guides and Technical Information in Westenbroek, S.M., Kelson, V.A., Dripps, W.R., Hunt, R.J., and Bradbury, K.R., 2010, SWB-A modified Thornthwaite-Mather Soil-Water-Balance code for estimating groundwater recharge: U.S. Geological Survey Techniques and Methods 6-A31, 60 p.

Before running the demonstration you can generate or download the input data using the python notebooks available in the other folders. The notebooks describe the codes to generate the input, or the method used to generate them. The folders already contain all the input to run the codes for the demonstration case.
The result to be obtained are already loaded in the Demo_and_swb_executable.zip file (except for the climate data).

# note:
The notebooks (except the ones contained in the Demo_and_swb_executable folder) has been prepared and tested using Google Colab. If executed of line it may be necessary to install some libraries.

# References 

Westenbroek, S.M., Kelson, V.A., Dripps, W.R., Hunt, R.J., and Bradbury,  K.R. 2009 SWB-A modified Thornthwaite-Mather Soil-Water-Balance code for estimating groundwater recharge, Techniques and Methods 6-A31, Groundwater Resources Program.

Jyrkma, M.I., and Sykes, J.F. 2007, The impact of climate change on spatially varying groindwater recharge in the GradnRiver watershed (Ontario) Journal of Hydrology , v.338, no. 3-4, p.273-250. 

Dripps, W.R., 2003, The spatial and temporal variability  of groundwater recharge within the Troit lake basin of northern Wisconsin 
