# Exploration of Business License Data in Calgary, Alberta, Canada

Here I explore a dataset of license transactions made by businesses in Calgary, Alberta, Canada downloaded directly from the Calgary Open Data Portal linked at the bottom of this README. 

**Column descriptions at time of download:**

- TRADENAME: the business name (eg. Walmart, Tim Hortons, Lenny's Vaccuum Cleaners)
- ADDRESS: address of business (eg. 11201 30 ST SW) 
- LICENCETYPES: type of business license, 88 unique types in data (eg. Liquor Store, Wholesaler)
- COMDISTNM: community district name (eg. BELTLINE, ARBOUR LAKE, SUNALTA)
- JOBSTATUSDESC: the description of the transaction with the city related to their business license: ['RENEWAL LICENSED', 'LICENSED', 'EXPIRED', 'RENEWAL INVOICED', 'PENDING RENEWAL', 'RENEWAL NOTIFICATION SENT'] 
- JOBCREATED: Date of transaction (eg. 2009/10/16 in yyy/mm/dd) 
- longitude, latitude: self-explanatory (floats)
- location: tuple of longitude, latitude as (longitude, latitude)
- Count: just a column of 1s

**Directory Description**

fig/ -> Any saved figures are saved here.

dat/ -> All data-files: raw, cleaned, and shapefiles of Calgary Community Boundaries

**Notes**

_All businesses created before October 7, 1994 reflect this date as their JOBCREATED date._ 

We use _Geopandas_ to merge the business license data with a map of Calgary (a shapefile (.shp) that knows the shape of each of Calgary's communities) that was also downloaded from Calgary Open Data. This allows us to show visually where areas as "booming" with new licenses and track this through time using the time of transaction.

**Dataset Provided By:** The City of Calgary

**Dataset Owner:** Calgary Open Data

**License/URL Attribution:** https://data.calgary.ca/d/Open-Data-Terms/u45n-7awa

**Directly Exported from:** https://data.calgary.ca/Business-and-Economic-Activity/Calgary-Business-Licences/vdjc-pybd

**Example figure from this analysis**:

![Calgary By Variable](/figs/community_boundaries_by_variable.png)
