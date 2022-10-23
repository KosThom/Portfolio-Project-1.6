# Portfolio-Project-6
PowerBI Dashboard using cleaned data from Portfolio Project 1.
Our scope in this Project is to use the already cleaned (via SQL) Nashville-Housing dataset from Project 1 (almost 25.000 rows of data), in order to create an interactive dashboard in PowerBI.
The following steps were applied:
  1. At first we used excel to break down the dataset into three separate sheets (within the same excel file), namely Housing, Location and Date.
     In the latter only the distinct values of sale dates were included, so that an independent calendar table could be created in PowerBI.
  2. Before we import the 3 sheets into PowerBI, the query editor was used mainly in order to create some new columns in the date table and change some data types in the Housing and Location Tables.
  3. Within the Data tab, all date formats were converted in m/d/yyyy form (Date and Housing Tables), the LandValue, BuildingValue and TotalValue Fields were converted in US currency format
     and all geographical fields within the Location table were converted in Geospatial data. Moreover, a new column was created (Property_City_Location) due to geolocation problems on the map (some places appeared in other countries) by merging PropertyCity and OwnerState columns
     (did prior check that all Ownerstate data were identical with the PropertyState).
  4. The relationships between the 3 tables were created in the Modelling tab. 
  5. Added DAX measures: Created Price-Tier, LandValue-Tier, Acreage-Tier and YearBuilt-Tier columns using IF.
                         Created Total Houses Sold Measure using DISTINCTCOUNT.
                         Created Total Sales Measure using SUMX.
                         Created Average Sale Price and Average Land Value using AVERAGE,
                         as well as some other measures using CALCULATE, ALL and some Time Intelligence formulas
  6. Finally the dashboard was created. The "edit interaction" button in the format sheet was used so that all charts, matrixes and maps to be filtered and not just highlighted when one of them is used as reference.  
 
