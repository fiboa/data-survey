# SIGPAC Extremadura

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Junta de Extremadura - Consejería de Infraestructuras, Transporte y Vivienda
- **Homepage:** https://www.juntaex.es/lajunta/consejeria-de-infraestructuras-transporte-y-vivienda

## Overview

Layer relating to enclosures, which constitute a continuous surface of land, within a plot, with the same agricultural use.

SIGPAC is the Geographic Information System for the Identification of Agricultural Plots , 
created through collaboration between the Spanish Agricultural Guarantee Fund (FEGA) and 
the different Autonomous Communities, within the scope of their territories, as an element 
of the Integrated Management and Control System of the direct aid regimes. It has the character 
of a public register of administrative profile, and contains updated information on the 
plots that may benefit from community aid related to the surface area, providing graphic 
support for these and their subdivisions (ENCLOSURES) with defined agricultural uses or 
developments.

## Data

- **URL:** http://sitex.gobex.es/SITEX/centrodescargas/viewsubcategoria/45
- **File Format:** Shapefile
- **Projection:** EPSG:4258
- **License:** CC-BY 4.0 See http://sitex.gobex.es/SITEX/files/CondicionesUsoCICTEX.pdf
- **Attribution:** Junta de Extremadura

### Properties

| Property    | Data Type | Constraints | Description                               |
|-------------|-----------|-------------|-------------------------------------------|
| dn_surface  | Real      |             | Area                                      |
| dn_perimet  | String    |             | Perimeter                                 |
| provincia   | Real      |             | Adminstrative subdivision Province ID     |
| municipio   | Real      |             | Adminstrative subdivision municipality ID |
| agregado    | int       |             |                                           |
| zona        | int6      |             |                                           |
| poligono    | Real      |             |                                           |
| parcela     | Real      |             |                                           |
| recinto     | Real      |             | Precinct                                  |
| pendiente   | int       |             |                                           |
| coef_regad  | int       |             |                                           |
| uso_sigpac  | String    |             | Land use code                             |
| id          | int       |             | identifier                                |
| numero      | int       |             |                                           |
| pdte_media  | Real      |             |                                           |
