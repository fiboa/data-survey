# Planet Field Boundaries

## Submission Details

- **Submitter (Affiliation):** Matej Batič, Planet Labs
- **Data Provider (Legal Entity):** Planet Labs PBC
- **Homepage:** https://area-monitoring.sinergise.com/docs/markers/field-delineation/

## Overview

The field delineation marker produces boundaries of the agricultural parcels by clustering the agricultural pixels according to spatial, spectral and temporal properties. The delineated boundaries can aid the farmers speed up the declaration process and the paying agencies to better monitor changes in agricultural use. 

## Data

- **URL:** n/a 
- **Documentation:** https://medium.com/sentinel-hub/automatic-field-delineation-new-release-1c2938399f0
- **File Format:** GeoPackage
- **Projection:** EPSG:4326
- **License:** Commercial
- **Data Creation Details:** output of deep learning model
- **Computer Vision / AI Details:**  We use a deep neural network based on the popular U-net architecture to estimate the parcel’s extent, boundary, and the distance of the segmented image pixels to the boundary. We added a super-resolution layer to our U-net architecture to produce estimates of extent and boundaries at 4x the input image resolution: given the four B02, B03, B04, and B08 Sentinel-2 bands at 10 m pixel size, the network estimates parcel boundaries at 2.5 m. 



### Properties

| Property | Data Type | Constraints | Description |
| -------- | --------- | ----------- | ----------- |
| polygon_id | integer | >=0 | Each polygon in the resulting GeoPackage file has assigned a unique identification number. | 
| area_ha | number | > 0 | Polygon area in hectares. |
| micd | number | > 0 | Maximum Inscribed Circle Diameter (MICD) is an intuitive proxy for the width of a field, even in case of rotated and narrow-but-curved fields. | 
| ca_ratio | number | > 0 | Circumference-Area ratio (CA ratio) is calculated by dividing the circumference of a given polygon by the square root of its area. This ratio is then adjusted so that a circle corresponds to 0, and scaled so that a square corresponds to 1. |
| qa | integer | 0,1,2 | The Quality Assessment attribute presents three values: <ul><li>0: Polygons with high quality, i.e. with micd > 30 m.</li><li>1: Polygons with micd < 30 m. The quality for these polygons cannot be guaranteed.</li><li>2: Polygons clipped by the AOI.</li></ul> |



### Example

https://devext.sinergise.com/parcelio/

