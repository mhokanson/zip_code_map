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