# Spain Basque Country Declared CAP fields (SIGPAC)

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Basque Government
- **Homepage:** https://www.euskadi.eus/gobierno-vasco/inicio/

## Overview

SIGPAC, the geographic information system for the identification of agricultural plots, is the system 
that farmers and ranchers must use to apply for community aid related to the area. The reason for 
putting this system into effect was the result of a requirement imposed by the European Union on 
all Member States. Sigpac began to be used from February 1, 2005, together with the beginning of 
the 2005 community aid application period.

## Data

- **URL:** https://www.geo.euskadi.eus/cartografia/DatosDescarga/Agricultura/SIGPAC/SIGPAC_CAMPA%C3%91A_2024_V1/
- **Documentation:** https://www.geo.euskadi.eus/sigpac-euskadiko-nekazal-lursailak-identifikatzeko-informazio-geografikoaren-sistema/webgeo00-dataset/eu/
- **File Format:** Shapefile+ZIP, spread over 255 zip-files
- **Projection:** EPSG:25830
- **License:** CC-BY
- **Attribution:** Basque Government
- _Any use is permitted using this text as the creator: Basque Government / Gobierno Vasco._

https://www.geo.euskadi.eus/cartografia/DatosDescarga/Documentacion/SIGPAC/20180608_NNGG_SISTEMA_DE_INFORMACION_GEOGRAFICA_VF.pdf


### Properties

| Property   | Data Type | Constraints | Description                               |
|------------|-----------|-------------|-------------------------------------------|
| DN_SURFACE | Real      |             | Area                                      |
| DN_PERIMET | String    |             | Perimeter                                 |
| AGREGADO   | int64     |             |                                           |
| ZONA       | int64     |             |                                           |
| PROVINCIA  | Real      |             | Adminstrative subdivision Province ID     |
| MUNICIPIO  | Real      |             | Adminstrative subdivision municipality ID |
| POLIGONO   | Real      |             |                                           |
| PARCELA    | Real      |             |                                           |
| RECINTO    | Real      |             | Precinct                                  |
| USO        | String    |             | Land use code                             |
| PTE        | Real      |             | Some identifier? Not crop                 |
| REGION     | Real      |             |                                           |
| CAP        | Real      |             |                                           |
| CAMPANA    | Integer   |             | campaign year                             |


## API

| Standard  | URL                                                                              | Documentation   |
|-----------|----------------------------------------------------------------------------------|-----------------|
| OGC WMS   | https://www.geo.euskadi.eus/WMS_NEKAZARITZA?request=getcapabilities&SERVICE=WMS  | -               |

## Example

https://www.geo.euskadi.eus/geobisorea/?lang=eu&extent=-277973.5727,5288315.52,-274916.0916,5290393.6517,102100&layers=AGRICULTURA_EUS_3611_94,AGRICULTURA_EUS_3611_95,AGRICULTURA_EUS_3611_96,AGRICULTURA_EUS_3611_97,AGRICULTURA_EUS_3611_98,AGRICULTURA_EUS_3611_99,AGRICULTURA_EUS_3611_100,AGRICULTURA_EUS_3611_101
