# USDA Crop Sequence Boundaries

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** United States Department of Agriculture (USDA) National Agricultural Statistics Service (NASS)
- **Homepage:** https://www.nass.usda.gov/

## Overview

Crop Sequence Boundaries (CSB) is a vector-based geospatial dataset which are fully synthetic representations of agricultural fields, their acreage, and cropping rotation history. These new data are primarily derived from a historical stack of Cropland Data Layers over a set time frame based on an algorithm of geospatial functions. It was developed in cooperation with the Economic Research Service.

The Crop Sequence Boundaries (CSB) developed with USDA's Economic Research Service, produces estimates of field boundaries, crop acreage, and crop rotations across the contiguous United States. It uses satellite imagery with other public data and is open source allowing users to conduct area and statistical analysis of planted U.S. commodities and provides insight on farmer cropping decisions.

NASS needed a representative field to predict crop planting based on common crop rotations such as corn-soy and ERS is using this product to study changes in farm management practices like tillage or cover cropping over time.

CSB represents non-confidential single crop field boundaries over a set time frame. It does not contain personal identifying information. The boundaries captured are of crops grown only, not ownership boundaries or tax parcels (unit of property). The data are from satellite imagery and publicly available data, it does not come from producers or agencies like the Farm Service Agency.

Available free for download at https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/. 
Github repository containing the code used to create the Crop Sequence Boundaries (CSB) can be found at 
https://github.com/USDA-REE-NASS/crop-sequence-boundaries/tree/main/csb-project.

## Data & Metadata

- **URL:** https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/datasets/NationalCSB_2016-2023_rev23.zip
- **Documentation:** https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/index.php
- **Documentation:** https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/metadata_Crop-Sequence-Boundaries-2023.htm
- **Code list:** https://www.nass.usda.gov/Research_and_Science/Cropland/docs/CDL_codes_names_colors.xls
- **File Format:** ESRI-GDB/zip
- **Projection:** "Albers Conical Equal Area as used by mrlc.gov (NLCD)" [info](https://gis.stackexchange.com/questions/59673/calculating-points-in-the-usdas-cropland-data-layer-coordinate-system)
- **License:** The USDA NASS Crop Sequence Boundaries and the data offered at https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries are provided to the public as is and are considered public domain and free to redistribute. Users of the Crop Sequence Boundaries (CSB) are solely responsible for interpretations made from these products. The CSB are provided 'as is' and the USDA NASS does not warrant results you may obtain using the data. Contact our staff at (SM.NASS.RDD.GIB@usda.gov) if technical questions arise.


### Properties

| Property     | **Data Type** | Constraints | Description       |
|--------------|---------------|-------------|-------------------|
| CSBID        | String        |             | Identifier        |
| CSBYEARS     | String        |             |                   |
| CSBACRES     | Real          |             | Area in acres     |
| CDL2016      | Integer       |             | Crop code 2016    |
| CDL2017      | Integer       |             | Crop code 2017    |
| CDL2018      | Integer       |             | Crop code 2018    |
| CDL2019      | Integer       |             | Crop code 2019    |
| CDL2020      | Integer       |             | Crop code 2020    |
| CDL2021      | Integer       |             | Crop code 2021    |
| CDL2022      | Integer       |             | Crop code 2022    |
| CDL2023      | Integer       |             | Crop code 2023    |
| STATEFIPS    | String        |             | State identifier  |
| STATEASD     | String        |             | State identifier  |
| ASD          | String        |             |                   |
| CNTY         | String        |             | County            |
| CNTYFIPS     | String        |             | County identifier |
| INSIDE_X     | Real          |             |                   |
| INSIDE_Y     | Real          |             |                   |
| Shape_Length | Real          |             |                   |
| Shape_Area   | Real          |             |                   |


### Example

See https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/Viewer/index.php
