# Belgium Wallonia: Parcellaire Agricole Anonyme

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Service public de Wallonie (SPW). Contact: helpdesk.carto@spw.wallonie.be
- **Homepage:** https://geoportail.wallonie.be/catalogue/

## Overview

The Crop Fields (PAA) covers land use in agricultural and forestry areas managed as part of the implementation 
of the Common Agricultural Policy by the Paying Agency of Wallonia.

The PAA represents the public version of the agricultural plot. It therefore does not include personal 
information allowing the operator to be identified. It is provided on an annual basis. Data from a 
year of cultivation are made available to the public during the following year.

You can download the data yourself, but the license does not allow public distribution. You can obtain a 
personal/company license for free, or freely use a WMS service for visualization.

## Data

To download the data, create an account at https://geoportail.wallonie.be/ . 
Go to [the dataset](https://geoportail.wallonie.be/catalogue/49294570-2a8d-49ca-995c-1b0890672bc8.html) . 
Select `Accès` and add the data to your downloads (click _AJOUTER À MES TÉLÉCHARGEMENTS_). Then finish the download
[finalisez votre demande de téléchargement](https://geoportail.wallonie.be/geodata-donwload.html) and select the
required data format and projection. Choose `gpkg` in _Lambert 72_ projection to use the converter in fiboa-cli.
Select "Region Wallone" at _DÉCOUPAGE_ for the full dataset. Select "Je souhaite une license" to acquire a license.
Indicate whether it's Professional or Personal (particulier) use and choose an end-date of the license. 
You will receive an e-mail with the file.

- **URL:** https://geoportail.wallonie.be/catalogue/49294570-2a8d-49ca-995c-1b0890672bc8.html
- **Documentation:** https://geoportail.wallonie.be/catalogue/49294570-2a8d-49ca-995c-1b0890672bc8.html
- **File Format:** GeoPackage, Shapefile, ESRI File Geodatabase
- **Projection:** EPSG:31370 (Belgian Lambert 72)
- **License:** Propietary, no distribution allowed https://geoportail.wallonie.be/files/documents/ConditionsSPW/DataSPW-CGU.pdf

### Properties

| Property    | Data Type | Constraints | Description           |
|-------------|-----------|-------------|-----------------------|
| OBJECTID    | float     |             | Global identifier     |
| CAMPAGNE    | string    | 4 chars     | Year (2022) in string |
| CULT_COD    | string    | 6 chars     | Crop code             |
| CULT_NOM    | string    | 254 chars   | Crop name             |
| GROUPE_CULT | string    | 50 chars    | Crop group name       |
| SURF_HA     | float     |             | Surface area          |

### Example

See https://geoportail.wallonie.be/walonmap#SHARE=1AA1E98EB46B2C97E0630AB6A49D44D4 

## API (optional)

See https://geoportail.wallonie.be/catalogue/49294570-2a8d-49ca-995c-1b0890672bc8.html 

It has a specific access license: https://geoportail.wallonie.be/files/documents/ConditionsSPW/DataSPW-CGA.pdf 

| Standard | URL                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| OGC WFS  | https://geoservices.wallonie.be/arcgis/services/WFS/SIGEC_PARC_AGRI_ANON/MapServer/WFSServer                                          |
| OGC WMS  | https://geoservices.wallonie.be/arcgis/services/AGRICULTURE/SIGEC_PARC_AGRI_ANON__2022/MapServer/WMSServer                            |
| OGC WMTS | https://geoservices.wallonie.be/arcgis/rest/services/AGRICULTURE/SIGEC_PARC_AGRI_ANON__2022/MapServer/WMTS/1.0.0/WMTSCapabilities.xml |

Inspire WMS is available without terms & conditions. No conditions apply to access and use the WMS.

https://geoportail.wallonie.be/catalogue/d752fab9-4560-4a32-9da6-227b51fca867.html
Projection: ETRS89-extended / LAEA Europe (EPSG: 3035)

| Standard | URL                                                                                          |
|----------|----------------------------------------------------------------------------------------------|
| OGC WFS  | https://geoservices.wallonie.be/arcgis/services/WFS/SIGEC_PARC_AGRI_ANON/MapServer/WFSServer |
