# Norway AR50 Agricultural land

Norway lacks a decent, open crop field map. The Norwegian governments publish a decent amount of open data,
however not crop fields. After some deliberation, we will try to use the AR Land resource map with a categorization for
Agricultural land. The fine-grained AR5 map is off limits, so for now we settle for the coarser grained AR50
(Land resource map 1:50.000) - Agricultural land.

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** NIBIO - Norsk institutt for bioøkonomi
- **Homepage:** https://www.nibio.no/en

## Overview

Land type "20 Agricultural land" grouped into the following classes from AR5: 24) Fully and surface cultivated land; 25) Pasture; 99) Unspecified agriucultural land.

The national land resource database (AR) classifies the land cover of mainland Norway according to its 
suitability for agriculture and natural plant production. National land resource datasets are available 
at scale 1:5.000 (AR5), 1:50.000 (AR50) and 1:250.000 (AR250). AR50 is the Norwegian medium resolution land resource 
dataset which covers the whole of mainland Norway. It is build and maintained for cartographic representations 
at regional level (1:100.000 to 1:300.000). The dataset is not intended for spatial analysis. Features in 
AR50 are continuous areas representated as polygons with attributes assigned according to the AR50 classification 
criteria. The primary level of classification is land type (arealtype) based on a combination of land cover and 
land useSecond level attributes are forest site quality class (skogbonitet) and forest cover type (treslag). 
Areas above the tree line, mountains and other open areas have been classified according to richness of the vegetation. 
AR50 contain also includes information about arable land when the land cover is bare land, marsh or forest. 
In AR50, the general minimum mapping unit is 1.5 hectares for polygons that have identical combinations of 
attribute values. Smaller mapping units occur between identical land types if they have different 
forest cover or forest site quality.

The dataset is primarily intended as a visual product for use in conjunction with land use planning, 
public management, agriculture and forestry. The dataset is not suitable for geometric analysis or area statistics 
in areas below the tree line. For this purpose, please use AR5. Note that AR5 is not available 
for download without an agreement with NIBIO who represents the agricultural partners in the 
National Spatial Data Infrastructure - “Norway Digital”.

## Data & Metadata

- **URL:** https://kartkatalog.geonorge.no/metadata/ar50-land-resource-map-150000-agricultural-land/76255ebe-2a0e-401e-87c8-7618dd196cf2
- **Documentation:** https://register.geonorge.no/data/documents/produktspesifikasjoner_ar50_v3_produktspesifikasjon-nibio-ar50-20220523_.pdf
- **File Format:** FileGDB
- **Projection:** EPSG:4258
- **License:** Norsk lisens for offentlige data (NLOD)
- **Attribution:** NIBIO - Norsk institutt for bioøkonomi / Norwegian Institute of Bioeconomy Research

Filter for `artype == 20`, which stands for land class "fully cultivated land, superficially cultivated land, and home fields grazing land".

### Properties

| Property  | **Data Type** | Constraints | Description                        |
|-----------|---------------|-------------|------------------------------------|
| artype    | Integer       |             | Arealtype; main categorization     |
| arskogbon | Integer       |             | Skogbonitet; forest quality        |
| artreslag | Integer       |             | Treslag; kind of wood              |
| arjordbr  | Integer       |             | Jordbruk; Agriculture              |
| arveget   | Integer       |             | Vegetasjonsdekke; Vegetation cover |
| areal     | Real          |             | Area                               |
| arkartstd | String        |             | Kartstandard; map standard         |
| kilde     | String        |             | Source                             |


| Property | code | name                              | description                                  |
|----------|------|-----------------------------------|----------------------------------------------|
| arjordbr | 24   | Fulldyrka- og overflatedyrka jord | Fully cultivated and surface cultivated soil |
| arjordbr | 98   | Ikke relevant                     | Not relevant                                 |
| arjordbr | 25   | Innmarksbeite                     | Inland pasture                               |
| arjordbr | 99   | Uspesifisert jordbruksareal       | Unspecified agricultural area                |

