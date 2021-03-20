**An Analysis & Prediction of New York City Housing Complaints**

**Problem Statement**

**Problem Description:**

The people of New Yorker use the 311 system to report complaints about the non-emergency problems to local authorities. Various agencies in New York are assigned these problems. The Department of Housing Preservation and Development of New York City is the agency that processes 311 complaints that are related to housing and buildings. In the last few years, the number of 311 complaints coming to the Department of Housing Preservation and Development has increased significantly. Although these complaints are not necessarily urgent, the large volume of complaints and the sudden increase is possibly impacting the overall efficiency of operations of the agency. Therefore, a better solution for Department of Housing Preservation and Development will probably help them to manage the large volume of 311 complaints they are receiving every year.

**Questions to the Dataset:**

Which complaint type should the Department of Housing Preservation and Development of New York City focus on first?

Should the Department of Housing Preservation and Development of New York City focus on any specific geographical area (borough, zip codes, or street) for the determined complaint type?

Is there any obvious relationship between the characteristics of a house or building in the determined geographical area and the determined complaint type?

Can a predictive model be built for future possible complaints of the determined complaint type?

**Datasets used:**

For this project, we are planning to use the following 3 datasets to analyse & solve the questions stated above.

311-complaint dataset that contains information on complaints to the Department related to housing and building complaints https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9

PLUTO dataset which has information on every building's characteristics https://www1.nyc.gov/assets/planning/download/zip/data-maps/open-data/nyc_pluto_18v1.zip

We also found a coordinate data on the boundaries of New York boroughs that will be useful to help visualise the locations of a sample of heating complaints https://data.cityofnewyork.us/City-Government/Borough-Boundaries/tqmj-j8zm

**311 Complaint Dataset**
The original dataset is available at https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9 which can be downloaded by using the API.

This dataset contains metadata of complaints made to the Department relating to housing and building problems. The original 311 complaint dataset has 46 columns of information however, for this project, we are planning to use only a selection of the following columns to analyse the data. These were:

• Created Date - The date and time the complaint was made and entered into the 311 system

• Closed Date - The date and time the complaint was closed by the department

• Complaint Type - The category of complaint identifying the topic of the incident or condition

• Location Type - Describes the type of location used in the address information

• Incident Zip - Incident location zip code

• Incident Address - House number of incident address provided by submitter

• Street Name - Street name of incident address provided by the submitter

• Address Type - Type of incident location information available

• City - City of the incident location

• Status - Status of the complaint

• Resolution Description - Describes the last action taken on the incident. May describe next or future steps

• Borough - Borough of the incident location provided by the submitter

• Latitude - Geo based Lat of the incident location

• Longitude - Geo based Lat of the incident location

**PLUTO dataset for housing**
The PLUTO dataset which contains information on every building in New York City's characteristic will be used to find whether complaints have any correlation with complaints being made. obtained the data set from here: https://www1.nyc.gov/assets/planning/download/zip/data-maps/open-data/nyc_pluto_18v1.zip. This dataset contains a lot of information about individual buildings but the features we are planning to use in the analysis were:

• Lot Number - The number of the tax lot

• ZipCode - The zip code that the tax lot is located in

• Address - The address of the tax lot

• Lot Area - The total area of the tax lot in square feet

• Building Area - The total gross building floor area in square feet

• Residential Area - An estimate of the exterior dimensions of the portion of the structure(s) allocated for residential use

• Office Area - An estimate of the exterior dimensions of the portion of the structure(s) allocated for office use

• Retail Area - An estimate of the exterior dimensions of the portion of the structure(s) allocated for retail use

• Num of Buildings - The number of buildings on the tax lot

• Num of Floors - In the tallest building on the tax lot, the number of full and partial stories starting from the ground floor

• Lot Depth - The tax lot's depth measured in feet

• Building Depth - The building’s depth, which is the effective perpendicular distance, measured in feet

• Year Built - The year construction of the building was completed

• Year 1st Altered - If a building has only been altered once, this value is the date of the alteration. If a building has been altered more than once, this value is the year of the second most recent alteration.

• Floor Area Ratio - The Built Floor Area Ratio (FAR) is the total building floor area divided by the area of the tax lot

• Max Residential FAR - The Maximum Allowable Residential Floor Area Ratio (FAR)

• Max Commercial FAR - The Maximum Allowable Commercial Floor Area Ratio (FAR)

• Max Facility FAR - The Maximum Allowable Community Facility Floor Area Ratio (FAR)

• X Coord - The X coordinate of the XY coordinate pair which depicts the approximate location of the lot.

• Y Coord - The Y coordinate of the XY coordinate pair which depicts the approximate location of the lot.

**Data on borough boundaries in New York**
This contained geographical data about the boundaries of the boroughs in New York in a GeoJSON format. This will be useful to help with the analysis of the geographical effects on the number of complaints made. This data can be accessed from https://data.cityofnewyork.us/City-Government/Borough-Boundaries/tqmj-j8zm.


**Prediction Model Results **

For binary target (complaint made or not):

Logistic regression -> Jaccard score of 0.9899, F1 score of 0.99

**For predicting the number of complaints:**

K-Nearest Neighbors -> accuracy score of 0.97,

Multiple linear regression: Residual sum of squares of 31763.86, R^2/coeffient of determination of 0.07

**Conclusion**

Depending on the method the Department of Housing Preservation and Development wants to employ, it is possible to make a predictive model from the data they have.

If they would like to use the binary approach, a logistic regression model will be a good fit for future predictions.

On the other hand, if they would like to predict the total number of complaints for a building, then I would recommend the KNN model as I believe that it is a better fit than the multiple linear regression model.
