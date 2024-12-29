# Comunidad de Madrid Crop Fields

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Comunidad de Madrid
- **Homepage:** https://www.comunidad.madrid/

## Overview

SIGPAC is the Agricultural Parcel Identification System implemented throughout the European Union for the application of CAP (Common Agricultural Policy) aid to farmers and ranchers.

SIGPAC is configured as a database containing digitalized cartographic images of the entire national territory (aerial orthoimages) and a geographic delimitation of each plot of land with its individual reference and the attributes corresponding to its geometry and agricultural use.

## Data

- **URL:** https://idem.comunidad.madrid/catalogocartografia/srv/spa/catalog.search#/metadata/spacm_atom_sigpac
- **Documentation:** https://www.comunidad.madrid/servicios/medio-rural/sigpac
- **File Format:** Shapefile
- **Projection:** EPSG:4258 (ETRS89 geographic coordinates))
- **License:** [No Limitations to public access](https://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/noLimitations) as documented at source https://idem.comunidad.madrid/catalogocartografia/srv/spa/catalog.search#/metadata/spacm_sigpac

License;  No limitations to public access
The use, graphic delimitation or other attributes of the enclosures that appear in the SIGPAC are intended to make it easier for farmers to complete their application for CAP aid. When the use that appears in the SIGPAC is different from the actual use, farmers must make their application for aid based on the latter, the actual use, and must report the incident to the competent service of their Autonomous Community.
https://www.fega.gob.es/orig/pdfs/20230627-MESA-SGC-Acuerdo-Distribuci%C3%B3n-Datos-SIGC_ES_FIRMADO.pdf

### Properties

| Property   | Data Type | Constraints | Description       |
|------------|-----------|-------------|-------------------|
| DN_OID     | Real      |             | Identifier        | 
| DN_SURFACE | Real      |             | Area in m^2       | 
| PROVINCIA  | Integer   |             | Province code     | 
| MUNICIPIO  | Integer   |             | Municipality code | 
| AGREGADO   | Integer   |             |                   |
| ZONA       | Integer   |             |                   |
| POLIGONO   | Integer   |             |                   | 
| PARCELA    | Integer64 |             |                   |
| RECINTO    | Integer64 |             |                   |
| FACTOR_SUE | Integer64 |             |                   |
| FACTOR_PEN | Integer64 |             |                   |
| FACTOR_VEG | Integer64 |             |                   |
| CAP_RESU01 | Integer64 |             |                   |
| PENDIENTE_ | Integer   |             |                   |
| FACTOR_V01 | Integer64 |             |                   |
| ALTITUD    | Integer64 |             |                   |
| COEF_REGAD | Integer   |             |                   |
| USO_SIGPAC | String    |             | Crop code         |
| INCIDENCIA | String    |             |                   |
| PARCELA_AG | String    |             |                   |
| REGION_201 | String    |             |                   |
| GRUPO_CULT | String    |             | Crop Group        |
| REGION     | Integer   |             |                   |

