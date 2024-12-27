# Spain Cantabria Crop fields (SIGPAC)

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Gobierno de Cantabria
- **Homepage:** https://mapas.cantabria.es/

## Overview

Cantabria offers the SIGPAC data as an Inspire-based service. The data is free to use, and you're allowed to
redestribute the data under a non-commercial license.

## Data

- **URL:** https://mapas.cantabria.es/
- **File Format:** OGC/ESRI webservices
- **Projection:** EPSG:4326
- **License:** For non-commerical usage; CC-BY-NC-4.0 (a non-free license)
  - Original license: https://boc.cantabria.es/boces/verAnuncioAction.do?idAnuBlob=260596
  - A commercial use license is available for free on request. See https://www.territoriodecantabria.es/cartografia-sig/datos-abiertos-y-politica-de-licencias
  - License FAQ under https://www.territoriodecantabria.es/web/territorio-de-cantabria/cartografia-sig/descargas-y-politica-de-licencias/preguntas-frecuentes
  - "Our licenses allow the reproduction or redistribution of the licensed digital information to third parties. In such cases, it is essential that when redistributing or transferring the data to said third parties, they clearly and explicitly accept the conditions of our non-commercial use license."
- **Attribution:** ©Government of Cantabria. Free information available at https://mapas.cantabria.es

### Properties

| Property   | Data Type | Constraints | Description     |
|------------|-----------|-------------|-----------------|
| OBJECTID   | Integer64 |             |                 |
| DN_OID     | Integer64 |             |                 |
| DN_SURFACE | Real      |             | Area in m^2     |
| DN_PERIMET | Real      |             | Perimeter in m  |
| PROVINCIA  | Integer64 |             | Province ID     |
| MUNICIPIO  | Integer64 |             | Municipality ID |
| POLIGONO   | Integer64 |             |                 |
| PARCELA    | Integer64 |             |                 |
| RECINTO    | Integer64 |             |                 |
| PENDIENTE_ | Integer64 |             |                 |
| COEF_REGAD | String    |             |                 |
| COEF_ADMIN | Integer64 |             |                 |
| USO_SIGPAC | String    |             | SIGPAC use code |
| INCIDENCIA | String    |             |                 | 
| MOTIVO_MOD | String    |             |                 | 
| REFERENCIA | String    |             |                 | 
| DATA       | Integer64 |             |                 |
| CERCA      | String    |             |                 | 
| ANYS       | Integer64 |             |                 |
| Shape_Leng | Real      |             |                 |
| Shape_Area | Real      |             |                 |

## API

| Standard | URL                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------| 
| OGC WMS  | https://geoservicios.cantabria.es/inspire/services/SIGPAC/MapServer/WMSServer?request=GetCapabilities&service=WMS |
| OGC WFS  | https://geoservicios.cantabria.es/inspire/services/SIGPAC/MapServer/WFSServer?request=GetCapabilities&service=WFS |
