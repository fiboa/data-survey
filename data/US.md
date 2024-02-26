# USDA: Crop Sequence Boundaries (2022)

## Submission Details

- **Submitter (Affiliation):** Eddie Choi, Washington University in St. Louis
- **Data Provider (Legal Entity):** United States Department of Agriculture National Agricultural Statistics Service (USDA NASS)
- **Homepage:** https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/

## Overview

*The Crop Sequence Boundaries developed with USDA's Economic Research Service, produces estimates of field boundaries, crop acreage, and crop rotations across the contiguous United States. It uses satellite imagery with other public data and is open source allowing users to conduct area and statistical analysis of planted U.S. commodities and provides insight on farmer cropping decisions.*

*NASS needed a representative field to predict crop planting based on common crop rotations such as corn-soy and ERS is using this product to study changes in farm management practices like tillage or cover cropping over time.*

*CSB represents non-confidential single crop field boundaries over a set time frame. It does not contain personal identifying information. The boundaries captured are of crops grown only, not ownership boundaries or tax parcels (unit of property). The data are from satellite imagery and publicly available data, it does not come from producers or agencies like the Farm Service Agency.*

*From [Homepage](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/
)*

Note that there are annual datasets from 2015 ~ 2022, with the 2023 dataset set to be published in April 2024, along with updates on previous datasets to reflect changes and updates in methodology.

## Data

<!-- Any important information about your field boundary data and metadata,
e.g. in which format and projection the geometry is provided. -->

- **URL:** https://jeodpp.jrc.ec.europa.eu/ftp/jrc-opendata/DRLL/AI4BOUNDARIES/sampling/
- **Documentation:**
   - Documentation (as well as metadata):
      - https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/metadata_Crop-Sequence-Boundaries-2022.htm#1
   - Repository to create dataset:
      - https://github.com/USDA-REE-NASS/crop-sequence-boundaries/tree/main/csb-project
- **File Format:** Geodatabase (.gdb)
- **Geometry Format (if different from data):**
   - Geometry available in MultiPolygon
- **Metadata Format (if different from data):**
   - HTML, XML
- **Projection:**
   - EPSG:9822 (Planar Map Projection; Albers Equal Area Projection)
   - EPSG:4269 (Geodetic Model; North American Datum of 1983)
- **License:** U.S. Public Domain
- **Data Creation Details:** Created based on [Cropland Data Layers (CDL)](https://www.nass.usda.gov/Research_and_Science/Cropland/SARS1a.php)

### Properties

<!-- A list of properties with e.g. a short description, data type, constraints such as value range or allowed values, etc. This can be found by opening the data file in qgis, then 
   right clicking on the layer and selecting 'layer properties', and then going to the 'fields' section. The 'name' in qgis is the property in this table, and the 'Type name' is the Data Type -->

| Property | Data Type | Constraints | Description |
| -------- | --------- | ----------- | ----------- |
| SHAPE (geometry)  | MultiPolygon |        | Feature geometry. |
| CSBID | String | 15 digits of numbers | CSB Identifier: First (left) 2 places are state FIPS, places 3 and 4 are last two digits of the starting year used to create CSB, places 5 and 6 are last two digits of the ending year used to create CSB, remaining places are assigned sequentially. |
| CSBYEARS | String | 4 digits of numbers | Corresponds to places 3 ~ 6 of CSBID. |
| CBSACRES | Float |        | Area of polygon in acres. |
| R15 ~ R22 | Integer |        | Majority crop type within CSB polygon as identified as 20(15 ~ 22) CDL. |
| STATEFIPS | String | Composed of numbers | US State FIPS code. |
| STATEASD | String | Composed of numbers | US State FIPS code + USDA NASS Agricultural Statistics District (ASD). |
| ASD | String | Composed of numbers | USDA NASS Agricultural Statistics District (ASD). |
| CNTY | String |        | US County names. |
| CNTYFIPS | String | Composed of numbers | US County FIPs code . |
| INSIDE_X | Float |        | Center X coordinate of CSB polygon. |
| INSIDE_Y | Float |        | Center Y coordinate of CSB polygon. | 
| Shape_Length | Float |       | Shape length in meters. |
| Shape_Area | Float |        | Shape area in square meters. |

More information of which crop the values of properties R15 ~ R22 denote can be found in the metadata.

### Example

<!-- Please provide a link to the data or embed it into this document as a code block. -->
| Property     | Example Value   |
| --------     | -------------   |
| CSBID        | 271522000000003 |
| CSBYEARS     | 1522            |
| CSBACRES     | 2.853923        |
| R15          | 121             |
| R16          | 121             |
| R17          | 121             |
| R18          | 121             |
| R19          | 23              |
| R20          | 23              |
| R21          | 5               |
| R22          | 23              |
| STATEFIPS    | 27              |
| STATEASD     | 2710            |
| ASD          | 10              |
| CNTY         | Marshall        |
| CNTYFIPS     | 089             |
| INSIDE_X     | -65686.929489   |
| INSIDE_Y     | 2799947.170035  | 
| Shape_Length | 1644.136416     |
| Shape_Area   | 11549.418442    |

## API

<!-- Any important information about your API that is not captured in the chapters above,
e.g. an example response of a field boundary. -->

No publicly documented API found.

<!-- ### Example -->

<!-- Please provide a link to the data or embed it into this document as a code block. -->
