# Spain Balearic Islands SIGPAC

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Govern de les Illes Balears
- **Homepage:** https://www.caib.es/webgoib/

## Overview

The Geographic Information System of the Common Agricultural Policy of agricultural sites (SIGPAC), allows to identify geographically the enclosures declared by farmers and farmers, to any aid scheme related to the area cultivated or taken advantage of by the herd. The service includes protection strips on the banks of watercourses by application of BCAM 4.

BCAM4: Do not apply fertilizers or plant protection products (in strips with a minimum width of 5 meters along watercourses, as well as reservoirs, lakes and lagoons (SIGPAC layer)). Do not carry out agricultural production (except for existing plantations and the sowing of wild flora, grazing or mowing).

## Data

- **URL:** https://ideib.caib.es/geoserveis/rest/services/public/GOIB_SIGPAC_IB/MapServer/
- **Documentation:** https://intranet.caib.es/opendatacataleg/dataset/sigpac-2024
- **File Format:** GeoJSON
- **Projection:** EPSG:4326
- **License:** CC-BY-4.0 ( http://www.opendefinition.org/licenses/cc-by )
- **Attribution:** Govern de les Illes Balears

### Properties

| Property     | Data Type | Constraints | Description          |
|--------------|-----------|-------------|----------------------|
| OBJECTID     | int       |             | Identifier           |
| DN_OID       | int       |             | Identifier           |
| DN_SURFACE   | Real      |             | Area in m2           |
| DN_PERIMET   | Real      |             | Perimeter            |
| PROVINCIA    | int       |             | Province code        |
| MUNICIPIO    | int       |             | Municipality code    |
| POLIGONO     | int       |             |                      |
| PARCELA      | int       |             |                      |
| RECINTO      | int       |             |                      |
| PENDIENTE_   | int       |             |                      |
| COEF_REGAD   | int       |             |                      |
| COEF_ADMIS   | int       |             |                      |
| USO_SIGPAC   | String    |             | SIGPAC Land use code |
| INCIDENCIA   | String    |             |                      |
| MOTIVO_MOD   | int       |             |                      |
| REFERENCIA   | String    |             |                      |
| DATA         | int       |             |                      |
| CERCA        | String    |             |                      |
| ANYS         | int       |             |                      |
| Shape_Length | Real      |             |                      |
| Shape_Area   | Real      |             |                      |


## API

| Standard | URL                                                                              | Documentation   |
|----------|----------------------------------------------------------------------------------|-----------------|
| ESRI     | https://ideib.caib.es/geoserveis/rest/services/public/GOIB_SIGPAC_IB/MapServer/  | -               |


