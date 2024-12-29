# Spain Castilla la Mancha Crop fields

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Castilla-la-Mancha
- **Homepage:** https://datosabiertos.castillalamancha.es/dataset/sistema-de-informaci%C3%B3n-geogr%C3%A1fica-de-parcelas-agr%C3%ADcolas-de-castilla-la-mancha-sigpac

## Overview

SIGPAC is a Geographic Information System dedicated to the control of agricultural aid under 
the CAP (Common Agricultural Policy). This tool is mandatory for the management of community aid, and is 
the identification basis for any type of aid related to the surface area.

## Data

https://datosabiertos.castillalamancha.es/dataset/sistema-de-informaci%C3%B3n-geogr%C3%A1fica-de-parcelas-agr%C3%ADcolas-de-castilla-la-mancha-sigpac


- **URL:** https://datosabiertos.castillalamancha.es/dataset/sistema-de-informaci%C3%B3n-geogr%C3%A1fica-de-parcelas-agr%C3%ADcolas-de-castilla-la-mancha-sigpac
- **Documentation:** https://datosabiertos.castillalamancha.es/dataset/sistema-de-informaci%C3%B3n-geogr%C3%A1fica-de-parcelas-agr%C3%ADcolas-de-castilla-la-mancha-sigpac-2
- **File Format:** GeoJSON
- **Projection:** EPSG:
- **License:** CC-BY-SA-4.0 (see https://datosabiertos.castillalamancha.es/dataset/sistema-de-informaci%C3%B3n-geogr%C3%A1fica-de-parcelas-agr%C3%ADcolas-de-castilla-la-mancha-sigpac)
- **Attribution:** Unidad de Cartografía. Secretaría General. Consejería de Agricultura , Ganadería y Desarrollo Rural.

### Properties

| Property         | Data Type | Constraints | Description       |
|------------------|-----------|-------------|-------------------|
| objectid_1       | Integer   |             | object_id         |
| dn_oid           | Integer   |             | identifier        |
| dn_surface       | Real      |             | area in m2        |
| dn_perimet       |           |             | perimeter in m    |
| provincia        |           |             | province code     |
| municipio        |           |             | municipality code |
| agregado         | Integer   |             |                   |
| zona             | Integer   |             |                   |
| poligono         | Integer   |             |                   |
| parcela          | Integer   |             |                   |
| recinto          | Integer   |             |                   |
| pdte_media       | Integer   |             |                   |
| coef_admis       | Integer   |             |                   |
| factor_sue       | Integer   |             |                   |
| factor_pen       | Integer   |             |                   |
| factor_veg       | Integer   |             |                   |
| porc_int_p       | Integer   |             |                   |
| cap_result       | Integer   |             |                   |
| factor_inc       | Integer   |             |                   |
| cap_resu01       | Integer   |             |                   |
| pendiente_       | Integer   |             |                   |
| altitud          | Integer   |             |                   |
| geocentro_       | Real      |             |                   |
| geocentr01       | Real      |             |                   |
| objectid         | Integer   |             |                   |
| coef_regad       | String    |             |                   |
| uso_sigpac       | String    |             |                   |
| incidencia       | String    |             |                   |
| parcela_ag       | String    |             |                   |
| region_201       | String    |             |                   |
| grupo_cult       | String    |             |                   |
| region           | Integer   |             |                   |
| tm               | String    |             |                   |
| codigo           | String    |             |                   |
| factor_v01       | Integer   |             |                   |
| porc_int_f       | Integer   |             |                   |
| porc_int_d       | Integer   |             |                   |
| porc_int01       | Integer   |             |                   |
| st_area(shape)   | Real      |             |                   |
| st_length(shape) | Real      |             |                   |

## API

Open data portal: https://datos-abiertos-castillalamancha.opendata.arcgis.com/
Web Viewer: https://datosabiertos.castillalamancha.es/dataset/sistema-de-informaci%C3%B3n-geogr%C3%A1fica-de-parcelas-agr%C3%ADcolas-de-castilla-la-mancha-sigpac-1

## API

| Standard | URL                                                                  | Documentation                        |
|----------|----------------------------------------------------------------------|--------------------------------------|
| ESRI     | https://geoservicios.castillalamancha.es/arcgis/rest/services/Vector | Layers Vector/Recintos_sigpac_<YEAR> |
