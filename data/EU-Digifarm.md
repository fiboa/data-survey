# Merelbeke, Belgium

## Submission Details

- **Submitter (Affiliation):** Santiago Nullo (Digifarm)
- **Data Provider (Legal Entity):** Digifarm (Private)
- **Homepage:** https://digifarm.io/

## Overview

We delineate field boundaries and seeded acres in the growing season based on the super-resolved Sentinel-2 at 1m per pixel using 4-bands (RGB + NIR) and we serve the latest, most up-to-date data through our API to your digital solution (or through Shape/KML/Geojson), which is crucial for in-season analysis and season-planning.

Field boundaries are served as Geojson via API for a given point, bbox or field id. Field id can be obtained from a low resolution API endpoint (that allows to show low res polygons on the map for the user to select the field and get a high res boundary).

## Data & Metadata

- **URL:** https://digi-map.s3.eu-central-1.amazonaws.com/dev-raster-viewer/index.html?tables=demo_belgium_merelbeke#12.55/50.95761/3.74169
- **Documentation:** Available online
- **File Format:** GeoPackage / Shapefile / GeoJson
- **Geometry Format (if different from data):** -
- **Metadata Format (if different from data):** -
- **Projection:** EPSG:4326 
- **License:** *No license information found*

### Properties

Some of the documented fields are missing in the GeoPackage. These are marked with "(missing)".

| Property              | **Data Type** | Constraints                | Description                                                  |
| --------------------- | ------------- | -------------------------- | ------------------------------------------------------------ |
| ID                    | integer       | not null                   | Identifier                                                   |
| AREA                  | string        | 200 chars                  | Area (ha)                                                    |
| PROPS                 | string        | json string                | Feature properties                                           |
| PERIMETER             | number        | >0                         | Perimeter (m)                                                |
| CONFIDENCE            | number        | 0-100                      | Automatic delineation confidence level                       |


## API

The API provides a GeoJSON object of delineated fields in the given bbox. Returned GeoJSON features will be limited to max 1000 features. In case you get 1000 features, split the querying bbox further to get complete features.

API: https://digifarming.readme.io/reference/get_delineated-fields