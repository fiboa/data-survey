# Belgium Wallonia: Parcellaire Agricole Anonyme / Land Use

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** INSPIRE Geoportal by the European Commission
- **Homepage:** https://inspire-geoportal.ec.europa.eu/
- **Documentation:** https://inspire-mif.github.io/technical-guidelines/data/lu/dataspecification_lu.pdf

## Overview

The Crop Fields (PAA) covers land use in agricultural and forestry areas managed as part of the implementation 
of the Common Agricultural Policy by the Paying Agency of Wallonia. This dataset has been published as an
Inspire Land Use (LU) dataset.

The PAA represents the public version of the agricultural plot. It therefore does not include personal 
information allowing the operator to be identified. It is provided on an annual basis. Data from a 
year of cultivation are made available to the public during the following year.

## Data

The data is distributed in two ways: either at the source of the paying agency (more attributes
but no public distribution, you can obtain a personal/company license for free) or 
at the European Commission data portal (no limitations). 

### Download free

The data is distributed through Inspire (European Directive 2007/2/EC). Under Inspire guidelines,
the data is distributed with a license stating "No conditions apply to access and use". Data acquired from the
inspire portal can be distributed freely, but it lacks some attributes. See also 
[analysis by EuroCrops](https://github.com/maja601/EuroCrops/wiki/Belgium#wallonia) on this subject.

For the free/open dataset, go to the European Commission portal distribution at
https://inspire-geoportal.ec.europa.eu/srv/eng/catalog.search#/metadata/2a0d9be0-ac3d-443e-9db0-a7cfb0f128e2
The projection is EPSG:3035

- **URL:** https://inspire-geoportal.ec.europa.eu/srv/eng/catalog.search#/metadata/2a0d9be0-ac3d-443e-9db0-a7cfb0f128e2
- **Documentation:** https://inspire-mif.github.io/technical-guidelines/data/lu/dataspecification_lu.pdf
- **File Format:** gml.zip
- **Projection:** EPSG:3035
- **License:** No conditions apply to access and use. Distributed through Inspire guidelines

### Download original / full

To download the data, create an account at https://geoportail.wallonie.be/ . 
Go to [the dataset](https://geoportail.wallonie.be/catalogue/49294570-2a8d-49ca-995c-1b0890672bc8.html) . 
Select `Accès` and add the data to your downloads (click _AJOUTER À MES TÉLÉCHARGEMENTS_). Then finish the download
[finalisez votre demande de téléchargement](https://geoportail.wallonie.be/geodata-donwload.html) and select the
required data format and projection. Choose `OGC GeoPackage (.gpkg)` in _Lambert 72_.
Select "Region Wallone" at _DÉCOUPAGE_ for the full dataset. Select "Je souhaite une license" to acquire a license.
Indicate whether it's Professional or Personal (particulier) use and choose an end-date of the license. 
You will receive an e-mail with the file.

- **URL:** https://geoportail.wallonie.be/catalogue/49294570-2a8d-49ca-995c-1b0890672bc8.html
- **Documentation:** https://geoportail.wallonie.be/catalogue/49294570-2a8d-49ca-995c-1b0890672bc8.html
- **File Format:** GeoPackage, Shapefile, ESRI File Geodatabase
- **Projection:** EPSG:31370 (Belgian Lambert 72)
- **License:** Propietary, no distribution allowed https://geoportail.wallonie.be/files/documents/ConditionsSPW/DataSPW-CGU.pdf

### Properties

| Property    | Data Type | Constraints | Description       |
|-------------|-----------|-------------|-------------------|
| localId     | string    |             | Global identifier |
| validFrom   | date      |             | 2022-01-01        |
| validTo     | date      |             | 2022-12-31        |
| crop_code   | string    | 6 chars     | Crop code         |
| crop_name   | string    | 254 chars   | Crop name         |

### Example

See https://geoportail.wallonie.be/walonmap#SHARE=1AA1E98EB46B2C97E0630AB6A49D44D4 

## API (optional)

This describes the original dataset (proprietary license)

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
