# Gallicia SIXPAC Crop Fields

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Xunta de Galicia - Oficina Virtual del Medio Rural
- **Homepage:** https://ovmediorural.xunta.gal/es/consultas-publicas/sixpac

## Overview

The Geographic Information System for Agricultural Plots (SIXPAC) is an official reference database for the 
identification of agricultural plots, which is mandatory in Spain for making applications for direct CAP aid that 
require declaring surface areas.

The purpose of SIXPAC is to provide information to farmers applying for these aid schemes, so that they can indicate 
the location of the farm surfaces that may be eligible for subsidies, as well as to facilitate the submission of
requests for changes to data relating to land uses contained in the system.

## Data

- **URL:** https://ideg.xunta.gal/servizos/rest/services/ParcelasCatastrais/SIXPAC_2023/MapServer/
- **Documentation:** https://sixpac.xunta.es/visorhtml5/
- **File Format:** GeoJSON from ESRI/mapserver exports
- **Projection:** EPSG:25829
- **License:** CC-BY-4.0 (See https://mapas.xunta.gal/gl/aviso-legal , https://medioambiente.xunta.gal/seccion-organizacion/c/CMAOT_Instituto_Estudos_Territorio?content=Direccion_Xeral_Sostibilidade_Paisaxe/Informacion_publica/seccion.html&std=pgcix_2022_2025.html)
- **Attribution:** Información procedente do FOGGA

## Example

https://mapas.xunta.gal/visores/conservaciondanatureza/

### Properties

| Property                      | Data Type | Constraints | Description     |
|-------------------------------|-----------|-------------|-----------------|
| OBJECTID                      | Int       |             | Identifier      |
| CARTOGRAFIA_REFERENCIA_AUX_CP | Int       |             |                 |
| DN_OID                        | Int       |             | Identifier      |
| DN_VERSION                    | Int       |             |                 |
| DN_INITIALDATE                | Int       |             | Retrieval data  |
| DN_ENDDATE                    | Int       |             | Retrieval data  |
| DN_SURFACE                    | Real      |             | Area in m2      |
| DN_PERIMETER                  | Reak      |             | Perimeter in m  |
| PROVINCIA                     | Int       |             | Province code   |
| MUNICIPIO                     | Int       |             | Municipal code  |
| AGREGADO: 0                   | Int       |             |                 |
| ZONA                          | Int       |             |                 |
| POLIGONO                      | Int       |             |                 |
| PARC_REEMPLAZO                | Int       |             |                 |
| REGION_2015                   | String    |             |                 |
| GRUPO_CULTIVO                 | String    |             | Sigpac use code |
| NOM_ZONACP                    | String    |             |                 |
| SP_REEMPLAZO                  | int       |             |                 |
| USO_SIGPAC:                   | String    |             | Not filled?     |
| COEF_REGADIO                  |           |             |                 |
| COEF_ADMISIBILIDAD            |           |             |                 |
| INCIDENCIAS                   |           |             |                 |
| REGION                        | int       |             |                 |
| SHAPE.AREA                    | Real      |             |                 |
| SHAPE.LEN                     | Real      |             |                 |

## API

| Standard | URL                                                                              | Documentation   |
|----------|----------------------------------------------------------------------------------|-----------------|
| ESRI     | https://ideg.xunta.gal/servizos/rest/services/ParcelasCatastrais  | -               |


