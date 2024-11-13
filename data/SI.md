# Slovenia

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Ministry of Agriculture, Forestry and Food  (Ministrstvo za kmetijstvo, gozdarstvo in prehrano)
- **Homepage:** https://www.gov.si/drzavni-organi/ministrstva/ministrstvo-za-kmetijstvo-gozdarstvo-in-prehrano/

## Overview

The Slovenian government provides slightly different, relevant open data sets called GERK, KMRS, RABA and EKRZ.
Gerk includes all arable land, is updated monthly and describes 28 generic land coverage categories. The KRMS dataset 
includes CAP applications of the last year and discerns around 150 different crop categories.

The LPIS is a part of the Farm register (called RKG) and works as a spatial representation of areas utilized by 
agricultural holdings (called KMG). The reference parcel of LPIS is the farmer's block (**block**). 
A block is a contiguous area of agricultural land in agricultural use by one Farm (exceptions are
defined in the legislation). The Farm land use unit (GERK) is a contiguous area of agricultural land with the same type
of land use within each block. LPIS includes landscape features (called KRZ), which can only be declared in certain parts
of the country. Farmers declare their land in the form of GERK or KRZ. Published LPIS data is available at the
GERK/KRZ level with block id as an attribute and is updated monthly.

The [MKGP-RKG public geographic data viewer](http://rkg.gov.si/GERK/WebViewer/) provides up-to-date data 
for all GERKs in Slovenia, and data from the last aggregated application are available for download and via WMS.

Example; KMRS_2023 layer includes farmers declarations for 2023. The data is for main crop - it is possible that
this is not the only crop on certain area in this year. The date of data august 2023. A farmer can change
the declaration until the control is announced by the paying agency.

More information are available at: https://eprostor.gov.si/imps/srv/eng/catalog.search#/metadata/21ecba4a-1214-4617-8bf4-020d2f235a25

## Data & Metadata

- **URL:** https://rkg.gov.si/vstop/
- **File Format:** Shapefile-rar
- **Projection:** EPSG:3794
- **License:** https://rkg.gov.si/vstop/ "Javno dostopni podatki" (Publicly available data)

Download either [GERK](https://rkg.gov.si/arhiv/GERK/GERK_2024_10_31.zip) (current field usage) or 
[KMRS](https://rkg.gov.si/razno/portal_analysis/KMRS_2023.rar) (farmer application)

### Properties

| Property   | **Data Type** | Constraints | Description         |
|------------|---------------|-------------|---------------------|
| ID         | integer       |             | Internal identifier |
| GERK_PID   | integer       |             | Gerk ID             |
| SIFRA_KMRS | integer       |             | Crop code?          |
| AREA       | real          |             | Area in m^2         |
| RASTLINA   | string        |             | Crop name Slovenian |
| CROP_LAT_E | string        |             | Crop name English   |

### Example

See [example map for GERK](http://rkg.gov.si/GERK/WebViewer/)

### API

| Standard | URL                                                                                                                                                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OGC WMS  | https://rkg.gov.si/GERK/WebViewer/gerk_viewer/wms?REQUEST=GetMap&SERVICE=WMS&VERSION=1.3.0&EXCEPTIONS=INIMAGE&LOCALE=sl&FEATURE_COUNT=1000&CRS=EPSG%3A3794&TRANSPARENT=FALSE&FORMAT=image%2Fjpeg&LAYERS=&STYLES=&&BBOX=393322%2C76822%2C396862%2C78582&WIDTH=885&HEIGHT=440 |
