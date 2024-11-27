# Vlaanderen, Belgium

## Submission Details

- **Submitter (Affiliation):** Matthias Mohr
- **Data Provider (Legal Entity):** Agriculture and Marine Fisheries Agency of the Flemish government (Government)
- **Homepage:** https://landbouwcijfers.vlaanderen.be/open-geodata-landbouwgebruikspercelen
- **Alternative URL:** https://www.vlaanderen.be/datavindplaats/catalogus/landbouwgebruikspercelen-lv-2022

## Overview

Since 2020, the Department of Agriculture and Fisheries has been publishing a more extensive set of data related to agricultural use plots (from the 2008 campaign). 

From 2023, the downloadable dataset of agricultural use plots will also include the specialization given by the company (= company typology) and that is given to the plots of the company. Based on the typology, the companies are divided into 4 major specializations: arable farming, horticulture, livestock farming and mixed farms. The specialization of each company is calculated annually according to a European method and is based on the standard output of the various agricultural productions on the company. It is therefore an economic specialization and not a reflection of all agricultural production on the company. 

## Data & Metadata

- **URL:** https://landbouwcijfers.vlaanderen.be/open-geodata-landbouwgebruikspercelen
- **Documentation:** contained in the ZIP packages
- **File Format:** GeoPackage / Shapefile
- **Projection:** EPSG:31370 (Belgian Lambert 72)
- **License:** CC-0 (described as "Publiek" and "Toegang zonder voorwaarden")

### Properties

Some of the documented fields are missing in the GeoPackage. These are marked with "(missing)".

| Property              | **Data Type** | Constraints                | Description                                                                                  |
|-----------------------|---------------|----------------------------|----------------------------------------------------------------------------------------------|
| fid                   | integer       |                            | Identifier                                                                                   |
| BT_OMSCH              | string        | 200 chars                  | Business type (economic specialization)                                                      |
| BT_BRON               | string        | 50 chars                   | Source of the business type  (year of calculation or specialization indicated)               |
| GRAF_OPP              | number        |                            | Area (ha, accurate to 1m²)                                                                   |
| REF_ID                | integer       |                            | Unique identification number for the field.                                                  |
| GWSCOD_V              | string        | 5 chars (digits), nullable | Pre-cultivation code                                                                         |
| GWSNAM_V              | string        | 90 chars, nullable         | Pre-cultivation name                                                                         |
| GWSCOD_H              | string        | 5 chars (digits), nullable | Main cultivation/crop code                                                                   |
| GWSNAM_H              | string        | 90 chars, nullable         | Main cultivation/crop name                                                                   |
| GWSGRPH_LB            | string        | 150 chars, nullable        | Main cultivation/crop group name                                                             |
| GWSCOD_N              | string        | 5 chars (digits), nullable | First cultivation/crop code                                                                  |
| CWSNAM_N              | string        | 90 chars, nullable         | First cultivation/crop name                                                                  |
| GWSCOD_N2             | string        | 5 chars (digits), nullable | Second cultivation/crop code                                                                 |
| GWSNAM_N2             | string        | 90 chars, nullable         | Second cultivation/crop name                                                                 |
| AMKM (missing)        | string        |                            | Agri-environment code                                                                        |
| AMKM_LB (missing)     | string        |                            | Agri-environment name                                                                        |
| ECOREGELING (missing) | string        |                            | Eco-regulation code                                                                          |
| ECOR_LB (missing)     | string        |                            | Eco-regulation name                                                                          |
| BLS (missing)         | string        |                            | Planting subsidy code (forest farming systems)                                               |
| BLS_LB (missing)      | string        |                            | Planting subsidy name (forest farming systems)                                               |
| GESP_PM               | string        | 11 chars, nullable         | Specialized production method                                                                |
| GESP_PM_LB            | string        | 150 chars, nullable        | Description of specialized production method                                                 |
| BIOCERT (missing)     | string        | `J` or `N`                 | Plot under bio-control with a bio-control body.                                              |
| ERO_NAM               | string        | 20 chars,                  | Erosion color code for the field                                                             |
| STAT_BGV              | string        | 2 chars, nullable          | Status Permanent Grassland under greening (BG)                                               |
| MEERJARIG_GRASLAND    | string        |                            | Status Perennial Grassland (MG6 or higher). Example: MG16 = 16th year grassland              |
| LANDBSTR              | string        | 2 chars, nullable          | Agricultural region in which the center of the field is located                              |
| STAT_AAR              | string        | 10 chars, nullable         | Status Potatoes, follow up rotation duty                                                     |
| PCT_EKBG              | string        | 10 chars, nullable         | Percentage range of field that is ecologically sensitive permanent pasture. Example: `0-10%` |
| PCT_WETVEEN           | string        | 10 chars, nullable         | Percentage range of field that is wetland and/or peatland. Example: `0-10%`                  |
| PRC_GEM               | string        | 30 chars                   | Municipality in which the center of the field is located                                     |
| PRC_NIS               | string        | 5 chars (digits)           | NIS code of the municipality in which the center of the field is located                     |
| X_REF                 | number        |                            | X coordinate of the center of the field (Lambert)                                            |
| Y_REF                 | number        |                            | Y coordinate of the center of the field (Lambert)                                            |
| WGS84_LG              | string        | 11 chars                   | Longitude of the center of the field (WGS84). Example: `3°21'44"`                            |
| WGS84_BG              | string        | 11 chars                   | Latitude of the center of the field (WGS84). Example: `51°11'39"`                            |

Note: Many integer-like numbers are encoded as strings.

## API

The open data viewer https://geopunt.be/ shows the data in a viewer (search term: landbouwgebruikspercelen)
See https://www.vlaanderen.be/datavindplaats/catalogus/landbouwgebruikspercelen-lv-2022 for more info

| Standard     | URL                                                         | Documentation                                                                                        |
|--------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| OGC WFS      | https://geo.api.vlaanderen.be/Landbgebrperc/wfs             | https://www.vlaanderen.be/datavindplaats/catalogus/wfs-landbouwgebruikspercelen                      |
| OGC Features | https://geo.api.vlaanderen.be/Landbgebrperc/ogc/features/v1 | https://metadata.vlaanderen.be/srv/dut/catalog.search#/metadata/01f408db-df8a-49a2-8ce4-0f66b8efe17b |
| OGC WMS      | https://geo.api.vlaanderen.be/ALV/wms                       | https://www.vlaanderen.be/datavindplaats/catalogus/wms-departement-landbouw-en-visserij              | 
