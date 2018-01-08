# zip_code_map
## Synopsis
This project is intended to provide guidance on one possible way to match zip codes to a pair of lat/long coordinates and displaying those on a Google Map.

## Motivation
Several medical clinics have expressed interest in being able to map their patients homes for a rough idea where to expand services. This process gives them one possible way to see that.

## Requirements
* A valid [Google Maps API key](https://developers.google.com/maps/documentation/javascript/get-api-key)
* A working internet connection to reach the Google Maps service and reach the markerclusterer.js file hosted by Cloudflare.

## Notes
In this process all the pins are stored within the html document to reduce the number of data sources and connections that administrative staff need to connect to, especially when sharing maps with outside parties, like consultants. 

## Data Sources
[ZCTA crosswalk](https://udsmapper.org/zcta-crosswalk.cfm)
* Contains ZIP code to Zip Code Tabulation Area (ZCTA) mappings
[ZCTA coordinates](https://www.census.gov/geo/maps-data/data/gazetteer2017.html)
* Contains latitude and longitude for each ZCTA

Both have been matched into the zip_zcta_lat_long.csv file in this repository.


## Instructions
You need to match the zip codes you want to map to latitudes and longitudes to utilize them in Google Maps. How you do this will depend on where you are getting your zip code data from. In the sample map you should see that these are turned into an array of JSON objects with the properties "latitude", "longitude", and "Zipcode". The "Zipcode" property is optional and only there for human readability.

Once you have your JSON array you can use the [sample_map - template.html] as a starting point, making the following changes:

1. Replace <key> on line 40 with your own Google Maps API key
2. Replace the JSON array (lines 45-495) with your own data
3. You may also want to update where the maps centers at line 507
