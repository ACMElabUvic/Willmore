# Willmore
Test repository for willmore camera data

<hr>

### GENERAL INFORMATION

**Project Information**   
UPDATE FOR WILLMORE

Details for the Willmore Wilderness research program [here](http://www.acmelab.ca/willmore.html).

Also visit the [ACME website](http://www.acmelab.ca/osm2022.html) more information about the ACME lab.

**Author Information (data):**  
 Principal Investigator Contact Information  
 Name: Jason T. Fisher, PhD   
 Institution: University of Victoria  
 Address: 3800 Finnerty Rd, Victoria, BC V8P 5C2  
 Email: [fisherj@uvic.ca](mailto:fisherj@uvic.ca) 

**Author Information (code):**  

**Date of data collection:** 

**Geographic location of data collection:** TO FILL IN 

INPUTS
OUTPUTS
RELEVANT LITERATURE

DETAILS ON INPUTS

DETAILS ON OUTPUTS


**File List:**  

*Files in main folder*
		
* <span style = "color: #7B0F17;">**OSM_2022-2023.Rproj**</span>; R project to run code for data cleaning and analyses. 

*Files in data folder*

**relevant literature**  
This folder provides pdf copies of previously published papers using the Willmore Wilderness remote camera dataset. The purpose of this folder is to provide background/information on previously published work using this dataset. Note that sample numbers may vary between individual manuscripts due to specifics of individual projects, as well as the multiple deployment designs within the Willmore dataset.

<hr>

### Data specific information for : [outputs/willmore_camop.csv]  

* **Number of variables/columns:** 5
* **Number of observations/rows:** 115 (one per camera site) 

**Variable List:**
* site : camera site ID
* Easting : camera site Easting location
* Northing : camera site Northing location
* start_date : first day of camera operation as recorded by a camera trigger (no timelapse function used)
* end_date : last day of camera operation as recorded by a camera trigger (no timelapse function used)

### Data specific information for : [outputs/willmore_30min_independent_detections.csv]  

* **Number of variables/columns:** 5
* **Number of observations/rows:** 19072 (one row for each independent detection of a species at each site) 

**Variable List:**
* site : camera site ID
* datetime : the datetime (year-month-day hour:minute:second) of the first camera image of each independent detection. Multiple images may be taken during a detection event, and this data has been sliced to the first image for simplicity. Note there was an error in the raw data resulting in no "seconds" being recorded from the timelapse data, therefore all detections end at the top of the hour (e.g. 6:03:00 AM). This should be of little consequence, but is annoying. 
* species : the species in the independent detection. Note this still contains "Unknowns" and will need to be filtered/cleaned before any analysis.
* timediff : the difference in time between subsequent independent detections (mins). Note this could be calculated using the datetime column between subsequent detections. NA's represent the first detection of a species at a given camera, as there can be no difference in time from this event to a previous event. 
* Event.ID : a unique identifier for a species' independent detection at a camera site. 



**relevant literature**
 * Barnas et al. 2024 How landscape traits affect boreal mammal responses to anthropogenic disturbance.
 * Fisher and Bradbury 2014 A multi-method hierarchical modeling approach to quantifying bias in occupancy from noninvasive genetic tagging studies
 * Fisher et al. 2011 Body mass explains characteristic scales of habitat selection in terrestrial mammals
 * Fisher et al. 2013 Spatial segregation of sympatric marten and fishers- the influence of landscapes and species-scapes
 * Fisher et al. 2014 Spatial patterns of breeding success of grizzly bears derived from hierarchical multistate models
 * Frey et al. 2020 Move to nocturnality not a universal trend in carnivore species on disturbed landscapes
 * Khan et al. 2023 Shifts in diel activity of rocky mountain mammal communities in response to anthropogenic disturbance and sympatric invasive white-tailed deer
 * Stewart et al. 2015 Wolverine behavior varies spatially with anthropogenic footprint - implications for conservation an inferences about declines
