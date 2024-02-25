# AI4SmallFarms: A Dataset for Crop Field Delineation in Southeast Asian Smallholder Farms

## Submission Details

- **Submitter (Affiliation):** Snehal Chaudhari, ASU.
- **Data Provider (Legal Entity):** 
   - Prof. Dr. Ir. C Persello (University of Twente, Faculty of Geo-Information Science and Earth Observation (ITC))
   - J Grift (University of Twente, Faculty of Geo-Information Science and Earth Observation (ITC))
   - Dr. X Fan (Delft University of Technology (TU Delft))
   - Dr. Ir. C Paris (University of Twente, Faculty of Geo-Information Science and Earth Observation (ITC))
   - Dr. R Hänsch (German Aerospace Center (DLR))
   - Dr. M. N. Koeva (University of Twente, Faculty of Geo-Information Science and Earth Observation (ITC))
   - Prof. Dr. A Nelson (University of Twente, Faculty of Geo-Information Science and Earth Observation (ITC))
- **Homepage:** https://easy.dans.knaw.nl/ui/datasets/id/easy-dataset:321745

## Overview

This repository contains an open data set for training and benchmarking machine learning methods to delineate agricultural field boundaries in polygon format. The large-scale data set consists of 439,001 field polygons divided into 62 tiles of approximately 5x5 km distributed across Vietnam and Cambodia, covering a range of fields and diverse landscape types.

## Data

<!-- Any important information about your field boundary data and metadata,
e.g. in which format and projection the geometry is provided. -->

- **URL:** https://doi.org/10.17026%2Fdans-xy6-ngg6
- **Documentation:** https://easy.dans.knaw.nl/ui/datasets/id/easy-dataset:321745/tab/1
- **File Format:** GeoPackage
- **Projection:** EPSG:32648
- **License:** [CC BY 4.0](http://creativecommons.org/licenses/by/4.0)
- **Data Creation Details:** The field polygons were meticulously digitized using S2 and GM images.For each tile, all the visible crops were manually digitized. 

The data is origanized as follows: 
```
	- sentinel-2-asia/ (dataset with tiles from Vietnam and Cambodia)
		- reference/ (lines and area representations of the reference boundaries)
		- test/ (test images, masks and predictions)
		- train/ (train images and masks)
		- validate/ (validate images and masks)
		- tiles_asia.gpkg
		- benchmark.qgz (QGIS project with all the previously described data)
	- README.md
```
...

### Properties

<!-- A list of properties with e.g. a short description, data type, constraints such as value range or allowed values, etc. This can be found by opening the data file in qgis, then 
   right clicking on the layer and selecting 'layer properties', and then going to the 'fields' section. The 'name' in qgis is the property in this table, and the 'Type name' is the Data Type -->

Fields in tiles_asia.gpkg
| Property    | Data Type | Constraints | Description                     |
| ----------- | --------- | ----------- | ------------------------------- |
| id          | int64     |             | Tile Identifier                 |
| country     | string    |             | Country Name                    |
| split       | string    |             | 'train', 'test', 'validate'     |
| month       | int64     |             | Recored Month                   |
| year        | int64     |             | Recored Year                    |
| month_text  | string    |             | Month in text                   |
| end_day     | int64     |             |                                 |


Fields in [tile_id]_[country_name]_areas.gpkg

| Property    | Data Type | Constraints | Description                                                                                             |
| ----------- | --------- | ----------- | ------------------------------------------------------------------------------------------------------- |
| id          | int64     |             | Tile Identifier                                                                                         |
| country     | string    |             | Country Name                                                                                            |
| _predicate  | string    |             | No official description but looks like this check is the geometry in withi or intersectiong the parcels |

Valid values for _predicate are : INTERSECTS and WITHIN

### Example

- tiles_asia.gpkg

   | Property    | Example Value | 
   | ----------- | ------------- | 
   | id          | 0             |
   | country     | vietnam       |
   | split       | train         |
   | month       | 01            |
   | year        | 2021          |
   | month_text  | Jan           |
   | end_day     | 31            |


- [tile_id]_[country_name]_areas.gpkg

   | Property    | Example Value | 
   | ----------- | ------------- | 
   | id          | 0             |
   | country     | vietnam       |
   | _predicate  | INTERSECTS    |

